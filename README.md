# enable1
JS object for leveraging the enable1 word list.

## Basic Info

Basically, be sure to include the enableWordlist.js file in your page/code resources, then create a new object by calling the enable1() function.

```javascript
<script src="js/enableWordlist.js"></script>
var myEnable = new enable1();
```

From there, you should be able to access properties and methods from within the object you created. Like this:

```javascript
myEnable.search("slipes"); // returns true
myEnable.search("splipes"); // returns false
```

```javascript
myEnable.getRandomWord(); // returns furziest, or playdays, or nongenetic, etc.
```

If you play Wordle, and want to filter the wordlist down to only words with five letters:

```javascript
myEnable.wordlist = myEnable.getXLetterWords(5);
```

Want to filter in/filter out words containing specific letters?

```javascript
myEnable.wordlist = test.mustHaveTheseLetters("aei");
myEnable.wordlist = test.mustNotHaveTheseLetters("hunt");
```
