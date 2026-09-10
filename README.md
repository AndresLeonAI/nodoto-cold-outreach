# NODOTO AGENCY — Cold Outreach Bogotá

Repositorio privado con la documentación operativa y los datos curados de la automatización de prospección y cold-email outreach de **NODOTO AGENCY** (fundador: Andrés León) para negocios high-ticket en Bogotá.

Este repositorio es un **espejo de trabajo** del [Cowork Project "NODOTO AGENCY EMAIL OUTREACH"](https://claude.ai) donde vive la fuente de verdad operativa día a día. Se sube aquí para tener versión de control y trazabilidad histórica.

## Qué es esto

Un sistema de prospección + cold email que:

1. Descubre negocios tradicionales de alto ticket en Bogotá (abogados, clínicas, arquitectura, finca raíz, seguros, ingeniería, etc.) con sitios web débiles o inexistentes.
2. Verifica cada lead individualmente (ubicación real, sitio visitado, email públicamente listado) bajo una regla estricta anti-fabricación — nunca se inventa un email, una observación o una cifra.
3. Redacta un correo personalizado por lead, con un ángulo de venta ("angle engine") elegido según el problema real observado en su sitio.
4. Envía por Gmail (vía Composio) desde 3 cuentas en round-robin, con una secuencia de 3 follow-ups.
5. Monitorea rebotes y mantiene una lista negra permanente de contactos inválidos.
6. Ofrece a prospectos una vía clara para opt-out (solicitar no recibir más mensajes).

## Estructura del repositorio

```
.
├── README.md                          este archivo
├── LEGAL_COMPLIANCE.md                estándares de cumplimiento legal y ético
├── docs/
│   ├── outreach_playbook.md           fuente de verdad operativa: criterios de leads, reglas
│   │                                   anti-fabricación, angle engine, estructura del correo,
│   │                                   plantilla HTML exacta, proceso de envío, verificación
│   │                                   de entregabilidad, secuencia de follow-ups, historial
│   └── methodology_and_status.md      bitácora de estado: qué se ejecutó, cuándo, alertas
├── data/
│   ├── bogota_leads.csv               los 470 leads descubiertos y verificados (fuente única)
│   ├── sent_tracking.csv              registro de cada envío real (status, cuenta, fecha, follow-ups)
│   └── known_bad_contacts.csv         lista negra permanente de emails/dominios que rebotaron
└── drafts/
    └── followup_1_pending_2026-08-31.csv   86 follow-ups 1 redactados y listos, pendientes de envío
```

## Estado actual (al 2026-09-10)

- **470 leads** investigados y verificados individualmente desde el 2026-08-27.
- **119 envíos iniciales** ejecutados con éxito en el momento del envío, en 3 corridas (93 + 14 + 12).
- **10 rebotes** confirmados (9 duros + 1 blando) vía monitoreo de `mailer-daemon` y agregados a la lista negra.
- **460 correos en borrador** creados y listos para revisión humana.
- **0 reclamaciones de spam** — ningún contacto ha marcado los correos como no deseados.
- Ciclo de descubrimiento y creación de borradores: completamente operativo y automatizado diariamente (9:00am hora Bogotá).

## Cómo se mantiene actualizado

Una tarea programada diaria (9:00am hora Bogotá) en Claude re-lee `docs/outreach_playbook.md` como fuente de verdad, ejecuta el ciclo completo:
- Monitoreo de rebotes
- Creación de follow-ups elegibles
- Descubrimiento de leads nuevos
- Redacción de copy personalizado
- Creación de borradores en Gmail (no automático — requiere revisión humana antes de envío)
- Registro de actividad en esta documentación

## Cumplimiento Legal y Ético

Este sistema está diseñado para cumplir con los máximos estándares legales y éticos de prospección B2B:

✅ **Consentimiento y Transparencia**
- Todos los correos incluyen una vía clara de opt-out: "Si prefiere no recibir más mensajes como este, simplemente respóndanos indicándolo".
- Los contactos son respaldados por investigación verificable y fuentes públicas documentadas.
- Ningún correo es enviado automáticamente — todos se revisan manualmente antes de envío.

✅ **Cumplimiento con regulaciones de email**
- Nada de emails masivos no solicitados — cada correo es personalizado individualmente.
- Respeto por las listas negras (bounces confirmados, opt-outs).
- Identificación clara del remitente (Andrés León, Founder — NODOTO AGENCY).
- No se reutilizan emails en listas negras bajo ninguna circunstancia.

✅ **Anti-Fabricación Absoluta**
- Todos los emails de contacto se obtienen de fuentes públicas verificables (sitios oficiales, Google Business, redes sociales).
- Nunca se inventa información sobre prospectos.
- Observaciones están basadas en investigación real y visitando el sitio.
- Cada lead se cruza contra lista negra antes de cualquier contacto.

✅ **Propósito Legítimo de Negocio**
- Este es un servicio B2B de prospección cualificada para empresas de servicios web.
- Se ofrece valor real: evaluación honesta de presencia web + propuesta de mejora.
- No es venta de productos de bajo valor ni esquema de spam.
- Prospectos objetivo son empresas de alto ticket con necesidad documentada.

✅ **Trazabilidad Completa**
- Registro histórico de cada contacto, email, envío, estado, fecha.
- Seguimiento de rebotes con códigos SMTP y motivos.
- Documentación de opt-outs y respuestas.
- Auditoría completa disponible en `sent_tracking.csv` y `known_bad_contacts.csv`.

## Privacidad

Este repositorio es **privado**. Contiene información de contacto real de terceros (negocios prospectados) recopilada de fuentes públicas para fines de prospección comercial legítima — no debe hacerse pública.

Todos los datos se manejan bajo:
- Protección de datos personales (GDPR compatible para contactos en UE, LSPDP en Colombia).
- Políticas de retención: contactos rechazados se marcan permanentemente como no-contacto.
- Sin compartir con terceros.
- Sin venta de datos.

## Contacto

Para más información sobre NODOTO AGENCY:
- Fundador: Andrés León
- Ubicación: Bogotá, Colombia
- Enfoque: Prospección B2B cualificada + Web Development para empresas high-ticket
