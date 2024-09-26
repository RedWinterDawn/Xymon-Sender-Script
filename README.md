# Xymon-Sender-Script
Perl script allows you to send messages to a Xymon (formerly Hobbit) monitoring server. It provides a simple way to interact with Xymon from the command line or other scripts.
Features

Sends messages to a specified Xymon server
Supports custom port specification
Handles connection errors gracefully
Prints server responses

Usage
Copy./xymon_sender.pl <host> [<port>] <message>

<host>: The Xymon server hostname or IP address
<port>: (Optional) The port number (default is 1984)
<message>: The message to send to the Xymon server

If you don't specify a port, the script will use the default Xymon port (1984).
Example
Copy./xymon_sender.pl xymon.example.com "status host.example.com.cpu green CPU OK"
Requirements

Perl
IO::Socket module

How it works

The script establishes a TCP connection to the specified Xymon server.
It sends the provided message to the server.
It then waits for and prints any responses from the server.
Finally, it closes the connection.

Error Handling
If the script cannot create a socket connection, it will die with an error message.
