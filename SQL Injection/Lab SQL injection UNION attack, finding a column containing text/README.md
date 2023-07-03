# Lab: SQL injection UNION attack, determining the number of columns returned by the query

**Link**: https://portswigger.net/web-security/sql-injection/union-attacks/lab-determine-number-of-columns

**Solution**: in Query parameter add multiple nullable unions until one is working to know columns number (3), add: 1' UNION SELECT NULL, NULL, NULL --

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/portswigger-labs/blob/main/SQL%20Injection/Lab%20SQL%20injection%20UNION%20attack,%20determining%20the%20number%20of%20columns%20returned%20by%20the%20query/image1.png?raw=true" width="500" hight="500"/>
</p>
