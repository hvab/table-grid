# Table Grid

> Inspired by [@mdo/table-grid](https://github.com/mdo/table-grid) + BEMCSS

This is simple, responsive CSS grid system based on `display: table`. The typical approach is to create twelve fixed-width columns in all the usual combinations.

```html
<div class="grid">
  <div class="grid__cell">Cell</div>
  <div class="grid__cell">Cell</div>
</div>
```

## Usage

```html
<link rel="stylesheet" href="table-grid.css">
```

```css
.grid /* container for cells */
.grid__cell /* simple cell */
```

```html
<div class="grid">
  <div class="grid__cell grid__cell_size_8">8</div>
  <div class="grid__cell grid__cell_size_4">4</div>
</div>
```

Fixed table layouts render equal-width columns when no other width is set.

See [demo](https://hobcode.github.io/table-grid/).

### Sizes

```css
.grid__cell_size_1 { width: 8.333333%; }
.grid__cell_size_2 { width: 16.666667%; }
.grid__cell_size_3 { width: 25%; }
.grid__cell_size_4 { width: 33.333333%; }
.grid__cell_size_5 { width: 41.666667%; }
.grid__cell_size_6 { width: 50%; }
.grid__cell_size_7 { width: 58.333333%; }
.grid__cell_size_8 { width: 66.666667%; }
.grid__cell_size_9 { width: 75%; }
.grid__cell_size_10 { width: 83.333333%; }
.grid__cell_size_11 { width: 91.666667%; }
```

### Nested

```html
<div class="grid">
  <div class="grid__cell grid__cell_size_8">
    8
    <div class="grid">
      <div class="grid__cell">Cell</div>
      <div class="grid__cell">Cell</div>
    </div>
  </div>
  <div class="grid__cell grid__cell_size_4">4</div>
</div>
```

### Grids with gutters

```html
<div class="grid grid_padded">
  <div class="grid__cell">Cell</div>
  <div class="grid__cell">Cell</div>
  <div class="grid__cell">Cell</div>
</div>
```

### Vertically center content

Requires the use of `inline`, `inline-block`, or `table` based elements within a cell.

```html
<div class="grid grid_middle">
  <div class="grid__cell">
    Free-form text wraps while remaining vertically centered.
  </div>
  <div class="grid__cell">
    Nested cell center, too.
      <div class="grid">
        <div class="grid__cell">Cell</div>
        <div class="grid__cell">Cell</div>
      </div>
  </div>
  <div class="grid__cell">
    <div class="grid-example__inline-block">A `div` with `inline-block` works great, too.</div>
  </div>
</div>
```

### Reverse cell sorting

```html
<div class="grid grid_reverse">
  <div class="grid__cell">Cell 1</div>
  <div class="grid__cell">Cell 2</div>
</div>
```
