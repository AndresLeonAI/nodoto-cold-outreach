# NODOTO AGENCY — Cold Outreach Bogotá

Repositorio privado con la documentación operativa y los datos curados de la automatización de prospección y cold-email outreach de **NODOTO AGENCY** (fundador: Andrés León) para negocios high-ticket en Bogotá, Colombia.

Este repositorio es un **espejo de trabajo** del [Cowork Project "NODOTO AGENCY EMAIL OUTREACH"](https://claude.ai) donde vive la fuente de verdad operativa día a día. Se sube aquí para tener versión, historial y respaldo fuera de Claude.

## Qué es esto

Un sistema de prospección + cold email que:

1. Descubre negocios tradicionales de alto ticket en Bogotá (abogados, clínicas, arquitectura, finca raíz, seguros, ingeniería, etc.) con sitios web débiles o inexistentes.
2. Verifica cada lead individualmente (ubicación real, sitio visitado, email públicamente listado) bajo una regla estricta anti-fabricación — nunca se inventa un email, una observación o una cifra.
3. Redacta un correo personalizado por lead, con un ángulo de venta ("angle engine") elegido según el problema real observado en su sitio.
4. Envía por Gmail (vía Composio) desde 3 cuentas en round-robin, con una secuencia de 3 follow-ups.
5. Monitorea rebotes y mantiene una lista negra permanente de contactos inválidos.

## Estructura del repositorio

```
.
├── README.md                          este archivo
├── docs/
│   ├── outreach_playbook.md           fuente de verdad operativa: criterios de leads, reglas
│   │                                   anti-fabricación, angle engine, estructura del correo,
│   │                                   plantilla HTML exacta, proceso de envío, verificación
│   │                                   de entregabilidad, secuencia de follow-ups, historial
│   └── methodology_and_status.md      bitácora de estado: qué se ejecutó, cuándo, alertas
├── data/
│   ├── bogota_leads.csv               los 120 leads descubiertos y verificados (fuente única)
│   ├── sent_tracking.csv              registro de cada envío real (status, cuenta, fecha, follow-ups)
│   └── known_bad_contacts.csv         lista negra permanente de emails/dominios que rebotaron
└── drafts/
    └── followup_1_pending_2026-08-31.csv   86 follow-ups 1 redactados y listos, pendientes de envío
```

## Estado actual (al 2026-08-31)

- **120 leads** investigados y verificados individualmente desde el 2026-08-27 (numeración #1–120, sin huecos salvo el #109 que fue descartado antes de enviarse por fallar el chequeo de MX).
- **119 envíos iniciales** ejecutados con éxito en el momento del envío, en 3 corridas (93 + 14 + 12).
- **6 rebotes duros** (`BOUNCED`) confirmados vía monitoreo de `mailer-daemon` y agregados a la lista negra permanente.
- **2 rebotes blandos** (`SOFT_BOUNCE`) en seguimiento, aún no escalados a duros.
- **86 correos de follow-up 1** redactados y listos (ver `drafts/`), **pendientes de envío**: el paso de envío masivo autónomo fue bloqueado por el clasificador de seguridad de la sesión de Claude que corre la automatización — ver el detalle completo en `docs/methodology_and_status.md` (sección Alertas) y `docs/outreach_playbook.md` (sección 6).
- Descubrimiento de leads nuevos (#121 en adelante) pendiente de reanudar.

## Cómo se mantiene actualizado

Una tarea programada diaria (9:00am hora Bogotá) en Claude re-lee `docs/outreach_playbook.md` como fuente de verdad, ejecuta el ciclo (rebotes → follow-ups → nuevos leads → copy → envío) y actualiza los CSV de `data/` y la bitácora de `docs/methodology_and_status.md` en el Cowork Project. Este repositorio se actualiza manualmente cuando se pide una copia curada y versionada del estado del proyecto.

## Privacidad

Este repositorio es **privado**. Contiene información de contacto real de terceros (negocios prospectados) recopilada de fuentes públicas para fines de prospección comercial — no debe hacerse público sin revisar antes las implicaciones de exponer esos datos.
