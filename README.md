# Hello, Mermaid!

![Static Badge](https://img.shields.io/badge/documentation-markdown-000?style=for-the-badge&logo=markdown&logoColor=white&labelColor=101010)
![Static Badge](https://img.shields.io/badge/diagrams-mermaid-FF3670?style=for-the-badge&logo=mermaid&logoColor=white&labelColor=101010)

> This repository is licensed under the terms of the [Apache License 2.0](LICENSE).


## Diagram Types

### 1. Flowchart

```mermaid
graph TD;
  A-->B;
  A-->C;
  B-->D;
  C-->D;
```

### 2. Sequence diagram

```mermaid
sequenceDiagram
  participant Alice
  participant Bob
  Alice->>John: Hello John, how are you?
  loop HealthCheck
    John->>John: Fight against hypochondria
  end
  Note right of John: Rational thoughts <br/>prevail!
  John-->>Alice: Great!
  John->>Bob: How about you?
  Bob-->John: Jolly good!
```

### 3. Gantt diagram

```mermaid
gantt
dateFormat YYYY-MM-DD
title Adding GANTT diagram to mermaid
excludes weekdays 2026-01-10

section A section
Completed task  : done, des1, 2026-01-06, 2026-01-08
Active task     : active, des2, 2026-01-09, 3d
Future task     : des3, after des2, 5d
Future task2    : des4, after des3, 5d
```

### 4. Class diagram

```mermaid
classDiagram
Class01 <|-- AVeryLongClass : Cool
Class03 *-- Class04
Class05 o-- Class06
Class07 .. Class08
Class09 --> C2 : Where am I?
Class09 --* C3
Class09 --|> Class07
Class07 : equals()
Class07 : Object[] elementData
Class01 : size()
Class01 : int chimp
Class01 : int gorilla
Class08 <--> C2: Cool label
```

### 5. Git Graph

```mermaid
gitGraph
  commit
  commit
  branch develop
  commit
  commit
  commit
  checkout main
  merge develop
  commit
  commit
```

### 6. Entity Relationship Diagram - Experimental

```mermaid
erDiagram
  CUSTOMER ||--o{ ORDER : places
  ORDER ||--|{ LINE-ITEM : contains
  CUSTOMER }|..|{ DELIVERY-ADDRESS : uses
```

### 7. User Journey Diagram

```mermaid
journey
  title My working day
  section Go to work
    Make tea : 3 : Me
    Go upstairs : 4 : Me
    Do work :  5 : Me, Cat
  section Go home
    Go downstairs : 5 : Me
    Sit down : 5 : Me
```

### 8. Quadrant Chart

```mermaid
quadrantChart
  title Reach and engagement of campaigns
  x-axis Low Reach --> High Reach
  y-axis Low Engagement --> High Engagement
  quadrant-1 We should expand
  quadrant-2 Need to promote
  quadrant-3 Re-evaluate
  quadrant-4 May be improved
  Campaign A: [0.3, 0.6]
  Campaign B: [0.45, 0.23]
  Campaign C: [0.57, 0.69]
  Campaign D: [0.78, 0.34]
  Campaign E: [0.40, 0.34]
  Campaign F: [0.35, 0.78]
```

### 9. XY Chart

```mermaid
xychart-beta
  title "Sales Revenue"
  x-axis [jan, feb, mar, apr, may, jun, jul, aug, sep, oct, nov, dec]
  y-axis "Revenue (in $)" 4000 --> 11000
  bar [5000, 6000, 7500, 8200, 9500, 10500, 11000, 10200, 9200, 8500, 7000, 6000]
  line [5000, 6000, 7500, 8200, 9500, 10500, 11000, 10200, 9200, 8500, 7000, 6000]
```

## Getting Started

### 1. Basic Workflow

```mermaid
graph TD
  A[Enter Chart Definition] --> B(Preview)
  B --> C{decide}
  C --> D[Keep]
  C --> E[Edit Definition]
  E --> B
  D --> F[Save Image and Code]
  F --> B
```

## Syntax and Configuration

### 1. Syntax Structure

```mermaid
erDiagram
  CUSTOMER }|..|{ DELIVERY-ADDRESS : has
  CUSTOMER ||--o{ ORDER : places
  CUSTOMER ||--o{ INVOICE : "liable for"
  DELIVERY-ADDRESS ||--o{ ORDER : receives
  INVOICE ||--|{ ORDER : covers
  ORDER ||--|{ ORDER-ITEM : includes
  PRODUCT-CATEGORY ||--|{ PRODUCT : contains
  PRODUCT ||--o{ ORDER-ITEM : "ordered in"
```

### 2. Frontmatter for diagram code

```mermaid
---
title: Frontmatter Example
displayMode: compact
config:
  theme: forest
gantt:
    useWidth: 400
    compact: true
---
gantt
    section Waffle
        Iron  : 1982, 3y
        House : 1986, 3y
```

### 3. Selecting Diagram Looks

```mermaid
---
config:
  look: handDrawn
  theme: neutral
---
flowchart LR
  A[Start] --> B{Decision}
  B -->|Yes| C[Continue]
  B -->|No| D[Stop]
```

### 4. Selecting Layout Algorithms

```mermaid
---
config:
  layout: elk
  look: handDrawn
  theme: dark
---
flowchart TB
  A[Start] --> B{Decision}
  B -->|Yes| C[Continue]
  B -->|No| D[Stop]
```

```mermaid
---
config:
  layout: elk
  elk:
    mergeEdges: true
    nodePlacementStrategy: LINEAR_SEGMENTS
---
flowchart LR
  A[Start] --> B{Choose Path}
  B -->|Option 1| C[Path 1]
  B -->|Option 2| D[Path 2]
```

```mermaid
---
config:
  layout: dagre
  look: classic
  theme: default
---

flowchart LR
  A[Start] --> B{Choose Path}
  B -->|Option 1| C[Path 1]
  B -->|Option 2| D[Path 2]
```

## Flowchart

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

### 13. A hexagon node

```mermaid
flowchart LR
  id1{{This is the text in the box}}
```

### 14. Parallelogram

```mermaid
flowchart TD
  id1[/This is the text in the box/]
```

### 15. Parallelogram alt

```mermaid
flowchart TD
  id1[\This is the text in the box\]
```

### 16. Trapezoid

```mermaid
flowchart TD
  A[/Christmas\]
```

### 17. Trapezoid alt

```mermaid
flowchart TD
  B[\Go shopping/]
```

### 18. Double circle

```mermaid
flowchart TD
  id1(((This is the text in the circle)))
```

### 19. Example Flowchart with New Shapes

```mermaid
flowchart RL
  A@{ shape: manual-file, label: "File Handling"}
  B@{ shape: manual-input, label: "User Input"}
  C@{ shape: docs, label: "Multiple Documents"}
  D@{ shape: procs, label: "Process Automation"}
  E@{ shape: paper-tape, label: "Paper Records"}
```

### 20. Process

```mermaid
flowchart TD
  A@{ shape: rect, label: "This is a process" }
```

### 21. Event

```mermaid
flowchart TD
    A@{ shape: rounded, label: "This is an event" }
```

### 22. Terminal Point (Stadium)

```mermaid
flowchart TD
  A@{ shape: stadium, label: "Terminal point" }
```

### 23. Subprocess

```mermaid
flowchart TD
  A@{ shape: subproc, label: "This is a subprocess" }
```

### 24. Database (Cylinder)

```mermaid
flowchart TD
  A@{ shape: cyl, label: "Database" }
```

### 25. Start (Circle)

```mermaid
flowchart TD
  A@{ shape: circle, label: "Start" }
```

### 26. Odd

```mermaid
flowchart TD
  A@{ shape: odd, label: "Odd shape" }
```

### 27. Decision (Diamond)

```mermaid
flowchart TD
  A@{ shape: diamond, label: "Decision" }
```

### 28. Prepare Conditional (Hexagon)

```mermaid
flowchart TD
  A@{ shape: hex, label: "Prepare conditional" }
```

### 29. Data Input/Output (Lean Right)

```mermaid
flowchart TD
  A@{ shape: lean-r, label: "Input/Output" }
```

### 30. Data Input/Output (Lean Left)

```mermaid
flowchart TD
  A@{ shape: lean-l, label: "Output/Input" }
```

### 31. Priority Action (Trapezoid Base Bottom)

```mermaid
flowchart TD
  A@{ shape: trap-b, label: "Priority action" }
```

### 32. Manual Operation (Trapezoid Base Top)

```mermaid
flowchart TD
  A@{ shape: trap-t, label: "Manual operation" }
```

### 33. Manual Operation (Trapezoid Base Top)

```mermaid
flowchart TD
  A@{ shape: dbl-circ, label: "Stop" }
```

### 34. Text Block

```mermaid
flowchart TD
  A@{ shape: text, label: "This is a text block" }
```

### 35. Card (Notched Rectangle)

```mermaid
flowchart TD
  A@{ shape: notch-rect, label: "Card" }
```

### 36. Lined/Shaded Process

```mermaid
flowchart TD
  A@{ shape: lin-rect, label: "Lined process" }
```

### 37. Start (Small Circle)

```mermaid
flowchart TD
  A@{ shape: sm-circ, label: "Small start" }
```

### 38. Stop (Framed Circle)

```mermaid
flowchart TD
  A@{ shape: framed-circle, label: "Stop" }
```

### 39. Fork/Join (Long Rectangle)

```mermaid
flowchart TD
  A@{ shape: fork, label: "Fork or Join" }
```

### 40. Collate (Hourglass)

```mermaid
flowchart TD
  A@{ shape: hourglass, label: "Collate" }
```

### 41. Comment (Curly Brace)

```mermaid
flowchart TD
  A@{ shape: comment, label: "Comment" }
```

### 42. Comment Right (Curly Brace Right)

```mermaid
flowchart TD
  A@{ shape: brace-r, label: "Comment" }
```

### 43. Comment with braces on both sides

```mermaid
flowchart TD
  A@{ shape: braces, label: "Comment" }
```

### 44. Com Link (Lightning Bolt)

```mermaid
flowchart TD
  A@{ shape: bolt, label: "Communication link" }
```

### 45. Document

```mermaid
flowchart TD
  A@{ shape: doc, label: "Document" }
```

### 46. Delay (Half-Rounded Rectangle)

```mermaid
flowchart TD
  A@{ shape: delay, label: "Delay" }
```

### 47. Direct Access Storage (Horizontal Cylinder)

```mermaid
flowchart TD
  A@{ shape: das, label: "Direct access storage" }
```

### 48. Disk Storage (Lined Cylinder)

```mermaid
flowchart TD
  A@{ shape: lin-cyl, label: "Disk storage" }
```

### 49. Display (Curved Trapezoid)

```mermaid
flowchart TD
  A@{ shape: curv-trap, label: "Display" }
```

### 50. Divided Process (Divided Rectangle)

```mermaid
flowchart TD
  A@{ shape: div-rect, label: "Divided process" }
```

### 51. Extract (Small Triangle)

```mermaid
flowchart TD
  A@{ shape: tri, label: "Extract" }
```

### 52. Internal Storage (Window Pane)

```mermaid
flowchart TD
  A@{ shape: win-pane, label: "Internal storage" }
```

### 53. Junction (Filled Circle)

```mermaid
flowchart TD
  A@{ shape: f-circ, label: "Junction" }
```

### 54. Lined Document

```mermaid
flowchart TD
  A@{ shape: lin-doc, label: "Lined document" }
```

### 55. Loop Limit (Notched Pentagon)

```mermaid
flowchart TD
  A@{ shape: notch-pent, label: "Loop limit" }
```

### 56. Manual File (Flipped Triangle)

```mermaid
flowchart TD
  A@{ shape: flip-tri, label: "Manual file" }
```

### 57. Manual Input (Sloped Rectangle) 

```mermaid
flowchart TD
  A@{ shape: sl-rect, label: "Manual input" }
```

### 58. Multi-Document (Stacked Document)

```mermaid
flowchart TD
  A@{ shape: docs, label: "Multiple documents" }
```

### 59. Multi-Document (Stacked Document)

```mermaid
flowchart TD
  A@{ shape: processes, label: "Multiple processes" }
```

### 60. Paper Tape (Flag)

```mermaid
flowchart TD
  A@{ shape: flag, label: "Paper tape" }
```

### 61. Stored Data (Bow Tie Rectangle)

```mermaid
flowchart TD
  A@{ shape: bow-rect, label: "Stored data" }
```

### 62. Summary (Crossed Circle)

```mermaid
flowchart TD
  A@{ shape: cross-circ, label: "Summary" }
```

### 63. Tagged Document 

```mermaid
flowchart TD
  A@{ shape: tag-doc, label: "Tagged document" }
```

### 64. Tagged Process (Tagged Rectangle)

```mermaid
flowchart TD
  A@{ shape: tag-rect, label: "Tagged process" }
```



> Made with '\u{2665}' (♥) by Jesús Domínguez [@bluefeatherdev](https://github.com/bluefeatherdev)
