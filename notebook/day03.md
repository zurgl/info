## Day 03

### Mailing
To solve the issue and being able to receive email, i've find a new way too redirect mailing to a domain to my personal mailbox **gmail**
This is done using At the same time I've realize 

### Docker
Learn so basic stuff about **docker**



### Nginx
Learn some cool stuff about nginx configuration. The best one is about load balacing base on ip_hash.

```
  upstream ws-backend {
    # enable sticky session based on IP
    ip_hash;

    server server01:3000;
    server server02:3000;
    server server03:3000;
  }
  ```
  
  Learn some interesting stuff about http2, push directy and keep alive connection.
  
  
  ### Websocket 
  Find some cool tutorail [here](https://www.serverlab.ca/tutorials/linux/web-servers-linux/how-to-configure-nginx-for-websockets/) and [here](https://www.tutorialspoint.com/how-to-configure-nginx-as-reverse-proxy-for-websocket)
  
  
