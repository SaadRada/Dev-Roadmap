# Http & Https

## Whats is Http and Https?

- ### Http :
  - Http is stand for Hyper text Transfer Protocol
  - Communication between web servers and clients
  - Http has requests and responses
  - Every request is completly independant
- ### Https :
  - Https is stand for Hyper text Transfer Protocol Secure
  - Data sent is encrypted by SSL(Secure socket layer)
  - install certificate on web host

## Http Methods :
- GET : Retrieves Data From The Server
- POST : Submit Data to The Server
- PUT : Update Data Alredy in The Server
- DELETE : Deletes Data From The Server

## Http Header Field :
![Http Header](https://cdn.tutsplus.com/cdn-cgi/image/width=590/net/uploads/legacy/511_http/request_header.png)
- ### Generale :
  - Request URL
  - Request Method (GET, POST ...)
  - Status Code
  - Remote Adress (IP)
  - Refer Policy (Historie of previous pagesand more)
- ### Response : 
  - Server (Apache, Nginx ...)
  - Set-Cookie
  - Content Type (html : text/html, css : text/css, image : image/png ...)
  - Content Length
  - Date
- ### Request : 
  - Cookies
  - Accept-xxx
  - Content Type
  - Content Length
  - Autorization (Token)
  - User-Agent (OS, Browser infos ...)
  - Referrer

## Http Status Codes :
- #### 1XX : Informational
  Reauest received / processing
- #### 2XX : Success
  Succesfully Received, understood and accepted
- #### 3XX : Redirect
  Further action must be taken/redirect
- #### 4XX : Client Error
  Request does not have what it needs
- #### 5XX : Server Error
  Server failed to fulfil an apparent valid request
<img src="https://www.infidigit.com/wp-content/uploads/2019/12/20191227_012601_0000.png">