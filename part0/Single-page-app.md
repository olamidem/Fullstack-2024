# 0.5: Single page app diagram
```mermaid
sequenceDiagram
  browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa

server-->>browser: The SPA

 browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
server-->>browser: The SPA

browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
server-->>browser: The SPA

browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json

Note right of browser:The server return a response with the below and Status Code: 200 OK
server-->>browser: [{"content": "Rylläys","date": "2024-07-05T10:23:38.801Z"},........, {"content": "Spa","date": "2024-07-05T17:33:23.163Z"}]
