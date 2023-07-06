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
 - [Lab CORS vulnerability with basic origin reflection](https://github.com/aboelkassem/portswigger-labs/tree/main/CORS/Lab%20CORS%20vulnerability%20with%20basic%20origin%20reflection)
 - [Lab CORS vulnerability with trusted null origin](https://github.com/aboelkassem/portswigger-labs/tree/main/CORS/Lab%20CORS%20vulnerability%20with%20trusted%20null%20origin)
 - [Lab CORS vulnerability with trusted insecure protocols](https://github.com/aboelkassem/portswigger-labs/tree/main/CORS/Lab%20CORS%20vulnerability%20with%20trusted%20insecure%20protocols)
