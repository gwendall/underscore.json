JSON manipulation methods for Underscore.js

**get** - get(json, selector)

<sub>Gets a value in a json</sub>

```javascript
var json = {some:{nested:"value"}}
_.json.get(json, "some.nested")
=> "value"
```

**set** - set(json, selector, value)

```javascript
var json = {some:{nested:"value"}}
_.json.set(json, "some.nested", "thing")
=> {some:{nested:"thing"}}
```

**remove** - remove(json, selector)

```javascript
var json = {some:{nested:"value"}}
_.json.remove(json, "some.nested")
=> {some:null}
```

**push** - push(json, selector, value)

```javascript
var json = {some:{array:[1,2,3]}}
_.json.push(json, "some.array", "hello")
=> {some:{array:[1,2,3,"hello"]}}
```

**unshift** - unshift(json, selector, value)

```javascript
var json = {some:{array:[1,2,3]}}
_.json.unshift(json, "some.array", "hello")
=> {some:{array:["hello",1,2,3]}}
```

**flatten** - flatten(json)

```javascript
var json = {some:{nested:"value"}}
_.json.flatten(json)
=> {some.nested:"value"}
```

**unflatten** - unflatten(data)

```javascript
var json = {some.nested:"value"}
_.json.unflatten(json)
=> {some:{nested:"value"}}
```

**is** - is(data)

```javascript
_.json.is("bonjour")
=> false

var json = {some:{nested:"value"}}
_.json.is(json)
=> true

```

**isStringified** - isStringified(string)

```javascript
_.json.isStringified("bonjour")
=> true

var json = {some:{nested:"value"}}
var stringified = JSON.stringify(json)
_.json.isStringified(stringified)
=> true
```
