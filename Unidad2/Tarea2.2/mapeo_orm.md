# Implicaciones para el desarrollo orientado a objetos (mapeo con un ORM)

| Construcción UML | Implementación en código | Implementación en la base de datos |
|---|---|---|
| Clase | Clase de dominio / entidad del ORM | Tabla |
| Herencia (Mascota → Canino…) | `extends` / herencia de clases | Tabla por jerarquía, o tabla por subclase con clave compartida |
| Composición con «dataType» | Objeto incrustado (`@Embedded`) | Columnas dentro de la tabla del propietario |
| Atributo multivalorado [1..*] | Colección (`List<String>`) | Tabla aparte con clave foránea |
| Atributo derivado `/` | Método o propiedad calculada, no persistente | No se almacena |
| Asociación 1 — 0..* | Referencia y colección | Clave foránea en el lado «muchos» |
| Asociación 0..* — 1..* (Suministra) | Colecciones en ambos lados | Tabla intermedia con dos claves foráneas |
| Composición Consulta ◆ Receta | Colección propia de la consulta (cascade) | Clave foránea; se elimina junto con la consulta |
