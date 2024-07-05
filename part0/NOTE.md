# 0.4: New note diagram

## Diagram

```mermaid
sequenceDiagram
  browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note

Note right of browser: When the button on the form is clicked: the browser will send the user input to the server. i.e form data is sent with HTTP POST

server-->>browser: The server responds with HTTP status code 302  URL redirect. Location: /notes

Note right of browser: The server asks the browser to perform a new HTTP GET

 browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes
Note right of the browser: The browser reloads the Notes page. The reload causes three more HTTP requests

  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/notes

 server-->>browser: HTML document

Note right of browser: fetching the style sheet (main.css)
browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css

 server-->>browser: The css file
Note right of the browser: fetching the JavaScript code (main.js)
browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.js

server-->>browser: The JavaScript file

Note right of the browser: fetching the  raw data of the notes (data.json)
browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
server-->>browser: [{"content": "hiuyhiio","date": "2024-07-05T09:45:37.203Z"},{"content": "oihuiuhu","date": "2024-07-05T09:45:46.367Z"},{"content": "好 的","date": "2024-07-05T09:52:22.653Z"}, ...  {"content": "add mine","date": "2024-07-05T17:08:10.578Z"}]

