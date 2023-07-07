# Lab: 2FA bypass using a brute-force attack

**Link**: https://portswigger.net/web-security/authentication/multi-factor/lab-2fa-bypass-using-a-brute-force-attack

**Solution**:

This lab, If I entered a wrong 2fa-code twice, it return me to login page with different session token and CSRF.

We will brute force using [Macros](https://portswigger.net/burp/documentation/desktop/settings/sessions#macros) which we define a sequence of requests which if the request failed, it will update the session and CSRF token with new ones in the next requests.

Burp Setting > sessions > session handling rules

Change scope

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

Add new Rule Action

with the following requests sequence

- GET /login (to get new sessions)
- POST /login (add the credentails)
- GET /login2
  

<p align="center" width="100%">
  <img src="image2.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image3.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image4.png" width="800" hight="500"/>
</p>

And in the POST request of 2fa-code, send it to the intruder to brute force 2fa codes

<p align="center" width="100%">
  <img src="image5.png" width="800" hight="500"/>
</p>

And change the concurrent request pool to 1 max

You will find in the requests, it automatically changes the session token and CSRF token when failed

<p align="center" width="100%">
  <img src="image6.png" width="800" hight="500"/>
</p>

here we find the code `0050`

<p align="center" width="100%">
  <img src="image7.png" width="800" hight="500"/>
</p>

Show the response in the browser.

<p align="center" width="100%">
  <img src="image8.png" width="800" hight="500"/>
</p>
