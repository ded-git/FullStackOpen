# FullStackOpen

## 0.4: New note diagram
```mermaid

sequenceDiagram
    

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    activate Server
    Server->>Browser: HTML file
    deactivate Server

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate Server
    Server->>Browser: CSS file
    deactivate Server
    
    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    activate Server
    Server->>Browser: JS file
    deactivate Server

    Note right of Browser: The browser starts executing the JavaScript code that fetches the JSON from the Server

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate Server
    Server->>Browser: [{content: "Hello world", date: "2023-03-27T14:59:15.818Z"},…]
    deactivate Server

    Note right of Browser: The browser executes the callback function that renders the notes

    Browser-->>Server: GET https://studies.cs.helsinki.fi/favicon.ico
    activate Server
    Server->>Browser: ico file
    deactivate Server

    Browser-->>Server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    activate Server
    Note right of Browser: The Server add form data {content: "greeting from Ukraine",date: "2023-03-27T20:06:28.485Z"}
    Server->>Browser: response with code 302 (redirection)
    deactivate Server

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    activate Server
    Server->>Browser: HTML file
    deactivate Server

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate Server
    Server->>Browser: CSS file
    deactivate Server
    
    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    activate Server
    Server->>Browser: JS file
    deactivate Server

    Note right of Browser: The browser starts executing the JavaScript code that fetches the JSON from the Server

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate Server
    Server->>Browser: [{content: "Hello world", date: "2023-03-27T14:59:15.818Z"},…]
    deactivate Server

    Note right of Browser: The browser executes the callback function that renders the notes

    Browser-->>Server: GET https://studies.cs.helsinki.fi/favicon.ico
    activate Server
    Server->>Browser: ico file
    deactivate Server
``` 
## 0.5: Single page app diagram
```mermaid

sequenceDiagram
    participant Browser
    participant Server

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/spa
    activate Server
    Server->>Browser: HTML file
    deactivate Server

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate Server
    Server->>Browser: CSS file
    deactivate Server
    
    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
    activate Server
    Server->>Browser: JS file
    deactivate Server

    Note right of Browser: The browser starts executing the JavaScript code that fetches the JSON from the Server

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate Server
    Server->>Browser: [{content: "Hello world", date: "2023-03-27T14:59:15.818Z"},…]
    deactivate Server

    Note right of Browser: The browser executes the callback function that renders the notes

    Browser-->>Server: GET https://studies.cs.helsinki.fi/favicon.ico
    activate Server
    Server->>Browser: ico file
    deactivate Server
```

## 0.6: New note in Single page app diagram
```mermaid

sequenceDiagram
    participant Browser
    participant Server

    Browser-->>Server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate Server
    deactivate Server

```