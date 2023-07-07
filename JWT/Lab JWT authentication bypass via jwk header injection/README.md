# Lab: JWT authentication bypass via jwk header injection

**Link**: https://portswigger.net/web-security/jwt/lab-jwt-authentication-bypass-via-jwk-header-injection

**Solution**:
In this lab, the web server supports the `jwk` parameter (this token is used by the server to verify the JWT token).

To solve it, we will create our own jwk and pass it to the request.

In JWT editors keys, create new RSA Key

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

In the request, Attack > Embedded JWT > Choose our created one.

<p align="center" width="100%">
  <img src="image2.png" width="800" hight="500"/>
</p>
  
<p align="center" width="100%">
  <img src="image3.png" width="800" hight="500"/>
</p>
