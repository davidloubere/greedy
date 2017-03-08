# Greedy

A basic CSS grid system, fluid and responsive.

## Install

1. Copy the [`greedy.css`](https://github.com/davidloubere/greedy/blob/master/greedy.css) file into the web assets folder of your project.
2. Link to the stylesheet within the `<head>` section of the HTML page:

```html
<link rel="stylesheet" href="css/greedy.css" type="text/css">
```

## Usage

### Markup

```html
<div class="greedy">
    <div class="cake">
        <div class="layer">
            <div class="slice">
                <!-- Content goes here (tile, card, thumbnail etc.) -->
            </div>
        </div>
        <div class="layer">
            <div class="slice slice-half">
                <!-- Content goes here (tile, card, thumbnail etc.) -->
            </div>
            <div class="slice slice-quarter">
                <!-- Content goes here (tile, card, thumbnail etc.) -->
            </div>
            <div class="slice slice-quarter">
                <!-- Content goes here (tile, card, thumbnail etc.) -->
            </div>
        </div>
    </div>
</div>
```

### Grid options

#### Coating

To get padding around the grid, attach the `.coat` class:
```html
<div class="cake coat">
```

#### Gutters

To add default gutters to the grid, attach the `.gutter` class:
```html
<div class="cake gutter">
```

#### Coating along with gutters

You can apply coating and gutters options together:
```html
<div class="cake coat gutter">
```

### Customization

To customize gutters (including coating), begin with defining a custom class (`.gutter-8px` for instance) and add it to your markup:
```html
<div class="cake coat gutter gutter-8px">
```
Then, override Greedy CSS into your stylesheet as follow:
```css
.greedy .cake.gutter.gutter-8px .layer {
    margin: 8px -4px;
}
.greedy .cake.gutter.gutter-8px .layer .slice {
    padding: 0 4px;
}
.greedy .cake.gutter.gutter-8px.coat {
    padding: 8px;
}
@media (max-width: 767px) {
    .greedy .cake.gutter.gutter-8px .layer .slice {
        margin: 8px 0;
    }
}
```

## Examples

- [Basic examples](https://github.com/davidloubere/greedy/blob/master/docs/examples/basic/index.html)
- [Board example](https://github.com/davidloubere/greedy/blob/master/docs/examples/board/index.html)
