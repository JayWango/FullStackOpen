```mermaid

sequenceDiagram
  participant browser
  participant server
  
  browser-->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
  activate server
  server-->>browser: HTML document
  deactivate server
 
  browser-->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
  activate server
  server-->>browser: CSS document
  deactivate server
  
  browser-->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
  activate server
  server-->>browser: JSON data
  Note right of browser: All the javascript in the browser instead of being fetched from the server
  deactivate server
  
  
