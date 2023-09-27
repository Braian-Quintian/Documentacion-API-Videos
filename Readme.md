# API VIDEOS

## Cursos Disponibles

- react
- docker
- git
- nodejs
- sql
- javascript

## Endpoints

> Recuerda que solo puedes acceder desde la red interna de Campus

#### 1 .Obtener un curso en especifico (Metodo Objeto)

> Para visualizar todas las secciones que tiene un curso en especifico:

**DETALLES DEL API**

- **Metodo por el cual se solicita**: `GET`

- **Parametros que necesita el endpoint**:

  - `nombreDelCurso` (obligatorio) - `nombreDelCurso` es el nombre del curso que se desea obtener.

- **Esta es la URL a la que deben acceder**:

  ```js
  http://192.168.128.23:5010/cursos?course=nombreDelCurso
  ```

**Observacion**: **Debes reemplazar el parametro `nombreDelCurso` por el nombre del curso que deseas obtener.**

**Ejemplo JSON que recibes**

```json
{
  "1": {
    "sectionName": "Sección 1: Introducción",
    "videos": [
      {
        "1": {
          "Titulo": "Introducción al curso",
          "video": "react-1-01-Introducción",
          "links": {}
        }
      },
      {
        "2": {
          "Titulo": "¿Cómo funcionará el curso?",
          "video": "react-1-02-Como_funcionara_el_curso",
          "links": {}
        }
      },
      {
        "3": {
          "Titulo": "¿Cómo hacer preguntas?",
          "video": "react-1-03-Como-hacer-preguntas",
          "links": {}
        }
      },
      {
        "4": {
          "Titulo": "Instalaciones necesarias y recomendadas",
          "video": "react-1-04-Instalaciones_necesarias_y_recomendadas",
          "links": [
            {
              "titulo-link": "Instalaciones necesarias",
              "link": "https://gist.github.com/Klerith/4a4abfd88a88b2d1f16efd95fea41362"
            }
          ]
        }
      }
    ]
  }
}
```

**Captura de pantalla**

![Metodo Objeto](./assets//img/GET-seccion-Metodo-Objeto.png)





#### 1.1.Obtener un curso en especifico (Metodo Array)

> Para visualizar todas las secciones que tiene un curso en especifico:

**DETALLES DEL API**

- **Metodo por el cual se solicita**: `GET`

- **Parametros que necesita el endpoint**:

  - `nombreDelCurso` (obligatorio) - `nombreDelCurso` es el nombre del curso que se desea obtener.

- **Esta es la URL a la que deben acceder**:

  ```js
  http://192.168.128.23:5010/cursos/v2?course==nombreDelCurso
  ```

**Observacion**: **Debes reemplazar el parametro `nombreDelCurso` por el nombre del curso que deseas obtener.**

**Ejemplo JSON que recibes**

```json
[
  {
    "sectionName": "Sección 1: Introducción",
    "videos": [
      {
        "Titulo": "Introducción al curso",
        "video": "react-1-01-Introducción",
        "Texto": ""
      },
      {
        "Titulo": "¿Cómo funcionará el curso?",
        "video": "react-1-02-Como_funcionara_el_curso",
        "Texto": ""
      },
      {
        "Titulo": "¿Cómo hacer preguntas?",
        "video": "react-1-03-Como-hacer-preguntas",
        "Texto": ""
      },
      {
        "Titulo": "Instalaciones necesarias y recomendadas",
        "video": "react-1-04-Instalaciones_necesarias_y_recomendadas",
        "Texto": "",
        "links": [
          {
            "titulo-link": "Instalaciones necesarias",
            "link": "https://gist.github.com/Klerith/4a4abfd88a88b2d1f16efd95fea41362"
          }
        ]
      }
    ]
  }
]
```

**Captura de pantalla**

![Metodo Objeto](./assets//img/GET-seccion-Metodo-Array-Object.png)

---

### 2. Obtener una sección en especifico (Metodo Objeto)

> Para visualizar todos los videos que tiene una sección en especifico:

**DETALLES DEL API**

- **Metodo**: `GET`
- **Parametros que necesita el endpoint**:

  - `nombreDelCurso` (obligatorio) - Nombre del curso que se desea obtener.
  - `numeroDeLaSeccion` (obligatorio) - Número de la sección que se desea obtener.

- **Esta es la URL a la que deben acceder**:
  ```js
  http://192.168.128.23:5010/cursos/filter?course=nombreDelCurso&section=numeroDeLaSeccion
  ```

**Observacion:** **Recuerda que debes reemplazar los parametros `nombreDelCurso` y `numeroDeLaSeccion` por los valores que deseas obtener.**

### Reproducir un video

> Para visualizar un video:

**DETALLES DEL API**

- **Metodo**: `GET`
- **Parametros que necesita el endpoint**:

  - `nombreDelCurso` (obligatorio) - Nombre del curso que se desea obtener.
  - `numeroDeSeccion` (obligatorio) - Número de la sección que se desea obtener.
  - `nombreDelVideo` (obligatorio) - Nombre del video que se desea obtener.

- **Esta es la URL a la que deben acceder**:

```js
http://192.168.128.23:5010/cursos/play?course=nombreDelCurso&seccion=numeroDeSeccion&video=nombreDelVideo
```

**Observacion:** **Recuerda que debes reemplazar los parametros `nombreDelCurso`, `numeroDeSeccion` y `nombreDelVideo` por los valores que deseas obtener.**

## Extension que utilizo para visualizar el JSON:

[JSON-VIEWER](https://chrome.google.com/webstore/detail/json-formatter/bcjindcccaagfpapjjmafapmmgkkhgoa?utm_source=ext_sidebar&hl=en-US)