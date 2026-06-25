# COMANDA. — Vocero Digital

Sello curatorial gastronómico · Buenos Aires · 2026

---

## Estructura del repositorio
├── README.md
├── assets/
│   ├── personaje_comanda.png         ← Imagen del vocero (Leonardo.ai)
│   ├── ElevenLabs_voice.mp3          ← Voz clonada (ElevenLabs)
│   └── la_mesa.mp3                   ← Jingle de marca (Suno v4)
└── output/
    └── COMANDA_vocero_v1.mp4         ← Video final (HeyGen, 1080p)

---

## Qué es este proyecto

COMANDA. es un sello curatorial gastronómico que opera como pop-up itinerante en Buenos Aires. No es un restaurante. Es una editorial que usa la mesa. Cada edición es un capítulo cerrado: cocina, vino y música elegidos con el mismo criterio.

Este repositorio documenta la creación del vocero digital de la marca: un personaje visual consistente con la identidad del sello, sincronizado con voz generada en ElevenLabs y ensamblado en HeyGen.

---

## 1. Guión

**Técnica utilizada:** Chain-of-Thought — se explicita la cadena de razonamiento antes de llegar al texto final. Cada decisión narrativa tiene una causa de marca.

### Proceso de construcción

| Paso | Pregunta | Decisión |
| 1 | ¿Qué es Comanda en una sola verdad? | Un sello editorial que usa la gastronomía como lenguaje. La voz anuncia, no invita. |
| 2 | ¿A quién le habla? | A alguien que ya tiene criterio. Sin definiciones ni explicaciones. |
| 3 | ¿Qué emoción busca dejar? | Anticipación contenida. El silencio antes de abrir algo que sabés que va a ser bueno. |
| 4 | ¿Qué palabras están prohibidas? | "Experiencia", "propuesta", "únete", "reservá tu lugar". |
| 5 | ¿Cuál es la estructura? | Gancho → Tensión → Propuesta → Prueba → Cierre. Sin CTA. |

### Guión final (45–55 segundos)
— GANCHO —
Hay mesas que no aparecen en ninguna app.
Ni en Google. Ni en Instagram.

— TENSIÓN —
Hoy comer bien no alcanza.
Lo que falta es criterio.
Saber por qué está ese vino en esa copa.
Por qué suena eso. Por qué importa lo que se sirve.

— PROPUESTA —
Comanda es un sello curatorial gastronómico.
Una sola noche. Una sola edición.
Cocina, vino y música elegidos con el mismo criterio.
No es un restaurante. No es un evento.
Es una mesa con punto de vista.

— PRUEBA —
La primera edición reunió cincuenta personas
en una vinoteca de Buenos Aires.
Argentina y España en la misma mesa.
La segunda edición está por llegar.

— CIERRE —
COMANDA.


### Notas de dirección de voz
- **Tono general:** Enunciativo. No seductor. No dramático. Como alguien que dice algo que sabe verdadero.
- **"Lo que falta es criterio."** → La frase más importante. Pausa antes y después. No subir el tono, bajar la velocidad.
- **"No es un restaurante. No es un evento."** → Ritmo binario, cortante. Cada "no" es un golpe suave.
- **"COMANDA."** → Registro más grave, no más fuerte. El punto se escucha en cómo se cierra la boca. Silencio de 2 segundos después.

---

## 2. Voz — ElevenLabs

### Prompt utilizado para la generación

El guión fue pegado íntegramente en **Text to Speech** de ElevenLabs con los siguientes parámetros:

| Parámetro | Valor | Justificación |
| Idioma | Español | Entonación rioplatense, no acento neutro |
| Estilo | Narración / Documentary | Peso editorial, no calidez marketinera |
| Stability | 0.80 | Consistencia sin rigidez robótica |
| Similarity Boost | 0.65 | Naturalidad sobre fidelidad perfecta |
| Style Exaggeration | 0.15 | Mínimo estilismo, máxima autenticidad |
| Speed | 0.85 | Ritmo pausado acorde al guión |
| Formato | MP3 | Compatible con HeyGen, entrega académica |

**Archivo generado:** `ElevenLabs_voice.mp3` · 48 segundos · Mono · 44.1kHz

---

## 3. Personaje visual

### Prompt utilizado en Leonardo.ai
**Modelo:** Leonardo Kino XL / PhotoReal v2  
**Image Reference:** `pose_2.jpg` con strength 0.30  
**Guidance Scale:** 7–8

**Prompt:**
Portrait of a man, late 30s, messy curtain fringe hair, loose strands 
falling over forehead, slightly overgrown, undone. Visible tattoos on 
neck and hands. Dark eyes, strong jaw, few days stubble. 
Calm and unbothered expression, not looking at camera. 
Worn dark linen shirt, open collar. 
Dramatic chiaroscuro lighting, single warm light source from the left. 
Deep dark background, dark petrol green shadow tones. 
Holding a wine glass loosely. Cinematic, editorial, indie, raw. 
Film grain. Buenos Aires underground aesthetic.

**Negative prompt:**
suit, tie, clean cut, lawyer, corporate, preppy, smile, bright background, 
studio lighting, stock photo, generic, HDR, oversaturated, plastic skin, 
symmetrical hair, gel hair, neat haircut

### Decisiones de diseño del personaje

- **Flequillo con caído y tatuajes:** el vocero representa la cultura underground de Buenos Aires, no el lujo aspiracional. Turro con criterio.
- **Expresión sin contacto visual con cámara:** coherente con la postura de marca — Comanda no busca aprobación.
- **Tonos verde petróleo en el fondo:** conecta directamente con la paleta del Manual de Identidad Visual (#024539).
- **Camisa de lino gastada:** textura presente, no perfección. Igual que la identidad visual.

---

## 4. Proceso de sincronización en HeyGen

### Paso a paso

**Paso 1 — Subir el personaje**
HeyGen → Photo Avatar → Upload Photo → subir `personaje_comanda.png`.
Activar **Talking Photo** para habilitar sincronización labial.

**Paso 2 — Configurar el audio**
En la línea de tiempo: **Upload Audio** → subir `ElevenLabs_voice.mp3`.
No usar voces nativas de HeyGen — la voz clonada es activo de marca.

**Paso 3 — Fondo del video**
Color sólido **#024539** (verde petróleo de la paleta de marca).

**Decisión de diseño:** se eligió fondo liso en lugar de imagen o textura para que el personaje ocupe el centro sin competencia visual. El color ancla la pieza al manual de identidad sin necesitar elementos adicionales.

**Paso 4 — Música de fondo**
Agregar `la_mesa.mp3` como pista secundaria en la línea de tiempo.
Volumen: **15–20%** respecto a la voz.

**Decisión de diseño:** el volumen de la música se mantuvo en el rango 15–20% para que funcione como contexto sonoro sin competir con el guión. Por encima del 20% la letra del jingle interfiere con la comprensión de la voz. Por debajo del 15% se pierde la identidad sonora de la marca en el video.

**Paso 5 — Exportación**
Resolución: **1080p (1920×1080)** · Formato: **MP4**
Archivo final: `COMANDA_vocero_v1.mp4` → carpeta `/output/`

---

## 5. Alineación con la identidad visual de marca

| Elemento visual | Decisión en el video |
| Paleta: verde petróleo (#024539) | Fondo sólido del video |
| Fotografía sin overlay ni filtro | Personaje sin efectos en post, imagen directa |
| Textura, no perfección | Personaje con lino gastado, tatuajes, pelo sin gel |
| "COMANDA." con punto. Contundente. | Cierre del guión con silencio de 2 segundos |
| Edición, curación | Guión de 5 bloques, sin palabras de relleno |

---

## 6. Reflexión sobre los resultados

El principal desafío del proceso fue mantener la coherencia entre tres sistemas que se producen de forma independiente: la voz (ElevenLabs), el personaje (Leonardo.ai) y el ensamble (HeyGen). Cada herramienta tiene su propia lógica estética y el riesgo es que el resultado final parezca un collage en lugar de una pieza de marca.

La solución fue trabajar desde los adjetivos de identidad sonora y visual como hilo conductor: **editorial, fermentado, táctil**. Cada decisión — el tono de voz, el flequillo del personaje, el fondo liso, el volumen de la música — se evaluó contra esos tres adjetivos antes de confirmarla.

El resultado es una pieza donde la voz no intenta convencer sino anunciar, el personaje no mira a cámara porque Comanda no busca validación, y la música existe como fondo de criterio y no como decoración.

---

## Herramientas utilizadas

| Herramienta | Rol |
| Claude (Anthropic) | Estrategia de marca, guión, Chain-of-Thought |
| Leonardo.ai | Generación del personaje visual |
| ElevenLabs | Síntesis de voz clonada en español |
| Suno v4 | Jingle de marca (`la_mesa.mp3`) |
| HeyGen | Ensamble final: avatar + voz + música |

---

## Licencia

Todo el contenido de este repositorio es propiedad de **COMANDA.** y sus fundadoras.

Los archivos generados mediante herramientas de IA (Leonardo.ai, ElevenLabs, Suno, HeyGen) son activos de marca privados. Prohibida su distribución o uso en producciones de terceros sin autorización escrita.

---

COMANDA. no ambienta. Edita.
