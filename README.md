# MEAN Period 5

#### 2. Explain polling and long-polling strategies, their pros and cons.

Polling:
The browser sends a HTTP requests and immediately recieves a response. This is done at regular intervals. Polling is used to deliver real-time information. This is a good solution of the intervals are known, since you can synchronize to only occur when data is available on the server. Obviously real-time data is not this predictable, which results in unnecessary requests, and many opened and closed connections.

Long-Polling:
The browser sends a HTTP request to the server, and the request is kept "on hold" for a period of time. If a notification is recieved within the period, a response containing the data is sent to the client. If a notification is not recieved within the time period, the server sends a response for the request to be terimated.

#### 3. What is HTTP streaming, SSE (Server sent events)?

#### 4. What is WebSocket protocol, how is it different from HTTP communication, what advantages it has over HTTP?

#### 5. Explain what the WebSocket Protocol brings to the Web-world.

#### 6. Explain and demonstrate the process of WebSocket communication - From connecting client to server, through sending messages, to closing connection.

#### 7. What's the advantage of using libraries like Socket.IO, Sock.JS, WS, over pure WebSocket libraries in the backend and standard APIs on frontend? Which problems do they solve?

#### 8. What is Backend as a Service, Database as a Service, why would you consider using Firebase in your projects?

#### 9. Explain the pros & cons of using a Backend as a Service Provider like Firebase.

#### 10. Explain and demonstrate “three-way data binding” using Firebase and Angular

#### 11. Explain and demonstrate the difference between the simple chat system in your own WebSocket + Node.js
backend vs. Firebase.
