```mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server->>browser: HTTP Status Code 201 - Confirmation of new note
    deactivate server

    Note right of browser: Redrawing the page and inserting the note is handled client-side by browser

```
