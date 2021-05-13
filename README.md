# repljs
REPLjs is a JavaScript tool to execute code in virtual machines (Based on JSJava).

# API
Example code:
```JavaScript
var repljs=new REPLjs();
repljs.setLanguage('python3');
repljs.setFileName('main.py');
repljs.setCode("print('Hello World! :)')");
repljs.onCallback=function(a){
console.log(a);
}
repljs.run();
```
