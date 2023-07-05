# XML external entity (XXE)

# Explaination

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>

can be used in
- Any request that process XML (like SOAP services)
- Upload .xml file or svg

can be used to

- extract data, execute a remote request, or DDOS

https://portswigger.net/web-security/xxe
https://portswigger.net/web-security/xxe/xml-entities

### Types:
- In-band ⇒ display the results of the execution
- Error ⇒ display the error and the results
- Out of band (blind xxe) ⇒ didn’t show results (show general error message), so you don’t know if it really executed or not

# Labs
- [Lab Exploiting XXE using external entities to retrieve files](https://github.com/aboelkassem/portswigger-labs/tree/main/XXE/Lab%20Exploiting%20XXE%20using%20external%20entities%20to%20retrieve%20files)
- [Lab Exploiting XXE to perform SSRF attacks](https://github.com/aboelkassem/portswigger-labs/tree/main/XXE/Lab%20Exploiting%20XXE%20to%20perform%20SSRF%20attacks)
- [Lab Blind XXE with out-of-band interaction](https://github.com/aboelkassem/portswigger-labs/tree/main/XXE/Lab%20Blind%20XXE%20with%20out-of-band%20interaction)
- [Lab Blind XXE with out-of-band interaction via XML parameter entities](https://github.com/aboelkassem/portswigger-labs/tree/main/XXE/Lab%20Blind%20XXE%20with%20out-of-band%20interaction%20via%20XML%20parameter%20entities)
