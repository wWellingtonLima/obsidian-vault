---
tags:
  - area
links: "[[My Area]]"
---
## Não começados
```dataview
table Status, Deadline
from [[]] AND #project 
where contains(Status, "🔴")
```

## Em Progresso
```dataview
table Status, Deadline
from "1. Projects" AND #project 
where contains(Status, "🟡")
```
