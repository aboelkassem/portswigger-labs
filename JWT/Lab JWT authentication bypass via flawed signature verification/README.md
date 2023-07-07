# Lab: JWT authentication bypass via unverified signature

**Link**: https://portswigger.net/web-security/jwt/lab-jwt-authentication-bypass-via-unverified-signature

**Solution**:

In this lab we will use burp extension called JWT editor.

- Highlight the requests that used JWT
- In the repeater, there is JWT token editor
  
<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

This lab is not to verify the signature which consists of

<p align="center" width="100%">
  <img src="image2.png" width="400" hight="500"/>
</p>

So, if I change the username in the payload, it accept it and go admin panel.

<p align="center" width="100%">
  <img src="image3.png" width="400" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image4.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image5.png" width="800" hight="500"/>
</p>
