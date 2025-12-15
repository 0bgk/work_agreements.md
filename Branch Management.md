## Qué es

Estrategia para gestionar ramas en el repositorio: cómo crearlas, nombrarlas y mergearlas.

## Estrategia: GitHub Flow (trunk-based)

```
main ──●───●───●───●───●───●───
       ↑   ↑   ↑   ↑   ↑   ↑
     feat fix feat chore fix feat
```

- Solo `main` es permanente y siempre deployable
- Features/fixes en branches cortas que nacen y mueren en main
- CI/CD controla a qué entorno va
- Sin ramas intermedias (dev, staging, release)

## Branch Naming

### Opción A: Ticket + descripción (simple)

```
PROJ-123-google-oauth
PROJ-456-fix-null-pointer
PROJ-789-update-aws-sdk
```

**Pros**

- Mínima fricción, muy simple
- JIRA conecta automáticamente
- Sin confusión con tipos de commit
- El ticket ya tiene el contexto

**Contras**

- No sabes el tipo de cambio a simple vista
- Dependes de JIRA para contexto

### Opción B: Tipo + ticket + descripción (GitFlow style)

```
feature/PROJ-123-google-oauth
bugfix/PROJ-456-null-pointer
hotfix/PROJ-789-payment-crash
chore/PROJ-101-update-deps
```

**Tipos**

- `feature/` → nueva funcionalidad
- `bugfix/` → corrección de bug
- `hotfix/` → fix urgente en prod
- `chore/` → mantenimiento, dependencias

**Pros**

- Sabes el propósito de la branch a simple vista
- Más contexto sin abrir JIRA
- Diferencia clara entre bugfix y hotfix

**Contras**

- Más largo de escribir
- Una regla más que recordar

## Reglas comunes

- Minúsculas siempre
- Guiones entre palabras (no underscores)
- Descripción corta: 2-4 palabras
- Siempre incluir ticket de JIRA

## Flujo

```
1. Ticket en JIRA (PROJ-123)
         ↓
2. Crear branch desde main
   feature/PROJ-123-google-oauth
         ↓
3. Commits
   feat: add OAuth provider
   fix: handle null token
         ↓
4. PR a main
         ↓
5. Merge → CI/CD deploya
```

## Referencia

		- Semantic commit messages: https://gist.github.com/joshbuchea/6f47e86d2510bce28f8e7f42ae84c716
- GitHub Flow: [https://docs.github.com/en/get-started/using-github/github-flow](https://docs.github.com/en/get-started/using-github/github-flow)
- Trunk Based Development: [https://trunkbaseddevelopment.com/](https://trunkbaseddevelopment.com/)
- Branch 

---

[[Index|← Índice]] | [[Pre-commit Hooks|Siguiente: 3. Pre-commit Hooks →]]