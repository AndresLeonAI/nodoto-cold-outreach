# NODOTO AGENCY — Playbook Completo de Prospección + Cold Email (para la automatización diaria)

_Documento de referencia permanente. Cualquier ejecución (manual o automatizada) debe seguir exactamente estas reglas. No es un resumen — es la fuente de verdad operativa._

## 0. Identidad del remitente

- Nombre: **Andrés León**
- Cargo/firma: **Founder — NODOTO AGENCY**
- Toda comunicación se firma así, en español colombiano, tono profesional-cercano (nunca informal en exceso, nunca corporativo-frío).

## 1. Criterios de calificación de leads (quién SÍ y quién NO)

**Perfil objetivo:** negocios de servicio, tradicionales/analógicos, de "high-ticket" (transacciones o contratos de valor alto — no ventas de bajo ticket recurrente), ubicados físicamente en Bogotá, Colombia.

**Categorías válidas (igual que las 93 leads originales):**
abogados/firmas legales especializadas, consultoría financiera/tributaria/contable, clínicas y médicos especialistas (odontología premium, estética/dermatología, psiquiatría, laser/medspa), arquitectura y diseño de interiores, construcción/remodelación integral, finca raíz de alto valor (venta y arriendo comercial/residencial premium), seguros corporativos, ingeniería industrial, autos usados de lujo, eventos/bodas de alto presupuesto, salud especializada (fisioterapia, ortodoncia), administración de propiedad horizontal institucional, avalúos certificados.

**Excluir siempre:**
agencias de marketing/web/SEO/IT, freelancers individuales sin empresa constituida, restaurantes/bares, retail pequeño, peluquerías/spa de bajo ticket, gimnasios/fitness de bajo ticket, franquicias sin contacto propio en Bogotá, cualquier negocio cuyo sitio web ya sea moderno/profesional/bien construido.

**Requisito de "website problem" (obligatorio, uno de estos, verificado visitando el sitio real o confirmando que no existe):**
sin sitio web, sitio caído/no carga, plantilla genérica sin terminar (placeholders visibles), diseño muy anticuado, no responsive/mal en móvil, sin formulario de contacto ni WhatsApp visible, sin testimonios/reseñas/casos reales, enlaces rotos, información de contacto incorrecta (mapa equivocado, teléfono viejo), bloqueo de buscadores (robots.txt cerrado), SEO inexistente, contacto principal es un Gmail/Hotmail personal en vez de dominio propio, mezcla varios de estos.

## 2. Verificación anti-fabricación (regla más importante de todo el sistema)

- **Nunca inventar** un email de contacto. Debe salir de: el pie del sitio propio, Google Business Profile, redes sociales oficiales (Instagram/Facebook/LinkedIn), o el registro de Cámara de Comercio de Bogotá.
- **Nunca inventar** una observación sobre el sitio web. Cada frase de "vi que..." / "noté que..." debe corresponder a algo que se visitó y confirmó directamente en esa ejecución (no reciclar observaciones de otro negocio, no generalizar).
- **Nunca inventar** cifras (años de trayectoria, número de reseñas, número de empleados, rango de precios) — solo usar lo que aparece públicamente y se puede citar.
- **Nunca inventar** una URL de Cal.com. Reutilizar exactamente la URL real ya en uso: `https://cal.com/tu-clinica-agenda/30min` (o la que el usuario haya indicado que reemplace esta, si la actualiza).
- Antes de enviar cualquier lote, cruzar cada `business_name` y `recipient_email` contra `data/bogota_leads.csv`, `data/sent_tracking.csv` **y `data/known_bad_contacts.csv`** (ver sección 7) para: (a) confirmar que no es un duplicado, (b) confirmar que el email coincide exactamente con el que se va a usar en el envío, (c) confirmar que ni el email ni su dominio están en la lista negra de contactos ya comprobados como inválidos.
- **Regla de "nunca insultar el sitio actual":** la observación se presenta como una oportunidad de mejora concreta y específica, nunca como una crítica genérica o despectiva ("su sitio es feo/malo/anticuado" está prohibido tal cual — se describe el hecho técnico observado, ej. "el footer todavía muestra enlaces de plantilla sin relación con el negocio").
- **Si un dato encontrado por un agente es ambiguo o internamente inconsistente** (ej. un email citado que no coincide con la fuente descrita), se omite el lead por completo en vez de usarlo — pasó exactamente esto el 2026-08-28 con "Ramos Lozano Asociados", descartado por esa razón.
- **Copiar el email exactamente como aparece en la fuente**, carácter por carácter (incluyendo el dominio completo). No completar, corregir, "normalizar" ni adivinar ninguna parte de la dirección — cualquier transcripción manual es una fuente de error real: el 2026-08-27 se envió a `Contacto@hygabogados1.com` cuando el dominio real de esa firma es `hygabogados.com` (sin el "1"), y el correo rebotó porque el dominio con "1" no existe.
- **Preferir el email que esté en un enlace `mailto:` clicable** (dentro del código fuente de la página) por encima de uno que solo aparezca como texto plano en una imagen o en un directorio de terceros — un `mailto:` es más probable que esté sincronizado con el buzón real que usan, porque literalmente es el que dispara el cliente de correo del visitante.
- **Si el dominio del email de contacto es distinto al dominio del sitio web del negocio** (ej. el sitio es `xyz.com` pero el contacto es `contacto@otrodominio.com`), tratar esa discrepancia como una señal de riesgo elevado de que sea un dato desactualizado o mal transcrito — antes de aceptarlo, buscar al menos una segunda fuente independiente (Google Business Profile, red social oficial, directorio de Cámara de Comercio) que confirme esa misma dirección exacta. Si no se encuentra una segunda confirmación, es preferible omitir el lead a arriesgarse a un rebote.

## 3. Angle Engine — exactamente UNO de estos 8 por lead

- **A — Authority Gap:** el negocio tiene trayectoria/credenciales reales que el sitio no comunica.
- **B — Conversion Gap:** el sitio no facilita la conversión (sin forma de contacto clara, CTA débil o ausente).
- **C — Trust Gap:** falta de testimonios, reseñas, casos reales, evidencia social.
- **D — Google/Technical Gap:** problemas técnicos (SEO bloqueado, enlaces rotos, errores, mapas/datos incorrectos).
- **E — Positioning Gap:** el sitio no refleja el nivel/posicionamiento premium real del negocio.
- **F — Mobile Gap:** mala experiencia en dispositivos móviles.
- **G — Competitive Gap:** el sitio se ve peor que el de competidores directos evidentes.
- **H — Booking Gap:** no hay sistema de reservas/agendamiento en línea, todo depende de WhatsApp/llamada.

Cada lead recibe un único ángulo, elegido por el problema más evidente y verificable de ese negocio específico.

## 4. Estructura del correo (texto plano antes de convertir a HTML)

1. Saludo breve ("Hola," o "Hola [Nombre]," si se conoce un contacto).
2. Un párrafo de observación específica y verificada (el "gancho" — basado en el ángulo asignado).
3. Un párrafo de contexto/implicación de negocio (por qué esto importa para SU tipo de cliente).
4. Un párrafo de propuesta de valor breve ("Te podemos crear un nuevo sitio web que...").
5. Un párrafo de cierre con pregunta directa y de baja fricción ("Preparé una idea de cómo lo haría para [Negocio]. ¿Quieres que te la mande?" o variantes "¿Te la mando?").
6. Firma: "Andrés León" / "Founder — NODOTO AGENCY".

**Longitud:** 4-6 párrafos cortos, correo completo entre ~90-160 palabras. Sin bullet points, sin negritas excesivas, tono conversacional.

**Asunto:** corto y específico, variantes usadas: "Una idea para [Negocio]", "Sobre el sitio de [Negocio]", "Sobre [tema específico]", "Un detalle en su web". Nunca genérico tipo "¿Interesado en un sitio nuevo?".

## 5. Plantilla HTML (usar exactamente esta estructura — un solo CTA)

```python
CAL_URL = "https://cal.com/tu-clinica-agenda/30min"  # NUNCA cambiar sin confirmación explícita del usuario

def render_html(plain_text_body: str) -> str:
    paragraphs = [p.strip() for p in plain_text_body.split("\n\n") if p.strip()]
    body_html = ""
    for p in paragraphs:
        p_html = html.escape(p).replace("\n", "<br>")
        body_html += f'<p style="margin:0 0 16px 0;">{p_html}</p>\n'
    template = f"""<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>NODOTO AGENCY</title>
</head>
<body style="margin:0;padding:0;background-color:#f4f4f5;font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',Helvetica,Arial,sans-serif;">
<table role="presentation" width="100%" cellpadding="0" cellspacing="0" style="background-color:#f4f4f5;padding:32px 16px;">
<tr><td align="center">
<table role="presentation" width="100%" cellpadding="0" cellspacing="0" style="max-width:600px;background-color:#ffffff;border-radius:8px;overflow:hidden;">
<tr><td style="padding:40px 40px 24px 40px;">
<div style="font-size:15px;line-height:1.7;color:#27272a;">
{{body_html}}
</div>
</td></tr>
<tr><td style="padding:0 40px 40px 40px;" align="left">
<a href="{{CAL_URL}}" target="_blank" style="display:inline-block;background-color:#18181b;color:#ffffff;text-decoration:none;font-size:14px;font-weight:600;padding:13px 26px;border-radius:6px;">Ver la idea que preparé &rarr;</a>
</td></tr>
<tr><td style="padding:20px 40px 32px 40px;border-top:1px solid #e4e4e7;">
<p style="margin:0;font-size:12px;color:#a1a1aa;line-height:1.6;">
NODOTO AGENCY &middot; Bogotá, Colombia<br>
Este correo fue enviado porque identificamos su negocio como un posible caso de mejora en su presencia web. Si prefiere no recibir más mensajes como este, simplemente respóndanos indicándolo y no volveremos a escribirle.
</p>
</td></tr>
</table>
</td></tr>
</table>
</body>
</html>"""
    return template
```

(El bloque de opt-out en el footer fue añadido por decisión propia de la ejecución del 2026-08-27 como práctica de entregabilidad; mantenerlo salvo instrucción contraria del usuario.)

## 6. Envío — Composio + Gmail (3 cuentas)

- Herramientas: `COMPOSIO_MANAGE_CONNECTIONS` (mode: list) para confirmar que las 3 cuentas siguen activas ANTES de cada tanda de envío.
- Envío real: `COMPOSIO_MULTI_EXECUTE_TOOL`, `tool_slug: "GMAIL_SEND_EMAIL"`, argumentos `{recipient_email, subject, body: <html>, is_html: true}`, campo `account` con el alias de la cuenta (ej. `gmail_sleep-acerra`, `gmail_flame-gliff`, `gmail_ranter-slop` — confirmar los alias vigentes con MANAGE_CONNECTIONS ya que pueden cambiar).
- **Reparto:** round-robin estricto (`i % 3`) para que cada cuenta reciba un tercio exacto del lote del día.
- **Pacing:** enviar en tandas de ~13-16 correos (no un solo batch de 90+), con cada tanda como una llamada separada a `COMPOSIO_MULTI_EXECUTE_TOOL`. Esto reduce el riesgo de que Gmail marque las cuentas como spam.
- Verificar `success_count`/`error_count` de cada tanda antes de continuar a la siguiente.
- **Manejo de fallos de conexión:** si `COMPOSIO_MULTI_EXECUTE_TOOL` o `COMPOSIO_MANAGE_CONNECTIONS` son rechazados por el clasificador de modo automático o el servidor MCP de Composio se desconecta a mitad de una corrida, reintentar unas pocas veces (incluyendo con `ToolSearch`); si sigue sin estar disponible, NO seguir reintentando indefinidamente — registrar en `bogota_leads.csv` los leads ya verificados (para no perder el trabajo de investigación ni duplicarlos mañana), NO registrarlos en `sent_tracking.csv` como enviados, dejar constancia detallada en la sección "⚠️ Alertas" de `methodology_and_status.md`, y priorizar el reenvío de esos leads pendientes al inicio de la siguiente ejecución, antes de buscar leads nuevos.
- **Bloqueo del clasificador de seguridad (2026-08-31):** si la propia preparación o ejecución del envío masivo es rechazada por el clasificador de modo automático con un mensaje del tipo "Blocked by classifier" (a diferencia de un fallo técnico de Composio/Gmail), esto es una señal de la plataforma, no un error transitorio — **no se debe intentar rodear el bloqueo por otra vía** (otro tool, otro método). Confirmado el mismo día: el bloqueo ocurre tanto al preparar un lote como al intentar un envío individual directo, con el usuario presente en vivo pidiéndolo explícitamente — es un control a nivel de sesión, no depende de estar desatendido. En ese caso: detener el envío por completo para esa corrida, dejar el copy/HTML ya generado documentado para reutilizarlo en la siguiente corrida (o entregarlo al usuario para que lo envíe por su cuenta), y registrar la alerta explicando que el envío autónomo quedó bloqueado y que la resolución depende de quien administre los permisos de la cuenta/sesión de Claude, no de la automatización en sí.

## 7. Verificación de entregabilidad — SOLO herramientas gratuitas, sin cuentas de pago

**Contexto:** el 2026-08-28 se confirmaron 5 rebotes duros y 1 blando sobre 107 envíos (~5.6%). El usuario pidió explícitamente resolverlo **sin herramientas de pago**.

**Lo que se investigó y NO funciona en este entorno:**
- Verificación SMTP propia (`RCPT TO`): el puerto saliente 25 está bloqueado por la política de red del entorno.
- APIs públicas gratuitas de verificación de correo: "EVA" descontinuada; "Disify" bloqueada por robots.txt para las herramientas del entorno. Llamadas HTTP directas por shell bloqueadas salvo a dominios de paquetes.
- **Conclusión honesta:** ningún método (pago o gratis) garantiza el 100% sin una conexión SMTP en vivo contra el buzón exacto — ni Hunter/ZeroBounce lo prometen.

**Nivel 1 — Chequeo de MX (obligatorio, gratis).** Antes de agregar cualquier email nuevo, confirmar que el dominio tiene registros MX válidos vía DNS estándar:

```python
import dns.resolver  # pip install dnspython --break-system-packages

def has_mx(domain: str) -> bool:
    try:
        answers = dns.resolver.resolve(domain, "MX")
        return len(answers) > 0
    except Exception:
        return False
```

Si `has_mx()` devuelve `False`, el lead se descarta por completo.

**Nivel 2 — Corroboración de fuente reforzada (obligatorio, gratis).**
- Preferir siempre el email en un `mailto:` clicable del sitio propio sobre uno en texto plano o directorio externo.
- Si el dominio del email no coincide con el del sitio web, exigir una segunda fuente independiente o descartar el lead.
- Tratar con más cautela los emails hallados en páginas con señales de abandono.

**Nivel 3 — Monitoreo de rebotes post-envío + lista negra permanente (obligatorio, gratis).** Al inicio de cada ejecución diaria, revisar las 3 cuentas Gmail con `GMAIL_FETCH_EMAILS` (`query: "from:mailer-daemon"`). Para cada rebote:
1. Confirmar que el `threadId` coincide con un `gmail_message_id` conocido en `sent_tracking.csv` (ignorar los que no coincidan).
2. Clasificar: **duro/permanente** (SMTP 5.x.x, o "Delivery Status Notification (Failure)" tras agotar reintentos aunque el código sea 4.x.x) → `status = BOUNCED`, nunca recibe follow-up, se agrega a `known_bad_contacts.csv` (bloqueando el email o, si el dominio no existe, el dominio completo). **Blando/temporal** (4.x.x con asunto "Delay", Gmail sigue reintentando) → `status = SOFT_BOUNCE`, no se agrega a la lista negra, se reintenta en 5-7 días. Revisar en cada corrida si un SOFT_BOUNCE escaló a BOUNCED.
3. Guardar cambios en `sent_tracking.csv` y `known_bad_contacts.csv`.

**Regla de exclusión de follow-ups:** solo se consideran filas `status = SENT` (nunca `BOUNCED`).

**Regla de "nunca dos veces el mismo error":** cruzar cualquier lead nuevo contra `known_bad_contacts.csv` (email y dominio) antes de agregarlo.

## 8. Secuencia de follow-up (3 pasos)

- **Follow-up 1** (~4 días después del envío inicial): recordatorio breve, mismo Cal.com CTA, tono ligero, sin repetir el ángulo/observación original.
- **Follow-up 2** (~4 días después del follow-up 1): nuevo ángulo de valor o refuerzo social, mismo CTA.
- **Follow-up 3** (~4-5 días después del follow-up 2, último contacto): cierre breve de baja presión, mismo CTA.
- Si el lead responde en cualquier punto, se detiene la secuencia.
- Nunca se envía follow-up a un lead `BOUNCED`.

## 9. Registro y trazabilidad

- **`data/bogota_leads.csv`**: única fuente de verdad de todos los leads jamás descubiertos (`#, Business Name, Industry/Niche, Bogota Location, Website, Website Problem, Business Email, Evidence/Source, Why High-Ticket Prospect, Lead Score`). Numeración consecutiva, nunca se reutiliza un número.
- **`data/sent_tracking.csv`**: registro de cada envío realmente efectuado (`row_number, business_name, recipient_email, gmail_account, gmail_message_id, status, sent_at, followup_1_sent_at, followup_2_sent_at, followup_3_sent_at`). Status válidos: `SENT`, `BOUNCED (motivo)`, `SOFT_BOUNCE (motivo)`, `RESPONDED`, `OPTED_OUT`.
- **`data/known_bad_contacts.csv`**: lista negra permanente (`email, domain, reason, detection_method, date_detected, source_row`). Nunca se borran entradas.
- **`docs/methodology_and_status.md`**: bitácora de alto nivel, actualizada al final de cada ejecución.

## 10. Historial de ejecuciones

- **2026-08-27:** primera ejecución. 93 leads verificados, 93/93 correos enviados (31/31/31 entre 3 cuentas). (Después se confirmaron 3 rebotes duros y 1 blando.)
- **2026-08-28:** segunda ejecución (primera automatizada). 27 leads nuevos verificados (#94–120), por debajo de la meta de 93 por agotamiento de presupuesto de búsqueda. 14 enviados ese día, 13 al día siguiente.
- **2026-08-28 (correcciones):** el usuario reportó rebotes reales. Se confirmaron 5 duros y 1 blando sobre 107 envíos. Se implementó la sección 7 (MX + corroboración de fuente + monitoreo de rebotes + lista negra), 100% gratis, sin servicios de pago.
- **2026-08-29:** se enviaron los 13 leads pendientes (#108–120); 12 de 13 (el #109 se excluyó por MX inválido).
- **2026-08-31 (cuarta ejecución):** 2 rebotes duros nuevos (#50, #74, timeout tras agotar reintentos) y 1 blando nuevo (#103). 86 follow-ups 1 redactados y listos, pero el envío masivo fue bloqueado por el clasificador de seguridad de la sesión — confirmado que el bloqueo persiste tanto en lote como individual, con el usuario presente en vivo. 0 follow-ups enviados. Descubrimiento de leads nuevos no iniciado. Se creó este repositorio de GitHub (privado) como copia curada y versionada del estado del proyecto.
