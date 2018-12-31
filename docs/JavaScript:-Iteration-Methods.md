Built-in JavaScript methods that help to iterate through an array are called iteration methods or iterators. Let's have a look at the different type of iterators:

1. forEach
2. map
3. filter
4. find
5. findIndex
6. every
7. some
8. reduce
9. for...in

## 1. The .forEach() method:
* .forEach() takes an argument of callback function.
* .forEach() will loop through the array and execute the callback function for each element of the array. 
* During each iteration, the current element will be passed as an argument to the callback function.
* The callback function can be in function declaration format, function expression or an arrow function.
* The return value for .forEach() will be undefined.

```javascript
const boxes = [
    { height: 10, width: 30 },
    { height: 20, width: 50 },
    { height: 30, width: 60 }
  ];
  let areas = [];
  
  boxes.forEach(function(box){
      areas.push(box.height*box.width);
  });

console.log(areas);
```
**output:**
```
[ 300, 1000, 1800 ]
```

## 2. The .map() method:
* when we call .map() on an array, it takes an argument of a callback function and returns a new array.

```javascript
let students = [{id: 1, name: 'Tim', course: 'Java'}, 
                {id: 2, name: 'James', course: 'JavaScript'}, 
                {id: 3, name: 'David', course: 'Python'}];

//directly getting a property value from array using map
let name = students.map(function(student){
    return student['name'];
});    

function pluck(array, property){
    let a2 = array.map(function(obj){
        return obj[property];
    });
    return a2;
}

console.log(name);

//getting desired peroperty values using a function
console.log(pluck(students, 'id'));
console.log(pluck(students, 'name'));
console.log(pluck(students, 'course'));

```
**output:**
```
[ 'Tim', 'James', 'David' ]
[ 1, 2, 3 ]
[ 'Tim', 'James', 'David' ]
[ 'Java', 'JavaScript', 'Python' ]
```

## 3. The .filter() method:
* The .filter() method returns a new array after filtering out certain elements from the original array.
* The callback function for the .filter() method returns either true or false depending on the element that is passed to it. 
* The elements for which the callback function returns true as value is added to the new array.

```javascript
let employees = [{id: 1, name: 'James', dept: 'IT'},
                {id: 2, name: 'David', dept: 'Accounts'},
                {id: 3, name: 'Tim', dept: 'HR'}, 
                {id: 4, name: 'Vinod', dept: 'IT'}];

const deptCS_Filter = employees.filter(function(employee){
   return employee.dept === 'IT';
});

console.log(deptCS_Filter);
```
**output:**
```
[ { id: 1, name: 'James', dept: 'IT' },
{ id: 4, name: 'Vinod', dept: 'IT' } ]
```

## 4. The .find() method:
* find() method executes a callback function once for each element in the array until it finds a value that returns as true.
* find() only returns the **first element** matching the given search criteria.
* If nothing is found matching the given search criteria, undefined is returned.
* find() does not mutate or change the original Array.

```javascript
let employees = [{id: 1, age: 35, name: 'James', dept: 'IT', education: 'Masters'},
                {id: 2, age: 25, name: 'David', dept: 'Accounts', education: 'High School'},
                {id: 3, age: 45,name: 'Tim', dept: 'HR', education: 'Graduate'}, 
                {id: 4, age: 50,name: 'Vinod', dept: 'IT', education: 'PHD'}];
               

function chooseEmployee(arrEmployee){
    
     return arrEmployee.find(function(emp){
        return emp.name === 'David';     
    });

}

console.log(chooseEmployee(employees));
```
**output:**

```
{ id: 2, age: 25, name: 'David', dept: 'Accounts', education: 'High School' }
```

## 5. The .findIndex() method:
* findIndex() returns the **index** of the first element in the array that satisfies the given search criteria.
* If nothing is found matching the given search criteria, -1 is returned.

```javascript
let employees = [{id: 1, age: 35, name: 'James', dept: 'IT', education: 'Masters'},
                {id: 2, age: 25, name: 'David', dept: 'Accounts', education: 'High School'},
                {id: 3, age: 45,name: 'Tim', dept: 'HR', education: 'Graduate'}, 
                {id: 4, age: 50,name: 'Vinod', dept: 'IT', education: 'PHD'}];
               

function chooseEmployee(arrEmployee){
    
     return arrEmployee.findIndex(function(emp){
        return emp.name === 'Tim';     
    });

}

console.log(chooseEmployee(employees));
```

output:
```
2
```

## 6. The .every() method:

```javascript
var students = [
    { id: 1, passed: true },
    { id: 2, passed: false},
    { id: 3, passed: true }
  ];
  
const hasPassed;

hasPassed = students.every(function(student){
    return student.passed === true;
});

console.log(hasPassed);
```

output:
```
false
```

## 7. The .some() method:

```javascript
let students = [
    { id: 1, passed: true },
    { id: 2, passed: false},
    { id: 3, passed: true }
  ];
  
let hasFailed;

hasFailed = students.some(function(student){
    return student.passed === false;
});

console.log(hasFailed);
```
**output:**
```
true
```

## 8. The .reduce() method:

* The .reduce() method returns a single value after iterating through the elements of an array
* The .reduce() method takes a callback function as first argument. This callback function has two parameters.
* The .reduce() method can also take an optional second parameter to set an initial value for the first argument in the callback function.

```javascript
let passed = [{ year: 2016 ,pass: 64 }, { year: 2017 , pass: 42 } , { year: 2018 ,pass: 52 }];
const totalPassed;

totalPassed = passed.reduce(function(total, student){
    return student.pass + total;
},0);

console.log(totalPassed);
```

**output:**
```
158
```

## 9. for...in
* for...in will execute a given block of code for each property in an object.

```javascript
let dept = 
    {
      finance: {
      'employee1': {id: 1, age: 35, name: 'James', dept: 'IT', education: 'Masters'},
      'employee2': {id: 2, age: 25, name: 'David', dept: 'Accounts', education: 'High School'},
      'employee3': {id: 3, age: 45,name: 'Tim', dept: 'HR', education: 'Graduate'}, 
      'employee4': {id: 4, age: 50,name: 'Vinod', dept: 'IT', education: 'PHD'}
    }
    };
               

for (let employee in dept.finance) {
 console.log( employee + ': ' + dept.finance[employee].name);
};
```

**output:**
```
"employee1: James"
"employee2: David"
"employee3: Tim"
"employee4: Vinod"
```