JSON manipulation methods for Underscore.js


**get** - get(json, selector)

Gets a value in a json

```javascript
var json = {some:{nested:"value"}}
_.json.get(json, "some.nested")
=> "value"
```


**set** - set(json, selector, value)

Sets a value in a json

```javascript
var json = {some:{nested:"value"}}
_.json.set(json, "some.nested", "thing")
=> {some:{nested:"thing"}}
```


**remove** - remove(json, selector)

Removes a value in a json

```javascript
var json = {some:{nested:"value"}}
_.json.remove(json, "some.nested")
=> {some:null}
```


**push** - push(json, selector, value)

Inserts a value at the end of an array in a json

```javascript
var json = {some:{array:[1,2,3]}}
_.json.push(json, "some.array", "hello")
=> {some:{array:[1,2,3,"hello"]}}
```


**unshift** - unshift(json, selector, value)

Inserts a value at the beginning of an array in a json

```javascript
var json = {some:{array:[1,2,3]}}
_.json.unshift(json, "some.array", "hello")
=> {some:{array:["hello",1,2,3]}}
```


**flatten** - flatten(json)

Flatten the nested keys in a json

```javascript
var json = {some:{nested:"value"}}
_.json.flatten(json)
=> {some.nested:"value"}
```


**unflatten** - unflatten(data)

Builds a json from a dictionnary of dot-separated keys / values

```javascript
var json = {"some.nested":"value"}
_.json.unflatten(json)
=> {some:{nested:"value"}}
```


**is** - is(data)

Checks if a variable is a valid json [need to work on that one]

```javascript
_.json.is("bonjour")
=> false

var json = {some:{nested:"value"}}
_.json.is(json)
=> true
```


**isStringified** - isStringified(string)

Checks if a string is a stringified json

```javascript
_.json.isStringified("bonjour")
=> false

var json = {some:{nested:"value"}}
var stringified = JSON.stringify(json)
_.json.isStringified(stringified)
=> true
```

**prettyprint** - prettyprint(json)

Returns a stringified / prettyprinted variable from the JSON

```javascript
var json = {some:{nested:"value"}}
_.json.prettyprint(json)
=> "{
    "some": {
      "nested": "value"
    }
  }"
```
