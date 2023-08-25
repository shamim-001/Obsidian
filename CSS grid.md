#grid 
# code
```css
.grid-container {
	display: grid;

	place-items: center; [justify-item & align-item: center]

	grid-template-columns: 1fr 2fr 1fr;

	grid-template-columns: repeat(3,1fr);
	grid-template-columns: 1fr 2fr 1fr;
	
	gap: 10px 20px; [row column]
	
	grid-template-areas: "main"
	"sidebar"
	
}

.grid-item {
	grid-area: main; 
}
```

# grid vs flex:
In practice, you can often combine CSS Grid and Flexbox to achieve more advanced and flexible layouts. For example, you can use CSS Grid to create the overall grid structure and then use Flexbox to handle the alignment and distribution of items within each grid cell.

CSS Grid is a two-dimensional layout system that allows you to create complex grid-based layouts. It divides the available space into rows and columns, and you have precise control over the placement and sizing of grid items within the grid. You can define explicit rows and columns, and also create named grid areas for more advanced layout structures. CSS Grid is especially useful when you need to create grid-like structures or when you have a complex layout with multiple rows and columns. It provides powerful features for both horizontal and vertical alignment of items.

Flexbox, on the other hand, is a one-dimensional layout system that focuses on arranging items along a single axis, either horizontally or vertically. It provides a flexible way to distribute space and align items within a container. Flexbox is particularly useful for creating responsive layouts and handling the alignment and ordering of items within a row or column. It simplifies the process of creating flexible and dynamic layouts, especially when dealing with single-directional layouts.

# properties

- `grid-template-rows` and `grid-template-columns`: Specifies the size and number of rows and columns in the grid.
  
- `grid-row` and `grid-column`: Controls the placement of grid items within specific rows and columns.
  
- `grid-area`: Assigns a grid item to a named grid area.
- `grid-gap`: Sets the gap between grid items.
  
- `grid-template-areas`: Defines named grid areas and assigns them to grid items.
  
- `grid-auto-rows` and `grid-auto-columns`: Sets the size of implicitly created rows and columns.