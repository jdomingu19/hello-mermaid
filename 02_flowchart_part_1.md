
## Flowchart Part 1

### 1. A node (default)

```mermaid
---
title: Node
---
flowchart LR
  id
```

### 2. A node with text

```mermaid
---
title: Node with text
---
flowchart LR
  id1[This is the text in the box]
```

### 3. Unicode text

```mermaid
flowchart LR
  id["This ❤ Unicode"]
```

### 4. Markdown formatting

```mermaid
---
config:
  flowchart:
    htmlLabels: false
---
flowchart LR
  markdown["`This **is** _Markdown_`"]
  newLines["`Line1
  Line 2
  Line 3`"]
  markdown --> newLines
```

### 5. Direction

```mermaid
flowchart TD
  Start --> Stop
```

```mermaid
flowchart TB
  Start --> Stop
```

```mermaid
flowchart BT
  Start --> Stop
```

```mermaid
flowchart RL
  Start --> Stop
```

```mermaid
flowchart LR
  Start --> Stop
```

### 6. A node with round edges

```mermaid
flowchart LR
  id1(This is the text in the box)
```

### 7. A stadium-shaped node

```mermaid
flowchart LR
  id1([This is the text in the box])
```

### 8. A node in a subroutine shape

```mermaid
flowchart LR
  id1[[This is the text in the box]]
```

### 9. A node in a cylindrical shape

```mermaid
flowchart LR
  id1[(Database)]
```

### 10. A node in the form of a circle

```mermaid
flowchart LR
  id1((This is the text in the circle))
```

### 11. A node in an asymmetric shape

```mermaid
flowchart LR
  id1>This is the text in the box]
```

### 12. A node (rhombus)

```mermaid
flowchart LR
  id1{This is the text in the box}
```
> Made with '\u{2665}' (♥) by Jesús Domínguez [@bluefeatherdev](https://github.com/bluefeatherdev)

