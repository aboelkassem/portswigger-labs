# CORS
## Explanation

SOP= Same origin policy ⇒ is the browser preventing any connections/reading from other websites

- Should have the same protocol, name, and port to be considered as the same policy ⇒ http://example.com:80
- If one of above parts have changed, then its different origin policy like ⇒ http://sub.example.com:80

CORS = cross origin resource sharing ⇒ predefined rules for specific websites to be allowed for sharing/exchange resources between these websites

- Depends in two headers
    - Access-Control-Allow-Origin: *
    - Access-Control-Allow-Credentials: true ⇒ enable host to request another host even if the user logged in (allow credentials exchange)

 ## Labs 
 - 
