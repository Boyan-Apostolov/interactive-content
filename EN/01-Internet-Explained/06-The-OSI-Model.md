# The OSI Model

[slide hideTitle]

# What is The OSI Model?

Almost every network protocol is built according to the **OSI (Operation Systems Interconnection)** model.

The **OSI** model splits the **communication process** into 7 layers of smaller processes.

This model has a **hierarchical structure**.

Every layer **provides services** for layer **above** and is **served** by the layer **below**.

The **OSI** model is important to learn as it **improves** the **overall understanding of the internet**.

Being familiar with it also makes it easier for **troubleshooting** and **error handling.**

[/slide]

[slide hideTitle]

# OSI Layers

The **OSI** model creates the following 7 distinct layers:

- `Layer 7: Application` - A **high-level** layer, that connects the **user** and other **applications** with the rest of the **OSI** model **layers**

- `Layer 6: Presentation` - Uses various operations to transform data into an **appropriate format** for the **application layer**

- `Layer 5: Session` - Responsible for **creating**, **executing**, and **cancelling** connections between **local** and **remote** applications

- `Layer 4: Transport` - Transfers **data** through a **network**

- `Layer 3: Network` - **Connects** and **controls** multiple **nodes**

- `Layer 2: Data-link` - Relays data between **physically** connected **nodes**

- `Layer 1: Physical` - Passes **raw data** as **electrical or optical** signals on a physical level

The following picture is a visual representation of these **layers** and their **protocols**:

[image assetsSrc="Java-Web-Introduction-To-The-Internet-4.png" /]

[/slide]

[slide hideTitle]

# TCP/IP model mapping to OSI

The **OSI** reference model can be mapped to the **TCP/IP** with the help of protocols.

Here is how it happens:

[image assetsSrc="Java-Web-Introduction-To-The-Internet-5.png" /]

[/slide]

[slide hideTitle]

# Application Layer - 7

The **application layer** is the **highest-level** layer.

It is what the user **interacts** with.

Applications **present the information** from a network in a **readable format**.

The following protocols work on the application layer:

- `DNS` - Domain Name System

- `FTP` - File Transfer Protocol

- `HTTP` - Hypertext Transfer Protocol

- `SMTP` - Simple Mail Transfer Protocol

[/slide]

[slide hideTitle]

# Presentation Layer - 6

The **presentation layer** is in the Operating System.

This is the final place the data has to pass, before reaching the **application layer**.

It is responsible for data **translation** between **network** and **application formats**.

Some of the things it takes care of are:

- **character encoding**

- **data compression**

- **encryption**

For example, an **encrypted message** is sent over the **internet**.

On arrival, it is **decrypted** back to the **original message**.

All of this is done by the **presentation layer**.

[/slide]

[slide hideTitle]

# Session Layer - 5

The **session layer** is like a **call center**.

It controls the **communication sessions**.

A **communication session** consists of numerous interactions between nodes.

This layer is responsible for the **initiation**, **coordination** and **termination** of application connection.

If the communication is **interrupted**, a **reconnection** is possible through the **session layer**.

It also provides **authentication services**.

An example of a **session layer structure** is a **network socket**.

[/slide]

[slide hideTitle]

# Transport Layer - 4

It was established that the **session layer** **coordinates** communication sessions.

The **transport layer** is responsible for the **logical part** of that **communication**.

It implements **error-checking** to assure that the data quality is as good as possible.

**Transport layer** protocols can be **state-oriented** or **connection-oriented**.

Here are two protocols that work on the **transport layer**:

- `TCP` - Transmission Control Protocol

- `UDP` - User Datagram Protocol

[/slide]

[slide hideTitle]

# Network Layer - 3

The **network layer** provides the **functionality** for **packet transferring**.

It is a **connection** of many **nodes**.

Each node has a **unique address** and **permissions** about whether or not certain data can be sent through it.

It is the **network layer**'s task to determine how to send a piece of information.

If the information is **too large**, it can be broken into **packets** and **reconstructed** on arrival.

The following protocols work on the **network layer**:

- `IP`- Internet Protocol

- `IPSec` - Internet Protocol + Auth

[/slide]

[slide hideTitle]

# Data Link Layer - 2

The **data link** layer is the **individual** connection between **two nodes** in a **network**.

It is responsible for the **data transmission rate** or the **termination** of their connection.

This layer can also **detect and fix** errors in the **physical layer**.

The **data link** layer has two sublayers:

- **Medium Access Control** - Controls the **access** to the **network layer** and the **transmission permissions**

- **Logical Link Control** - Responsible for **error checking** and network layer **protocol detection**

The following protocols work on the **data link** layer:

- `ATM` - Asynchronous Transfer Mode

- `Ethernet` - LAN technology

- `MAC` - Medium Access Protocol

[/slide]

[slide hideTitle]

# Physical Layer - 1

The **physical layer** is the hardware part of the **OSI model**.

It is responsible for the translation of **bits** into **radio** or **optical** signals.

The following hardware elements are within the **physical layer**:

- **USB**

- **Bluetooth**

- **Hubs**

- **Network Interface Cards**

[/slide]
