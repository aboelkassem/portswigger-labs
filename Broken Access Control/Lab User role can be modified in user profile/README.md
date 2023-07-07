# Lab: User role can be modified in user profile

**Link**: https://portswigger.net/web-security/access-control/lab-user-role-can-be-modified-in-user-profile

**Solution**:

If we navigate to account settings and change email, you will notice that the roleId returned in the response.

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

We will try to add this parameter to the body and it accepts it 😃

<p align="center" width="100%">
  <img src="image2.png" width="800" hight="500"/>
</p>

Then, we are admin now

<p align="center" width="100%">
  <img src="image3.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image4.png" width="800" hight="500"/>
</p>
