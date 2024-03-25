# Advanced Array Methods

1. Looping Methods in Javascript:
    * __'forEach'__: iterate through each element, useful for accessing or modifying
    * __'map'__: transform each element into something else and store it in a new array
    * __'filter'__: create a new array containing only elements that meet a specific condition

2. Common Looping Patterns:
    * __'for'__ loop: traditional method for stepping through every element in an array
    * Using a function within a loop for encapsulating functionality

3. Introduction to forEach:
    * Replace traditional 'for' loops with 'forEach' for simplicity
    * 'forEach' takes a function as a parameter, which is called for each element in the array

4. Introduction to map:
    * Similar to 'forEach' but expects a returned value for every element to create a new array
    * Useful for transforming each element into something else

5. Introduction to filter:
    * Extract specific elements from an array based on a condition
    * Create a new array containing only elements that satisfy the condition

6. Example putting it all together:

```javascript
// Array of friends' information
const myFriends = [
    { firstname: 'Isma', lastname: 'Kirby', age: 27 },
    { firstname: 'Aaliya', lastname: 'Becker', age: 35 },
    { firstname: 'Adnaan', lastname: 'Tang', age: 22 },
    { firstname: 'Rafi', lastname: 'Pearson', age: 29 },
    { firstname: 'Eshaal', lastname: 'Gould', age: 29 },
    { firstname: 'Scarlett', lastname: 'Whitehead', age: 45 },
    { firstname: 'Arslan', lastname: 'Esparza', age: 38 },
    { firstname: 'Isla-Mae', lastname: 'Hastings', age: 46 },
    { firstname: 'Eamonn', lastname: 'Vang', age: 21 },
    { firstname: 'Haya', lastname: 'Mcdougall', age: 31 },
];

// Loop 1: Calculate total age and add initials to each friend
let totalAge = 0;
myFriends.forEach(friend => {
    const firstInitial = friend.firstname[0];
    const lastInitial = friend.lastname[0];
    friend.initials = firstInitial + lastInitial;
    totalAge += friend.age;
});

// Calculate average age
const averageAge = totalAge / myFriends.length;

// Loop 2: Filter friends older than the average age
const olderFriends = myFriends.filter(friend => friend.age > averageAge);

// Loop 3: Map older friends' information to initials and age string
const report = olderFriends.map(friend => friend.initials + ': ' + friend.age);

// Output report to console
console.log(report); // Expected output: [ 'AB: 35', 'SW: 45', 'AE: 38', 'IH: 46' ]
```
