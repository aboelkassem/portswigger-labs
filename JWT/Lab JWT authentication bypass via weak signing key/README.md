# Lab: JWT authentication bypass via flawed signature verification

**Link**: https://portswigger.net/web-security/jwt/lab-jwt-authentication-bypass-via-flawed-signature-verification

**Solution**:

This lab is accept unsigned JWTs, so we will give it null in the signature

In JSON Web token editor, in the Attack button below, choose `non signing algorithm`

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

Send the request.

<p align="center" width="100%">
  <img src="image2.png" width="400" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image3.png" width="400" hight="500"/>
</p>
