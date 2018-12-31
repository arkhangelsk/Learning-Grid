## Getters:

```javascript
const employee = {
  _name: 'Tom',
  _yearOfExp: 20,
  _dept: 'CS',
  get yearOfExp(){
    
    if((typeof this._yearOfExp) === 'number'){
      return `employee current year of experience is ${this._yearOfExp}`;
    } else {
      return 'Error: cannot retrieve value';
    }
  }
};

console.log(employee.yearOfExp);

```

**output:**
```
"employee current year of experience is 20"
```

## Setters:

```javascript
const employee = {
  _name: 'Ambreen',
  _yearOfExp: 20,
  _dept: 'CS',
 
  
  set yearOfExp(num){
  if((typeof num) === 'number'){
      this._yearOfExp = num;
      return `employee current year of experience is ${this._yearOfExp}`;
    } else {
      return 'Error: cannot set value';
    }
}
   
  
};

employee.yearOfExp = 25

console.log(employee._yearOfExp);

```

**output:**
```
25
```

## Factory Functions:

```javascript
const empFactory = (name, department) => {
  return {
    name: name,
    department: department,
    task() {
      console.log('Manufacturing');
    }
    
  }
};

const emp1 = empFactory('John', 'Finance');

emp1.task();

```

**output:**
```
"Manufacturing"
```

We can re-write above code by using the destructuring technique that was introduced in ES6 and is also known as property value shorthand:

```javascript
const empFactory = (name, department) => {
  return {
    name,
    department,
    task() {
      console.log('Manufacturing');
    }
    
  }
};

const emp1 = empFactory('John', 'Finance');

emp1.task();

```

## Destructured Assignment:

It allows extracting data from arrays, objects, maps and sets into their own variables.

```javascript
const employee = {
    first: 'Ambreen',
    last: 'Khan',
    country: 'Canada',
    city: 'Toronto',
    twitter: '@ambysan'
  };
  
//Getting data in old-fashoined way:
//   const first = person.first;
//   const last = person.last;

  //This data can be destructured as below; Here curly brackets show new destructuring syntax
const {first, last} = employee;

console.log(first); // Ambreen
console.log(last); // Khan
```

## Built-in Object Methods:

**Object.keys()**
```javascript
const employee = {
    first: 'Ambreen',
    last: 'Khan',
    country: 'Canada',
    city: 'Toronto',
    twitter: '@ambysan'
  };
  
const employeeKeys = Object.keys(employee);
console.log(employeeKeys);
```

output:
```
["first", "last", "country", "city", "twitter"]
```

**Object.entries()**
```javascript
const employee = {
    first: 'Ambreen',
    last: 'Khan',
    country: 'Canada',
    city: 'Toronto',
    twitter: '@ambysan'
  };
  
const objEntries = Object.entries(employee);
console.log(objEntries);

```
output:
```
[["first", "Ambreen"], ["last", "Khan"], ["country", "Canada"], ["city", "Toronto"], ["twitter", "@ambysan"]]
```

**Object.assign()**
```javascript
const employee = {
    first: 'Ambreen',
    last: 'Khan',
    country: 'Canada',
    city: 'Toronto',
    twitter: '@ambysan'
  };
  
const techEmployee = Object.assign({skill1: 'JavaScript', skill2: 'Node.JS'}, employee);

console.log(techEmployee);
```
output:
```
[object Object] {
  city: "Toronto",
  country: "Canada",
  first: "Ambreen",
  last: "Khan",
  skill1: "JavaScript",
  skill2: "Node.JS",
  twitter: "@ambysan"
}
```