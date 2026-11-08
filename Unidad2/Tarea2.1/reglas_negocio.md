# Reglas de negocio: Clínica veterinaria

| # | Regla de negocio |
|---|---|
| 1 | Un propietario puede registrar varias mascotas; toda mascota pertenece a un solo propietario responsable. |
| 2 | Un propietario tiene uno o más teléfonos de contacto. |
| 3 | Toda mascota se clasifica en exactamente una categoría: canino, felino o exótico (especialización disjunta y total), cada una con atributos propios. |
| 4 | El personal se clasifica en veterinario, gerente, recepcionista o auxiliar. Una persona puede tener más de un rol, por ejemplo un veterinario que también es gerente (especialización solapada). |
| 5 | Un veterinario tiene cédula profesional y una o más especialidades; algunos se registran como veterinarios especialistas con una subespecialidad (jerarquía de tres niveles). |
| 6 | Una cita (relación Agenda) se agenda para una mascota con un veterinario, con fecha y hora, motivo y estado. Un veterinario no puede tener dos citas a la misma hora. |
| 7 | Una atención (relación Atiende) vincula a la mascota con el veterinario y registra folio, fecha, diagnóstico y observaciones. No toda cita se concreta. |
| 8 | En cada atención el veterinario puede recetar cero o más medicamentos, indicando dosis y duración (relación Receta sobre la agregación Atiende). |
| 9 | Un medicamento es suministrado por uno o varios proveedores; un proveedor puede surtir varios medicamentos. |
| 10 | Las vacunas aplicadas en una atención se registran con lote y fecha de caducidad (relación Aplica). |
| 11 | Toda atención genera exactamente una factura; el total se deriva de subtotal, servicios y medicamentos (relación Genera). |
| 12 | No se vende un medicamento caducado ni sin existencia. |
