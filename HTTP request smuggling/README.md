# HTTP request smuggling
https://portswigger.net/web-security/request-smuggling

<p align="center" width="100%">
  <img src="image1.png" width="800" hight="500"/>
</p>


When the user send a request to client/load-balancer, the server process these requests sequential and based on that take decicions
So, we will fool the server with fake request that we've done with first request and start process the request after that

In this case, the server depends on two headers
- Content- Length = size of request
- Transaction-Encoding = transfer format (the request chunked)
    - if the value of chunked = 0, mean the request is finished

<p align="center" width="100%">
  <img src="image2.png" width="800" hight="500"/>
</p>

We will see which server support each way

And start playing 😃

1- Change method request to POST

<p align="center" width="100%">
  <img src="image3.png" width="800" hight="500"/>
</p>
Burp extensions ⇒ [HTTP Request Smuggler](https://portswigger.net/blog/http-desync-attacks-request-smuggling-reborn#demo)

How to know if your request has really passed?

- From response messages (401 or 401)
- Or giving it a bigger content-length bytes than the body (will response with time-out or internal server error)
    - this mean The server still waiting the rest of body content
 
# Labs
- 
