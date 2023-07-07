# Lab: Basic SSRF against the local server

**Link**: https://portswigger.net/web-security/ssrf/lab-basic-ssrf-against-localhost

**Solution**:

In the stock check (you will notice, the website is requesting another internal app to check the stock item) 

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

stockApi takes the URL of the internal app (only accessed throw the website not public to all users)

if we decode it stockAPI = http://stock.weliketoshop.net:8080/product/stock/check?productId=2&storeId=1

If we changed it to localhost, it will replay with the internal home page

<p align="center" width="100%">
  <img src="image2.png" width="800" hight="500"/>
</p>
so we can request anything

<p align="center" width="100%">
  <img src="image3.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image4.png" width="800" hight="500"/>
</p>
