# data-grid-cartograms

A curated collection of grid cartograms, in a machine readable format.

> A grid cartogram is a representation barely similar to a map, that distorts the forms and areas, and assigns to every subdivision one and only one unit of a grid. They are also referred as grid map, mosaic cartogram, pseudo-Demers cartogram, square cartograph maps, geofacets, geogrid, tile grid map, or tile map. For example, the following map represents every state of the United States by exactly one square in a rectangular grid:

![Example of a grid cartogram, with one cell by state](./docs/cartogram_us_example.png)

## Structure of this collection

The collected grid cartograms are stored in a directory structure that follows the pattern:

```
.
└── <whole>
    └── <parts>
        └── <name>
            ├── grid.csv
            ├── ids.csv
            └── README.md
```

Where:

- <whole> is the whole entity that the cartogram represents, such as "United States", "Europe", or "World".
- <parts> is the parts that the whole is divided into, such as "States", "Countries", or "Seats".
- <name> is the name of the cartogram
- `grid.csv` contains the grid cartogram as ASCII art. A filled cell is represented by an identifier. For readability, all the identifiers should have the same length and an empty cell should be contain the same number of spaces.
- `ids.csv` contains the mapping between the identifiers in `grid.csv` and the actual names of the parts. The first column contains the identifier, and the second column contains the name. Additional columns can be added for metadata.
- `README.md` contains a description of the cartogram, including the source, date, and any other relevant information.

## Read more on grid cartograms

https://observablehq.com/@severo/grid-cartograms

https://observablehq.com/collection/@severo/grid-maps
