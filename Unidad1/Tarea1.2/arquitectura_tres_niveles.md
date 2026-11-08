# Arquitectura de tres niveles (ANSI/SPARC)

![Arquitectura de tres niveles (ANSI/SPARC)](arquitectura_tres_niveles.svg)

## Código Mermaid

```mermaid
graph TD
    subgraph Nivel_Externo [1. Nivel Externo / Vistas]
        V1[Vista Usuario A: Recursos Humanos]
        V2[Vista Usuario B: Contabilidad]
        V3[Vista Usuario C: Operaciones]
    end

    subgraph Nivel_Conceptual [2. Nivel Conceptual / Lógico Global]
        NC[Esquema Conceptual Global: Entidades, Tablas, Relaciones y Reglas]
    end

    subgraph Nivel_Interno [3. Nivel Interno / Físico]
        NF[Esquema Interno: Estructuras de Almacenamiento, Índices y Archivos]
    end

    V1 --> NC
    V2 --> NC
    V3 --> NC
    NC --> NF
```

## Archivos del diagrama

- [`arquitectura_tres_niveles.svg`](arquitectura_tres_niveles.svg): fuente vectorial (SVG)
- [`arquitectura_tres_niveles.pdf`](arquitectura_tres_niveles.pdf): versión en PDF vectorial
- [`arquitectura_tres_niveles.mmd`](arquitectura_tres_niveles.mmd): código fuente Mermaid
