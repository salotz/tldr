# dot

> A command-line tool to produce layered drawings of directed graphs.

- Render an image file and determine output filename based on input filename and selected format:

`dot -Tpng -O {{path/to/file.dot}}`

- Create an SVG from DOT file:

`dot -Tsvg -o {{path/to/out_file.svg}} {{path/to/file.dot}}`

- Apply the layout without rendering to `stdout`

`dot {{file.dot}}`

- Use another layout engine like `neato`

`neato {{file.dot}}`

