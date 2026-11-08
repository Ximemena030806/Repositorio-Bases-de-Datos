# Clasificación de las bases de datos

| Criterio | Tipo | Descripción |
|---|---|---|
| **Variabilidad de los datos** | Estáticas (OLAP / lectura) | Diseñadas para el análisis de grandes volúmenes de datos históricos. Su contenido es de solo lectura y no sufre modificaciones constantes. Se emplean en inteligencia de negocios (Business Intelligence) y almacenamiento de datos (Data Warehouse). |
| | Dinámicas (OLTP / lectura y escritura) | Diseñadas para operaciones transaccionales en tiempo real. La información se modifica, elimina y actualiza constantemente (por ejemplo, sistemas de punto de venta, reservas bancarias). |
| **Ubicación y arquitectura física** | Centralizadas | Todos los datos y el SGBD residen en una sola localización física o servidor central. |
| | Distribuidas | Los datos se almacenan en múltiples nodos interconectados por una red de comunicación, aparentando ser una sola base de datos homogénea para el usuario. |
| **Contenido o tipo de datos** | Bibliográficas y de texto completo | Contienen metadatos, resúmenes o textos íntegros de documentos. |
| | Directorios / especializadas | Optimizadas para lecturas rápidas de listas y jerarquías (por ejemplo, protocolos LDAP, catálogos telefónicos). |
