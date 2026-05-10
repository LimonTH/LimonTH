<div align="center">
  <h1 align="center">✦ architecture & ecosystems ✦</h1>
  <p align="center">
    <i style="color: #666;">java modifications • quantitative trading • network infrastructure</i>
  </p>
</div>

---

### ⚗️ Core Topology

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#FAF8F5', 'primaryTextColor': '#2D2A26', 'primaryBorderColor': '#DCD6CC', 'lineColor': '#A39E93', 'secondaryColor': '#E8E4DB', 'tertiaryColor': '#F0EBE1'}}}%%
graph LR;
    Hub([Dev Workspace]) -->|Java| Mod(BlackOut Utility Client);
    Hub -->|Go| Net(VLESS / Routing Node);
    Hub -->|Python| Quant(Algo-Trading Engine);

    Mod -->|Fabric API| Game{Game Environment};
    Net -->|WebRTC / TCP| Tunnel{Secure Network};
    Quant -->|REST / WSS| Exchange{Exchange APIs};
    Quant --> DB[(Market Data Cache)];
    
    classDef default fill:#FAF8F5,stroke:#DCD6CC,stroke-width:1px,color:#2D2A26;
    classDef accent fill:#E8E4DB,stroke:#CFC8BD,stroke-width:1px,color:#2D2A26;
    
    class Hub default;
    class Mod,Net,Quant,Game,Tunnel,Exchange,DB accent;
