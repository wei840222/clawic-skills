# Common Requests

| Request | Interpret As |
|---------|--------------|
| "Draw my API flow" | Sequence diagram: client → API → services |
| "Show the architecture" | Flowchart with subgraphs for components |
| "Database schema" | ER diagram with relationships |
| "How the auth works" | Sequence or flowchart depending on complexity |
| "User journey" | Flowchart with decision points |

# Required Practices

- ✅ Maintain clarity by splitting complex diagrams into multiple smaller diagrams rather than using too many nodes
- ✅ Use icons only when they contribute meaningful semantic value
- ✅ Keep abstraction levels consistent (e.g. keep database tables separate from high-level business concepts)
- ✅ Ensure flow arrows follow a consistent direction (e.g. strict left-to-right or top-to-bottom)
- ✅ Keep labels short and concise; use a legend if extensive explanation is needed
