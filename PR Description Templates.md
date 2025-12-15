## Qué **es**

Un formato estandarizado para descripciones de pull requests que las mantiene concisas y útiles para los reviewers.

## Propuestas

### Opción A: Estándar comunidad

markdown

```markdown
## Description

(what it does and why, 2-4 lines)

PROJ-123
```

**Pros**

- Simple y flexible
- Formato más común en proyectos open source
- Escritura natural, sin estructura forzada
- El ticket tiene el contexto detallado

**Contras**

- Menos guía para devs que escriben mucho o muy poco
- El qué y el por qué pueden mezclarse

### Opción B: Estructurado con card

markdown

```markdown
## What
(one line)

## Why
(minimal context)

## Testing
(how it was tested)

PROJ-123
```

**Pros**

- Estructura clara, cada sección tiene su propósito
- Más fácil de escanear rápido
- Obliga a pensar en el testing

**Contras**

- Más rígido
- Puede sentirse redundante si el ticket ya tiene contexto
- Un poco más de overhead

## Referencia

No existe un estándar oficial. Esto se basa en patrones comunes de React, Vue, Next.js y otros proyectos open source importantes.

---

[[Index|← Índice]] | [[PR Size|Siguiente: 5. PR Size →]]