graph TD
    classDef sov fill:#8B0000,color:#fff
    classDef nazi fill:#4F4F4F,color:#fff
    classDef dec fill:#FFBF00,color:#000

    Start("MAYO 1941: El Dilema Estratégico") --> D1{¿Atacar primero?}
    
    D1 -- SÍ --> Sov["RAMA SOVIÉTICA: Relámpago Rojo"]:::sov
    Sov --> D2{¿Objetivo?}
    D2 -- Petróleo --> EndS1(("ÉXITO UCRO: Colapso Nazi"))
    D2 -- Choque --> EndS2(("FALLO: Desgaste Mecánico"))

    D1 -- NO --> Real["HISTORIA REAL: Barbarroja"]:::nazi
    Real --> D3{¿Prioridad?}
    D3 -- Moscú --> UcroA["UCRONÍA: Caída de Moscú"]:::nazi
    D3 -- Kiev --> RealK["CAMINO REAL: Cerco de Kiev"]:::nazi

    RealK --> D4{¿Ética de Guerra?}
    D4 -- Rigor --> Partis["GUERRA TOTAL: Partisanos"]
    D4 -- Logística --> Mius["ESTABILIDAD: Río Mius"]

    Partis & Mius & UcroA --> Final["EPÍLOGO: El Mito de la Wehrmacht Limpia"]
    
    class D1,D2,D3,D4 dec