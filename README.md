# PrimeQueryClientServerSocket
Java Application to Design Client Server Application For Prime Number Query Using Socket and Multithreading

**Project Description**
**Prime Number Check**
Design Server-side code that opens a socket connection on the localhost. The port number for the server should be read from the command line. The server-code should accept connections on the socket. Each connection should be handled by a new thread. This ServerWorker thread should read the following from the socket: the client name and an integer value. The server should check if the integer value is greater than a threshold "THRESHOLD". The "THRESHOLD" value should be defined as a constant, 3, in the Server code. The client input could be in the following format, or any other format that you choose:
**< primeQuery>< clientName>Bill< /clientName>< isPrime>17< /isPrime>< /primeQuery>**
The server side should use a class named CheckPrime with a method that determines if a given interger is prime.
The server should respond back to the client with either of these messages:
**< primeQueryResponse>< intValue>17< /intValue>< isPrime>Yes< /isPrime>< /primeQueryResponse>**
**or
< primeQueryResponse>< intValue>3558< /intValue>< isPrime>No < /isPrime>< /primeQueryResponse>
or
< primeQueryResponse>< intValue>2< /intValue>< isPrime>Invalid < /isPrime>< /primeQueryResponse>**


[Note: You need not have whitespaces as shown above. Response should be "Invalid" if the input is below the threshold.]

The server side should define a class named, AllPrimeQueries, that has a data structure that stores all the client names and values that were queries.
The server side should have a text-based menu that allows provides the following options:
**[1] Client Name [print the name and query integer]
[2] All Client Queries [print all names and queries so far]
[3] Quit [quit the server]**
The server side menu is just to view the requests that have been received so far. The CheckPrime class should have a method to take an int parameter and return a String. The server menu does not ask the user to determine if the client input is prime or not.
If a client sends multiple requests, then all the name-value pairs can be printed in this way
**johnDoe 13 17 19**
If the server quits, all connected clients should catch the exception and quit too.
Design Client-side code that opens a socket connection to a port and host. The port and host should be read from the command line. The client should also be driven by a text-based menu for
**[1] Set client name
[2] Enter number to query for prime
[3] What is the server response?
[4] Quit**
Assume that the client will always use #1 before #2. It should be possible to keep using option #1 to change the client name. When #2 is chosen, the latest client name should be used. Also, assume the choices are always selected correctly, and in the right order. For example, the client will not select #2 twice.
The server response on the prime number will be printed when the option #3 is chosen.
The PrimeDriver has the main function. It calls ClientDriver or ServerDriver depending on the command line argument.
The server needs 1 argument, which is the port. The client needs 2 args, which are the port and host name (or IP address). In addition, you need a debug value. So, PrimeDriver should be written to accept the correct number of arguments depending on whether you are starting the client side or server side.
Debug
Define a Singleton Debug class and design your own scheme for what to print for different debug values.
