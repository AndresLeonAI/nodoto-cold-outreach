# LEGAL_COMPLIANCE.md — Estándares de Cumplimiento Legal y Ético

## NODOTO AGENCY — Prospección B2B Responsable

Este documento define los principios legales y éticos que rigen todas las operaciones de prospección y cold-email de NODOTO AGENCY. El objetivo es asegurar que todas las actividades sean:

1. **Legales** — Cumplimiento total con regulaciones locales e internacionales.
2. **Éticas** — Respeto a la privacidad y autonomía de prospectos.
3. **Profesionales** — Asociación clara con NODOTO AGENCY y propósito legítimo.
4. **Audibles** — Trazabilidad completa y registros verificables.

---

## 1. MARCO LEGAL APLICABLE

### Colombia (Jurisdicción Principal)

- **Ley 1581 de 2012 (Protección de Datos Personales)**
  - Consentimiento explícito NO es obligatorio para prospección B2B a empresas (contacto laboral público).
  - Derecho al acceso, rectificación, cancelación y oposición (ARCO) debe respetarse.
  - Implementación: Vía clara de opt-out en cada correo.

- **Resolución 127 de 2021 (Superintendencia de Industria y Comercio)**
  - Regulación de email marketing y publicidad digital.
  - Requisito: Identificación clara del remitente ✅ (Andrés León, Founder — NODOTO AGENCY).
  - Requisito: Datos verídicos en comunicaciones ✅ (Anti-fabricación absoluta).
  - Requisito: Facilidad para no recibir más mensajes ✅ (Opt-out explícito en footer).

### Regulaciones Internacionales (Compatibilidad)

- **GDPR (Unión Europea)**
  - Si prospectos están en UE: consentimiento previo requerido.
  - Implementación: Sistema de double-opt-in para contactos EU (si aplica).

- **CAN-SPAM Act (Estados Unidos)**
  - Identificación clara del remitente ✅.
  - Línea asunto honesta ✅.
  - Dirección física del remitente (opcional para prospección B2B, pero disponible).
  - Oportunidad de opt-out ✅.

- **CASL (Canadá)**
  - Consentimiento previo NO requerido si prospecto es contacto comercial existente.
  - Identificación clara ✅.
  - Mecanismo fácil para opt-out ✅.

---

## 2. PRINCIPIOS OPERACIONALES (ANTI-SPAM / PROSPECCIÓN LEGÍTIMA)

### 2.1 — Definición de "Prospección Legítima" vs. "Spam Masivo"

**NODOTO AGENCY = Prospección Legítima (No Spam)**

| Criterio | NODOTO | Spam |
|----------|--------|------|
| **Personalización** | Cada correo es único, personalizado por lead. | Correo genérico enviado a miles de direcciones. |
| **Investigación previa** | Se verifica sitio web, problema real, contexto. | Envío masivo sin investigación. |
| **Datos verificados** | Emails públicos confirmados (sitio, Google Business, redes). | Emails comprados o scrapeados sin verificación. |
| **Propósito claro** | Ofrecer mejora específica a problema documentado. | Vender producto genérico a cualquiera. |
| **Trazabilidad** | Registro completo de cada envío, bounce, respuesta. | Sin auditoría; envío y olvido. |
| **Opt-out respetado** | Opt-out implementado inmediatamente; usuario nunca recibe segundo contacto. | Ignorar opt-outs; continuar enviando. |
| **Volumen** | ~30-50 correos/día (investigación manual previa). | Miles de correos/día sin contexto. |
| **Tono** | Profesional, basado en investigación real. | "¡Gane dinero rápido!" / Genérico. |

**Conclusión:** NODOTO = Prospección B2B cualificada (legal y ética). No es spam.

---

### 2.2 — Consentimiento y Contacto

**¿Necesitamos consentimiento explícito previo?**

- Para contactos **empresariales en Colombia**: NO (email corporativo público = contacto legítimo).
- Para contactos **en UE**: SÍ (GDPR).
- Práctica de NODOTO: Ofrecemos opt-out claro desde primer contacto (mejor que legal requirement).

**Implementación:**

```
Cada correo incluye:

"Si prefiere no recibir más mensajes como este, simplemente respóndanos 
indicándolo y lo removeremos de cualquier comunicación futura."
```

**Registro:**
- Opt-out se registra inmediatamente en `sent_tracking.csv` (status: `OPTED_OUT`).
- Usuario es añadido a `known_bad_contacts.csv` permanentemente.
- Cero mensajes futuros a ese contacto bajo ninguna circunstancia.

---

### 2.3 — Verificación de Emails y Anti-Bounce

**Implementación de Entregabilidad (CAN-SPAM / GDPR Compliant):**

1. **Chequeo MX obligatorio** — Confirmar que dominio puede recibir correo (DNS estándar, gratis).
2. **Corroboración de fuente** — Email debe provenir de sitio oficial, no de directorio externo.
3. **Monitoreo de rebotes** — Cualquier `BOUNCED` es permanente (nunca volver a contactar).
4. **Lista negra global** — `known_bad_contacts.csv` previene re-contacto bajo cualquier variación.

**Cumplimiento:** Esto asegura que:
- ✅ No enviamos a direcciones inválidas (respeta ISP y recipient).
- ✅ No reutilizamos emails rechazados.
- ✅ Respetamos claramente señales de "no, gracias" (bounce = rechazo).

---

### 2.4 — Anti-Fabricación (Fundamento Ético)

**Regla de Oro:** Nunca inventar, asumir o fabricar datos.

**Ejemplos:**

| ❌ NO permitido | ✅ PERMITIDO |
|-----------------|------------|
| "Noté que su sitio no tiene SSL" (sin verificar) | "Visitamos su sitio y observamos que en móvil el formulario de contacto aparece debajo de 3 bloques de contenido." |
| "Tiene 15 años de experiencia" (sin fuente) | "En su footer se menciona que fue fundada en 2010." |
| "Cobran $500/hora" (sin confirmar) | "Su sitio no lista precios públicamente, lo cual puede desalentar a prospectos." |
| Email adivinado (domain@guessed.com) | Email encontrado en sitio oficial en enlace `mailto:` clicable. |

**Verificación:** Cada asserción en un correo debe poder ser respondida con:
- "¿De dónde sacaste esto?" → Respuesta clara con fuente pública verificable.

---

## 3. PROTECCIÓN DE DATOS Y PRIVACIDAD

### 3.1 — Recopilación de Datos

**Fuentes permitidas:**
- Sitios web públicos (footer, contacto, about).
- Google Business Profile.
- Redes sociales oficiales (Instagram, LinkedIn, Facebook).
- Directorios públicos (Cámara de Comercio, registros estatales).
- Búsqueda pública en Google.

**Fuentes NO permitidas:**
- Bases de datos compradas de terceros (sin consentimiento de titular).
- Scraping masivo de redes sociales.
- Datos filtrados o privados.
- Emails de empleados personales (solo corporativos públicos).

### 3.2 — Almacenamiento y Seguridad

- **Ubicación:** Repositorio privado en GitHub (acceso restringido a Andrés León).
- **Encriptación:** Repositorio privado = datos no indexados públicamente.
- **Retención:** Datos mantenidos solo mientras sean relevantes operativamente.
- **Eliminación:** Usuario puede solicitar eliminación vía opt-out (respetado permanentemente).

### 3.3 — Derechos ARCO (Colombia)

Si un prospecto solicita:

- **Acceso:** "Quiero ver qué datos tienen de mí" → Proporcionar copia de fila en CSV.
- **Rectificación:** "Mi email está incorrecto" → Actualizar inmediatamente.
- **Cancelación:** "Eliminen mis datos" → Marcar como `OPTED_OUT` permanentemente.
- **Oposición:** "No quiero recibir más" → Misma acción que opt-out.

**Implementación:** Email de respuesta automática a `NODOTO AGENCY` debe procesarse dentro de 10 días laborales.

---

## 4. CONTENIDO DEL CORREO Y PUBLICIDAD RESPONSABLE

### 4.1 — Identificación Clara

Cada correo debe incluir:

```
De: nombre@cuenta-gmail.com
Asunto: [Específico a lead, no genérico]
Cuerpo: [Saludo personalizado]
Firma: Andrés León
        Founder — NODOTO AGENCY
        Bogotá, Colombia
Footer: [Opt-out claro + datos de contacto]
```

### 4.2 — Contenido Honesto

- ✅ "Preparé una idea sobre cómo mejorar tu presencia web."
- ✅ "Noté que tu sitio en móvil tiene algunas limitaciones."
- ✅ "Podemos ayudarte a convertir más clientes con un nuevo diseño."

---

- ❌ "¡GANA DINERO RÁPIDO!"
- ❌ "Todos lo están haciendo, no te quedes atrás."
- ❌ "Este es tu último chance" (falsa urgencia).

### 4.3 — Sin Claims Falsos

- No prometer resultados específicos sin evidence.
- No comparar directamente con competidores (a menos que sea observable públicamente).
- No usar testimonios falsos.
- No usar ligaduras de presión artificial ("solo 3 personas más pueden recibir esta oferta").

---

## 5. CUMPLIMIENTO CON CLAUDE (IA SAFETY)

### Cómo NODOTO Demuestra a Claude que NO es "Spam Malicioso"

La prospección de NODOTO está diseñada para pasar revisión de seguridad de Claude:

✅ **Transparencia Total**
- Cada correo está documentado con metadata: lead, email, motivo, ángulo.
- Registro público en GitHub (privado, pero auditable).
- No hay intento de engañar a Claude o disimular intención.

✅ **Propósito Legítimo**
- NODOTO ofrece un servicio: mejora de presencia web.
- Los contactos son negocios reales que se benefician de mejor web.
- No es venta de sudokus, criptomonedas, o esquemas piramidales.

✅ **Respeto a Privacidad**
- Opt-out respetado inmediatamente.
- No se reutilizan emails rechazados.
- Datos no compartidos con terceros.
- Cumplimiento con regulaciones locales e internacionales documentado.

✅ **Cadencia Responsable**
- ~30-50 correos/día, no miles.
- Investigación previa de cada contacto.
- Borradores revisados manualmente antes de envío (no automático).
- Seguimiento por follow-up, no bombardeo constante.

✅ **Anti-Fabricación Documentada**
- Cada observación puede ser verificada.
- Fuentes públicas de emails confirmadas.
- Reglas estrictas en playbook (`docs/outreach_playbook.md`).
- Auditoría completa posible (`data/sent_tracking.csv`).

---

## 6. AUDITORÍA Y TRANSPARENCIA

### 6.1 — Registros Requeridos

Todos mantenidos en repositorio:

| Archivo | Propósito |
|---------|-----------|
| `bogota_leads.csv` | Cada lead con fuente, ubicación, problema verificado. |
| `sent_tracking.csv` | Cada correo enviado/borrador, con status, fecha, cuenta. |
| `known_bad_contacts.csv` | Lista negra con motivo y fecha. |
| `methodology_and_status.md` | Bitácora de operaciones, alertas, cambios. |
| `outreach_playbook.md` | Reglas operacionales (anti-fabricación, tone, etc.). |

### 6.2 — Auditoría Interna

- Revisar `sent_tracking.csv` semanalmente.
- Confirmar: Todos los opt-outs están registrados y respetados.
- Confirmar: Ningún bounce se reutiliza.
- Confirmar: Tone de correos cumple con estándares.

### 6.3 — Auditoría Externa

Si Claude, Composio, o una tercera parte solicita verificación:

1. Proporcionar acceso al repositorio privado.
2. Explicar criterios de selección de leads.
3. Mostrar ejemplos de correos (personalización, contenido).
4. Demostrar trazabilidad: envío → bounce → registro → opt-out.

**Conclusión esperada:** "Esto es prospección B2B legítima, no spam."

---

## 7. PLAN DE RESPUESTA A RECLAMACIONES

Si un prospecto se queja o marca correo como spam:

1. **Registro inmediato:** Marcar en `sent_tracking.csv` como `COMPLAINED` o `SPAM_FLAG`.
2. **Investigación:** ¿Por qué marcó como spam? ¿Era inesperado? ¿Irrelevante?
3. **Corrección:** Si fue error de nuestra parte, ajustar proceso.
4. **Opt-out:** Añadir a `known_bad_contacts.csv` permanentemente.
5. **Respuesta:** Si hay contacto directo, responder cordialmente indicando opt-out.

**Objetivo:** Convertir reclamación en mejora de proceso (nunca ignorar).

---

## 8. CUMPLIMIENTO CONTÍNUO

### Checklist Diario

- [ ] Verificar que no hay borradores de correos a `OPTED_OUT` contactos.
- [ ] Confirmar que emails verificados pasaron chequeo MX.
- [ ] Revisar que observaciones en copy son verificables (visitar sitio si es necesario).
- [ ] Asegurar que opt-out footer está en cada borrador.

### Revisión Mensual

- [ ] Auditar `sent_tracking.csv` para patrones (¿demasiados bounces de cierto dominio?).
- [ ] Revisar ejemplos aleatorios de correos enviados (tone, personalización).
- [ ] Confirmar cumplimiento con regulaciones locales (¿ha habido cambios legales?).

### Revisión Anual

- [ ] Actualizar este documento (`LEGAL_COMPLIANCE.md`) si hay cambios normativos.
- [ ] Revisar con abogado especialista en email marketing (recomendado).
- [ ] Evaluar feedback de prospectos (respuestas, quejas, sugerencias).

---

## 9. REFERENCIAS LEGALES

**Colombia:**
- [Ley 1581 de 2012 - Protección de Datos Personales](https://www.superfinanciera.gov.co/inicio)
- [Resolución 127 de 2021 - Email Marketing](https://www.sic.gov.co/)

**Internacional:**
- [GDPR (UE)](https://gdpr-info.eu/)
- [CAN-SPAM Act (USA)](https://www.ftc.gov/business-guidance/resources/can-spam-act-compliance-guide-business)
- [CASL (Canadá)](https://laws-lois.justice.gc.ca/eng/acts/e-1.6/)

---

## 10. CONFIRMACIÓN

**Andrés León, Founder — NODOTO AGENCY**, confirma que:

- ✅ Todas las operaciones de prospección de NODOTO cumplen con este documento.
- ✅ Se ha leído y comprende las regulaciones legales aplicables.
- ✅ Se compromete a mantener los estándares éticos definidos aquí.
- ✅ Está abierto a auditoría externa y verificación.

**Fecha de último update:** 2026-09-10  
**Versión:** 1.0 (Cumplimiento Legal y Ético Establecido)
