# Top 10 ES6 Featues
## 1. Default Parameters in ES6
Existing Function
var link = function (height, color, url) {
    var height = height || 50
    var color = color || 'red'
    var url = url || 'http://azat.co'
    ...
}

 when the input parameter is not passed to a function then the default is used 

 var link = function(height = 50, color = 'red', url = 'http://azat.co') {
  ...
}

## 2.Template Literals in ES6
Template literals or interpolation in other languages is a way to output variables in the string.
var name = 'Your name is ' + first + ' ' + last + '.';
var url = 'http://localhost:3000/api/messages/' + id;

 In ES6 we can use a new syntax ${NAME} inside of the back-ticked string
 
var name = `Your name is ${first} ${last}.`;
var url = `http://localhost:3000/api/messages/${id}`;

## 3. Destructuring Assignment in ES6

## 4. Enhanced Object Literals in ES6

## 5. Arrow Functions in ES6
Tradition function Syntax
  var _this = this
  $('.btn').click(function(event){
    _this.sendData()
  })

Arrow function Syntax.
$('.btn').click((event) =>{
  this.sendData()
})

## 6. Promises in ES6
## 7. Block-Scoped Constructs Let and Const
## 8.Classes in ES6
 We have a class baseModel in which we can define a constructor and a getName() method:
  
 `class baseModel {
    constructor(options = {}, data = []) { // class constructor
      this.name = 'Base'
      this.url = 'http://azat.co/api'
      this.data = data
      this.options = options
    }
    getName() { // class method
      console.log(`Class name: ${this.name}`)
    }
 }`
 
 The AccountModel inherits from baseModel with class NAME extends PARENT_NAME:
 To call the parent constructor, effortlessly invoke ## super()  with params:
 
 `class AccountModel extends baseModel {
    constructor(options, data) {
       super({private: true}, ['32113123123', '524214691']) //call the parent method with super
       this.name = 'Account Model'
       this.url +='/accounts/'
     }
     ## set up a getter like this and accountsData will be a property:
    get accountsData() { //calculated attribute getter
      // ... make XHR
       return this.data
    }
 }

let accounts = new AccountModel(5)
accounts.getName()
console.log('Data is %s', accounts.accountsData);`

OUTPUT : 
Class name: Account Model
Data is %s 32113123123,524214691

## 9.Modules in ES6
Default module exports and require.
    module.exports = {
      port: 3000,
      getAccounts: function() {
        ...
      }
    }
 var service = require('module.js')
console.log(service.port) // 3000  
## You can't selectively load only the pieces you need with require but with imports, you can selectively load only the pieces you need.That can save memory.
## Loading is synchronous(step by step) for require on the other hand import can be asynchronous(without waiting for previous import) so it can perform a little better than require
export var port = 3000
  export function getAccounts(url) {
    ...
  }
 we use import {name} from 'my-module' syntax. For example, 
   import {port, getAccounts} from 'module'
   console.log(port) // 3000
 
 Or we can import everything as a variable service in main.js:
   import * as service from 'module'
   console.log(service.port) // 3000


## 10.Default rest & spread Operator
## 11.New data structures like Map and Set
## Top Javascript Concepts :
https://www.sitepoint.com/implementing-memoization-in-javascript/
https://medium.com/@madasamy/15-javascript-concepts-that-every-nodejs-programmer-must-to-know-6894f5157cb7
