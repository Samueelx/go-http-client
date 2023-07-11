# HTTP CLIENT
HTTP is a sessionless client-server protocol in which the client initiates a request to the server and the server responds to the client.

HTTP is an application layer protocol and serves as the foundation for communication over the web. It uses TCP as its underlying transport layer protocol.

An *HTTP Request* is a message sent from a client to a web server that asks the server to respond with a specific resource. The request consists of a *method*, *target resource*, *headers* and a *body*. The method tells the server what you want it to do with the target resource.

*Request headers* contain metadata about the content of the request you are sending. The *request body* is the payload of the request. If you upload a new profile picture to a web server, the request body will contain the image encoded in a format suitable for transport over the network, and the Content-Length header’s value will be set to the size in bytes of the image in the request body.

Using Go's `net/http` library, you can create a request with nothing but an HTTP method and a URL. This package contains constants of the common [RFC 7231](https://www.rfc-editor.org/rfc/rfc7231) and [RFC 5789](https://www.rfc-editor.org/rfc/rfc5789) request methods.

Just like your web browser, Go can communicate with web servers by using the `net/http` package’s HTTP client. You could use Go to scrape data from websites (such as financial stock details), submit form data, or interact with APIs that use HTTP for their application protocol, to name a few examples.

## Using Go’s Default HTTP Client

The `net/http` package includes a default client that allows you to make one-off HTTP requests. 
- You can use the `http.Get` function to send a *GET* request to a given URL. 