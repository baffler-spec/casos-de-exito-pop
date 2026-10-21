# Casos de éxito · POP Media Technology

Landing pages de dos casos de éxito 2026 para [popmt.com](https://popmt.com), con el formato de los casos de éxito actuales del sitio (por ejemplo, [Aeropuerto MTY OMA](https://popmt.com/aeropuerto-mty-oma/)).

| Página | Ruta | Video |
|---|---|---|
| C5 Estado de México (ganador CALA Awards 2026) | `c5-estado-de-mexico/` | [Proyecto](https://youtu.be/s3Ot4irKkxU) · [Mensaje CALA Awards](https://youtu.be/HIdA1ALR9Yw) |
| Estadio Banorte | `estadio-banorte/` | [Caso técnico](https://youtu.be/h8XRDZT2cJU) |

## Estructura

```
index.html                      Índice para revisar ambas páginas
c5-estado-de-mexico/index.html
estadio-banorte/index.html
assets/css/styles.css           Estilos base y responsivos compartidos
assets/img/c5/                  Fotos optimizadas para web (JPG, 1400–2200 px)
assets/img/banorte/
```

HTML estático, sin dependencias ni build. Tipografía Montserrat (Google Fonts) y rosa de marca `#E0174E`. Los videos se cargan embebidos desde YouTube (`youtube-nocookie.com`), por lo que el repo no incluye archivos de video.

## Banner CALA Awards 2026 (home)

Componente independiente para el home de popmt.com, en `banner-cala-home/`. Va justo debajo del slider principal y lleva al caso de éxito del C5.

```
banner-cala-home/index.html     Vista previa: desktop + vista en celular (390 px)
banner-cala-home/banner.html    El banner solo, como página
banner-cala-home/snippet.html   El HTML para pegar en un widget HTML de Elementor
banner-cala-home/banner-cala.css  Estilos del banner (clases con prefijo .pmt-cala)
banner-cala-home/img/           Foto del premio y fondo del C5
```

Es un solo bloque responsivo: en desktop texto a la izquierda y foto a la derecha; en celular (≤760 px) la foto pasa arriba y los botones van a todo el ancho.

Para integrarlo: pega `banner-cala.css` en el CSS adicional del tema (o en un `<style>` del widget), pega `snippet.html` en un widget HTML debajo del slider y cambia las rutas `img/...` por las URLs de la biblioteca de medios. El botón principal apunta a `https://popmt.com/c5-estado-de-mexico/`; ajústalo si la landing queda en otra URL.

## Ver en local

Abre `index.html` en el navegador, o levanta un servidor:

```bash
python3 -m http.server 8000
# http://localhost:8000
```

## Al integrarlo en WordPress (Elementor)

- Header y footer de cada página son una réplica para revisión: en el sitio se usan los globales del tema.
- Sube las fotos de `assets/img/` a la biblioteca de medios y actualiza las rutas.
- Ajusta `canonical` y `og:image` a las URLs finales (hoy apuntan a `/c5-estado-de-mexico/` y `/estadio-banorte/` y a rutas relativas).

## Pendientes antes de publicar

- Nombre completo del Ing. Aguirre (pie de foto y texto del premio CALA).
- Confirmar el dato “la red SDVoE 10G de un solo sistema más grande del mundo” (Estadio Banorte).
- Confirmar que las pantallas de palcos son Samsung.
- Testimonio del cliente o de POP para el caso Banorte (opcional).

---
Desarrollado por [Baffler](https://baffler.mx).
