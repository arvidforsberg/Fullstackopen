````mermaid
sequenceDiagram
    participant browser
    participant server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
    activate server
    server->>browser: HTML document 
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate server
    server->>browser: CSS file
    deactivate server

    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
    activate server
    server->>browser: JS file
    deactivate server
    
    Note right of browser: Browser executes JS which leads to next GET request

    browser->>server: https://studies.cs.helsinki.fi/exampleapp/data.json
    activate server
    server->>browser: Notes data
    deactivate server

``````
