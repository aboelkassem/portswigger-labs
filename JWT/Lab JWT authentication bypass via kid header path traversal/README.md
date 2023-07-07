# Lab: JWT authentication bypass via jku header injection

**Link**: https://portswigger.net/web-security/jwt/lab-jwt-authentication-bypass-via-jku-header-injection

**Solution**:

In this lab, the server supports `jku` header which contains the URL of public key to verify the signature of JWT from remote trusted source instead of hardcoded.

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

To solve this lab, we will create own key and host it into remote server with adding this header to tell the JWT to verify its signature from it.

In JWT editors keys, create new RSA key

<p align="center" width="100%">
  <img src="image2.png" width="800" hight="500"/>
</p>

Copy this key and go to the exploit server to past it in the body.

```bash
{
 "keys": [
   {
    "p": "6kw8lSQ0_hEmmiFV5JWYEXSjp8vFFSVlS2Go8gXfse_CuW5fdPk7m0arZK7As9EUq4Fxjx1VHQ-gDZC7rQMPsdeal1BETjD4rlB9spk_3u4vMGcU-4AjrDMtB4PRA9HeO_8axS1jUai0nzujgIstaaVhDTynul2f6_WFpwj1RLc",
    "kty": "RSA",
    "q": "2f5_PaqBLUCeB_-71Rg9F7_ABbFtlcvDix4z6oMiLDASdNGHoedMqmJmxN3rpfYzy27953zntzOKQpOE7YekT8eUIVEmCd6nkSyXkmISbMrSowfJsxFGgod_IrlUNbnWMpgwTYxU1VlASlysOKSMJ1xWdz-Q31uqJEqOo-kkKF0",
    "d": "I3CtAS943Vo5sqDMpY2FAvnIzuGLP21FZnxxJa90oJ-zCsMzvLYbcsT1K_apRR0Q3LrKVsQNgI0Yhv0gtr4zMAlcJPgp0bQmiL1QgevS_HhpBv4Ww3NzcMGBHVGGVfEtkc5BaI4meHMXa9v4CXKTlakUecNIEYP8ZI8A32wh0Wiog6o63O0Udne0lU8QbFxG2tBph-kN6eAJSrMGRM5bzN21UFK37PPrzeaGv7UKNfCPVwp-_S_lWpZv17FGNHuRm-KFtbUjxjnAqsuZ23_FGQUuOqwDW-8SkHWmfSBQEKQJD_Nq5wHUMJxs6Y2-M9quuDD5BJu26QdZ9nmgWH-i3Q",
    "e": "AQAB",
    "kid": "e93c1617-fb33-4d6e-812e-5129c8a1f925",
    "qi": "0FDGWECF8SuMh4qZEt-JYZrzboPyd7Qiu_lBh_xM1ipdraugzQJ_LQJzcG4sG7-RyK2zBUPHDLQsxF12ytspzqkL79T_rwLNT9GQVVUeBYq5o2LYetTX1UgXNX2jV7q5x4mQCs3BZpPh59Bn35AVxnIJqIffe0hQAdss3lPWFjg",
    "dp": "Q-pHYV_2cHMeQm1JTZJDW0P5MGlzvnZxj1FGvKkRN63tPv0MdIbOTWtFwVCakUUY_cHu3fI9usfNuEDs9fC-OunpaNUeh5_QZg708LFVf1SBn0EyJtj0_jRzaAtAqh_KkI-Y_fDzKjeB6-pIsbkmN8p1gHXFlNMQyUAJNur01a8",
    "dq": "tfoq1Bqi7VjU046biX9LeKjcrqP3_CV2norfAfToMQUMUzKazAAfUtkEO3GahxepEzkbggQWFyxSTdOCExu5gdP0h3-Lho-1SI52FYADK4iBIBGfQfm457we2KjncFYrRl8fa40rQFLaRXlpV3udeDowACozURHfTZ5jxtcYFQ0",
    "n": "x4OLcsnwHoCk8isE4OudzV-1P2UPKWLagx_pLUfADdEs4aAzA_zhgfuI4HkmUCl5IQhkC8ugAO_OTcWnOOuDt0_n3KV46SPyyArYvdPXaZK4HJFk-vU7vb311iqhrtK45N8CHi7XAyVeoldG9fmUXNuN2E1brx7zBtYx58RNOEeP8K2E9xtEY67R77cbwQurK1XSBaN5XQVTxbjL82YtwZJP6A1boizrSZMKKdrvcaXXb1DXq_LBeKbuNe9kKlvTyDKBcKBq7859wVMqHJ4ZNNRgoSfuqFaRMQHLR6QzcUCwyA5o4bxbWq3XIjdJbEL5cmNrlUBMKItA5mehzJKOew"
}
 ]
}
```

<p align="center" width="100%">
  <img src="image3.png" width="800" hight="500"/>
</p>

In the request, 

- Add jku header
- Modify kid header to match the one in the jwt
- Sign the request with our key

<p align="center" width="100%">
  <img src="image4.png" width="800" hight="500"/>
</p>

<p align="center" width="100%">
  <img src="image5.png" width="800" hight="500"/>
</p>
