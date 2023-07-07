# Lab: JWT authentication bypass via weak signing key

**Link**: https://portswigger.net/web-security/jwt/lab-jwt-authentication-bypass-via-weak-signing-key

**Solution**:

This lab has weak signing key, we can bypass it using brute-force with this list https://github.com/wallarm/jwt-secrets/blob/master/jwt.secrets.list

And will use `hashcat` or [john](https://github.com/openwall/john) tools to brute-force

https://portswigger.net/web-security/jwt#brute-forcing-secret-keys-using-hashcat

1- Brute force the secret key using hashcat using the following command

```bash
hashcat-a 0 -m 16500 "eyJraWQiOiJjOTU1ZDlmNS1hYjZlLTQ1YWQtYTU5My0xNWYwMzJlOTMzMzYiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJwb3J0c3dpZ2dlciIsInN1YiI6IndpZW5lciIsImV4cCI6MTY3OTE0MjUyNH0.16kGAs15tikJPMTEUQlToZfSRuKmrKbhmQzfgIXUxgo" "C:\Users\Mohamed\Downloads\jwt.secrets.list"
```

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

- Encode this signing key into base64

<p align="center" width="100%">
  <img src="image2.png" width="800" hight="500"/>
</p>

- Take this value and will create a signing key with this secret.
  
<p align="center" width="100%">
  <img src="image3.png" width="800" hight="500"/>
</p>

In the request, choose the signing key we’ve been created

<p align="center" width="100%">
  <img src="image4.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image5.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image6.png" width="800" hight="500"/>
</p>
