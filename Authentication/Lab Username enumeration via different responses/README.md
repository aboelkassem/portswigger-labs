# Lab: Username enumeration via different responses

**Link**: https://portswigger.net/web-security/authentication/password-based/lab-username-enumeration-via-different-responses

**Solution**:

In this lab, we will brute force usernames. 

When I tried to enter a invalid username and password, it gives me that this username only is invalid. So we will enumerate usernames until one of them is valid.

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

We will use this list of usernames and pass it to Turbo Intruder (for concurrently requests) or Intruder [usernames.txt](/usernames.txt)

<p align="center" width="100%">
  <img src="image2.png" width="800" hight="500"/>
</p>
  
<p align="center" width="100%">
  <img src="image3.png" width="800" hight="500"/>
</p>

Click StartAttack, after completed, Check/filter requests length to see different responses

<p align="center" width="100%">
  <img src="image4.png" width="800" hight="500"/>
</p>

This mean that this username is correct

We will freeze this username, and brute-force the password

<p align="center" width="100%">
  <img src="image5.png" width="800" hight="500"/>
</p>

This means the correct password is `jessica`

<p align="center" width="100%">
  <img src="image6.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image6.png" width="800" hight="500"/>
</p>
