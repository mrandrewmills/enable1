# enable1
JS object for leveraging the enable1 word list.

## Basic Info

Include the enableWordlist.js file in your page/code resources, then create a new object by calling the enable1() function.

```javascript
<script src="js/enableWordlist.js"></script>
var myEnable = new enable1();
```

You should now be able to access properties and methods from within the object you created. Like this:

```javascript
myEnable.search("slipes"); // returns true
myEnable.search("splipes"); // returns false
```

```javascript
myEnable.getRandomWord(); // returns a random word, such as furziest, or playdays, or nongenetic, etc.
```

If you play Wordle, and want to filter the wordlist down to only words with five letters:

```javascript
myEnable.getXLetterWords(5); // this reduces myEnable.candidates from 172,820 words to 8,636 words with exactly five letters in them
myEnable.Wordle(); // convenient alias to .getXLetterWords(5);
```

Want to filter in/filter out words containing specific letters?

```javascript
myEnable.mustHaveTheseLetters("aei");  // myEnable.candidates now contains only words with the letters, a, e, and i in them
myEnable.mustNotHaveTheseLetters("hunt"); // myEnable.candidates now contains only words WITHOUT the letters, h, u, n, and t in them
```

If you make a mistake and/or want to reset your candidates from scratch:

```javascript
myEnable.init();  // myEnable.candidates now contains 172,820 words again, just like when you first created the object
```
