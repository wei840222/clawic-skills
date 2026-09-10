# Diagram Types

| Type | Use For | Format |
|------|---------|--------|
| Flowchart | Processes, decisions, workflows | Mermaid `flowchart` |
| Sequence | API calls, interactions, protocols | Mermaid `sequenceDiagram` |
| Architecture | System components, infrastructure | Mermaid `flowchart` or `C4` |
| ER/Data model | Database schemas, relationships | Mermaid `erDiagram` |
| Class | Object structure, inheritance | Mermaid `classDiagram` |
| State | Lifecycles, status transitions | Mermaid `stateDiagram-v2` |
| Timeline | Project phases, history | Mermaid `timeline` |
| Mindmap | Brainstorming, concept mapping | Mermaid `mindmap` |

# Output Methods

| Method | When |
|--------|------|
| Mermaid code block | User can render (docs, GitHub, Notion) |
| Render to PNG/SVG | User needs image file |
| ASCII inline | Quick sketch in chat |
| HTML + Mermaid.js | Interactive viewing |

### Rendering Mermaid to Image

```bash
# Using mmdc (mermaid-cli)
npx -y @mermaid-js/mermaid-cli mmdc -i diagram.mmd -o diagram.png -b transparent

# Or via browser tool
# Write HTML with Mermaid, screenshot the rendered diagram
```

### Rendering PlantUML to Image

If PlantUML is requested, you may output the PlantUML text block directly (e.g. ` ```plantuml `). To render it, the user typically requires the PlantUML jar or a server:

```bash
java -jar plantuml.jar diagram.puml
```
