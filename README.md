# Angie & Alejandro

Álbum de recuerdos de pareja: portada, contador de días juntos, frase del día, recuerdos con fotos y videos por año, playlist de canciones dedicadas y lugares.

- `index.html` es la página. No hace falta tocarla.
- `datos.json` tiene todo el contenido: fechas, recuerdos, canciones y frases.
- `fotos/` guarda las fotos y videos.

## Cómo editar `datos.json`

Ábrelo en GitHub y toca el lápiz (Edit). Cuando termines, dale a **Commit changes**.

### Fecha en que empezaron (para el contador)

```json
"inicio": "2024-05-18",
```

Formato año-mes-día.

### Agregar un recuerdo

Dentro de `"recuerdos": [ ... ]`:

```json
{
  "titulo": "Nuestra primera cita",
  "fecha": "2024-05-18",
  "lugar": "Lexington, Kentucky",
  "nota": "Lo que pasó ese día.",
  "fotos": ["fotos/2024-05-18-primera-cita/1.jpg", "fotos/2024-05-18-primera-cita/video.mp4"]
}
```

Si agregas varios recuerdos, sepáralos con una coma: `{ ... }, { ... }`.

### Agregar una canción

Dentro de `"canciones": [ ... ]`:

```json
{
  "cancion": "Nombre de la canción",
  "artista": "Artista",
  "de": "Alejandro",
  "fecha": "2024-06-01",
  "link": "https://open.spotify.com/track/...",
  "porque": "Por qué te la dediqué."
}
```

En `"de"` va quién la dedicó: `"Angie"`, `"Alejandro"` o `"Los dos"`.

### Frases propias

Se mezclan con las frases del día:

```json
"frases_propias": ["Una frase que solo nosotros entendemos."]
```

## Errores comunes

Si la página dice que no pudo leer `datos.json`, casi siempre falta una coma entre dos elementos o sobra una coma después del último.

## Ver la página en el computador

Abrir `index.html` con doble clic no carga los datos, porque el navegador bloquea la lectura de `datos.json`. Hay que abrirla con un servidor, por ejemplo desde la carpeta del repo:

```
python3 -m http.server
```

y luego entrar a http://localhost:8000.
