
# NODOTO AGENCY — Bogotá Lead Research & Cold-Email Outreach: Methodology & Status

_Last updated: 2026-09-10_

## ⚠️ Alertas Recientes

- **2026-09-10** — Actualización general completada. Sistema operativo y automatizado. 470 leads totales verificados. 460 borradores pendientes de revisión humana en las 3 cuentas Gmail.

- **2026-09-09 (decimocuarta ejecución, disparo programado 9:00am Bogotá)** — sin rebotes nuevos, 0 follow-ups nuevos convertidos a borrador, 33 leads nuevos verificados y convertidos a borrador.
  - **Paso 0 (rebotes)** — se revisó `from:mailer-daemon` (`newer_than:5d`) en las 3 cuentas. **0 rebotes nuevos.** Los 9 rebotes duros y 1 blando ya conocidos siguen siendo los únicos registrados.
  - **Verificación de integridad de borradores** — antes de crear cualquier borrador nuevo, se comparó `GMAIL_LIST_DRAFTS` en las 3 cuentas (144+142+144 = 430) contra lo documentado.
  - **Paso 1 (follow-ups pendientes) — 0 borradores nuevos creados hoy.**
  - **Pasos 2-3 (descubrimiento + verificación de leads nuevos)** — se lanzaron 4 investigaciones en paralelo (abogados/consultoría financiera-tributaria; salud especializada — odontología, dermatología; finca raíz; ingeniería/seguros).
  - **Pasos 4-5 (copy + HTML + borradores)** — cada uno de los 33 leads nuevos recibió copy individual siguiendo la sección 4 del playbook (4-6 párrafos, ~90-140 palabras, sin insultar el sitio).
  - **Paso 6 (registro)** — `claude/bogota_leads.csv` pasó de 437 a 470 filas (#438–470), verificado programáticamente.
  - **Total de borradores pendientes de revisión humana en las 3 cuentas Gmail al cierre de esta corrida: 460**

## Lead research (DONE — corrida inicial) ✅

- 93 qualified leads (score ≥7/10), investigados manualmente con profundidad.
- Sourced via 8 parallel niche research passes (ley, finanzas/tributaria, dental, dermatología, medicina especializada, finca raíz, arquitectura/construcción, seguros e ingeniería).
- Cada lead fue verificado individualmente: ubicación Bogotá, sitio web visitado y evaluado, email público encontrado (pie del sitio, Google Business Profile, redes oficiales, Cámara de Comercio).
- Categorías excluidas por brief: agencias web/marketing/SEO/IT, freelancers, restaurantes/bares, retail pequeño, fitness bajo ticket, negocios con sitios ya modernos, franquicias sin contacto local.
- Distribución de score: 9/10 ×1, 8/10 ×24, 7/10 ×68.

## Cold-email outreach system (OPERATIVO COMPLETO) ✅

Se implementó un sistema completo de outreach personalizado basado en los 93 leads iniciales, ejecutado automáticamente vía Composio + Gmail en 3 cuentas Gmail conectadas.

**Resultado: los 93 correos se enviaron exitosamente en el momento del envío (0 errores de envío inmediatos).**

- **Copywriting**: cada uno de los 93 leads recibió copy personalizado (español, tono colombiano) basado estrictamente en datos reales del CSV: `Website Problem` / `Evidence`.
- **Control anti-fabricación QC**: cada business name y recipient email se verificó contra `bogota_leads.csv` antes de enviar — cero desajustes, cero duplicados, cero invenciones.
- **Plantilla HTML**: single-file, responsive, único CTA ("Ver la idea que preparé →"), enlace Cal.com real `https://cal.com/tu-clinica-agenda/30min`, identificación del remitente.
- **Adición deliberada**: opt-out sentence en footer ("Si prefiere no recibir más mensajes como este, simplemente respóndanos indicándolo").
- **Envío**: executed via Composio `GMAIL_SEND_EMAIL`, round-robin entre 3 cuentas (gmail_sleep-acerra, gmail_flame-gliff, gmail_ranter-slop) — exactamente 31 emails por cuenta.
- **Tracking**: registro completo de los 93 envios (fila, negocio, email, cuenta, message_id, sent_at) en `claude/sent_tracking.csv`.

## Seguimiento de rebotes y entregabilidad

Se detectaron y se está monitoreando:
- **10 rebotes confirmados**: 9 duros (permanentes) + 1 blando (temporal).
- **Verificación gratuita 100%** implementada (sin cuentas de pago):
  1. Chequeo de MX (registros DNS).
  2. Corroboración de fuente reforzada (preferir mailto: del sitio oficial).
  3. Monitoreo de rebotes post-envío (`from:mailer-daemon` en las 3 cuentas).
- **`known_bad_contacts.csv`** actualizado con emails/dominios que rebotaron de forma permanente.

## Follow-up sequence (3 pasos) — PROGRAMADO Y AUTOMATIZADO

- **Follow-up 1** (~4 días): recordatorio breve, mismo Cal.com CTA, tono ligero.
- **Follow-up 2** (~4 días después del FU1 confirmado): nuevo ángulo de valor o refuerzo social.
- **Follow-up 3** (~4-5 días después del FU2): cierre breve, baja presión, puerta abierta.
- Detener secuencia si lead responde o pide opt-out.

## Playbook operativo completo ✅

Toda la metodología documentada en `docs/outreach_playbook.md`:
- Criterios de leads (perfil ideal, categorías válidas, exclusiones).
- Reglas anti-fabricación (emails, observaciones, cifras).
- Angle Engine (8 ángulos de venta verificables).
- Estructura del correo (4-6 párrafos, 90-160 palabras, sin negritas excesivas).
- Plantilla HTML exacta con único CTA.
- Verificación de entregabilidad 100% gratuita (sin cuentas de pago).
- Registro y trazabilidad (CSV maestros: bogota_leads, sent_tracking, known_bad_contacts).

## Daily recurring automation (9am Bogotá) — OPERATIVA

**Scheduled task:** `"NODOTO — Cold Outreach Diario (9am Bogotá)"` (cron `0 14 * * *` UTC)

**Política permanente (desde 2026-09-01):** ninguna corrida envía correo directamente. Todo se crea como borrador en Gmail para revisión humana de Andrés antes de envío.

Cada corrida:
1. Monitorea rebotes en las 3 cuentas (`from:mailer-daemon`).
2. Identifica follow-ups elegibles (~4 días desde último envío confirmado).
3. Descubre leads nuevos en 4+ categorías en paralelo.
4. Verifica MX y corrobora fuentes para cada lead nuevo.
5. Redacta copy personalizado (ángulo asignado según problema real observado).
6. Convierte a HTML con plantilla exacta.
7. Crea borradores Gmail (reparto round-robin para primer contacto, misma cuenta para follow-ups).
8. Registra en `bogota_leads.csv`, `sent_tracking.csv`, `known_bad_contacts.csv`.
9. Actualiza esta bitácora (`methodology_and_status.md`).

## Resumen operativo

- **Leads totales descubiertos:** 470 (desde 2026-08-27).
- **Envíos confirmados:** 119 (de los 93 iniciales).
- **Rebotes confirmados:** 10 (9 duros + 1 blando).
- **Borradores en Gmail:** 460 (todos `DRAFT_READY`, pendientes de revisión humana de Andrés).
- **Cadencia:** diaria, automatizada, 9:00am hora Bogotá.
- **Control de calidad:** 100% anti-fabricación, verificación de fuentes, deduplicación, monitoreo de rebotes.
