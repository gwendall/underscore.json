JSON manipulation methods for Underscore.js

**get** get(json, selector)

```javascript
_.json.get({some:{nested:"value"}}, "some.nested")
=> "value"
```

**set** set(json, selector, value)

```javascript
_.json.set({some:{nested:"value"}}, "some.nested", "thing")
=> {some:{nested:"thing"}}
```

**remove** remove(json, selector)

```javascript
_.json.remove({some:{nested:"value"}}, "some.nested")
=> {some:null}
```

**push** push(json, selector, value)

```javascript
_.json.push({some:{array:[1,2,3]}}, "some.array", "hello")
=> {some:{array:[1,2,3,"hello"]}}
```

**unshift** unshift(json, selector, value)

```javascript
_.json.unshift({some:{array:[1,2,3]}}, "some.array", "hello")
=> {some:{array:["hello",1,2,3]}}
```

**flatten** flatten(json)

```javascript
_.json.flatten({some:{nested:"value"}})
=> {some.nested:"value"}
```

**unflatten** unflatten(data)

```javascript
_.json.unflatten({some.nested:"value"})
=> {some:{nested:"value"}}
```

**is** is(data)

```javascript
_.json.is("bonjour")
=> false
_.json.is({some:{nested:"value"}})
=> true

```

**isStringified** isStringified(string)

```javascript
_.json.isStringified("bonjour")
=> true
var stringified = JSON.stringify({some:{nested:"value"}});
_.json.isStringified(stringified)
=> true
```
