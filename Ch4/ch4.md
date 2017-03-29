# Chapter 4 
Hmm. So, don’t you think it is time to fly with some coding and see some tricks and examples with nodeJs and ES6?

#### Note(1): 
This section was harder more than what I thought anyway, clone the files and check them out. A lot of new things and tricks it took me some effort to remember everything but I tried to write some coding and copy some from many recourses check them and enjoy.

### Why not ES6 from the beginning?
Because a lot of examples online could be old and ES6 syntax not used, therefore I start this work earlier with normal JavaScript not ES6 
But, now I believe you have a good knowledge regarding JavaScript.so, you can follow the new syntax very easy. 

### What have I to do? 
Basically, just you have to use this new feature when you coding.

Ok. Real code and best examples exist online and hand coded examples?

**Let’s we start:** 
- Open your visual studio code editor 
- Go to Extensions 
- Search for these two Marketplaces 

1. Code runner:
   Adding this extension will allow you running your code directly from js files and see the results 

2. JavaScript ES6 code snippet:
   Provide nice interlaces regarding JavaScript code and suggestion to correct. 

#### Note(2)
Check the appendix for common Marketplaces that we use at Apegroup  

Now, check these sections one by one and Enjoy! 

# Classes 

```javascript
/*******************************************************************************
1.Class definition  
*******************************************************************************/
class Person {
    constructor(name, age, city) {
        this.name = name;
        this.age = age;
        this.city = city;
    }
    //Getter 
    get data() {
        return `the person name is ${this.name} and the age is ${this.age}`;
    }
    //Setter 
    set data(name) {
        this.name = name;
        this.age = age;

    }
    static saySomething() {
        return `well the name is ${this.name}`;
    }
}
/*******************************************************************************
2.Test getter and setter   
*******************************************************************************/

let p1 = new Person(`Eva`, 23, `damscuse`);
console.log(p1.name);
console.log(p1);

//use gettter
console.log(p1.data);

//use setter 
p1.data = `Nali`;

console.log(p1.name);
console.log(p1.data);

/*******************************************************************************
1.Notes 
        The difference between normal function and getter/setter is that: 
        in case of the functions we call them as obj.func(); 
        but in case of using getter and setter the way will be 
        just be obj.getName; 
        mean like preoperties of that object that it:) 
*******************************************************************************/

```

# Functions 

```javascript

/*******************************************************************************
1. Arrow functions 
*******************************************************************************/

function test() {
    return `yes`;
}
/* Same as */
let test2 = () => {
    return `no`;
}

console.log(test2()); //print this way 

/*******************************************************************************
2. Arrow functions with an Array 
*******************************************************************************/

const ages = [23, 62, 45];

const old = ages.filter(age => age > 60)
console.log(old);//62


/*******************************************************************************
3. Where I shouldnot use Arrow functions 
*******************************************************************************/
/* Dont use arrow here */
const obj = {
    name: "myname",
    grade: 32,
    result() {
        return grade * 5;
    }
}

/* Dont use arrow here */
//with the constructor in case if you need to intialize
class Student {
    constructor(name, age) {
        this.name = name;
        this.age = age;
    }
}
/* Dont use arrow here */
//in case of prototype 
Student.prototype.city = function () {
    return `somthing`;
}

// 1. Given this array: `[3,62,234,7,23,74,23,76,92]`, use the array filter method and an arrow function 
//to create an array of the numbers greater than `70`
  const numbers = [3, 62, 234, 7, 23, 74, 23, 76, 92];
  const ar2=numbers.filter(i=>i>70);
  console.log(ar2);


/*******************************************************************************
2. Arrow functions from web bos videos  
*******************************************************************************/

const names = ['wes', 'kait', 'lux'];

const fullNames = names.map(function (name) {
    return `${name} bos`;//name + normal string 
});

const fullNames2 = names.map((name) => {
    return `${name} bos`;//name + normal string 
});

const fullNames3 = names.map(name => {
    return `${name} bos`;
});

const fullNames4 = names.map(name => `${name} bos`);

const fullNames5 = names.map(() => `cool bos`);

const sayMyName = (name) => {
    alert(`Hello ${name}!`)
}

sayMyName('Wes');


```
# Spreed Operator 

```javascript
/*******************************************************************************
1. How to use spreed ooperator 
*******************************************************************************/
const num = {
    even: 2,
    odd: 1,
    zero: 0,
    alphabet: ['A', 'B']
};
//See how the spreed-ooperator works :) 
const combine = [num.even, num.odd, ...num.alphabet];
console.log(combine);

/*******************************************************************************
2. Arrays with Spreed operator 
*******************************************************************************/

const comments = [
    { id: 20 },
    { id: 523423 },
    { id: 632429},
    { id: 192834 },
];
const id = 63249;
const commentIndex = comments.map(function (comment) {

    let [a, d] = [`yes`, `no`];
     (comment.id == id)?console.log(a): console.log(d);
    
});

console.log(commentIndex); // undefined why? Yes, Right no return :) 


/*******************************************************************************
3.combine two array together with spreed
*******************************************************************************/

const arr1=[1,2,3,4,5]
const arr2=[6,7,8,9,10]

const join = [...arr1, ...arr2, 30,40,50,60];
console.log(join);

//Note 1: You can use concat 
//There are many ways to merge two or three arrays.

```


## Appendix:
### Vs Code Extensions: 
We make that easier for you and we created a gist on GitHub so all what you should do is just to clone 

1. Code Runner:
add this extension to be able running your code directly from js files and see the results 
1. Debugger for Chrome:
Add this for debugging with google chrome where you can set some break points and track your project
1. JSLint:
This will help you to analysis you code with JavaScript syntax 
1. HTML and CSS snippet 
Those two extension will help you easily to show the markup language intelligence 
1. Polymer IDE:
This will help you to see cool suggestion regarding polymer and its syntax 
1. JavaScript ES6 code snippet:
Provide nice interlaces regarding JavaScript code and suggestion to correct 
Extension for butterfly:
Add seta/icon: for nice icons and folder tree 
1. Rainbow Brackets:
This will produce nice color for your code and parentheses 
1. Material icon theme:
Also for icons and nice folder trees 

For more details check with your colleagues to see theirs favorites or surf and add by yourself 
