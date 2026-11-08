# Tabla comparativa de modelos de bases de datos

| Modelo | Definición | Forma de representación |
|---|---|---|
| **Jerárquico** | Organiza los datos en una estructura de árbol invertido (relación 1:N). Cada registro hijo tiene un único registro padre. | Nodos interconectados en niveles jerárquicos mediante enlaces unidireccionales. |
| **En Red** | Evolución del modelo jerárquico que permite relaciones de muchos a muchos (N:M). Un hijo puede conectarse a múltiples padres. | Grafos o redes donde los registros se relacionan mediante punteros multidireccionales. |
| **Relacional** | Modelo estándar que organiza los datos en tablas compuestas por filas y columnas interconectadas mediante claves. | Tablas bidimensionales (matrices de tuplas y atributos) conectadas por claves primarias y foráneas. |
| **Orientado a Objetos** | Almacena datos integrando conceptos del paradigma POO (clases, objetos, herencia, métodos y encapsulamiento). | Jerarquías de clases y objetos que encapsulan atributos y comportamientos. |
| **NoSQL** | Modelos no relacionales diseñados para alta escalabilidad, volumen y flexibilidad de datos no estructurados. | Colecciones de documentos (JSON), pares clave-valor, grafos o columnas anchas. |
