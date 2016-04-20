# MEAN Period 5

#### 2. Explain polling and long-polling strategies, their pros and cons.

Polling:
The browser sends a HTTP requests and immediately recieves a response. This is done at regular intervals. Polling is used to deliver real-time information. This is a good solution of the intervals are known, since you can synchronize to only occur when data is available on the server. Obviously real-time data is not this predictable, which results in unnecessary requests, and many opened and closed connections.

Long-Polling:
The browser sends a HTTP request to the server, and the request is kept "on hold" for a period of time. If a notification is recieved within the period, a response containing the data is sent to the client. If a notification is not recieved within the time period, the server sends a response for the request to be terimated.

#### 3. What is HTTP streaming, SSE (Server sent events)?
