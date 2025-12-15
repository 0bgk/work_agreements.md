## Qué es

Bots que escanean tus dependencias y crean PRs automáticos cuando hay actualizaciones disponibles.

## Por qué usarlo

- Parches de seguridad llegan solos
- Menos deuda técnica acumulada
- Visibilidad de qué está desactualizado
- No depende de que alguien se acuerde

## Opciones

### Dependabot

Integrado en GitHub, cero setup inicial.

**Pros**

- Ya disponible en cualquier repo de GitHub
- Configuración mínima
- Alertas de seguridad incluidas

**Contras**

- Menos configurable
- No agrupa PRs
- Puede generar ruido con muchas dependencias

### Renovate

Más potente y configurable.

**Pros**

- Agrupa PRs por tipo
- Auto-merge inteligente
- Muy flexible

**Contras**

- Más config inicial
- Curva de aprendizaje

## Propuesta

Empezar con Dependabot. Si genera demasiado ruido, migrar a Renovate.

## Setup básico (Dependabot)

Archivo `.github/dependabot.yml`:

yaml

```yaml
version: 2
updates:
  - package-ecosystem: "npm"
    directory: "/"
    schedule:
      interval: "weekly"
    open-pull-requests-limit: 5
    labels:
      - "dependencies"
```

## Qué aporta

- Dependencias actualizadas sin esfuerzo manual
- Seguridad: vulnerabilidades parcheadas rápido
- CI valida que las actualizaciones no rompan nada

## Referencia

- Dependabot: [https://docs.github.com/en/code-security/dependabot](https://docs.github.com/en/code-security/dependabot)
- Configuración: [https://docs.github.com/en/code-security/dependabot/dependabot-version-updates/configuration-options-for-the-dependabot.yml-file](https://docs.github.com/en/code-security/dependabot/dependabot-version-updates/configuration-options-for-the-dependabot.yml-file)
- Renovate: [https://docs.renovatebot.com/](https://docs.renovatebot.com/)

---

[[Index|← Índice]] | [[Integración con Claude|Siguiente: 7. Integración con Claude →]]