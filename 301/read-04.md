# Properties for the Parent


## Grid Container

## display
Defines the element as a grid container and establishes a new grid formatting context for its contents.

Values:

grid – generates a block-level grid
inline-grid – generates an inline-level grid

``.container {
  display: grid | inline-grid;
}``


## grid-template-columns
grid-template-rows
Defines the columns and rows of the grid with a space-separated list of values. The values represent the track size, and the space between them represents the grid line.

Values:

`<track-size>` – can be a length, a percentage, or a fraction of the free space in the grid (using the fr unit) <br>
`<line-name>` – an arbitrary name of your choosing <br>

![img](/assets/last.png)


## justify-items
Aligns grid items along the inline (row) axis (as opposed to align-items which aligns along the block (column) axis). This value applies to all grid items inside the container.

Values:

start – aligns items to be flush with the start edge of their cell <br>
end – aligns items to be flush with the end edge of their cell <br>
center – aligns items in the center of their cell  <br>
stretch – fills the whole width of the cell (this is the default) <br>

![img](/assets/last1.png)


# Properties for the Children 

## Grid Items

Note:<br>
float, display: inline-block, display: table-cell, vertical-align and column-* properties have no effect on a grid item. <br>

## grid-column-start
grid-column-end <br>
grid-row-start <br>
grid-row-end <br>
Determines a grid item’s location within the grid by referring to specific grid lines. grid-column-start/grid-row-start is the line where the item begins, and grid-column-end/grid-row-end is the line where the item ends.

Values:

`<line>` – can be a number to refer to a numbered grid line, or a name to refer to a named grid line <br>
span `<number>` - the item will span across the provided number of grid tracks <br>
span `<name>` – the item will span across until it hits the next line with the provided name <br>
auto – indicates auto-placement, an automatic span, or a default span of one <br>

![img](/assets/last2.png)


### Reference 
[grid](https://css-tricks.com/snippets/css/complete-guide-grid/)