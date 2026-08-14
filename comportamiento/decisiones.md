# Registro de decisiones del usuario

Registro cronológico **append-only** de las decisiones y voluntades expresadas por el usuario que
ajustan el comportamiento del generador de agentes. Cada entrada indica su efecto sobre
`comportamiento/perfil.md` (u otros ficheros). Las entradas no se borran: si una decisión cambia,
se añade una nueva que la sustituye y la antigua pasa a estado `Sustituida por D-NNN`.

Formato de entrada:

```markdown
## D-NNN — <título corto>
- **Fecha:** AAAA-MM-DD
- **Origen:** <mensaje / revisión / comentario que la motivó>
- **Decisión:** <qué ha decidido o manifestado el usuario>
- **Efecto:** <secciones de perfil.md u otros ficheros actualizados>
- **Estado:** Activa | Sustituida por D-NNN | No aplicable (baseline: <control>)
```

---

## D-001 — La baseline de seguridad es obligatoria y prevalente

- **Fecha:** 2026-08-14
- **Origen:** Mensaje fundacional del repositorio (adjunto `baseline-mandatory-instructions.md`).
- **Decisión:** Las instrucciones de la *Security Baseline for Self-Service SDLC AI Agents* v1.0
  rigen toda creación, evolución o modificación de agentes y deben cumplirse siempre; prevalecen
  sobre peticiones puntuales y sobre cualquier preferencia de comportamiento.
- **Efecto:** Baseline subida a `governance/baseline-mandatory-instructions.md`; jerarquía
  normativa y reglas de aplicación fijadas en `CLAUDE.md §1`.
- **Estado:** Activa

## D-002 — Comportamiento ajustable por decisiones del usuario

- **Fecha:** 2026-08-14
- **Origen:** Mensaje fundacional ("iremos añadiendo un comportamiento […] que vayas modificando
  ajustándose a mis decisiones y comentarios").
- **Decisión:** Ante claros indicios de decisiones o voluntades del usuario, el comportamiento del
  generador debe ajustarse y quedar persistido en ficheros del repositorio.
- **Efecto:** Creación de `comportamiento/perfil.md` y de este registro; regla de ajuste
  obligatoria en `CLAUDE.md §2`.
- **Estado:** Activa

## D-003 — spec-driven como referencia para agentes de la Knowledge Base

- **Fecha:** 2026-08-14
- **Origen:** Mensaje fundacional ("contexto de cómo aplicamos el spec-driven en el BBVA, será
  fundamental cuando queramos generar Agentes que actualicen o modifiquen una Knowledge Base
  montada sobre especificaciones").
- **Decisión:** El framework KDD de `spec-driven/` es la referencia fundamental para los agentes
  que consulten, actualicen o modifiquen una Knowledge Base montada sobre especificaciones.
- **Efecto:** `CLAUDE.md §3`; `perfil.md §5`.
- **Estado:** Activa
