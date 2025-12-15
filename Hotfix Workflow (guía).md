## Qué es

Proceso para corregir bugs críticos en producción de forma rápida pero controlada.

## Cuándo aplica

- Producción rota o degradada
- Usuarios afectados activamente
- No puede esperar al siguiente ciclo normal

No es hotfix: bugs menores, mejoras, cosas que "molestan un poco".

## Flujo

```
Bug crítico detectado
       ↓
Comunicar al equipo (canal acordado)
       ↓
Crear branch desde main
  hotfix/PROJ-XXX-descripcion
       ↓
Fix mínimo (solo lo necesario, no refactorizar)
       ↓
PR con review expedita (mínimo 1 persona)
       ↓
Merge a main → deploy a prod
       ↓
Verificar que el fix funciona
       ↓
Documentar qué pasó (opcional pero recomendado)
```

## Reglas

- **Fix quirúrgico**: solo lo necesario, no aprovechar para limpiar código
- **Review siempre**: aunque sea rápida, al menos un par de ojos
- **Comunicar**: que el equipo sepa que hay algo en curso
- **Verificar**: smoke test después del deploy

## Temas a definir en equipo

- ¿Qué canal usamos para comunicar incidentes?
- ¿Quién puede aprobar PRs de hotfix?
- ¿Hacemos post-mortem después? ¿Dónde lo documentamos?
- ¿Qué criterios definen "crítico"?

---

[← Volver al Índice](Index.md)