<div align="center">
  <h1 align="center">✦ core engineering ✦</h1>
  <p align="center">
    <i style="color: #666;">crafting mods • trading logic • network systems</i>
  </p>
</div>

---

### ⚗️ Project Ecosystem Weight

<!-- Обновленный абстрактный граф Mermaid. Показывает не топологию, а "вес" и связь проектов. Используются круги. -->
```mermaid
%%{init: {'theme': 'base', 'themeVariables': { 'primaryColor': '#FAF8F5', 'primaryTextColor': '#2D2A26', 'primaryBorderColor': '#DCD6CC', 'lineColor': '#A39E93', 'secondaryColor': '#E8E4DB', 'tertiaryColor': '#F0EBE1'}}}%%
graph TD;
    Dev([Development Console])
    
    subgraph mods [Java Fabric Mods]
    direction LR
    BlackOut(BlackOut Client)
    Mappings(Yarn Mappings)
    end
    
    subgraph quant [Algo-Trading Engine]
    direction LR
    Exchange(Exchange API)
    Bots(Bots)
    end
    
    subgraph network [Networking Node]
    direction LR
    VLESS(VLESS Node)
    end
    
    Dev -.-> mods
    Dev -.-> quant
    Dev -.-> network
    
    classDef default fill:#FAF8F5,stroke:#DCD6CC,stroke-width:1px,color:#2D2A26;
    classDef circleNode rx:50,ry:50,fill:#E8E4DB,stroke:#CFC8BD,color:#2D2A26;
    
    class Dev default;
    class BlackOut,Mappings,Exchange,Bots,VLESS circleNode;
