# FullStackOpen

## 0.4: New note diagram
```mermaid

sequenceDiagram
    participant Browser
    participant Server

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    Server activate
    Server->>Browser: HTML file
    Server deactivate

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    Server activate
    Server->>Browser: CSS file
    Server deactivate
    
    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    Server activate
    Server->>Browser: JS file
    Server deactivate

    Note right of Browser: The browser starts executing the JavaScript code that fetches the JSON from the Server

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    Server activate
    Server->>Browser: [{content: "Hello world", date: "2023-03-27T14:59:15.818Z"},…]
    Server deactivate

    Note right of Browser: The browser executes the callback function that renders the notes

    Browser-->>Server: GET https://studies.cs.helsinki.fi/favicon.ico
    Server activate
    Server->>Browser: ico file
    Server deactivate

    Browser-->>Server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    Server activate
    Note right of Browser: The Server add form data {content: "greeting from Ukraine",date: "2023-03-27T20:06:28.485Z"}
    Server->>Browser: response with code 302 (redirection)
    Server deactivate

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    Server activate
    Server->>Browser: HTML file
    Server deactivate

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    Server activate
    Server->>Browser: CSS file
    Server deactivate
    
    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    Server activate
    Server->>Browser: JS file
    Server deactivate

    Note right of Browser: The browser starts executing the JavaScript code that fetches the JSON from the Server

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    Server activate
    Server->>Browser: [{content: "Hello world", date: "2023-03-27T14:59:15.818Z"},…]
    Server deactivate

    Note right of Browser: The browser executes the callback function that renders the notes

    Browser-->>Server: GET https://studies.cs.helsinki.fi/favicon.ico
    Server activate
    Server->>Browser: ico file
    Server deactivate
``` 
## 0.5: Single page app diagram
```mermaid

sequenceDiagram
    participant Browser
    participant Server

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/spa
    Server activate
    Server->>Browser: HTML file
    Server deactivate

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    Server activate
    Server->>Browser: CSS file
    Server deactivate
    
    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
    Server activate
    Server->>Browser: JS file
    Server deactivate

    Note right of Browser: The browser starts executing the JavaScript code that fetches the JSON from the Server

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    Server activate
    Server->>Browser: [{content: "Hello world", date: "2023-03-27T14:59:15.818Z"},…]
    Server deactivate

    Note right of Browser: The browser executes the callback function that renders the notes

    Browser-->>Server: GET https://studies.cs.helsinki.fi/favicon.ico
    Server activate
    Server->>Browser: ico file
    Server deactivate
```

## 0.6: New note in Single page app diagram
```mermaid

sequenceDiagram
    participant Browser
    participant Server

    Browser-->>Server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    Server activate
    Server deactivate

```