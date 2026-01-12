
## Flowchart Part 6

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

### 65. Icon Shape

```mermaid
flowchart TD
  A@{ icon: "fa:user", form: "square", label: "User Icon", pos: "t", h: 60 }
```

### 66. Image Shape

```mermaid
flowchart TD
  A@{ img: "https://placehold.co/60x60", label: "Image Label", pos: "t", w: 60, h: 60, constraint: "off" }
```

```mermaid
flowchart TD
  %% My image with a constrained aspect ratio
  A@{ img: "https://mermaid.js.org/favicon.svg", label: "My example image label", pos: "t", h: 60, constraint: "on" }
```

### 67. A link with arrow head

```mermaid
flowchart LR
  A-->B
```

### 68. An open link

```mermaid
flowchart LR
  A --- B
```

### 69. Text on links

```mermaid
flowchart LR
  A-- This is the text! ---B
```

```mermaid
flowchart LR
  A---|This is the text|B
```

### 70. A link with arrow head and text

```mermaid
flowchart LR
  A-->|text|B
```

```mermaid
flowchart LR
  A-- text -->B
```

### 71. Dotted link

```mermaid
flowchart LR
  A-.->B;
```

### 72. Dotted link with text

```mermaid
flowchart LR
  A-. text .-> B
```

> Made with '\u{2665}' (♥) by Jesús Domínguez [@bluefeatherdev](https://github.com/bluefeatherdev)
