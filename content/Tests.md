This is an area used for testing different formats to be used in obsidian
## Diagrams

>[!Tip]
>You can also try Mermaid's [Live Editor](https://mermaid-js.github.io/mermaid-live-editor) to help you build diagrams before you include them in your notes.

```mermaid
sequenceDiagram
    Alice->>+John: Hello John, how are you?
    Alice->>+John: John, can you hear me?
    John-->>-Alice: Hi Alice, I can hear you!
    John-->>-Alice: I feel great!
```
```mermaid
graph TD

Biology --> Chemistry
```
### Diagrams with links

```mermaid
graph TD

Biology --> Chemistry

class Biology,Chemistry internal-link;
```
### Diagrams with many nodes + links
```mermaid
graph TD

A[Biology]
B[Chemistry]
C[History]
D[Math]
E[English]
F[Spanish]

A --> B
C --> D
D --> A

class A,B,C,D,E,F,G,H,I,J,K,L,M,N,O,P,Q,R,S,T,U,V,W,X,Y,Z internal-link;
```

