# Caesars Cipher

<h2>Exercise</h2>
<p>One of the simplest and most widely known ciphers is a Caesar cipher, also known as a shift cipher. In a shift cipher the meanings of the letters are shifted by some set amount.</p>

<p>A common modern use is the ROT13 cipher, where the values of the letters are shifted by 13 places. Thus A ↔ N, B ↔ O and so on</p>

<p>Write a function which takes a ROT13 encoded string as input and returns a decoded string.</p>

<p>All letters will be uppercase. Do not transform any non-alphabetic character (i.e. spaces, punctuation), but do pass them on.</p>

<h2>Code</h2>

```
function rot13(str) {
   let decodedStr = str.replace(/[A-Z]/g, function (char) {
    return String.fromCharCode(((char.charCodeAt(0) - 65 + 13) % 26) + 65);
  });

  console.log("==================\nCifra de Caesar 13\n==================\nCódigo:", str + "\nPalavra:", decodedStr);
}
```

<h2>Exemple</h2>

```
rot13("SERR PBQR PNZC");

==================
Cifra de Caesar 13
==================
Código: SERR PBQR PNZC
Palavra: FREE CODE CAMP
```
<a href="" target=_blank>Pages</a>
