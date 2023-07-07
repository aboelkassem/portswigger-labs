# Lab: Username enumeration via response timing

**Link**: https://portswigger.net/web-security/authentication/password-based/lab-username-enumeration-via-response-timing

**Solution**:

In this lab, we will notice that if the username is valid, it will take much time to response than the normal request.

But there is a IP protection which block your IP if you send it many times.

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

To bypass it, we will spoof it using `X-Forwarded-For` header and define it different IP address

<p align="center" width="100%">
  <img src="image2.png" width="800" hight="500"/>
</p>

So, for now we will send the intruder with different IPs in each request.

<p align="center" width="100%">
  <img src="image3.png" width="800" hight="500"/>
</p>

Notice, here we identified two different places to be changes in each request. So we must choose attack type to `Pitchfork` which treat each place separately.

 For first payload
 
<p align="center" width="100%">
  <img src="image4.png" width="800" hight="500"/>
</p>

For second payload

<p align="center" width="100%">
  <img src="image5.png" width="800" hight="500"/>
</p>

In the results, we will filter it using `Time Completed` column

<p align="center" width="100%">
  <img src="image6.png" width="800" hight="500"/>
</p>

So `vagrant` is the username based on time delay.

We will brute force it with password lists

<p align="center" width="100%">
  <img src="image7.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image8.png" width="800" hight="500"/>
</p>
