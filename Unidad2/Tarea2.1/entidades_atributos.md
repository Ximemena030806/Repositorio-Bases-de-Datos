# Clasificación de entidades y atributos

Notación: **PK** = clave; **(c)** = compuesto; **{m}** = multivalorado; **/d/** = derivado.

| Entidad | Tipo | Atributos |
|---|---|---|
| **Propietario** | Fuerte | **id_propietario** (PK), nombre (c: nombre_pila, ap_paterno, ap_materno), dirección (c: calle, colonia, cp), correo, {teléfono} |
| **Mascota** | Fuerte (superentidad) | **id_mascota** (PK), nombre, especie, raza, fecha_nacimiento, /edad/, peso |
| **Canino / Felino / Exótico** | Subentidades | Canino: tamaño, nivel_adiestramiento. Felino: pelaje, esterilizado. Exótico: tipo_hábitat, requiere_permiso |
| **Empleado** | Fuerte (superentidad) | **id_empleado** (PK), nombre (c), RFC, fecha_ingreso, /antigüedad/ |
| **Veterinario** | Subentidad de Empleado | cédula_profesional, {especialidad} |
| **Gerente / Recepcionista / Auxiliar** | Subentidades de Empleado | departamento / turno / área_asignada |
| **Veterinario_Especialista** | Subentidad de Veterinario | subespecialidad |
| **Medicamento** | Fuerte | **id_medicamento** (PK), nombre, presentación, existencia, precio |
| **Proveedor** | Fuerte | **id_proveedor** (PK), razón_social, contacto |
| **Vacuna** | Fuerte | **id_vacuna** (PK), nombre, enfermedad_prevenida |
| **Factura** | Fuerte | **no_factura** (PK), fecha, subtotal, /total/ |
