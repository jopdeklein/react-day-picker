---
layout: docs
title: Styling
permalink: docs/styling.html
redirect_from: 
  - /Styling.html
  - /docs/css-modules.html
---

You should style the component from your own stylesheet: start from [src/style.css](https://github.com/gpbl/react-day-picker/blob/master/src/style.css) as template, copy it in a new CSS file and update it to fit the desired style.

> The CSS classes follow a [BEM-like syntax](https://css-tricks.com/bem-101/). If you need to customize the CSS class names, use the [`classNames`](api-daypicker.md#classnames) prop. Using this prop you can also import a [CSS Module](#css-modules).

### Modifiers

Modifiers added to react-day-picker via the `modifiers` prop becomes CSS modifiers for the `DayPicker-day` class. For example, if you use a `isFirstDayOfMonth` modifier, the CSS class for the matched day cells will be `DayPicker-day--isFirstDayOfMonth`.

### Importing the style template

You can also import and extend the CSS template in your Sass files, for example from `node_modules`:

```css
@import "../node_modules/react-day-picker/lib/style"
```

or in your JS files (e.g. when using [webpack-css-loader](https://github.com/webpack/css-loader)):

```js
import "react-day-picker/lib/style.css";
```

Keep in mind the default style is not production-tested and may change between releases.

<a name="css-modules"></a>

## Styling with CSS Modules

Once you have setup your build system to import [CSS Modules](https://github.com/css-modules/css-modules), use the [classNames prop](api-daypicker.md#classnames) to pass to the component the imported styles:

```jsx
import React from 'react';
import DayPicker from 'react-day-picker';

import styles from '../styles/cssmodules.css';

export default function CSSModules() {
  return <DayPicker classNames={ styles } />
}
```