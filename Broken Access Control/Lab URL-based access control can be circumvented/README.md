# Lab: Insecure direct object references

**Link**: https://portswigger.net/web-security/access-control/lab-insecure-direct-object-references

**Solution**:

Notice in chat feature, there is view transcript (which created txt file and store it into file system)

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

The problem it download it as `int` with name 2.txt or 3.txt … etc

This is the Full URL

<p align="center" width="100%">
  <img src="image2.png" width="800" hight="500"/>
</p>

we can download any objects that belong to someone else from `/download-transcript/<any-in-secure-object>.txt`

If we navigate to `download-transcript/1.txt` we will see the chat with Calors containing sensitive info

<p align="center" width="100%">
  <img src="image3.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image4.png" width="800" hight="500"/>
</p>
