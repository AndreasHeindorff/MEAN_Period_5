# MEAN Period 5

#### 2. Explain polling and long-polling strategies, their pros and cons.

Polling:
The browser sends a HTTP requests and immediately recieves a response. This is done at regular intervals. Polling is used to deliver real-time information. This is a good solution of the intervals are known, since you can synchronize to only occur when data is available on the server. Obviously real-time data is not this predictable, which results in unnecessary requests, and many opened and closed connections.

Long-Polling:
The browser sends a HTTP request to the server, and the request is kept "on hold" for a period of time. If a notification is recieved within the period, a response containing the data is sent to the client. If a notification is not recieved within the time period, the server sends a response for the request to be terimated.

#### 3. What is HTTP streaming, SSE (Server sent events)?

Streaming is when the browser sends a request, but the server sends and maintains an open response, which is updated and kept open for a defined period of time. The response is updated whenever a message is ready to be sent. The server never requests to finish the response, resulting in the connection being kept open to deliver future messages. A major downside of Streaming is that it includes HTTP headers, which increases data and file size, thus increasing delay.

#### 4. What is WebSocket protocol, how is it different from HTTP communication, what advantages it has over HTTP?

All of the above mentioned methods include HTTP requests and response headers. These contain alot of extra header data, which will increase latency. Full-duplex connectivity requires more than the downstream connection from the server to the client. To simulate full-duplex communication over half-duplex HTTP, most of the solutions use 2 connections: 1 for downstream and 1 for upstream. Having 2 streams increases the amount of recourses needed and adds complexity. Because of this, HTTP is a poor solution for real-time communication.

HTML5 Web Sockets, however, introduces a full-duplex, bidirectional communication channel that operates on a single socket. HTML5 web sockets introduce a standard used to build scalable real-time web apps, and removes the overhead and reduces complexity.

#### 5. Explain what the WebSocket Protocol brings to the Web-world.

Above questions explain most of it, but instead of having to refresh pages manually to get up-to-date "real-time" information, websockets provide "automatic" real-time information on web applications.

#### 6. Explain and demonstrate the process of WebSocket communication - From connecting client to server, through sending messages, to closing connection.

By accessing the different sockets defined in the source code, you can accomplish things  such as connection to a server or sending messages. In my example, I have "defined" a bunch of sockets when a user connects to server.
While the user is conencted, he/she can access the other sockets such as sending a message, or creating a username.
These sockets are accessed by interacting with DOM elements on the HTML page, which are defined in the corrosponding JavaScript file.
When the user interacts with the DOM element, a function from the Javascript code is called, which uses "socket.emit("socketname", data)", in order to access the sockets.

Example: https://github.com/AndreasHeindorff/MEANPeriod5Chat

#### 7. What's the advantage of using libraries like Socket.IO, Sock.JS, WS, over pure WebSocket libraries in the backend and standard APIs on frontend? Which problems do they solve?

#### 8. What is Backend as a Service, Database as a Service, why would you consider using Firebase in your projects?

#### 9. Explain the pros & cons of using a Backend as a Service Provider like Firebase.

#### 10. Explain and demonstrate “three-way data binding” using Firebase and Angular

#### 11. Explain and demonstrate the difference between the simple chat system in your own WebSocket + Node.js backend vs. Firebase.
