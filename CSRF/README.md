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
- 
