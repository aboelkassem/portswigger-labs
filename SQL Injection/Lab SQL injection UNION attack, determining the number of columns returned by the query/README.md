# Lab: SQL injection UNION attack, determining the number of columns returned by the query

**Link**: https://portswigger.net/web-security/sql-injection/union-attacks/lab-determine-number-of-columns

**Solution**: in Query parameter add multiple nullable unions until one is working to know columns number (3), add: 1' UNION SELECT NULL, NULL, NULL --

<p align="center" width="100%">
  <img src="https://github.com/aboelkassem/portswigger-labs/raw/main/SQL%20Injection/Lab%20SQL%20injection%20vulnerability%20in%20WHERE%20clause%20allowing%20retrieval%20of%20hidden%20data/image1.png" width="500" hight="500"/>
</p>
