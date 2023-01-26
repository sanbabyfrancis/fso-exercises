sequenceDiagram
    participant browser
    participant server

    Note right of browser: When the button is clicked, the browser <br> creates a new note and renders the text on <br> to the screen. The content and timestamp of the <br> new note is sent to the server as a  request payload <br> via an HTTP POST request.
    
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: Status code: 201
    deactivate server

    Note right of browser: Browser does not reload
