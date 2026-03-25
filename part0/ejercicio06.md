# Ejercicio 0.6: New note in Single page app diagram

```mermaid
sequenceDiagram
    participant browser
    participant server

    Note right of browser: El usuario escribe y pulsa "Save"
    Note right of browser: El JS captura el evento e.preventDefault() y añade la nota localmente

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    Note right of browser: Envío de JSON: { "content": "...", "date": "..." }
    server-->>browser: 201 Created (Éxito)
    deactivate server

    Note right of browser: La página no se recarga, la nota ya está visible
```
