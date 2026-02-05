## Flowchart Part 7

### 73. Thick link

```mermaid
flowchart LR
  A ==> B
```

### 74. Thick link with text

```mermaid
flowchart LR
  A == text ==> B
```

### 75. An invisible link

```mermaid
flowchart LR
  A ~~~ B
```

### 76. Chaining of links

```mermaid
flowchart LR
   A -- text --> B -- text2 --> C
```

```mermaid
flowchart LR
  a --> b & c--> d
```

```mermaid
flowchart TB
  A & B--> C & D
```

```mermaid
flowchart TB
  A --> C
  A --> D
  B --> C
  B --> D
```

### 77. Attaching an ID to Edges

```mermaid
flowchart LR
  A e1@--> B
```

### 78. Turning an Animation On

```mermaid
flowchart LR
  A e1@==> B
  e1@{ animate: true }
```

### 79. Selecting Type of Animation

```mermaid
flowchart LR
  A e1@--> B
  e1@{ animation: fast }
```

### 80. Using classDef Statements for Animations

```mermaid
flowchart LR
  A e1@--> B
  classDef animate stroke-dasharray: 9,5,stroke-dashoffset: 900,animation: dash 25s linear infinite;
  class e1 animate
```

### 81. Circle edge example

```mermaid
flowchart LR
  A --o B
```

### 82. Circle edge example

```mermaid
flowchart LR
  A --x B
```

### 83. Multi directional arrows

```mermaid
flowchart LR
  A o--o B
  B <--> C
  C x--x D
```

### 84. Minimum length of a link

```mermaid
flowchart TD
  A[Start] --> B{Is it?}
  B -->|Yes| C[OK]
  C --> D[Rethink]
  D --> B
  B ---->|No| E[End]
```

```mermaid
flowchart TD
  A[Start] --> B{Is it?}
  B -- Yes --> C[OK]
  C --> D[Rethink]
  D --> B
  B -- No ----> E[End]
```

> Made with '\u{2665}' (♥) by Jesús Domínguez [@jdomingu19](https://github.com/jdomingu19)
