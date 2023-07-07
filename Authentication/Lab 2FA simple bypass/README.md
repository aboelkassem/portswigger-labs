# Lab: Broken brute-force protection, multiple credentials per request

**Link**: https://portswigger.net/web-security/authentication/password-based/lab-broken-brute-force-protection-multiple-credentials-per-request

**Solution**:

This lab, the username and password is send through the request body in JSON format

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

So, In password Instead of passing it string, we will pass it list of strings

<p align="center" width="100%">
  <img src="image2.png" width="800" hight="500"/>
</p>

return 302 redirect, show the response in the browser

<p align="center" width="100%">
  <img src="image3.png" width="800" hight="500"/>
</p>
