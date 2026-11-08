# Arquitectura funcional interna del SGBD

| Módulo | Componente | Función |
|---|---|---|
| **Procesador de consultas** | Compilador DDL/DML | Traduce las sentencias de definición (DDL) y manipulación (DML/SQL). |
| | Optimizador de consultas | Evalúa los planes de ejecución posibles y selecciona el algoritmo más eficiente, de menor costo de I/O. |
| **Gestor de almacenamiento (Storage Engine)** | Buffer Manager | Administra la memoria caché RAM, intermediando entre el disco y las consultas. |
| | File Manager | Gestiona la asignación de espacio en disco y las estructuras de archivos. |
| | Diccionario de datos (catálogo del sistema) | Almacena los metadatos sobre esquemas, tablas y permisos. |
| **Gestor de transacciones** | Control de transacciones | Garantiza las propiedades ACID (atomicidad, consistencia, aislamiento y durabilidad). |
| | Concurrencia y recuperación | Maneja la concurrencia mediante bloqueos y la recuperación ante fallos mediante archivos de registro (log). |
