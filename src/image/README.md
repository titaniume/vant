# Image

### Install

``` javascript
import Vue from 'vue';
import { Image } from 'vant';

Vue.use(Image);
```

## Usage

### Basic Usage

```html
<van-image
  width="100"
  height="100"
  src="https://img.yzcdn.cn/vant/cat.jpeg"
/>
```

### Fit Mode

```html
<van-image
  width="10rem"
  height="10rem"
  fit="contain"
  src="https://img.yzcdn.cn/vant/cat.jpeg"
/>
```

### Round

Show round image, it may not works at `fit=contain` and `fit=scale-down`

```html
<van-image
  round
  width="10rem"
  height="10rem"
  src="https://img.yzcdn.cn/vant/cat.jpeg"
/>
```

### Lazy Load

```html
<van-image
  width="100"
  height="100"
  lazy-load
  src="https://img.yzcdn.cn/vant/cat.jpeg"
/>
```

```js
import { Lazyload } from 'vant';

Vue.use(Lazyload);
```

## API

### Props

| Attribute | Description | Type | Default | Version |
|------|------|------|------|------|
| src | Src | *string* | - | - |
| fit | Fit mode | *string* | `fill` | - |
| alt | Alt | *string* | - | - |
| width | Width | *string \| number* | - | - |
| height | Height | *string \| number* | - | - |
| radius | Border Radius | *string \| number* | `0` | 2.1.6 |
| round | Whether to be round | *boolean* | `false` | - |
| lazy-load | Whether to enable lazy load，should register [Lazyload](#/en-US/lazyload) component | *boolean* | `false` | - |
| show-error | Whether to show error placeholder | *boolean* | `true` | 2.0.9 |
| show-loading | Whether to show loading placeholder | *boolean* | `true` | 2.0.9 |
| error-icon | Error icon | *string* | `warning-o` | 2.4.2 |
| loading-icon | Loading icon | *string* | `photo-o` | 2.4.2 |

### fit optional value

| name | desctription |
|------|------|
| contain | Keep aspect ratio, fully display the long side of the image |
| cover | Keep aspect ratio, fully display the short side of the image, cutting the long side |
| fill | Stretch and resize image to fill the content box |
| none | Not resize image |
| scale-down | Take the smaller of `none` or `contain` |

### Events

| Event | Description | Arguments |
|------|------|------|
| click | Triggered when click image | event: Event |
| load | Triggered when image loaded | - |
| error | Triggered when image load failed | - |

### Slots

| Name | Description |
|------|------|
| loading | Custom loading placeholder |
| error | Custom error placeholder |
