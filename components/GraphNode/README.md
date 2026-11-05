# GraphNode

A node in any graph, with a kind, a title and named ports.

Use `.sim-node`. Add `.sim-node--tall` for two port rows and `.sim-node--accent` for a node that calls the model or casts data. Add `.sim-port--sink` or `.sim-port--source` to name each port, `.sim-port--row2` for the second row, and `.sim-port--open` for a source left unwired. Set `aria-selected="true"` on the selected node.

The consumer positions nodes and draws edges from port to port in `arrow`. Sinks sit on the left and sources on the right. Keep port names short and lowercase.
