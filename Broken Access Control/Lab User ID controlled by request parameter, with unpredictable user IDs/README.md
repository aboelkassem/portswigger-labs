# Lab: User ID controlled by request parameter, with unpredictable user IDs

**Link**: https://portswigger.net/web-security/access-control/lab-user-id-controlled-by-request-parameter-with-unpredictable-user-ids

**Solution**:

Like the previous lab, but takes guid /my-account?id=newGuid

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

So, the target now is to get the GUID of carlos, While surfing the blog/posts

<p align="center" width="100%">
  <img src="image2.png" width="800" hight="500"/>
</p>

This navigate with guid of carlos user,

<p align="center" width="100%">
  <img src="image3.png" width="800" hight="500"/>
</p>

So, if we take it and replace it with my-account?id=ba09be5b-55c0-4014-96da-1dd318e912be

<p align="center" width="100%">
  <img src="image4.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image5.png" width="800" hight="500"/>
</p>
