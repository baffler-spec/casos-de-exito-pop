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
