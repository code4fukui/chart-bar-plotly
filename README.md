# chart-bar-plotly

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

A custom HTML element for creating bar charts using Plotly.js.

## Demo
The demo is available in the `index.html` and `script.html` files.

## Features
- Supports both vertical and horizontal bar charts
- Accepts data in various formats (JSON, CSV)
- Customizable options (width, height, legend, colors)

## Requirements
- [Plotly.js](https://plotly.com/) library

## Usage
To use the `<chart-bar>` element, include the `chart-bar.js` file and add the element to your HTML:

```html
<script type="module" src="./chart-bar.js"></script>
<chart-bar>
  name,count
  A,30
  B,20
  C,70
</chart-bar>
```

Alternatively, you can pass in data programmatically:

```javascript
import { ChartBar } from './chart-bar.js';

const data = {
  A: 30,
  B: 20,
  C: 70
};
const chart = new ChartBar(data);
document.getElementById('container').appendChild(chart);
```

You can also customize the chart options:

```javascript
const chart = new ChartBar(data, {
  width: 800,
  height: 600,
  orientation: 'h',
  legend: { position: 'right' }
});
```

## Data / API
This project can use data from various sources, including CSV files hosted online.

## License
MIT License — see [LICENSE](LICENSE).