# Broken Access Control
https://portswigger.net/web-security/access-control (should read it)
There are 3 types of access control

- Vertical Access control: Not all people have the permission to do something
- Horizontal Access control: You only authorize to access/manage your own resources.
- Context-dependent access control: depends on the context of logic

### [Examples of Broken Access Control](https://portswigger.net/web-security/access-control#examples-of-broken-access-controls)

- Vertical privilege escalation
    <p align="center" width="100%">
      <img src="image1.png" width="800" hight="500"/>
    </p>
    
- Unprotected functionality
    <p align="center" width="100%">
      <img src="image2.png" width="800" hight="500"/>
    </p>

- Broken access control resulting from platform misconfiguration
- Broken access control resulting from URL-matching discrepancies
- Horizontal privilege escalation
- Horizontal to vertical privilege escalation
- Insecure direct object references
- Access control vulnerabilities in multi-step processes
- Referer-based access control
- Location-based access control


## Labs
- [Lab Unprotected admin functionality](https://github.com/aboelkassem/portswigger-labs/tree/main/Broken%20Access%20Control/Lab%20Unprotected%20admin%20functionality)
- [Lab: Unprotected admin functionality with unpredictable URL (Page source)](https://github.com/aboelkassem/portswigger-labs/tree/main/Broken%20Access%20Control/Lab%20Unprotected%20admin%20functionality%20with%20unpredictable%20URL%20(Page%20source))
- [Lab User role controlled by request parameter](https://github.com/aboelkassem/portswigger-labs/tree/main/Broken%20Access%20Control/Lab%20User%20role%20controlled%20by%20request%20parameter)
- [Lab User role can be modified in user profile](https://github.com/aboelkassem/portswigger-labs/tree/main/Broken%20Access%20Control/Lab%20User%20role%20can%20be%20modified%20in%20user%20profile)
- [Lab User ID controlled by request parameter](https://github.com/aboelkassem/portswigger-labs/tree/main/Broken%20Access%20Control/Lab%20User%20ID%20controlled%20by%20request%20parameter)
- [Lab User ID controlled by request parameter, with unpredictable user IDs](https://github.com/aboelkassem/portswigger-labs/tree/main/Broken%20Access%20Control/Lab%20User%20ID%20controlled%20by%20request%20parameter%2C%20with%20unpredictable%20user%20IDs)
- [Lab User ID controlled by request parameter with data leakage in redirect](https://github.com/aboelkassem/portswigger-labs/tree/main/Broken%20Access%20Control/Lab%20User%20ID%20controlled%20by%20request%20parameter%20with%20data%20leakage%20in%20redirect)
- [Lab User ID controlled by request parameter with password disclosure](https://github.com/aboelkassem/portswigger-labs/tree/main/Broken%20Access%20Control/Lab%20User%20ID%20controlled%20by%20request%20parameter%20with%20password%20disclosure)
- [Lab Insecure direct object references](https://github.com/aboelkassem/portswigger-labs/tree/main/Broken%20Access%20Control/Lab%20Insecure%20direct%20object%20references)
- [Lab URL-based access control can be circumvented](https://github.com/aboelkassem/portswigger-labs/tree/main/Broken%20Access%20Control/Lab%20URL-based%20access%20control%20can%20be%20circumvented)
