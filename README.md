## MiniColorPicker

<center>

*A simple lightweight color picker component*

![ScreenShot](https://raw.github.com/jjssman/MiniColorPicker/master/docs/img/screenie.png)

</center>

### Usage

You can either clone this repository or download the latest build as a zip from: 
[https://github.com/jjssman/MiniColorPicker/zipball/master](https://github.com/jjssman/MiniColorPicker/zipball/master)

Include it in your code:

```html
<script type="module" src="minicolorpicker.min.js"></script>

<link href="minicolorpicker.css" rel="stylesheet"/>
```

You can then bind the component to any HTML element:

```html
<div id="container"></div>

<script language="javascript">
    (function() {
        let cp = new MiniColorPicker({ element: document.getElementById('container') });
    })();
</script>
```

### Options

There are some options you can set at the time of binding.

**Color Palette**

You can override the default color palette by passing your own color values.

```javascript
let cp = new MiniColorPicker({
  element: el,
  colors: [
    ['red', 'blue', 'yellow', 'orange', 'purple', 'green', 'brown'],
    ['#7B241C', '#5B2C6F ', '#0E6655', '#9C640C', '#797D7F', '#1C2833'],
    ['rgb(230, 176, 170)', 'rgb(210, 180, 222)', 'rgb(253, 235, 208)'] 
  ]
});
```

**Reset Button**

The reset color button can be hidden, and its default text changed.

```javascript
let cp = new MiniColorPicker({
  element: el,
  resetButton: true,
  resetButtonText: 'Restaurar color original'
});
```

### Events

The component has some events you can listen to.

**OnColorSelect**
```javascript
cp.onColorSelect((color) => {
    console.log('New color selected: '+color);
});
```

**OnColorReset**
```javascript
cp.onColorReset(() => {
	console.log('Color has been reset');
});
```
## Demo

[https://jjssman.github.io/MiniColorPicker/docs/demo.html](https://jjssman.github.io/MiniColorPicker/docs/demo.html)

### Issues & Suggestions

Please report any bugs or feature requests here: [https://github.com/jjssman/MiniColorPicker/issues](https://github.com/jjssman/MiniColorPicker/issues)
