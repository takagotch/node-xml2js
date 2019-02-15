### node-xml2js
---
https://github.com/Leonidas-from-XIV/node-xml2js

```js
var parseString = require('xml2js').parseString;
var xml = "<root>Hello xml2js</root>"
parseString(xml, function (err, result) {
  console.log(result);
});

{parseString} = require 'xml2js'
xml = "<root>Hello xml2js!</root>"
parseString xml, (err, result) ->
  console.log result
  
parseString(xml, {trim: true}, function (err, result) {
});

var fs = require('fs'),
  xml2js = require('xml2js');

var parser = new xml2js.Parser();
fs.readFile(__dirname + '/foo.xml', function(err, data){
  parser.parseString(data, function (err, result) {
    console.log(result);
    console.log('Done');
  });
});

fs = require 'fs',
xml2js = require 'xml2js'

parser = new xml2js.Parser()
fs.readFile __dirname + '/foo.xml', (err, data) ->
  parser.parserString data, (err, result) ->
    console.dir result
    console.log 'Done.'

var xml2js = require('xml2js');

var obj = {name: "Super", Surname: "Man", age: 23};

var builder = new xml2js.Builder();
var xml = builder.buildObject(obj);

var xml2js = require('xml2js');

var obj = {root: {$: {id: "my id"}}, _: "my inner text"};
var builder = new xml2js.Builder();
var xml = builder.buildObject(obj);

let obj =  {
  Foo: {
    $: {
      "xmlns": "http://foo.com"
    }
  }
};

let obj = {
  'foo:Foo': {
    $: {
      'xmlns:foo': 'http://foo.com'
    },
    'bar:Bar': {
      $: {
        'xmlns:bar': 'http://bar.com'
      }
    }
  }
}

function nameToUpperCase(name){
  return name.toUpperCase();
}

parseString(xml, {
  tagNameProcessors: [nameToUpperCase],
  attrnameProcessors: [nameToUpperCase],
  valueProcessors: [nameToUpperCase],
  attrValueProcessors: [nameToUpperCase]},
  function (err, result) {
});

function (name){
  return name
}

function (value, name) {
  return value
}

function (name) {
  return name
}

function (name){
  return name
}

function (name) {
  return name
}

function (name) {
  return name
}

var xml2js = require('xml2js');
var parser = new xml2js.Parser(xml2js.defaults["0.2"]);
```

```
<foo:Foo xmlns:foo="http://foo.com">
  <bar:Bar xmlns:bar="http://bar.com">
</foo:Foo>
```

```
```


