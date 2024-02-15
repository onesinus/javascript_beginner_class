## Basic Object
```javascript
const hp = {
    'name': 'Oddo A9 2020',
    'price': 2500000,
    'colors': ['blue', 'green', 'black'],
    'is_popular': true
}
console.log(hp);
console.log(hp.name); // get a value from an object using their key
console.log(hp["price"]);

hp.price = 3000000 // re-assigment a property in object
console.log(hp);
```