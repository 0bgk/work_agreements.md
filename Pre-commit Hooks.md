## Qué es

Scripts que se ejecutan automáticamente antes de cada commit. Si fallan, el commit se cancela. Permite pillar errores antes de que lleguen al PR.

## Herramientas base

### Husky

Gestiona los git hooks de forma sencilla. Es el estándar en proyectos JavaScript/TypeScript.

### lint-staged

Ejecuta los checks solo en archivos staged, no en todo el proyecto. Hace que el pre-commit sea rápido (segundos en vez de minutos).

## Checks propuestos

**ESLint**
Detecta errores de código y malas prácticas. Imprescindible.

**Prettier**
Formato consistente (espacios, comillas, etc.). Todo el equipo formatea igual.

**TypeScript check**
Valida que no haya errores de tipos antes de commitear.

**commitlint**
Valida que el mensaje de commit siga Semantic Commit Messages (`feat:`, `fix:`, etc.).

**sort-imports**
Ordena los imports automáticamente. Evita conflictos de merge y mantiene consistencia.

**unused-imports**
Detecta imports que no se usan. Mantiene el código limpio.

**no console.log**
Detecta `console.log` olvidados. Evita debugs en producción.

**detect-secrets / gitleaks**
Escanea el código buscando API keys, tokens o credenciales hardcodeadas. Seguridad básica.

## Qué aporta

- Pillar errores antes del PR
- Formato consistente sin discutir
- No más commits de "fix lint"
- Menos ruido en code reviews

## Referencia

- Husky: [https://typicode.github.io/husky/](https://typicode.github.io/husky/)
- lint-staged: [https://github.com/lint-staged/lint-staged](https://github.com/lint-staged/lint-staged)
- commitlint: [https://commitlint.js.org/](https://commitlint.js.org/)

---

[← Índice](Index.md) | [Siguiente: 4. PR Description Templates →](PR%20Description%20Templates.md)