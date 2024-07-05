# 0.6: Add new noted Single page app diagram
```mermaid
sequenceDiagram
  browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
Note right of browser:The broswer make a POST request by submitting the form with the payload of {content: "SPA", date: "2024-07-05T17:48:00.911Z"} and Status Code: 201 Created
server-->>browser:{"message":"note created"} 

Note right of browser:The broswer then reinvalidate and shows the newly added noted

