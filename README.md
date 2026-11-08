# RHR Arquitectura e Interiores · web de proyectos

Sitio: **https://rhr-interiores.github.io/**

| Parte | Dirección |
|---|---|
| Portada | `https://rhr-interiores.github.io/` |
| Visor de la Cocina 3.0 | `https://rhr-interiores.github.io/cocina-3-0/` |

## Qué hay en esta carpeta

| Archivo o carpeta | Para qué sirve |
|---|---|
| `index.html` | La portada: proyectos, cifras, antes y después, cómo trabajamos y contacto. |
| `config.js` | **Tus datos:** GoatCounter, Formspree y WhatsApp. Los usan la portada y todos los visores. |
| `img/`, `og.jpg` | Imágenes de la portada. `og.jpg` es la vista previa que aparece al compartir el link. |
| `cocina-3-0/` | El visor 3D de la Cocina 3.0, con su modelo, texturas e imagen para compartir. |

---

## 1 · Publicar (una sola vez)

1. Entrá a [github.com](https://github.com) con tu cuenta. Si no tenés, creá una; es gratis.
2. Arriba a la derecha tocá tu foto y elegí **Your organizations → New organization → Free**.
   - **Organization name:** `rhr-interiores`
   - Si el nombre está tomado, elegí otro y avisame, porque cambia el link.
3. Dentro de la organización tocá **New repository** y completá:
   - **Repository name:** `rhr-interiores.github.io`. Tiene que ser exactamente el nombre de la organización + `.github.io`.
   - Marcá **Public**.
   - Tocá **Create repository**.
4. Hacé clic en **uploading an existing file**.
5. Arrastrá **todo el contenido** de esta carpeta: los archivos sueltos y las carpetas `img` y `cocina-3-0` completas. Tocá **Commit changes** y esperá a que termine de subir.
6. Andá a **Settings → Pages** y fijate que diga:
   - **Deploy from a branch**
   - Branch `main` · `/ (root)`

   Si no está así, elegilo y tocá **Save**.
7. En 1 o 2 minutos el sitio queda publicado en `https://rhr-interiores.github.io/`.

## 2 · Estadísticas de visitas (GoatCounter, gratis)

1. Entrá a [goatcounter.com](https://www.goatcounter.com), tocá **Sign up** y elegí el código `rhr-interiores`.
2. En GitHub abrí `config.js`, tocá el lápiz y completá:
   ```js
   goatcounter: "rhr-interiores",
   ```
   Después tocá **Commit changes**.
3. Para que no se cuenten tus propias visitas, andá en GoatCounter a **Settings → Ignore IPs** y agregá tu IP actual.

**Cómo leer el panel**

- **Páginas:**
  - `/` es la portada.
  - `/cocina-3-0/` es el visor.
  - Vas a ver visitas por día, país, si entraron de celular o compu, y de dónde vinieron.
- **Eventos** (cada uno cuenta 1 vez por visita):

| Evento | Significa |
|---|---|
| `origen-instagram` · `origen-linkedin` | Entró con un link etiquetado (ver abajo). |
| `portada-abrir-cocina-3-0…` | Desde la portada, entró al visor. |
| `portada-antes-despues` | Usó el comparador de antes y después. |
| `portada-whatsapp` · `portada-telefono` · `portada-instagram` | Tocó esos contactos en la portada. |
| `portada-formulario-empezado` · `portada-formulario-enviado` | Empezó a completar el formulario o lo envió. |
| `modelo-cargado` | El 3D terminó de cargar. |
| `tiempo-30-s` · `tiempo-2-min` · `tiempo-5-min` | Tiempo mirando el visor. |
| `abrir-horno`, `abrir-todo`, `ver-antes`, `modo-noche`, `vista-…` | Qué hizo dentro del visor. |
| `contacto-whatsapp` · `formulario-enviado` | Contactos desde el visor. |
| `cliente-…` | Abrió un link personal (ver abajo). |

**Links para compartir**

| Dónde | Link |
|---|---|
| Bio de Instagram | `https://rhr-interiores.github.io/?ref=instagram` |
| LinkedIn | `https://rhr-interiores.github.io/?ref=linkedin` |
| Un cliente puntual (directo al visor) | `https://rhr-interiores.github.io/cocina-3-0/?c=nombre` |

> Las estadísticas son **anónimas**: no usan cookies ni guardan datos personales. Dicen *cuántos* y *qué hicieron*, no *quiénes*. Los nombres te llegan solo por WhatsApp o por el formulario. Algunos bloqueadores de anuncios frenan el contador, así que tomá los números como un mínimo.

## 3 · Pedidos de presupuesto por email (Formspree, gratis)

Sin este paso, los formularios funcionan igual: arman el mensaje y lo abren en WhatsApp.

1. Entrá a [formspree.io](https://formspree.io), creá una cuenta y confirmá tu email.
2. Tocá **+ New form** y ponele de nombre "Web RHR".
3. Copiá el ID del formulario. Es lo que va después de `/f/`.
4. Ponelo en `config.js`:
   ```js
   formspree: "xabcdwxy",
   ```
5. Hacé un envío de prueba desde la portada.

Cada pedido llega con nombre, teléfono, email, mensaje y si vino de la portada o del visor. El plan gratis tiene un límite de envíos por mes; mirá formspree.io/plans.

## 4 · Sumar un proyecto nuevo

Cada proyecto es una carpeta nueva, por ejemplo `cocina-xyz/`, con su visor y una tarjeta más en la portada. Para subirlo:

1. Subí la carpeta nueva y el `index.html` de la portada con **Add file → Upload files**.
2. **No vuelvas a subir `config.js`**, así no perdés tus códigos.

---

*El repositorio es público: cualquiera que entre al link puede ver los modelos y las fotos del "Antes".*
