# Lab: Basic SSRF against another back-end system

**Link**: https://portswigger.net/web-security/ssrf/lab-basic-ssrf-against-backend-system

**Solution**:

Like the above lab but he told you that the internal system on `192.168.0.X` so we need to send this request to Intruder to brute force it.

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

Change payload

<p align="center" width="100%">
  <img src="image2.png" width="800" hight="500"/>
</p>

You will notice which service which reply to you with 200 OK with id (192.168.0.78)

<p align="center" width="100%">
  <img src="image3.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image4.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image5.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image6.png" width="800" hight="500"/>
</p>
