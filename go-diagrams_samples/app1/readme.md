## Prereqs

[Graphviz](https://graphviz.org/download/) needs to be installed. Then you'd have `dot` command available to use.

## Usage

- Run the code to generate the .dot file: `go run main.go`
- Create an image out of it:
    - `dot -Tpng app.dot > app.png` for a PNG
    - `dot -Tsvg app.dot > app.svg`

