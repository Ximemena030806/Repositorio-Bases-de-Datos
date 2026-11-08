# Correspondencia entidad → clase

| Objeto en el E-RE | Clase UML | Observación |
|---|---|---|
| Propietario | Propietario | Contiene Nombre y Direccion por composición |
| Mascota | «abstract» Mascota | Superclase; hereda a Canino, Felino, Exotico |
| Canino, Felino, Exótico | Canino, Felino, Exotico | Atributos propios de cada tipo |
| Empleado | «abstract» Empleado | Superclase con jerarquía solapada |
| Veterinario, Gerente, Recepcionista, Auxiliar | Veterinario, Gerente, Recepcionista, Auxiliar | Un empleado puede tener varios roles |
| Veterinario_Especialista | VeterinarioEspecialista | Hereda de Veterinario (nivel 3) |
| Relación Agenda | Clase Cita | Asociada 0..* con Mascota y con Veterinario |
| Relación Atiende (agregación) | Clase Consulta | Dueña de Receta y Aplicacion (composición); genera Factura |
| Relación Receta | Clase Receta | Atributos dosis y duracion; apunta a un Medicamento |
| Relación Aplica | Clase Aplicacion | Atributos lote y fechaCaducidad; apunta a una Vacuna |
| Medicamento, Proveedor, Vacuna, Factura | Medicamento, Proveedor, Vacuna, Factura | Con métodos estaVigente(), hayExistencia(), calcularTotal() |
| Atributos compuestos nombre y dirección | «dataType» Nombre y Direccion | Tipos de valor reutilizables |
