# Remote-python-debug
## Transmit Python message prints remotely to a terminal server

Two files are provided:

server.py - The remote terminal server which will receive the messages to print from the client and print them.

client.py - The client code to be embedded in the Python app, in order to either print messages locally on the local terminal or send them remotely to the remote terminal

Setting up the remote terminal server:
1. Edit the server.py file and set the 'host' parameter to the machine IP which will run the terminal server
2. Open a command terminal, go to the folder containing server.py and execute using 'python server.py'

Setting up the client code:
1. Add the client.py code to your project
2. showStatusMsg() replaces print() and supports both local and remote message print
3. Set 'terminal_server_ip' to the IP of the remote PC running the terminal server
4. Set 'send_msg_via_socket' to True/False. False = print locally using the standard print(). True = send messages to the remote terminal server
5. In any place that you inserted print() debug printing and would like to have the option to send the messages remotely to the terminal server, replace print() with showStatusMsg(). In case your print() includes more than one parameter such as print(i, j), replace it with showStatusMsg(f'{i} {j}')

Please let me know if you have any comment, issue, enhancement suggestion, etc.

ENJOY :-)
