# Lab: Web shell upload via obfuscated file extension

**Link**: https://portswigger.net/web-security/file-upload/lab-file-upload-web-shell-upload-via-obfuscated-file-extension

**Solution**:
The problem is whitelisted only two extensions (accept only two extensions jpg and png)

We can use null character injection ⇒ https://infosecwriteups.com/bypass-server-upload-restrictions-69054c5e1be4

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

if you give it this `payload.php%00.jpg` it will uploaded successfully but the server will ignore anything after %00 ⇒ `payload.php%00.jpg` = `payload.php .jpg` = `payload.php`

<p align="center" width="100%">
  <img src="image2.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image3.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image4.png" width="800" hight="500"/>
</p>
