# Tabla comparativa de correspondencia directa E-R Extendido ↔ UML

## a) Elementos estructurales

| Elemento E-R Extendido | Notación UML (clases) | Aplicación en la clínica veterinaria |
|---|---|---|
| Entidad (rectángulo) | Clase | Propietario, Medicamento, Proveedor, Vacuna, Factura |
| Superentidad con especialización total | Clase abstracta («abstract», nombre en cursiva) | Mascota y Empleado |
| Atributo simple | Atributo con visibilidad y tipo | `- peso: float`, `- correo: String` |
| Atributo clave (subrayado) | Atributo identificador (UML no tiene símbolo de PK) | `- idPropietario: int`, `- idMascota: int` |
| Atributo compuesto | Clase «dataType» unida por composición | Nombre (nombrePila, apPaterno, apMaterno) y Direccion (calle, colonia, cp) |
| Atributo multivalorado (doble elipse) | Atributo con multiplicidad [1..*] | `telefonos: String [1..*]`; `especialidades: String [1..*]` |
| Atributo derivado (elipse punteada) | Atributo con prefijo `/` y método de cálculo | `/ edad` con `calcularEdad()`; `/ antiguedad`; `/ total` con `calcularTotal()` |
| Relación M:N con atributos | Clase de asociación o clase intermedia (reificación) | Agenda → Cita; Atiende → Consulta; Receta; Aplica → Aplicacion |

## b) Relaciones, restricciones y jerarquías

| Elemento E-R Extendido | Notación UML (clases) | Aplicación en la clínica veterinaria |
|---|---|---|
| Relación 1:N (Posee) | Agregación con multiplicidad 1 y 0..* | Propietario 1 ◇— 0..* Mascota (rombo blanco) |
| Relación 1:1 (Genera) | Asociación con multiplicidad 1 a 1 | Consulta 1 — 1 Factura |
| Relación M:N (Suministra) | Asociación 0..* a 1..* | Medicamento 0..* — 1..* Proveedor |
| Participación total | Multiplicidad mínima 1 (o 1..*) | Mascota siempre tiene propietario; Medicamento 1..* Proveedor |
| Participación parcial | Multiplicidad mínima 0 | Propietario 0..* Mascota; Consulta 0..* Receta |
| Especialización disjunta y total (d) | Herencia con {disjoint, complete} | Canino, Felino y Exotico heredan de Mascota |
| Especialización solapada (o) | Herencia con {overlapping, complete} | Veterinario, Gerente, Recepcionista y Auxiliar heredan de Empleado |
| Jerarquía de varios niveles | Cadena de herencia | Empleado → Veterinario → VeterinarioEspecialista |
| Agregación E-R (relación como entidad abstracta) | Clase propia con composición hacia sus partes (rombo negro) | Consulta ◆ Receta; Consulta ◆ Aplicacion; Consulta — Factura |
| Atributo compuesto (parte del todo) | Composición (rombo negro) | Propietario ◆ Direccion; Propietario ◆ Nombre; Empleado ◆ Nombre |
