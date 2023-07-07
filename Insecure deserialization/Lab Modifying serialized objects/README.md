# Lab: Modifying serialized objects

**Link**: https://portswigger.net/web-security/deserialization/exploiting/lab-deserialization-modifying-serialized-objects

**Solution**:

In this lab, if we take the session string and decode it use URL encoding and then base64

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

We will see this object

<p align="center" width="100%">
  <img src="image2.png" width="800" hight="500"/>
</p>

Or we can use Burp inspector

<p align="center" width="100%">
  <img src="image3.png" width="800" hight="500"/>
</p>

we can modify it `b:0` (boolean: false) to `b:1` (admin:true) and encode it again

Edit the cookies and then `Apply Changes`

<p align="center" width="100%">
  <img src="image4.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image5.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image6.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image7.png" width="800" hight="500"/>
</p>
