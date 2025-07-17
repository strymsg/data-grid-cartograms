# data-grid-cartograms

A curated collection of grid cartograms, in a machine readable format.

> A grid cartogram is a representation barely similar to a map, that distorts the forms and areas, and assigns to every subdivision one and only one unit of a grid. They are also referred as grid map, mosaic cartogram, pseudo-Demers cartogram, square cartograph maps, geofacets, geogrid, tile grid map, or tile map. For example, the following map represents every state of the United States by exactly one square in a rectangular grid:

![Example of a grid cartogram, with one cell by state](./docs/cartogram_us_example.png)

## Structure of this collection

The collected grid cartograms are stored in a directory structure that follows the pattern:

```
.
└── <category>
    └── <whole>
        └── <parts>
            └── <name>
                ├── grid.csv
                ├── ids.csv
                └── README.md
```

Where:

- <category> is a broad category of the cartogram, such as "continents" or "countries".
- <whole> is the whole entity that the cartogram represents, such as "us", "africa", or "world".
- <parts> is the parts that the whole is divided into, such as "States", "Countries", or "Seats".
- <name> is the name of the cartogram
- `grid.csv` contains the grid cartogram as ASCII art. A filled cell is represented by an identifier. For readability, all the identifiers should have the same length and an empty cell should be contain the same number of spaces. For countries or states, the identifier can be the ISO 3166-1 alpha-2 or alpha-3 code.
- `ids.csv` contains the mapping between the identifiers in `grid.csv` and the actual names of the parts. The first column contains the identifier, and the second column contains the name. Additional columns can be added for metadata.
- `README.md` contains a description of the cartogram, including the source, date, and any other relevant information.

## Contribute

You want to signal a grid cartogram should be added to the collection? Please open an [issue](https://github.com/severo/data-grid-cartograms/issues/new?template=propose-a-new-grid-cartogram.md) and paste the reference URL. We will then take care of transcribing it to the ASCII-art data format.

You want to add the data for a grid cartogram? Open a [pull request](https://github.com/severo/data-grid-cartograms/pulls) where you add a new directory to the collection. Take care of following the [structure](#structure-of-this-collection) and the formats of `grid.csv` and `ids.csv`.

Other ideas? Open an issue or a pull request and let's discuss!

## Read more on grid cartograms

https://observablehq.com/@severo/grid-cartograms

https://observablehq.com/collection/@severo/grid-maps
