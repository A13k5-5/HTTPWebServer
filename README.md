## HTTP web server in Rust

This is a simple HTTP web server implemented in Rust.

It listens on port 7878 and serves  files 404.html and hello.html.

### How it works
1. A TCP listener is created on the specified address and port.
2. The server uses a thread pool of 4 threads to concurrently handle incoming connections.
3. For each incoming connection, the server reads the HTTP request and determines the requested path.
4. If the requested path is "/" or "/hello", the server responds with the contents of hello.html and a 200 OK status.
5. If the requested path is anything else, the server responds with the contents of 404.html and a 404 Not Found status.