# Lab: 2FA broken logic

**Link**: https://portswigger.net/web-security/authentication/multi-factor/lab-2fa-broken-logic

**Solution**:

This lab needs to access Carlos account without any password with your 2FA.

If we discover the login flow with our credentials.

We will notice in GET request /login2, it takes the username which will send the verification code to my email.

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image2.png" width="800" hight="500"/>
</p>

If we changed this flag to 

<p align="center" width="100%">
  <img src="image3.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image4.png" width="800" hight="500"/>
</p>

And in the POST request of /login2, there it takes 2fa-code parameter

<p align="center" width="100%">
  <img src="image5.png" width="800" hight="500"/>
</p>

we will brute-force this code using burp intruder.

<p align="center" width="100%">
  <img src="image6.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image7.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image8.png" width="800" hight="500"/>
</p>
