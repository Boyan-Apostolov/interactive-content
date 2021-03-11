# Valoare vs. Tipuri de Referință

[slide hideTitle]

# Valoare și Tipuri de Referință

[video src="https://videos.softuni.org/hls/01.fundamentals-functions-and-arrays/03.JS-Fundamentals-Functions/EN/03.JS-Fundamentals-Functions-23-24-25-value-and-reference-types-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

**Tipurile de valori** și **tipurile de referință** sunt cele două categorii principale de tipuri JavaScript

[image assetsSrc="Value-vs-Reference-Types(1).gif" /]

## Tipuri de valori

O variabilă a unui tip de valoare (date primitive) conține o instanță de tip și păstrează direct valoarea acestora.

Cu tipurile de valori, fiecare variabilă are **propria copie a datelor** și nu este posibil ca operațiunile pe o variabilă să **afecteze cealaltă**.

Când o valoare de tip primitiv este alocată unei alte variabile de același tip, se face o copie.

Când o valoare de tip primitiv este trecută într-o metodă, este transmisă doar o copie a valorii primitive.
Metoda apelată nu are acces la valoarea primitivă originală și, prin urmare, nu o poate modifica.

Metoda apelată poate modifica valoarea copiată.

- Tipurile de date primitive sunt: **undefined**, **boolean**, **number**, **string**, **bigint** și **symbol**

```js
i = 42;
ch = 'A';
result = true;
```


## Tipuri de Referință

Variabilele de **tip referință**  conțin o referință \(indicator, adresă de memorie\) a valorii în sine.

Atunci când un tip de referință este atribuit unui alt tip de referință, ambele vor indica același obiect.

Când un obiect este trecut într-o metodă, metoda numită poate schimba conținutul obiectului transmis acestuia, dar nu și adresa obiectului.

- Datele de tip referință sunt următoarele: **object**, **array** and **function**.


```js
let cars = ['NIO', 'XPang', 'Tesla'];
let obj = {firstName:'Maria', lastName:'Agarici'};
```

[/slide]

[slide hideTitle]
# Valoare și Tipuri de Referință: Demo

[video src="https://videos.softuni.org/hls/01.fundamentals-functions-and-arrays/03.JS-Fundamentals-Functions/EN/03.JS-Fundamentals-Functions-value-vs-refenrence-types-example-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]
[/slide]
