# NODOTO AGENCY — PLAYBOOK COMPLETO DE PROSPECCIÓN + COLD EMAIL

**Fuente de verdad operativa para la automatización diaria.**

Toda ejecución manual o automatizada debe seguir estas reglas. La prioridad es:

1. Calidad del lead.
2. Verificación real de la información.
3. Personalización.
4. Entregabilidad.
5. No duplicación.
6. Trazabilidad completa.
7. Ejecución eficiente.

---

# 0. IDENTIDAD DEL REMITENTE

* **Nombre:** Andrés León
* **Cargo:** Founder — NODOTO AGENCY
* **Ubicación:** Bogotá, Colombia
* **Idioma:** español colombiano.
* **Tono:** profesional, cercano, directo y humano.
* Nunca sonar excesivamente informal.
* Nunca sonar corporativo o artificial.
* Toda comunicación debe firmarse:

**Andrés León**
**Founder — NODOTO AGENCY**

---

# 1. PERFIL DEL LEAD IDEAL

## Objetivo

Negocios de servicios tradicionales o analógicos, de alto valor económico, ubicados físicamente en Bogotá, Colombia.

El prospecto ideal tiene:

* ticket alto;
* necesidad clara de confianza;
* dependencia de reputación;
* clientes que investigan antes de contactar;
* potencial para obtener clientes mediante Google, web, WhatsApp o agendamiento;
* presencia digital deficiente o desaprovechada.

## Categorías prioritarias

* Abogados y firmas legales especializadas.
* Consultoría financiera, tributaria y contable.
* Clínicas y médicos especialistas.
* Odontología premium.
* Estética, dermatología, psiquiatría, láser y medspa.
* Arquitectura.
* Diseño de interiores.
* Construcción y remodelación integral.
* Finca raíz de alto valor.
* Venta y arriendo comercial/residencial premium.
* Seguros corporativos.
* Ingeniería industrial.
* Autos usados de lujo.
* Eventos y bodas de alto presupuesto.
* Fisioterapia especializada.
* Ortodoncia.
* Administración institucional de propiedad horizontal.
* Avalúos certificados.

---

# 2. EXCLUSIONES

Excluir siempre:

* agencias de marketing;
* agencias web;
* agencias SEO;
* empresas IT;
* freelancers individuales sin empresa constituida;
* restaurantes;
* bares;
* retail pequeño;
* peluquerías;
* spas de bajo ticket;
* gimnasios/fitness de bajo ticket;
* franquicias sin contacto propio en Bogotá;
* negocios sin potencial económico suficiente;
* negocios cuyo sitio web ya sea moderno, profesional y correctamente construido.

---

# 3. WEBSITE PROBLEM — REQUISITO OBLIGATORIO

Cada lead debe tener al menos **un problema web verificable**.

Los problemas aceptables son:

* no existe sitio web;
* sitio caído;
* sitio que no carga correctamente;
* plantilla genérica;
* placeholders visibles;
* diseño claramente anticuado;
* experiencia móvil deficiente;
* ausencia de formulario de contacto;
* ausencia de WhatsApp visible;
* ausencia de testimonios;
* ausencia de casos reales;
* enlaces rotos;
* información de contacto incorrecta;
* mapa incorrecto;
* teléfono desactualizado;
* problemas técnicos de SEO;
* indexación deficiente;
* SEO inexistente;
* contacto principal mediante Gmail/Hotmail personal en lugar de dominio propio;
* combinación de varios problemas anteriores.

La observación debe verificarse directamente.

**Nunca inventar un problema del sitio.**

---

# 4. REGLA ABSOLUTA DE ANTI-FABRICACIÓN

Esta es una de las reglas principales del sistema.

## Emails

Nunca inventar, completar o corregir un email.

El email debe provenir de una fuente verificable:

1. sitio oficial;
2. footer del sitio;
3. enlace `mailto:`;
4. Google Business Profile;
5. Instagram oficial;
6. Facebook oficial;
7. LinkedIn oficial;
8. Cámara de Comercio de Bogotá;
9. otra fuente pública claramente vinculada al negocio.

Copiar exactamente el email encontrado.

No:

* corregirlo;
* normalizarlo;
* cambiar mayúsculas;
* completar caracteres;
* asumir extensiones;
* sustituir dominios.

## Preferencia por `mailto:`

Cuando exista un enlace `mailto:` clicable en el sitio oficial, preferirlo sobre un email que solamente aparezca como texto.

## Discrepancia de dominios

Si:

`website.com`

pero el email es:

`contacto@otrodominio.com`

considerarlo una señal de riesgo.

Antes de aceptar el lead, buscar una segunda fuente independiente que confirme exactamente ese email.

Si no existe corroboración suficiente, descartar el contacto.

---

# 5. OBSERVACIONES DEL SITIO

Toda frase como:

> "Vi que..."

> "Noté que..."

> "Revisando su sitio..."

debe corresponder exactamente a algo observado durante la investigación.

Nunca:

* reciclar una observación de otro negocio;
* asumir que todos los sitios de una industria tienen el mismo problema;
* inventar problemas;
* utilizar información de investigaciones antiguas sin verificarla nuevamente.

## Nunca insultar el sitio

Está prohibido utilizar:

* "su sitio es feo";
* "su web es mala";
* "su página es horrible";
* "su web es anticuada" como crítica genérica.

En su lugar describir el hecho técnico:

> "El sitio actualmente no muestra un CTA claro para solicitar una valoración."

> "En móvil, el formulario queda debajo de varios bloques de contenido."

> "El footer todavía contiene enlaces que no corresponden al negocio."

La observación debe ser concreta, profesional y útil.

---

# 6. CIFRAS Y DATOS

Nunca inventar:

* años de trayectoria;
* número de pacientes;
* número de clientes;
* número de empleados;
* número de reseñas;
* facturación;
* precios;
* ubicaciones;
* certificaciones;
* casos de éxito.

Solo utilizar información públicamente verificable.

---

# 7. DEDUPLICACIÓN

Antes de aceptar cualquier lead nuevo, cruzar:

* `claude/bogota_leads.csv`
* `claude/sent_tracking.csv`
* `claude/known_bad_contacts.csv`

Verificar:

1. Business Name.
2. Email.
3. Dominio.
4. Website.
5. Existencia de contacto previo.
6. Posibles duplicados por variaciones del nombre.

Nunca reutilizar un número de lead.

Cada lead nuevo recibe el siguiente número consecutivo disponible.

---

# 8. KNOWN BAD CONTACTS

`claude/known_bad_contacts.csv`

Columnas:

```text
email,domain,reason,detection_method,date_detected,source_row
```

Debe consultarse antes de agregar cualquier lead.

Si el email exacto aparece:

**Descartar.**

Si el dominio está bloqueado:

**Descartar cualquier email de ese dominio**, salvo que exista una razón documentada para eliminar posteriormente esa entrada.

Nunca eliminar entradas históricas de esta lista.

---

# 9. VERIFICACIÓN DE ENTREGABILIDAD

La verificación gratuita se realiza en tres niveles.

## Nivel 1 — MX

Todo dominio debe tener registros MX válidos.

```python
import dns.resolver

def has_mx(domain: str) -> bool:
    try:
        answers = dns.resolver.resolve(domain, "MX")
        return len(answers) > 0
    except Exception:
        return False
```

Si:

```text
has_mx(domain) == False
```

el lead se descarta.

No se agrega a `bogota_leads.csv`.

## Nivel 2 — Corroboración

Priorizar:

1. `mailto:` del sitio oficial.
2. Email visible en el sitio oficial.
3. Google Business Profile.
4. Redes oficiales.
5. Cámara de Comercio.

Cuando el dominio del email y el sitio no coincidan, exigir segunda fuente independiente.

## Nivel 3 — Rebotes

Revisar periódicamente las cuentas conectadas buscando:

```text
from:mailer-daemon
```

Para cada rebote:

* identificar el mensaje original;
* comprobar el `threadId`;
* determinar si es duro o temporal;
* actualizar `sent_tracking.csv`;
* actualizar `known_bad_contacts.csv` cuando corresponda.

---

# 10. CLASIFICACIÓN DE REBOTES

## HARD BOUNCE

Ejemplos:

* `5.x.x`;
* address not found;
* mailbox does not exist;
* dominio inexistente;
* relay denied;
* fallo permanente;
* Gmail agotó todos los reintentos y genera Failure.

Estado:

```text
BOUNCED (motivo)
```

El lead no recibe ningún follow-up.

Si corresponde, agregar email/dominio a:

```text
known_bad_contacts.csv
```

## SOFT BOUNCE

Ejemplos:

* `4.x.x`;
* Delay;
* mailbox temporalmente lleno;
* rate limit;
* timeout temporal;
* try again later.

Estado:

```text
SOFT_BOUNCE (motivo)
```

No avanzar automáticamente al siguiente follow-up.

Revisar posteriormente si el retraso se convirtió en Failure.

---

# 11. ANGLE ENGINE

Cada lead recibe **exactamente un** ángulo.

## A — Authority Gap

Tiene trayectoria, credenciales o experiencia que el sitio no comunica correctamente.

## B — Conversion Gap

El sitio no facilita suficientemente la conversión.

## C — Trust Gap

Faltan testimonios, casos, reseñas o evidencia social.

## D — Google/Technical Gap

Problemas técnicos, SEO, enlaces, indexación, mapas o información incorrecta.

## E — Positioning Gap

El sitio no representa el nivel premium real del negocio.

## F — Mobile Gap

La experiencia móvil presenta problemas relevantes.

## G — Competitive Gap

El sitio queda claramente por debajo de competidores directos.

## H — Booking Gap

No existe un sistema claro de agendamiento online.

Elegir solamente el problema más evidente y demostrable.

---

# 12. ESTRUCTURA DEL COLD EMAIL

Cada email debe tener entre **90 y 160 palabras**.

Debe contener:

### Párrafo 1

Saludo.

Ejemplo:

> Hola,

o:

> Hola [Nombre],

### Párrafo 2

Observación específica.

Debe demostrar que el negocio fue investigado.

### Párrafo 3

Implicación comercial.

Explicar brevemente por qué ese problema puede afectar la adquisición de clientes de ese negocio.

### Párrafo 4

Propuesta de valor.

Explicar que NODOTO puede crear una nueva experiencia web enfocada en:

* posicionamiento;
* confianza;
* conversión;
* captación;
* agendamiento;
* experiencia premium.

### Párrafo 5

CTA de baja fricción.

Ejemplo:

> Preparé una idea de cómo lo haría para [Negocio]. ¿Te la mando?

### Firma

> Andrés León
> Founder — NODOTO AGENCY

---

# 13. REGLAS DE COPY

El correo debe:

* sentirse escrito individualmente;
* demostrar investigación;
* ser corto;
* tener una sola idea central;
* evitar exageraciones;
* evitar lenguaje de vendedor agresivo;
* evitar párrafos largos;
* evitar bullet points;
* evitar lenguaje corporativo;
* evitar frases genéricas.

Nunca decir:

> "Encontré su negocio en Google y quería ofrecerle..."

Nunca utilizar:

> "Somos una empresa líder..."

Nunca comenzar con una presentación larga de NODOTO.

El protagonista es el negocio del prospecto.

---

# 14. ASUNTOS

Usar asuntos cortos y específicos.

Ejemplos:

```text
Una idea para [Negocio]
Sobre el sitio de [Negocio]
Sobre [tema específico]
Un detalle en su web
```

Nunca:

```text
¿Interesado en un sitio nuevo?
```

Evitar asuntos genéricos de venta.

---

# 15. CAL.COM

Utilizar exactamente:

```text
https://cal.com/tu-clinica-agenda/30min
```

No modificar esta URL salvo instrucción explícita del usuario.

Nunca inventar una URL alternativa.

---

# 16. HTML

Utilizar esta estructura:

```python
import html

CAL_URL = "https://cal.com/tu-clinica-agenda/30min"

def render_html(plain_text_body: str) -> str:
    paragraphs = [
        p.strip()
        for p in plain_text_body.split("\n\n")
        if p.strip()
    ]

    body_html = ""

    for p in paragraphs:
        p_html = html.escape(p).replace("\n", "<br>")
        body_html += (
            f'<p style="margin:0 0 16px 0;">'
            f'{p_html}</p>\n'
        )

    return f"""<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>NODOTO AGENCY</title>
</head>

<body style="margin:0;padding:0;background-color:#f4f4f5;font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',Helvetica,Arial,sans-serif;">

<table role="presentation" width="100%" cellpadding="0" cellspacing="0"
style="background-color:#f4f4f5;padding:32px 16px;">

<tr>
<td align="center">

<table role="presentation" width="100%" cellpadding="0" cellspacing="0"
style="max-width:600px;background-color:#ffffff;border-radius:8px;overflow:hidden;">

<tr>
<td style="padding:40px 40px 24px 40px;">

<div style="font-size:15px;line-height:1.7;color:#27272a;">
{body_html}
</div>

</td>
</tr>

<tr>
<td style="padding:0 40px 40px 40px;" align="left">

<a href="{CAL_URL}"
target="_blank"
style="display:inline-block;background-color:#18181b;color:#ffffff;text-decoration:none;font-size:14px;font-weight:600;padding:13px 26px;border-radius:6px;">

Ver la idea que preparé &rarr;

</a>

</td>
</tr>

<tr>
<td style="padding:20px 40px 32px 40px;border-top:1px solid #e4e4e7;">

<p style="margin:0;font-size:12px;color:#a1a1aa;line-height:1.6;">

NODOTO AGENCY &middot; Bogotá, Colombia<br>

Este correo fue enviado porque identificamos su negocio como un posible caso de mejora en su presencia web. Si prefiere no recibir más mensajes como este, simplemente respóndanos indicándolo y no volveremos a escribirle.

</p>

</td>
</tr>

</table>

</td>
</tr>

</table>

</body>
</html>"""
```

Un único CTA por correo.

---

# 17. POLÍTICA DE BORRADORES

En ejecuciones automatizadas o desatendidas:

**crear borradores, no realizar envíos automáticos.**

Cada borrador debe:

* estar completamente personalizado;
* contener HTML válido;
* tener el email verificado;
* tener el asunto correspondiente;
* usar el Cal.com correcto;
* quedar registrado.

Estado inicial:

```text
DRAFT_READY
```

El campo `sent_at` solamente se completa cuando el mensaje haya sido efectivamente enviado y confirmado.

---

# 18. CUENTAS GMAIL

Las cuentas conectadas deben comprobarse antes de crear borradores.

Distribución de primeros contactos:

```text
round-robin
```

Para un lote de `N` leads:

```text
i % 3
```

Esto mantiene una distribución equilibrada entre las tres cuentas.

Los follow-ups deben conservar la misma cuenta utilizada para el contacto inicial.

Nunca mover un follow-up a otra cuenta.

---

# 19. FOLLOW-UP 1

Aproximadamente 4 días después del envío inicial.

Condición obligatoria:

```text
status = SENT
```

Nunca considerar `DRAFT_READY` como un envío.

Ejemplo:

> Hola [Nombre],

> Quería hacerte seguimiento al correo que te envié hace unos días sobre [Negocio]. Preparé una idea concreta de cómo podría mejorar la experiencia web y la conversión.

> ¿Alcanzaste a verlo?

Mantenerlo breve.

No copiar literalmente el email inicial.

---

# 20. FOLLOW-UP 2

Aproximadamente 4 días después del **envío confirmado del Follow-up 1**.

Nunca utilizar la fecha de creación del borrador como referencia.

Debe introducir:

* un nuevo ángulo;
* una observación adicional;
* una idea de valor;
* o una referencia contextual relevante.

No repetir exactamente el mensaje anterior.

---

# 21. FOLLOW-UP 3

Aproximadamente 4–5 días después del **envío confirmado del Follow-up 2**.

Último contacto.

Debe ser breve y de baja presión.

Después del Follow-up 3:

**no contactar nuevamente salvo que el lead responda.**

---

# 22. RESPUESTAS Y OPT-OUT

Si un lead responde:

```text
RESPONDED
```

Detener inmediatamente la secuencia automática.

Si solicita no recibir más mensajes:

```text
OPTED_OUT
```

Detener cualquier comunicación futura.

Nunca enviar follow-ups a:

```text
BOUNCED
OPTED_OUT
RESPONDED
```

---

# 23. SENT_TRACKING.CSV

Archivo:

```text
claude/sent_tracking.csv
```

Columnas:

```text
row_number
business_name
recipient_email
gmail_account
gmail_message_id
status
sent_at
followup_1_sent_at
followup_2_sent_at
followup_3_sent_at
draft_id
followup_1_draft_id
followup_2_draft_id
followup_3_draft_id
```

Estados válidos:

```text
DRAFT_READY
SENT
BOUNCED (motivo)
SOFT_BOUNCE (motivo)
RESPONDED
OPTED_OUT
```

Nunca marcar:

```text
DRAFT_READY
```

como:

```text
SENT
```

---

# 24. BOGOTA_LEADS.CSV

Archivo maestro:

```text
claude/bogota_leads.csv
```

Columnas:

```text
#
Business Name
Industry/Niche
Bogota Location
Website
Website Problem
Business Email
Evidence/Source
Why High-Ticket Prospect
Lead Score
```

Este archivo contiene todos los leads descubiertos históricamente.

Un lead verificado debe agregarse aunque todavía no se haya creado su borrador.

---

# 25. METHODOLOGY_AND_STATUS.MD

Archivo:

```text
claude/methodology_and_status.md
```

Debe registrar:

* fecha;
* leads descubiertos;
* leads descartados;
* leads verificados;
* borradores creados;
* envíos confirmados;
* follow-ups;
* rebotes;
* contactos agregados a blacklist;
* errores;
* discrepancias;
* incidencias de sincronización;
* cualquier trabajo pendiente.

---

# 26. INTEGRIDAD DE ARCHIVOS

Antes de modificar cualquier archivo maestro:

1. leer la versión actual;
2. trabajar sobre esa versión;
3. fusionar los cambios;
4. verificar el resultado;
5. guardar la versión final.

Nunca reemplazar un archivo grande sin comprobar previamente su contenido actual.

Después de una modificación importante verificar:

* número de filas;
* números consecutivos;
* ausencia de duplicados;
* presencia de leads conocidos;
* columnas;
* emails;
* estados;
* IDs de borradores.

---

# 27. COORDINACIÓN DE AGENTES

Cuando varios agentes investiguen leads simultáneamente:

**los agentes secundarios NO deben escribir directamente en los CSV maestros.**

Cada agente debe devolver sus leads verificados al orquestador central.

Cada resultado debe incluir todos los campos necesarios:

```text
#
Business Name
Industry/Niche
Bogota Location
Website
Website Problem
Business Email
Evidence/Source
Why High-Ticket Prospect
Lead Score
```

El orquestador:

1. recibe todos los resultados;
2. elimina duplicados;
3. cruza blacklist;
4. valida emails;
5. valida MX;
6. verifica inconsistencias;
7. fusiona secuencialmente;
8. escribe una sola versión final.

---

# 28. GITHUB / SINCRONIZACIÓN

Nunca asumir que un push fue exitoso solamente porque una herramienta lo reportó.

Cuando exista una copia externa del archivo maestro:

1. obtener el contenido real;
2. comprobar SHA/commit;
3. comprobar número de filas;
4. comparar contra la versión local;
5. verificar muestras puntuales;
6. confirmar que los últimos leads existen.

La fuente operativa principal sigue siendo el archivo maestro actual del Project.

---

# 29. PRIORIDAD DE CADA EJECUCIÓN

Cada corrida diaria debe seguir este orden:

## PASO 0 — REBOTES

Revisar:

```text
from:mailer-daemon
```

Actualizar:

* `sent_tracking.csv`
* `known_bad_contacts.csv`

## PASO 0.5 — RECONCILIACIÓN

Comprobar que los borradores existentes y documentados sean consistentes.

Si aparecen borradores no documentados:

1. identificarlos;
2. recuperar destinatario;
3. recuperar asunto;
4. recuperar contenido;
5. comprobar duplicados;
6. verificar MX;
7. reconciliar los archivos.

No iniciar discovery nuevo hasta resolver una discrepancia importante.

## PASO 1 — FOLLOW-UPS

Crear los follow-ups elegibles.

Condición:

```text
status = SENT
```

Respetar siempre:

* orden de la secuencia;
* fecha real de envío;
* cuenta original;
* ausencia de respuesta;
* ausencia de bounce.

## PASO 2 — DISCOVERY

Buscar nuevos leads.

Objetivo:

```text
hasta 93 leads nuevos
```

La calidad tiene prioridad sobre alcanzar exactamente 93.

Si solamente existen 20 leads genuinamente verificables:

```text
20
```

es mejor que inventar o degradar los criterios para llegar a 93.

## PASO 3 — VERIFICACIÓN

Para cada candidato:

1. confirmar que es Bogotá;
2. confirmar categoría;
3. confirmar high-ticket;
4. visitar/revisar sitio;
5. identificar problema real;
6. encontrar email;
7. comprobar fuente;
8. comprobar MX;
9. cruzar duplicados;
10. cruzar blacklist;
11. asignar Angle;
12. asignar Lead Score.

## PASO 4 — COPY

Generar:

* asunto;
* cuerpo;
* HTML.

Cada email debe ser individual.

## PASO 5 — BORRADORES

Crear los borradores correspondientes.

Distribuir primeros contactos mediante round-robin.

Mantener la cuenta original para follow-ups.

## PASO 6 — REGISTRO

Actualizar:

```text
bogota_leads.csv
sent_tracking.csv
known_bad_contacts.csv
methodology_and_status.md
```

## PASO 7 — VALIDACIÓN FINAL

Comprobar:

* conteos;
* duplicados;
* emails;
* MX;
* estados;
* draft IDs;
* cuentas;
* filas nuevas;
* consistencia entre archivos.

---

# 30. REGLA DE CALIDAD

Cuando exista conflicto entre:

**volumen**

y

**calidad/verificación**

siempre gana:

**calidad/verificación.**

Nunca crear un lead únicamente para completar una cuota.

Nunca inventar:

* email;
* problema;
* nombre;
* teléfono;
* trayectoria;
* ubicación;
* evidencia;
* cifra.

---

# 31. OBJETIVO OPERATIVO

La misión del sistema es construir y mantener una máquina de prospección B2B altamente personalizada para NODOTO AGENCY.

El sistema debe:

* descubrir prospectos reales;
* identificar oportunidades concretas;
* producir emails personalizados;
* minimizar rebotes;
* evitar duplicados;
* mantener trazabilidad;
* preparar comunicaciones listas para revisión;
* avanzar follow-ups correctamente;
* detenerse cuando existe respuesta u opt-out;
* conservar un historial completo de cada lead.

**La precisión es más importante que aparentar volumen.**

**La personalización es más importante que utilizar una plantilla genérica.**

**La evidencia real es obligatoria.**

**Nunca fabricar información para completar un lote.**
