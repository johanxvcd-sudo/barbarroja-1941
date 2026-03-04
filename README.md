graph TD

    %% Estilos de clase
    classDef sov fill:#8B0000,color:#fff,stroke:#f00,stroke-width:2px
    classDef nazi fill:#4F4F4F,color:#fff,stroke:#333,stroke-width:2px
    classDef dec fill:#FFBF00,color:#000,stroke:#333,stroke-width:4px

    %% Nodos de la Narrativa
    Start("<b>MAYO 1941</b><br/>Informes confirman despliegue nazi"):::dec --> D1{"¿Aprobar el Plan de Mayo<br/>de Zhúkov?"}:::dec
    
    %% Rama Ucronía Soviética
    D1 -- SÍ --> Sov["<b>RELÁMPAGO ROJO</b><br/>Ataque Preventivo el 12 de junio"]:::sov
    Sov --> SovD{"¿Logística?"}:::dec
    SovD -- 15% Munición --> EndS1["<b>FALLO:</b><br/>Escasez de proyectiles AP"]:::sov
    SovD -- 100h Motor --> EndS2["<b>AVERÍA:</b><br/>Colapso mecánico en la estepa"]:::sov

    %% Rama Historia Real
    D1 -- NO --> Real["<b>BARBARROJA (22 JUN)</b><br/>Invasión alemana masiva"]:::nazi
    Real --> D2{"¿Guderian ataca Moscú<br/>en Agosto?"}:::dec
    
    D2 -- SÍ --> UcroA["<b>UCRONÍA:</b><br/>Caída de Moscú en Septiembre"]:::nazi
    D2 -- NO --> Kiev["<b>KIEV (HISTÓRICO):</b><br/>Cerco masivo (600k prisioneros)"]:::nazi
    
    Kiev --> D3{"¿Decreto Barbarroja?"}:::dec
    D3 -- RIGOR --> Resis["<b>GUERRA TOTAL:</b><br/>Auge de partisanos"]:::nazi
    D3 -- LÓGICA --> Mius["<b>ESTABILIDAD:</b><br/>Frente del río Mius"]:::nazi

    %% Epílogo
    EndS1 & EndS2 & Resis & Mius & UcroA --> Epilogue["<b>EPÍLOGO</b><br/>1950: El Mito de la Wehrmacht"]:::dec

    class Start,D1,D2,D3,SovD,Epilogue dec