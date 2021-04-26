### HW 11: HTTP server

You need to create an HTTP server that handles HTTP requests and returns responses. \
Complete API description can be found in the next paragraph. \
Your server should be able to accept multiple clients at the same time (i.e. you should use `epoll` for this h/w). \
The server should act like a controller of the files in the `contents` directory.
Also, you should add the `Server` header in order to tell the sender the name of the server.

### API Description

#### GET /file_name:
Returns contents of the file in the `contents` folder if the file exists, otherwise – `404` error.

##### Example 1
+ Request: `GET /file.txt HTTP/1.1`
+ Response:
```
HTTP/1.1 404 Not Found
Server: caos_hw11_server
```
##### Example 2
+ Request: `GET /text.txt HTTP/1.1`
+ Response:
```
HTTP/1.1 200 OK
Server: caos_hw11_server

A. Conan Doyle (18591930)With the words "Elementary, my dear Watson ...",
the most famous detective of all time, Sherlock Holmes, starts to explain a
crime to his friend, Dr. Watson. That phrase has now entered the English language.
Sherlock Holmes first appeared in a book called 'Study in Scarlet'.
He became famous in 'The Adventu...
```

#### POST /file_name:
Creates new file in the `contents` folder if there is no file with the same name yet, returs `409` error otherwise.

##### Example 1
+ Request:
```
POST /text.txt HTTP/1.1
Content-Type: text/plain
Content-Length: 12

Hello world!
```
+ Response:
```
HTTP/1.1 409 Conflict
Server: caos_hw11_server
```


##### Example 2
+ Request:
```
POST /file.txt HTTP/1.1
Content-Type: text/plain
Content-Length: 31

Hello world!
How are you doing?
```
+ Response:
```
HTTP/1.1 200 OK
Server: caos_hw11_server
```

#### How to pass?
You need to send me the `server.c` file and (optionally) `client.c` in order to pass the h/w.

#### Deadline:
May 10, 23:59:59

#### Points:
This task costs 18pts
