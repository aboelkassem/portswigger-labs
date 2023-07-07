# Lab: Username enumeration via subtly different responses

**Link**: https://portswigger.net/web-security/authentication/password-based/lab-username-enumeration-via-subtly-different-responses

**Solution**:

This lab like the previous one, but it shows `Invalid name or password`

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

So you cannot predict which username is valid.

We will brute brute-force the usernames first to see if there any differences in the error message.

We can make it by Intruder and In Options> Grep - Extract (to extract differences responses based on your selection)

<p align="center" width="100%">
  <img src="image2.png" width="800" hight="500"/>
</p>
  
<p align="center" width="100%">
  <img src="image3.png" width="800" hight="500"/>
</p>

We will see that there is different response message in final dot (.)

<p align="center" width="100%">
  <img src="image4.png" width="800" hight="500"/>
</p>

This means that `asdl` is valid username

We will do the same like previous lab to brute-force the passwords

<p align="center" width="100%">
  <img src="image5.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image6.png" width="800" hight="500"/>
</p>
