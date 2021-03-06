
# Install

### To play with a grid

Get the source code
```bash
git clone https://github.com/firepick/vue-g-row-col.git
cd vue-g-row-col
npm install 
npm run dev
```

Launch browser http://localhost:4000/

### To use grid components in your own application

Install new package dependency:
```bash
npm install --save vue-g-row-col
```

Import the grid Vue component:
```js
const grid = require("vue-g-row-col");
```

Declare your new grid componets:
```js  
components: Object.assign({
    // your other components
    }, grid),
```

Now you can use `<g-row>` and `<g-col>`!


# Examples

<img src="https://raw.githubusercontent.com/firepick/vue-g-row-col/master/images/row-of-cols.png" height=200px>

```HTML
<g-row>
    <g-col>
        <g-header>City</g-header>
        <g-label>San Francisco</g-label>
        <g-label>Boston</g-label>
        <g-label>Atlanta</g-label>
    </g-col>
    <g-col>
        <g-header>Q3 Sales</g-header>
        <g-number>41.01</g-number>
        <g-number>223.02</g-number>
        <g-number>324.03</g-number>
    </g-col>
    <g-col>
        <g-header>Q4 Sales</g-header>
        <g-number>42.01</g-number>
        <g-number>123.02</g-number>
        <g-number>1,234.03</g-number>
    </g-col>
</g-row>
```

<img src="https://raw.githubusercontent.com/firepick/vue-g-row-col/master/images/rows-cols-rows.png" height=300px>

```HTML
<g-row><g-header>City</g-header>
    <g-row>
        <g-header class="grid-w-2">Quarter</g-header><g-header>Sales</g-header>
    </g-row>
</g-row>
<g-row>
    <g-label class="grid-h-2">San Francisco</g-label>
    <g-col>
        <g-row><g-label class="grid-w-2">Q3</g-label><g-number>41.01</g-number></g-row>
        <g-row><g-label class="grid-w-2">Q4</g-label><g-number>42.01</g-number></g-row>
    </g-col>
</g-row>
<g-row>
    <g-label class="grid-h-2">Boston</g-label>
    <g-col>
        <g-row><g-label class="grid-w-2">Q3</g-label><g-number>223.02</g-number></g-row>
        <g-row><g-label class="grid-w-2">Q4</g-label><g-number>123.02</g-number></g-row>
    </g-col>
</g-row>
<g-row>
    <g-label class="grid-h-2">Atlanta</g-label>
    <g-col>
        <g-row><g-label class="grid-w-2">Q3</g-label><g-number>324.03</g-number></g-row>
        <g-row><g-label class="grid-w-2">Q4</g-label><g-number>1234.03</g-number></g-row>
    </g-col>
</g-row>
```
