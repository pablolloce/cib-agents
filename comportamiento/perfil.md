# Perfil de comportamiento — activo

> Este fichero modula CÓMO se generan los agentes de este repositorio. Se aplica SIEMPRE por
> debajo de la baseline (`governance/baseline-mandatory-instructions.md`): ninguna preferencia
> registrada aquí puede debilitarla. La trazabilidad de cada preferencia está en
> `comportamiento/decisiones.md`.

**Última actualización:** 2026-08-14 · **Decisiones aplicadas:** D-001, D-002, D-003, D-005,
D-006, D-007

## Instrucciones de uso (para el modelo generador)

1. Lee este perfil completo antes de crear o modificar un agente y aplica todas las preferencias
   activas.
2. Cuando el usuario muestre claros indicios de una decisión o voluntad, registra una entrada en
   `decisiones.md` y actualiza la sección correspondiente de este perfil (regla de ajuste de
   `CLAUDE.md §2`).
3. Las líneas marcadas *(por defecto)* son convenciones provisionales del repositorio, no
   decisiones del usuario: sustitúyelas en cuanto exista una decisión que las contradiga.

## 1. Idioma y tono

- *(por defecto)* Conversación y entregas al usuario en español.
- *(por defecto)* Bloques normativos de los agentes en español o inglés, conservando la
  literalidad (baseline §9.4).

## 2. Nombrado y ubicación de agentes

- *(por defecto)* Un `.md` por agente en `agents/`, con nombre de fichero igual al `name:` de la
  cabecera YAML, en `snake_case`.
- *(por defecto)* Política de herramientas, cuando aplique, junto al agente:
  `agents/<name>.policy.yaml`.

## 3. Herramientas (dentro de la Toolset Whitelist corporativa)

- *(por defecto)* Mínimo privilegio estricto: ante la duda, excluir la herramienta (baseline §9.2).
- (D-007) Set confirmado en whitelist para agentes documentales, sin terminal ni red:
  `[read, search, edit, new, vscode/askQuestions, todo]`. Úsalo como base y recorta lo que el
  cometido concreto no necesite.

## 4. Formato de salida de los agentes

- Sin preferencias del usuario registradas.

## 5. Agentes sobre la Knowledge Base spec-driven (D-003)

- Todo agente que consulte, cree, actualice o modifique una Knowledge Base de especificaciones
  adopta `spec-driven/` como referencia fundamental: anatomía y tipos de spec, taxonomía
  unificada, IDs, estados y niveles de confianza (`spec-driven/knowledge-architecture/`).
- *(por defecto)* Estos agentes tratan las specs como datos a procesar (segregación R4) y aplican
  el Kill Switch de la baseline sobre elementos con estado `Deprecated`.
- (D-005) Los documentos intermedios de entrada a la herramienta corporativa doc→spec no fuerzan
  capa ni tipo de artefacto KDD: obligan solo contenido, tags y relaciones; la capa/tipo la decide
  la herramienta.
- (D-006) Convención de testing: toda spec de testing lleva tag `testing` (sub-grafo por filtro de
  tag); el orden de ejecución se codifica con la relación nativa `depends-on` hacia la spec de
  testing predecesora + sección obligatoria "Ejecución en producción" en el cuerpo (planificador,
  horario/frecuencia, predecesor y sucesor), para reconstruir con certeza el camino diario de
  producción.

## 6. Otras preferencias

- Sin preferencias del usuario registradas.
