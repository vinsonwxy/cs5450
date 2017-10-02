Brief description of implemention of lisod


Once we start the server, we perform the following tasks:

1. create a socket
2. bind socket to port
3. listen on socket

We check and ensure any of the step above is successful, otherwise we print error to the log and return EXIT_FAILURE.

Now we start looping through and waiting for input and then write it back. If there is a request from listen fd, we accept the client request. If there is a request from client connection, we call connection_handler(int sock).

connection_handler(int sock) does the following:

1. read request
2. parse method, uri and version
3. check invalidity
4. handle HEAD, GET, or POST request
