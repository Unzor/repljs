# repljs
REPLjs is a JavaScript tool to execute code in virtual machines (Based on JSJava).

# Installation
You can install REPLjs by downloading the ```repljs.min.js``` file, or you can get it from jsdelivr:
```html
<script src="https://cdn.jsdelivr.net/gh/Unzor/repljs/repljs.min.js" type="text/javascript"></script>
```

Include the script at the beginning of the ```<body>``` tag.
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

Or, if you want to use a file instead, you can use this:

```JavaScript
repljs.runCodeFromFile('demo.py', function(a){
console.log(a);
});

```
This code will run Python 3, and it will print "Hello World! :)" in the console.

If you don't want to log the "Process Exited" messages at all, use this example:
```JavaScript
  repljs.runCode("print('Hello World! :)')", function(a){
    if (!a.includes('** Process exited - Return Code: ')){
    console.log(a);
    }
  });
```
And if you only want to log when there is an error, use this:
```JavaScript
  repljs.runCode("print('Hello World! :)')", function(a){
   var resultCode=Number(a.split('** Process exited - Return Code: ').pop().replaceAll('*', ''));
    if (resultCode !== 0){
    console.log(a);
    }
  });
```

To get the available languages, use this:
```JavaScript
repljs.getLanguages();
```

This will return the languages.
