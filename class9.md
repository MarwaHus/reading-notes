# Class 09

### Review: High-level HTTP
1. What are the five steps in the HTTP Request Lifecycle?
   * Local Processing: The browser extracts the domain name from the URL and checks it against the cache to find the corresponding IP address. If it's not in the cache, it initiates a DNS (Domain Name System) lookup to resolve the domain name to an IP address.

   * Server Processing: The browser opens a TCP (Transmission Control Protocol) connection to the server at the corresponding IP address on the specified port number. The request is then passed to the server via this open connection.

   * Processing the Request: The server processes the request and determines the appropriate action to take. This may include retrieving a resource, running a script, or providing an error message.

   * Receiving the Response: The server sends a response back to the browser with the requested resource, error message or other information. The response may include an HTTP status code, which indicates the success or failure of the request.

   * Displaying the Response: The browser receives the response and processes it based on its type. The response may be a web page, an image, a media file, or other content. The browser then renders the response for the user to view.
2. What are the two things the client needs before it can make an HTTP Request?
   * The Uniform Resource Locator (URL) of the resource it wants to access: The URL specifies the protocol (in this case, HTTP), the domain name or IP address of the server, and the path to the resource on the server.

   * The HTTP method to use for the request: The most common HTTP methods are GET (used to retrieve data), POST (used to submit data to be processed), PUT (used to update an existing resource), DELETE (used to delete a resource), and HEAD (used to retrieve metadata about a resource). The client needs to decide which method to use depending on what it wants to accomplish.
2. Explain the four way handshake and what it does.<br>
   The "four-way handshake" is a term used to describe the process by which a client and server establish a connection and then terminate it in a reliable manner. It is used in TCP (Transmission Control Protocol), which is responsible for ensuring reliable data transmission over the internet. Here are the steps of the four-way handshake:

   *  The client sends a SYN (synchronize) packet to the server to initiate the connection. The packet contains a random sequence number and a set of TCP flags that indicate the client's intent to start a connection.

   * The server responds with a SYN/ACK (synchronize/acknowledge) packet. This packet contains a random sequence number, an acknowledgment of the client's sequence number, and a set of TCP flags that indicate that the server has received the SYN packet and is willing to establish a connection.

   * The client sends an ACK (acknowledge) packet back to the server. This packet contains an acknowledgment of the server's sequence number and a set of TCP flags that indicate that the client has received the SYN/ACK packet and is ready to start sending data.

   * The server sends another ACK packet to the client to confirm that the connection has been established. This packet contains a final acknowledgment of the client's sequence number.
   
### Java HTTP Request example

1. True or False: When making an HTTP request, you MUST follow any redirect returned by the request. Back up your answer. <br>True, When making an HTTP request, following any redirect returned by the request is a must. The server may respond with a redirect status code which indicates that the requested resource has been moved to a new URL, and failing to follow it may result in not being able to retrieve the resource. Moreover, not following redirects can cause serious security issues, such as being tricked into visiting a phishing page or a malicious website. Thus, ensuring that HTTP requests are handled securely and follow all the redirects is vital.

2. Which built-in Java class can be used to perform an HTTP request?<br>The built-in Java class that can be used to perform an HTTP request is `HttpURLConnection`. It provides methods such as `connect()`, `setRequestMethod()`, `setRequestProperty()`, and `getResponseCode()` which can be used to establish a connection to a URL, specify the HTTP request method, set request headers, and receive the HTTP response code respectively. It also provides methods to read the response from the server and handle any errors or redirects that may occur during the HTTP request.

3. What HTTP status codes represent a successful response? A redirect? A client error?<br>
-  Successful responses (200-299):
     * 200 OK: request was successful.
     * 201 Created: a new resource was successfully created.
     * 204 No Content: the request was successful, but there is no response body.
- Redirects (300-399):
     * 301 Moved Permanently: the requested resource has been permanently moved to a new URL.
    * 302 Found: the requested resource has been temporarily moved to a new URL.
- Client errors (400-499):
    * 400 Bad Request: the request was invalid or could not be understood.
    * 401 Unauthorized: authentication is required or has failed for the requested resource.
    * 404 Not Found: the requested resource could not be found on the server.