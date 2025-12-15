## Qué es

Convención para escribir mensajes de commit con un formato simple y consistente:

```
tipo: descripción corta
```

## Tipos

- `feat`: nueva funcionalidad
- `fix`: corrección de bug
- `docs`: documentación
- `style`: formato, sin cambios de lógica
- `refactor`: cambio sin alterar comportamiento
- `test`: tests
- `chore`: mantenimiento, dependencias, configs

## Ejemplos

```
feat: add user registration
fix: resolve null pointer on logout
docs: update README with setup instructions
chore: upgrade React Native to 0.74
```

## Qué aporta

- Historial de git legible y navegable
- Filtrar commits por tipo (`git log --grep="^fix:"`)
- Code reviews más rápidas: sabes qué esperar antes de ver el código
- Debugging más fácil: descartar commits irrelevantes buscando bugs
- Onboarding: gente nueva entiende el historial sin preguntar
- Consistencia: evita commits tipo "cambios", "wip", "asdfasdf"

## Referencia

https://gist.github.com/joshbuchea/6f47e86d2510bce28f8e7f42ae84c716

---

[[Index|← Índice]] | [[Branch Management|Siguiente: 2. Branch Management →]]