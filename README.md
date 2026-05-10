<div align="center">
  <h1 align="center">✦ architecture & systems ✦</h1>
  <p align="center">
    <i style="color: #666;">java modifications • quantitative trading • network infrastructure</i>
  </p>
</div>

---

### ⚗️ Core Topology

```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#FAF8F5', 'primaryTextColor': '#2D2A26', 'primaryBorderColor': '#DCD6CC', 'lineColor': '#A39E93', 'secondaryColor': '#E8E4DB', 'tertiaryColor': '#F0EBE1'}}}%%
graph LR;
    Hub([Dev Workspace]) -->|Java / Fabric| Mod(BlackOut Utility Client);
    Hub -->|Go / C| Net(VLESS & Networking);
    Hub -->|Python| Quant(Trading Bots & Exchange API);

    Mod -->|Yarn Mappings| Game{Minecraft 1.21.x};
    Net -->|Routing| Tunnel{Bypass Infrastructure};
    Quant -->|WSS / REST| Exchange{Market Data};
    
    classDef default fill:#FAF8F5,stroke:#DCD6CC,stroke-width:1px,color:#2D2A26;
    classDef accent fill:#E8E4DB,stroke:#CFC8BD,stroke-width:1px,color:#2D2A26;
    
    class Hub default;
    class Mod,Net,Quant,Game,Tunnel,Exchange accent;
📊 Metrics & Activity
📈 Contribution Dynamics
