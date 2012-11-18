# grid.less - The smallest LESS grid in the world.

grid.less supports unlimited nested grids with custom gutter width. Instead of
push and pull, it has a notion of reverse, where the source order is the reverse
of the display order.

Column widths are available in splits of 2, 3, 4, 5, 6, 8, 10, and 12.

Modify the `@gutter` LESS variable to adjust the gutter width; the default is
set to `1em`.

## Installation

Simply compile the grid.less file found in src/ with a LESS compiler and link
the resulting CSS file from your html.

## Sample usage

Two columns, one third of the left serves as the sidebar:

```html
<div class="grid">
    <div class="col col-1-3">
        <p>This is the sidebar</p>
    </div>
    <div class="col col-2-3">
        <p>This is the main content</p>
    </div>
</div>
```

Nested grids, two levels deep:

```html
<div class="grid">
    <div class="col col-1-2">
        <p>1/2</p>
    </div>
    <div class="col col-1-2">
        <div class="grid">
            <div class="col col-1-2">
                <p>1/4</p>
            </div>
            <div class="col col-1-2">
                <p>1/4</p>
            </div>
        </div>
    </div>
</div>
```

Reverse grid, displays like the first example but with source order reversed:

```html
<div class="grid grid-reverse">
    <div class="col col-2-3">
        <p>This is the main content</p>
    </div>
    <div class="col col-1-3">
        <p>This is the sidebar</p>
    </div>
</div>
```

## License

grid.less is released under the [MIT License][MIT].

## Acknowledgments

Heavily inspired by techniques from [CSS-Tricks][css-tricks] and [Boon][boon].

[MIT]: http://en.wikipedia.org/wiki/MIT_License
[boon]: http://builtbyboon.com/blog/proportional-grids
[css-tricks]: http://css-tricks.com/dont-overthink-it-grids/
