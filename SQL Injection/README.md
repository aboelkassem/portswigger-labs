# SQL Injection (SQLi)
## Explanation

1- Search for any fields that take input in the web
2- Try to imagine the SQL query behind it 
3- Break it 😃

### Where can I inject my payload?

- SQL injection can be in GET based
   - http://digimon.com/index.php?id=1
- SQL injection can be in POST based
   - HTML form like login page
- SQL injection can be in Header based
  - header parameters like Referrer, HOST, user agent
- SQL injection can be in cookie-based
  - Cookie: id=asdasdasdasdas;

### How to check for SQL vulnerability ? or How to detect SQL injection?

1- SQL database Error

- Syntax error ⇒ you can use any of ( ‘ " @ # \ ) to check if sql vulnerable or not by returning Error

2- Blind boolean

- Any true or false condition like `id=2' and '1'='1' --+`  or `select substring('mohamed',1,1)='m'`

3- Time based


### How to exploit it?

1- Find injection point in any forms fields

2- Modify Query

- in GET we add `'--` // just to comment the rest of the query
- in POST we add --SPACE or ’ #

## Labs
- [Lab: SQL injection vulnerability in WHERE clause allowing retrieval of hidden data](https://github.com/aboelkassem/portswigger-labs/tree/main/SQL%20Injection/Lab%20SQL%20injection%20vulnerability%20in%20WHERE%20clause%20allowing%20retrieval%20of%20hidden%20data)
- [Lab SQL injection vulnerability allowing login bypass](https://github.com/aboelkassem/portswigger-labs/tree/main/SQL%20Injection/Lab%20SQL%20injection%20vulnerability%20allowing%20login%20bypass)
- [Lab SQL injection UNION attack, determining the number of columns returned by the query](https://github.com/aboelkassem/portswigger-labs/tree/main/SQL%20Injection/Lab%20SQL%20injection%20UNION%20attack%2C%20determining%20the%20number%20of%20columns%20returned%20by%20the%20query)
- [Lab SQL injection UNION attack, finding a column containing text](https://github.com/aboelkassem/portswigger-labs/tree/main/SQL%20Injection/Lab%20SQL%20injection%20UNION%20attack%2C%20finding%20a%20column%20containing%20text)
