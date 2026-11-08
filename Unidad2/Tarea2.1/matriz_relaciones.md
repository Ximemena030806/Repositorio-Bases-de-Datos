# Matriz de relaciones, cardinalidades y participación

| Relación | Entidades | Cardinalidad | Participación | Atributos |
|---|---|---|---|---|
| **Posee** | Propietario – Mascota | 1:N | Mascota total; Propietario parcial | — |
| **Agenda** | Mascota – Veterinario | M:N | Parcial en ambos | id_cita (PK), fecha_hora, motivo, estado |
| **Atiende** | Mascota – Veterinario | M:N | Parcial en ambos | folio (PK), fecha, diagnóstico, observaciones |
| **Receta** | Agregación (Atiende) – Medicamento | M:N | Parcial en ambos | dosis, duración |
| **Aplica** | Agregación (Atiende) – Vacuna | M:N | Parcial en ambos | lote, caducidad |
| **Genera** | Agregación (Atiende) – Factura | 1:1 | Total en ambos | — |
| **Suministra** | Medicamento – Proveedor | M:N | Medicamento total; Proveedor parcial | — |
