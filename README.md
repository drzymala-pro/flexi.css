# flexi.css
Minimalistic CSS layout library

## Usage:
There are only three style classes available in this stylesheet:

1. ***flexi-rows*** - Display children in a top-down fashion, like rows.
2. ***flexi-columns*** - Display children from left to right, like columns.
3. ***flexi-expand*** - Make the given element take as much space as possible.

### Examples
#### Display the page as three columns
```html
<link rel="stylesheet" href="flexi.css">
<style>
    .red { background-color: red; }
    .green { background-color: green; }
    .blue { background-color: blue; }
</style>
<div class="flexi-rows">
    <div class="flexi-columns flexi-expand">
        <div class="flexi-expand red">1</div>
        <div class="flexi-expand green">2</div>
        <div class="flexi-expand blue">3</div>
    </div>
</div>
```
First we define a rows container, so that we can **expand** the row to fill the page height. The row inside is a columns container. It contains three **div** elements, which we all **expand**, so they split the available space in three same-sized columns.

#### Display content in the center of a page:
```html
<link rel="stylesheet" href="flexi.css">
<style>
    .red { background-color: red; }
    .green { background-color: green; }
    .blue { background-color: blue; }
    .cyan { background-color: cyan; }
    .orange { background-color: orange; }
</style>
<div class="flexi-columns">
    <div class="flexi-expand red"></div>
    <div class="flexi-rows green">
        <div class="flexi-expand cyan"></div>
        <div style="border: 2px solid;">Center row</div>
        <div class="flexi-expand orange"></div>
    </div>
    <div class="flexi-expand blue"></div>
</div>

```
The code above creates three columns. The left and right column is expanding, which places the middle column in the center of the page. Then, inside the middle column there are three rows. The top and bottom row is expanding, so the middle row gets placed in the middle of the screen.

## Responsiveness
The flexi.css is responsive in a minimal way. On screens which width is smaller than 600px, the columns are displayed as rows and the content gets centered in the screen.

## Instalation
Just download the **flexi.css** file and include to your html code:
```html
  <link rel="stylesheet" href="flexi.css">
```

## Requirements
**flexi.css** will work with web browsers which support *flex-box* stylesheets:

| Chrome | IE / Edge | Firefox | Safari | Opera |
|--------|-----------|---------|--------|-------|
| 29.0   | 11.0      | 28.0    | 9.0    | 17.0  |

It is recommended to use normalization stylesheet to ensure the page will be laid out the same way in every browser. This one is sufficient: [necolas/normalize.css](github.com/necolas/normalize.css)

