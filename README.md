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
