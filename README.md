# [Distpicker](https://github.com/fengyuanchen/distpicker)

A jQuery plugin for picking provinces, cities and districts of China.

- [Documentation](http://fengyuanchen.github.io/distpicker)


# Getting started

## Quick start

Four quick start options are available:

- [Download the latest release](https://github.com/fengyuanchen/distpicker/archive/master.zip).
- Clone the repository: `git clone https://github.com/fengyuanchen/distpicker.git`.
- Install with [NPM](http://npmjs.org): `npm install distpicker`.
- Install with [Bower](http://bower.io): `bower install distpicker`.


## Installation

Include files:

```html
<script src="/path/to/jquery.js"></script><!-- jQuery is required -->
<script src="/path/to/distpicker.data.js"></script>
<script src="/path/to/distpicker.js"></script>
```

Create HTML elements:

```html
<div><!-- container -->
  <select></select><!-- province -->
  <select></select><!-- city -->
  <select></select><!-- district -->
</div>
```



## Usage

### Initialize with `data-distpicker` attribute

#### Basic

```html
<div data-distpicker>
  <select></select>
  <select></select>
  <select></select>
</div>
```

#### Custom placeholders
```html
<div data-distpicker>
  <select data-province="---- 选择省 ----"></select>
  <select data-city="---- 选择市 ----"></select>
  <select data-district="---- 选择区 ----"></select>
</div>
```

#### Custom districts

```html
<div data-distpicker>
  <select data-province="北京"></select>
  <select data-city="北京市"></select>
  <select data-district="朝阳区"></select>
</div>
```


### Initialize with `$.fn.distpicker` method

#### Basic
```javascript
$("#target").distpicker();
```

#### Custom placeholders

```javascript
$("#target").distpicker({
  province: "---- 所在省 ----",
  city: "---- 所在市 ----",
  district: "---- 所在区 ----"
});
```

#### Custom districts

```javascript
$("#target").distpicker({
  province: "北京",
  city: "北京市",
  district: "朝阳区"
});
```


## Options

#### autoSelect

- Type: `Boolean`
- Default: `true`

Selects the city and district automatically when the province changes.


#### placeholder

- Type: `Boolean`
- Default: `true`

Show placeholder option.


#### province

- Type: `String`
- Default: `—— 省 ——`

Set the default view of province. Maybe a placeholder or a really province under China.


#### city

- Type: `String`
- Default: `—— 市 ——`

Set the default view of city. Maybe a placeholder or a really city under the selected province.


#### district

- Type: `String`
- Default: `—— 区 ——`

Set the default view of district. Maybe a placeholder or a really district under the selected city.



## Methods

#### reset([deep])

Params | Type | Default | Description
------ | ---- | ------- | -----------
deep | `Boolean` | `false` | Undo changed

Reset the selects to default state.

**Examples:**

```javascript
$().distpicker('reset')
$().distpicker('reset', true)
```

#### destroy()

Destroy the distpicker instance, but keep the selected districts.

If you want to remove the selected districts, you can call `reset` method first and then call this method.



## Browser Support

- Chrome 33+
- Firefox 27+
- Internet Explorer 6+
- Opera 19+
- Safari 5.1+

As a jQuery plugin, you can reference to the [jQuery Browser Support](http://jquery.com/browser-support/).



## [License](https://github.com/fengyuanchen/distpicker/blob/master/LICENSE.md)

Released under the [MIT](http://opensource.org/licenses/mit-license.html) license.
