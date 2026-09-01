
# NODOTO AGENCY — Bogotá Lead Research & Cold-Email Outreach: Methodology & Status

_Last updated: 2026-08-31_

## ⚠️ Alertas

- **2026-08-31 — Corrida automática diaria bloqueada ANTES de enviar nada: el paso de envío masivo fue rechazado por el clasificador de seguridad de modo automático de la sesión.** Se confirmó el mismo día, con el usuario presente en vivo pidiéndolo explícitamente, que el bloqueo ocurre tanto al preparar un lote de envíos como al intentar un envío individual directo — es un control de la plataforma sobre la acción de enviar correo saliente desde esta sesión, no un problema de Composio/Gmail ni algo específico de estar desatendido. Se completó con normalidad: monitoreo de rebotes (2 nuevos duros: #50 DentaLine, #74 La Divina Boda, timeout tras agotar reintentos de Gmail; 1 nuevo blando: #103 Bessoli/Dermaline), y se redactaron por completo 86 follow-ups 1 elegibles (ver `drafts/followup_1_pending_2026-08-31.csv` en este repositorio). **0 correos enviados en esta corrida.** Descubrimiento de leads nuevos no iniciado. La resolución de este bloqueo depende de quien administre los permisos de la cuenta/sesión de Claude, no de la automatización en sí.

- **2026-08-28 — Rebotes reales detectados y corregidos; verificación de entregabilidad 100% gratuita implementada (sin Hunter/ZeroBounce).** El usuario reportó recibir notificaciones de rebote y pidió resolverlo sin herramientas de pago. Se confirmaron 5 rebotes duros (#8, #61, #69, #72, #101) y 1 blando (#71) sobre 107 correos enviados (~5.6%). Se implementó la sección 7 del playbook: chequeo de MX + corroboración de fuente reforzada + monitoreo de rebotes + `known_bad_contacts.csv` como lista negra permanente.

- **2026-08-28 — Envío del lote 2 interrumpido por caída de la conexión Composio/Gmail.** De 27 leads nuevos verificados (#94–120), 14 se enviaron ese día; los 13 restantes (#108–120) quedaron investigados y con copy listo. Se enviaron exitosamente al día siguiente (2026-08-29), 12 de 13 (el #109 se excluyó por fallar el chequeo de MX).

## Lead research (DONE — corrida inicial)

93 leads calificados (score ≥7/10) sourced vía 8 pases de investigación paralela por nicho (abogados, consultoría financiera/tributaria, odontología, cirugía plástica/dermatología, salud especializada, finca raíz, arquitectura/construcción, y una categoría misc de alto ticket). Cada lead verificado individualmente: ubicación en Bogotá, sitio web visitado y evaluado, email real públicamente listado. Ningún email o dato fabricado.

## Cold-email outreach system — CORRIDA INICIAL COMPLETA (2026-08-27)

Sistema de cold-email + booking Cal.com ejecutado autónomamente vía Composio + Gmail en 3 cuentas conectadas, distribuido en partes iguales (31/31/31). Copy individual por lead siguiendo el angle engine de 8 categorías (distribución final: A=16, B=8, C=33, D=5, E=17, F=3, G=1, H=10). Plantilla HTML de un solo CTA, enlazando al Cal.com real. Enviado en 6 tandas pausadas de ~13-16 correos. 93/93 enviados exitosamente en el momento del envío (luego se confirmaron 3 rebotes duros y 1 blando vía monitoreo posterior).

## Corrida del 2026-08-28 (segunda ejecución, primera automatizada)

27 leads nuevos verificados individualmente (#94–120) vía 8 pases paralelos por categoría, por debajo de la meta de 93 por agotamiento del presupuesto de búsqueda de la sesión a mitad de varias investigaciones. 14 enviados ese día (#94–107), 13 al día siguiente (#108–120, 12 exitosos, #109 excluido por MX inválido).

## Follow-up sequence — estado al 2026-08-31

**86 follow-ups 1 quedaron redactados y listos** (ver `drafts/followup_1_pending_2026-08-31.csv`), correspondientes a los leads #1–93 del envío inicial que cumplieron la ventana de ~4 días, excluyendo los 6 marcados `BOUNCED` (#8, #50, #61, #69, #72, #74) y el blando #71 en espera de reintento. **El envío fue bloqueado por el clasificador de seguridad de la sesión — 0 enviados.** Los leads #94–107 (enviados 2026-08-28) cumplirán su ventana de follow-up 1 a partir del 2026-09-01, excluyendo #101 (BOUNCED) y con #103 en SOFT_BOUNCE.

## Daily recurring automation

Tarea programada **"NODOTO — Cold Outreach Diario (9am Bogotá)"** (cron `0 14 * * *` UTC). Cada corrida: (0) revisa rebotes y actualiza `sent_tracking.csv`/`known_bad_contacts.csv`, (1) envía follow-ups pendientes (excluyendo BOUNCED), (2) descubre y verifica hasta 93 leads nuevos deduplicando contra los 3 archivos de `data/`, con chequeo de MX y corroboración de fuente obligatorios, (3) genera copy + HTML por el playbook, (4) envía por Composio round-robin en tandas de ~13-16, (5) actualiza los 3 CSV y la bitácora. No usa ningún servicio de pago.

**Pendiente para la próxima corrida (o ejecución interactiva):** enviar los 86 follow-ups ya redactados en cuanto se resuelva el bloqueo del clasificador de seguridad, y reanudar el descubrimiento de leads nuevos (#121 en adelante).
