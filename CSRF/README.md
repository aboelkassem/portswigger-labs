# CSRF
## Explanation

Send a POST or GET request from a form as your victim user. like transfer money, create admin user, change password, … etc

How to check it?

- Check if there is a token in POST or GET form
- Check if validate this token by multiple ways like
    - Request method
    - Existence
    - User Session
    - Try make an error like pass array of strings instead of one string

## Labs
- [Lab CSRF vulnerability with no defenses](https://github.com/aboelkassem/portswigger-labs/tree/main/CSRF/Lab%20CSRF%20vulnerability%20with%20no%20defenses)
- [Lab CSRF where token is not tied to user session](https://github.com/aboelkassem/portswigger-labs/tree/main/CSRF/Lab%20CSRF%20where%20token%20is%20not%20tied%20to%20user%20session)
- [Lab CSRF where token validation depends on request method](https://github.com/aboelkassem/portswigger-labs/tree/main/CSRF/Lab%20CSRF%20where%20token%20validation%20depends%20on%20request%20method)
- [Lab CSRF where token validation depends on token being present](https://github.com/aboelkassem/portswigger-labs/tree/main/CSRF/Lab%20CSRF%20where%20token%20validation%20depends%20on%20token%20being%20present)
