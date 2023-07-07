# Lab: User ID controlled by request parameter with data leakage in redirect

**Link**: https://portswigger.net/web-security/access-control/lab-user-id-controlled-by-request-parameter-with-data-leakage-in-redirect

**Solution**:

In site map of the target, you will find /my-account?id=wiener as you will see takes the username as parameter,

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

change it to `carlos`

<p align="center" width="100%">
  <img src="image2.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image3.png" width="800" hight="500"/>
</p>
