# Lab: User role controlled by request parameter

**Link**: https://portswigger.net/web-security/access-control/lab-user-role-controlled-by-request-parameter

**Solution**:

If we spider the website, we will see that if we navigate to /admin 

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

With normal user, there is in the cookies flag called `Admin=false`

If we changed it to true

<p align="center" width="100%">
  <img src="image2.png" width="800" hight="500"/>
</p>

It gives me the admin panel

<p align="center" width="100%">
  <img src="image3.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image4.png" width="800" hight="500"/>
</p>
