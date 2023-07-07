# Lab: Authentication bypass via OAuth implicit flow

**Link**: https://portswigger.net/web-security/oauth/lab-oauth-authentication-bypass-via-oauth-implicit-flow

**Solution**:

In this lab, it doesn’t validate the token with provided email in oauth server `/authenticate` 

and depends on the email for authentication process in the oauth

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

We will modify the email in the repeater

<p align="center" width="100%">
  <img src="image2.png" width="800" hight="500"/>
</p>

see the response in the browser

<p align="center" width="100%">
  <img src="image3.png" width="800" hight="500"/>
</p>
