# Server-side template injection

## Explanation

https://portswigger.net/web-security/server-side-template-injection

SSTI: this vuln that the developer trust user input and put it into template like

```bash
Console.Writeline($"hello {name}")
```

`name` here is taken from the user as input.

We can test this vuln when passing an operation like 2*2

it will print `hello 4` 

The methodology to perform this attack

![3jrizlvo.bmp](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/103b7afd-ce7c-4d6f-b251-c7cd1274e385/3jrizlvo.bmp)

1- **Detect**

- try inject `${{<%[%'"}}%\` If an exception is raised, this indicates that the injected template syntax is potentially being interpreted by the server in some way

2- Identity

- Try identity which template it use by causing an error and read the documentation of it

3- Exploit

- Use [PayloadsAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings) repo to identify which payload to use according to which template

  <p align="center" width="100%">
    <img src="image.bmp" width="400" hight="400"/>
  </p>

## Labs
- 
