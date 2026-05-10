<div align="center">
  <h1 align="center">✦ system & architecture ✦</h1>
  <p align="center">
    <i style="color: #666;">crafting resilient systems • network protocols • elegant logic</i>
  </p>
</div>

---

### ⚗️ Topology

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#FAF8F5', 'primaryTextColor': '#2D2A26', 'primaryBorderColor': '#DCD6CC', 'lineColor': '#A39E93', 'secondaryColor': '#E8E4DB', 'tertiaryColor': '#F0EBE1'}}}%%
graph LR;
    A([Client]) -->|HTTPS| B(API Gateway);
    B --> C{Load Balancer};
    C -->|gRPC| D[Core Service];
    C -->|REST| E[Analytics];
    D --> F[(Primary DB)];
    E --> F;
    E --> G[(Redis)];
    
    classDef default fill:#FAF8F5,stroke:#DCD6CC,stroke-width:1px,color:#2D2A26;
    classDef accent fill:#E8E4DB,stroke:#CFC8BD,stroke-width:1px,color:#2D2A26;
    
    class A,B,C default;
    class D,E,F,G accent;
