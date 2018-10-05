# ti.detect
A simple titanium library which detects things for you.

Right now it _only_ contains wether or not the current iPhone has a notch.

## Including it
Just require the library in `alloy.js`, nothing else is needed.

```js
require('ti.detect');
```

## Generated CFG / Reference
When you have required the library, CFG will be prefilled for you as follows

```json
{
    "statusbarHeight": 20 // or 44 when device has a notch
    "hasNotch": false // or true
}
```

## How to use it
You can access any property like this:

```Alloy.CFG.TiDetect.statusbarHeight```

So this is useful if you want to avoid the statusbar, regardless wether or not there is a notch, for example this tss

```
"#statusBar": {
    top: 0,
    height: Alloy.CFG.TiDetect.statusbarHeight,
    backgroundColor: "#777"
}
```
