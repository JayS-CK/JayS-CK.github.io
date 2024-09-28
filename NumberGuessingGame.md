```mermaid
flowchart TD
A[Generate random number] --> B{Is number between 1-20?}
B --> |Yes| C[Continue]
B --> |No| D[Regenerate Number]
D --> A
```