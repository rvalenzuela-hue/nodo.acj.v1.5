# FIX Firma directa Firestore

- Firma ya no depende de Cloud Function signActa.
- Firmante autenticado sólo puede firmar su propio registro actaFirmas.
- Reglas exigen actaEstado Cerrada, UID asignado y transición Pendiente -> Firmado.
- El estado se actualiza inmediatamente en el Portal y Minutas lo obtiene desde actaFirmas.
- Mensaje de éxito/error queda visible junto al botón Firmar documento.
