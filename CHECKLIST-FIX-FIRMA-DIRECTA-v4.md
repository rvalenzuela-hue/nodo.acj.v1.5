# FIX FIRMA DIRECTA v4

- La firma ya no depende del campo duplicado `actaEstado` dentro de `actaFirmas`.
- Firestore Rules consulta la minuta real `minutasMesa/{actaId}` y exige `estado == Cerrada`.
- También valida que `versionDocumento` coincida con la minuta cerrada.
- Tras escribir, el Portal vuelve a leer `actaFirmas/{token}` y sólo anuncia éxito si Firestore confirma `estado == Firmado`.
- No se modificaron cuentas, contraseñas, Agenda ni contenido de actas.
