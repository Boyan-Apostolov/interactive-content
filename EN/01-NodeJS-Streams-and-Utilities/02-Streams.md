# Streams

[slide]

# Stream

A stream is an abstract interface for working with streaming data in Node.js. 

It is a collections of data that is not available at once.

Data may come continuously in chunks.

There are many stream objects provided by Node.js. 

For instance, a request to an HTTP server is a stream instance.

Streams can be **Readable**, **Writable**, **Duplex** or **Transform**. 

All streams are instances of the "EventEmitter".

**Readable** - can only **read** data.

**Writable** - can only **write** data.

**Duplex** - both **readable** and **writable**.

**Transform** - it is a Duplex stream where the output is in some way related to the input.

Like all Duplex streams, Transform streams implement both the Readable and Writable interfaces.

[/slide]

[slide]

# Readable Stream

**Functions**

There are many useful functions that we can use on readable Streams.

The `.read()` method is used to read the data out of the internal buffer. 

It returns data as a buffer object if no encoding is being specified or if the stream is working in object mode.

This method accepts single parameter **size**, which specifies the number of bytes to be read from the internal buffer.

If no data exist in the buffer then **null** is returned.

```js
readable.read( size );
```

The `.pause()` method is used to stop the flowing mode from emitting data events. 

Any data that becomes accessible will continue to exist in the internal buffer.

This method does not accept any parameters.

```js
readable.pause();
```

The `.resume()` method is used to data that has been paused and can be resumed, so that data can start flowing again.

This method does not accept any parameters.

```js
readable.resume();
```

**Events**

All streams are instances of "EventEmitter". They emit events that can be used to read and write data.

The most important events on a readable stream are:

The **data** event is emitted whenever the stream passes a chunk of data to the consumer.

The **end** event is emitted when there is no more data to be received from the stream.

The **error** event is emitted when there is an error receiving data.

[/slide]

[slide]

# Readable Stream Example

An HTTP request is an instance of a readable stream.

Take a look at the following example.

To be able to create a server we need to require the "http" module from Node.js.

Then we use the `createServer()` method to create a server on your computer.

This is a function that receives two callbacks - **req** and **res**.

**req** stands for request and **res** stands for response.

The `req.on()` method binds an event to an object and adds a listener function for a specified event.

With the "data" event we attach the data to the `body` variable.

With the "end" event we end the data transfer.

The `.listen()` method creates a listener on the specified port or path.

```js
const http = require('http');
http.createServer((req, res) => {
    if (req.method === 'POST') {
        let body = '';
        req.on('data', data => { body += data });
        req.on('end', () => {
            console.log(body);
        });
    }
}).listen(5000);
```

[/slide]

[slide]

# Writable Stream

**Functions**

The `.write()` method takes three arguments:

The chunk is usually a buffer, unless we configure the stream differently.

The encoding argument is needed in that case, but usually we can ignore it.

The callback is a function that we need to call after we are done processing the data chunk.

It is what signals whether the write was successful or not. To signal a failure, call the callback with an error object.

```js
const { Writable } = require('stream');
const outStream = new Writable({
    write(chunk, encoding, callback) {
        console.log(chunk.toString());
        callback();
    }
});
process.stdin.pipe(outStream);
```

The `.end()` method ends writing data. The arguments chunk and encoding are optional, which will permit one final new chunk of data to be written instantly before closing the stream.

Moreover, the optional callback function is added as a listener for the **finish** event of the Writable stream.

```js
writable.end( chunk, encoding, callback);
```

**Events**

The most important events on a writable stream are:

The **drain** event is fired when a writable stream's internal buffer has been emptied.

The cause of something like this can be due to setups that involve reading a data source from one stream faster than it can be written to another resource.

The **finish** event in a Writable Stream is emitted after the Calling of `writable.end()` method when all the data is being flushed to the hidden system.

Exapmle:

```js
const stream = require('stream'); 
const writable = new stream.Writable({ 
  write: function(chunk, encoding, next) { 
    console.log(chunk.toString()); 
    next(); 
  } 
}); 
writable.write('Hello There'); 
writable.end(); 
writable.on('finish', function() { 
   console.log("Write is completed."); 
});
```

The **error** event is emitted when there is an error writing data.

[/slide]

[slide]

# Writable Stream Example

An HTTP response is an instance of a writable stream.

Take a look at the following example.

First we require the "fs" module from Node.js, then we create a server, which will be listening on port 5000.

We start reading from a file called './bigfile.txt', which is the name of the file in this example.

Then we use the `write()` method to write the data inside `src.on()` function.

Finally we use `end()` method to finish writing the data.

```js
const fs = require('fs');
const server = require('http').createServer();
server.on('request', (req, res) => {
    const src = fs.createReadStream('./bigfile.txt');
    src.on('data', data => res.write(data));
    src.on('end', () => res.end());
});
server.listen(5000);
```

[/slide]

[slide]

# Piping Streams

A typical example of using pipes is if you want to transfer data from one file to another.

Here is an example of how we can transfer data using pipes.

The `pipe()` function allows a readable stream to output directly to a writable stream.

We read from the './bigfile.txt' and then we send the data to the **response** using the pipe command to transfer the data from the `src` to the `res`. 

```js
const fs = require('fs');
const server = require('http').createServer();
server.on('request', (req, res) => {
    const src = fs.createReadStream('./bigfile.txt');
    src.pipe(res);
});
server.listen(5000);
```

[/slide]

[slide]

# Duplex and Transform Streams

A duplex stream is one which is both readable and writable similar to a Transform stream. 

However most often a Duplex stream is usually referring to a stream which actually has two full independent streams embedded in it, one flowing out and one flowing in.

A transform stream is a special kind of duplex stream where the output is a transformed version of the input.

In the following example we read from 'index.js' and then we compress it to 'index.js.gz'.

We require "fs" and "zlib" module from Node.js, then we create a readable and writable streams.

Finally using the `.pipe()` method we transfer data from one file to another.

```js
const fs = require('fs');
const zlib = require('zlib');
let readStream = fs.createReadStream('index.js');
let writeStream = fs.createWriteStream('index.js.gz');
let gzip = zlib.createGzip();
readStream.pipe(gzip).pipe(writeStream);
```

[/slide]