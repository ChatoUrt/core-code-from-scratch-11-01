# core-code-from-scratch-11-01

## ---Count Strings in Obj---

Solution / /

``` javascript
function strCount(obj){
  let value = null;
  let count = 0;
  for (let key in obj){
    value = obj[key];
    if (typeof value === 'string'){
    count++;
    } else if (typeof value === 'object'){
    count = count + strCount(value);
    } 
  }
  return count;
}

```

---
## ---Making .methods to Array---
Solution / / 
``` javascript
Array.prototype.first = function() {
  return this[0];
}

Array.prototype.last = function(){
  return this[this.length - 1];
}

```
## ---Obj oriented piracy test---
Solution / /
``` javascript
function Ship(draft, crew) {
  this,draft = draft;
  this.crew = crew;
  
  this.isWorthIt = function() {
  return (this.draft - (this.crew * 1.5)) > 20;
  }
}
```

---

## ---Knowledge base---
1. [Objects in JavaScript](https://www.w3schools.com/js/js_objects.asp)
2. [Prototypal inheritance](https://javascript.info/prototype-inheritance)
