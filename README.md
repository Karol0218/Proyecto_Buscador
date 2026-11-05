# 🔎 Buscador de usuarios de GitHub

Aplicación web desarrollada con **HTML, CSS y JavaScript puro** que permite buscar usuarios de GitHub mediante su API pública.

Este proyecto es un ejercicio didáctico de **manejo de errores con `try / catch / finally` y consumo de APIs asíncronas mediante `fetch`**.

## 🚀 Características

- Búsqueda de usuarios de GitHub por nombre de usuario.
- Consulta de información mediante la API pública de GitHub.
- Visualización del avatar, nombre y cantidad de repositorios públicos.
- Enlace directo al perfil del usuario.
- Validación de entradas antes de realizar la petición.
- Manejo de errores HTTP (`404`, `403` y otros).
- Captura de errores de conexión.
- Uso de `try / catch / finally` para controlar el flujo de ejecución.
- Consola de eventos que muestra paso a paso el proceso de búsqueda.
- Diseño neo-brutalista con tonos morados.
- Diseño adaptable y consideraciones de accesibilidad.

## 🛠️ Tecnologías utilizadas

- **HTML5:** estructura de la aplicación.
- **CSS3:** estilos, diseño y animaciones.
- **JavaScript:** validaciones, eventos y lógica de búsqueda.
- **Fetch API:** comunicación con la API de GitHub.

No utiliza frameworks, librerías externas ni herramientas de compilación.

## 📂 Estructura del proyecto

```text
buscador-github/
├── buscador-github.html
└── README.md
```

## ▶️ Cómo ejecutar el proyecto

1. Descarga o clona este repositorio.
2. Abre la carpeta del proyecto.
3. Haz doble clic en `buscador-github.html`.
4. Escribe un nombre de usuario de GitHub, por ejemplo: `octocat`.
5. Pulsa **Buscar** o presiona Enter.

**Nota:** No necesitas un servidor local. Para consultar los usuarios sí necesitas conexión a internet.

## 🧪 Casos de prueba

| Entrada | Resultado esperado |
|---|---|
| `octocat` | Muestra la información del usuario. |
| `torvalds` | Muestra la información del usuario. |
| `usuario-que-no-existe-987654` | Error 404: usuario no encontrado. |
| `@octocat` | Error: no debe incluir `@`. |
| Campo vacío | Error: campo obligatorio. |
| `octo cat` | Error: no puede contener espacios. |
| `octo!cat` | Error: caracteres no permitidos. |
| `-octocat` | Error: formato inválido. |
| Sin conexión a internet | Error de conexión y botón habilitado nuevamente. |

También se contemplan errores de longitud, formatos inválidos y límites de peticiones de la API.

## ⚙️ Manejo de errores: try / catch / finally

El proyecto demuestra cómo controlar una operación asíncrona y garantizar que la interfaz recupere su estado independientemente del resultado.

**1. TRY**
- Valida el nombre de usuario.
- Ejecuta la petición mediante `fetch`.
- Procesa y muestra la información recibida.
- Registra el resultado de la búsqueda.

**2. CATCH**
- Captura errores de validación.
- Identifica errores de conexión.
- Maneja respuestas HTTP como `404` y `403`.
- Muestra mensajes claros al usuario.

**3. FINALLY**
- Oculta el indicador de carga.
- Habilita nuevamente el botón de búsqueda.
- Registra que el proceso ha finalizado.

## 🎨 Diseño y accesibilidad

La interfaz utiliza un estilo **neo-brutalista en tonos morados**, con bordes negros marcados, sombras sólidas y una combinación de colores lavanda y violeta.

También incorpora:
- Etiquetas accesibles para los campos.
- Mensajes de error con atributos ARIA.
- Texto alternativo para el avatar.
- Respeto por la preferencia `prefers-reduced-motion`.
- Uso de `textContent` para mostrar los datos de forma segura.

## 📡 API utilizada

[GitHub REST API – Users](https://api.github.com/users/)

La aplicación consulta los perfiles públicos de GitHub sin necesidad de autenticación.

**Importante:** La API pública tiene un límite de peticiones para usuarios no autenticados (60 solicitudes por hora por dirección IP).

## 🎯 Objetivo de aprendizaje

Practicar conceptos fundamentales de JavaScript moderno:

- Funciones asíncronas (`async / await`).
- Consumo de APIs con `fetch`.
- Validación de formularios.
- Manejo de excepciones con `throw` y `Error`.
- Control de errores con `try / catch / finally`.
- Manipulación del DOM.
- Gestión de eventos y estados de interfaz.

---

**Proyecto educativo | Front-end | HTML + CSS + JavaScript**
