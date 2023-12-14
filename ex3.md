## Function Signatures

It's often conventional to write the 'signature' of a function to concisely
capture the function's name, the names and types of the arguments, and the type
of the return value. Below are the functions and data shapes from the previous exercise that you'll need for reference. The data types of the inputs and outputs might be primitive JavaScript types, or user-defined Objects represented in object 'shape' shorthand. For example, from the 'shape' of a Person, we know that all Person objects have a 'name' key that is a string, and an 'age' key that is a number.

```js
// Person: {
//  name: string,
//  age: number,
// }

function getName(person) {
  return person.name;
}

function getAge(person) {
  return person.age;
}

function makePerson(name, age) {
  return {
    name: name,
    age: age
  };
}

function birthday(person) {
  person.age += 1;
  return person;
}

// Point: {
// x: number
// y: number
// name: string
//}

function getDistance(pointA, pointB) {
  return Math.sqrt((pointA.x - pointB.x) ** 2 + (pointA.y - pointB.y) ** 2);
}
```

For the `getDistance` function above, the signature might
be written as:

```js
// getDistance(pointA: Point, pointB: Point): number
```

The `:` is used to indicate that the type is 'about' the preceding name. In
`pointA: Point`, `pointA` is a `Point`-object.

Reading this function signature out loud, you would say

> `getDistance` is a function that takes in Points pointA and pointB and returns
> a number.

### For practice, add the function signature to the functions in the table.

| Function | types of inputs | type of output | function signature                                  |
| ------------- | --------------- | -------------- | --------------------------------------------------- |
| `getName`     |  Person  |   person.name   |  getName(person): person.name    |
| `getAge`      |  person |   person.age    |  getAge(person):person.age      |
| `makePerson`  |name, age | object| makePerson(name, age):makes an object with a keys named name and age and a values named name and age    |
| `birthday`    |   Person    |  person     |  brithday(person): person          |
| `getDistance` | _Point, Point_  | _number_       | _getDistance(pointA: Point, pointB: Point): number_ |


[Main menu](README.md) | [Exercise 4 - Operators as 'Functions'](ex4.md)