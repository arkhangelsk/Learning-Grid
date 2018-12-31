## How to create a class:
* Classes are templates for JavaScript objects.
* A constructor method is called when we create a new instance of a class.

```javascript
class Employee {
  constructor(name, department) {
    this.name = name;
    this.department = department;
  }
}

const emp1 = new Employee('Tom', 'IT');
console.log(emp1.name);
```
**output:**
```
"Tom"
```

## Inheritance:
* A child class can inherit the properties and methods from a parent class.
* The **extends** keyword is used when we create a subclass from the parent class.
* The super keyword calls the constructor() of a parent class.
* Static methods are always called on the class, but not on instances of the class.

```javascript
class Employee {
  constructor(name) {
    this._name = name;
    this._totalVacationDays = 20;
  }

  get name() {
    return this._name;
  }

  get totalVacationDays() {
    return this._totalVacationDays;
  }

  static generateTempPassword(){
    return Math.floor(Math.random()*100000);
  }
}

class Accountant extends Employee {
  constructor(name, education) {
    super(name);
    this._education = education;
  } 

  get educationInfo() {
    return this._education;
  }
}

const accountant1 = new Accountant('Tom', 'Masters');

console.log(accountant1.totalVacationDays);  
console.log(Employee.generateTempPassword()); 

```

**output:**
```
20
7452        //generates any random number between 0 and 100000
```