# Mermaid Quick Reference

**Flowchart:**
```mermaid
flowchart LR
    A[Start] --> B{Decision}
    B -->|Yes| C[Action]
    B -->|No| D[End]
```

**Sequence:**
```mermaid
sequenceDiagram
    User->>API: Request
    API->>DB: Query
    DB-->>API: Result
    API-->>User: Response
```

**ER Diagram:**
```mermaid
erDiagram
    USER ||--o{ ORDER : places
    ORDER ||--|{ ITEM : contains
```

# Style Guidelines

- **Left-to-right (LR)** for processes, **top-to-bottom (TB)** for hierarchies
- **Max 10-15 nodes** per diagram, split if larger
- **Consistent naming** — all caps for systems, lowercase for actions
- **Subgraphs** to group related components
- **Color sparingly** — highlight critical paths only
