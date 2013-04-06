# DataBind.js 0.1.0 [Download](https://github.com/grnadav/databind/archive/master.zip)

## About

DataBind is a 2-way data binding library.
It lets you easily bind a DOM element (and optionally its subtree) to a Model (Object) and keep them at sync.

### Dependencies
It's only dependency is [Watch.JS](https://github.com/melanke/Watch.JS)


##Compatible with all serious browsers :P
Works with: IE 9+, FF 4+, SF 5+, WebKit, CH 7+, OP 12+

#### HTML Script TAG
```html
<script src="DataBind.js" type="text/javascript"></script>
<!-- DataBind will be global variable window.DataBind -->
```

#### RequireJS
```javascript
require("DataBind", function(DataBind){
    var bind = DataBind.bind;
    var unbind = DataBind.unbind;
});
```

# Examples
```html
<textarea   data-key="k1" id="id1" rows="5" cols="30"></textarea>
```

```javascript
var model = {
    k1: 'Some text'
};
DataBind.bind( document.getElementById('id1'), model );
```

## Allow deep key bindings
```html
<textarea   data-key="k1.x" id="id1" rows="5" cols="30"></textarea>
```

```javascript
var model = {
    k1: {
        x: 'Some text'
    }
};
DataBind.bind( document.getElementById('id1'), model );
```
