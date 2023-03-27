# FullStackOpen


## 0.4: New note diagram

sequenceDiagram
    participant Browser
    participant Server

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    server activate
    Server->>Browser: HTML file
    server deactivate

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    server activate
    Server->>Browser: CSS file
    server deactivate
    
    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    server activate
    Server->>Browser: JS file
    server deactivate

    Note right of Browser: The browser starts executing the JavaScript code that fetches the JSON from the server

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    server activate
    Server->>Browser: [{content: "Hello world", date: "2023-03-27T14:59:15.818Z"},…]
    server deactivate

    Note right of Browser: The browser executes the callback function that renders the notes

    Browser-->>Server: GET https://studies.cs.helsinki.fi/favicon.ico
    server activate
    Server->>Browser: ico file
    server deactivate

    Browser-->>Server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    server activate
    Note right of Browser: The server add form data {content: "greeting from Ukraine",date: "2023-03-27T20:06:28.485Z"}
    Server->>Browser: response with code 302 (redirection)
    server deactivate

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    server activate
    Server->>Browser: HTML file
    server deactivate

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    server activate
    Server->>Browser: CSS file
    server deactivate
    
    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    server activate
    Server->>Browser: JS file
    server deactivate

    Note right of Browser: The browser starts executing the JavaScript code that fetches the JSON from the server

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    server activate
    Server->>Browser: [{content: "Hello world", date: "2023-03-27T14:59:15.818Z"},…]
    server deactivate

    Note right of Browser: The browser executes the callback function that renders the notes

    Browser-->>Server: GET https://studies.cs.helsinki.fi/favicon.ico
    server activate
    Server->>Browser: ico file
    server deactivate


## 0.5: Single page app diagram

sequenceDiagram
    participant Browser
    participant Server

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/spa
    server activate
    Server->>Browser: HTML file
    server deactivate

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    server activate
    Server->>Browser: CSS file
    server deactivate
    
    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
    server activate
    Server->>Browser: JS file
    server deactivate

    Note right of Browser: The browser starts executing the JavaScript code that fetches the JSON from the server

    Browser-->>Server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    server activate
    Server->>Browser: [{content: "Hello world", date: "2023-03-27T14:59:15.818Z"},…]
    server deactivate

    Note right of Browser: The browser executes the callback function that renders the notes

    Browser-->>Server: GET https://studies.cs.helsinki.fi/favicon.ico
    server activate
    Server->>Browser: ico file
    server deactivate

## 0.6: New note in Single page app diagram

sequenceDiagram
    participant Browser
    participant Server

    Browser-->>Server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    server activate
    server deactivate

    