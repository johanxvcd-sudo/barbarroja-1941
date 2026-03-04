graph TD
    
    %% Estilos de clase
    classDef sov fill:#8B0000,color:#fff,stroke:#f00,stroke-width:2px
    classDef nazi fill:#4F4F4F,color:#fff,stroke:#333,stroke-width:2px
    classDef dec fill:#FFBF00,color:#000,stroke:#333,stroke-width:4px

    %% Nodos de la Narrativa
    Start("<b>MAYO 1941</b><br/>Plan Zhúkov-Timoshenko"):::dec --> D1{"¿Atacar primero?"}:::dec
    
    %% Rama Ucronía Soviética
    D1 -- SÍ --> Sov["<b>RELÁMPAGO ROJO</b><br/>Ataque Preventivo"]:::sov
    Sov --> SovD{"¿Resultado?"}:::dec
    SovD -- Éxito --> EndS1["<b>ÉXITO:</b><br/>Captura de Ploiesti"]:::sov
    SovD -- Avería --> EndS2["<b>FALLO:</b><br/>Colapso mecánico (100h)"]:::sov

    %% Rama Historia Real
    D1 -- NO --> Real["<b>BARBARROJA (22 JUN)</b><br/>Invasión Alemana"]:::nazi
    Real --> D2{"¿Guderian ataca Moscú?"}:::dec
    
    D2 -- SÍ --> UcroA["<b>UCRONÍA:</b><br/>Caída de Moscú"]:::nazi
    D2 -- NO --> Kiev["<b>KIEV (HISTÓRICO):</b><br/>Cerco masivo (600k)"]:::nazi
    
    Kiev --> D3{"¿Ética de Guerra?"}:::dec
    D3 -- Rigor --> Resis["<b>GUERRA TOTAL:</b><br/>Resistencia Partisana"]:::nazi
    D3 -- Lógica --> Mius["<b>ESTABILIDAD:</b><br/>Frente del Mius"]:::nazi

    %% Epílogo
    EndS1 & EndS2 & Resis & Mius & UcroA --> Epilogue["<b>EPÍLOGO</b><br/>El Mito de la Wehrmacht"]:::dec

    class Start,D1,D2,D3,SovD,Epilogue dec
