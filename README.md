# repljs
REPLjs is a JavaScript tool to execute code in virtual machines (Based on JSJava).

# API
Example code:
```JavaScript
var repljs=new REPLjs();
repljs.setLanguage('python3');
repljs.setFileName('main.py');

repljs.runCode("print('Hello World! :)')", function(a){
console.log(a);
});

```

Or, if you want to use a file instead, you can do this:

```JavaScript
var repljs=new REPLjs();
repljs.setLanguage('python3');
repljs.setFileName('main.py');

repljs.runCodeFromFile('demo.py', function(a){
console.log(a);
});

```
This code will run Python 3, and it will print "Hello World! :)" in the console.


To get the available languages, use this:
```JavaScript
repljs.getLanguages();
```

This will return the languages.
