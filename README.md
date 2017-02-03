# chat-server
A simple java chat server 

1. Open a terminal window and compile the java files with: "javac ChatServer.java" and "javac ChatClient.java".

2. Run each file in a separate terminal window. For running the chat server, run "java ChatServer",
   which should generate the server port number, in the following format:

   "Server port is XXXXX" where each X is a digit(0-9).

3. Using the port number, run a chat client (Client 1) in a separate terminal window with the command:
   "java ChatClient localhost XXXXX", where "XXXXX" is the server port number from step 4. This
   should tell the client to wait for another client to "pair" with, and generate the following line:

   "Waiting for another client to pair with..."

4. From another terminal window, run another chat client (Client 2) with the same command:
   "java ChatClient localhost XXXXX", where "XXXXX" is the server port number from step 4.
   This should redirect the client to connect to the waiting client so that the chatting can begin.

5. Start chatting from the second client (Client 2) by typing a message and pressing "Enter" on the
   keyboard (pressing "Enter" marks the end of the current client's turn). Client 1 should receive 
   the message and may begin sending a message back to Client 2, who sends another message back and 
   so on. Communication must start with Client 2, then Client 1, and so on in this strict alternate 
   fashion. Each user may send at most one message at a time.

6. Either client may choose to exit the conversation by sending a message "exit" (end of stream indicator) 
   which will close the current client's connection and cause the other client to contact the server and 
   either "pair" with another waiting client, or wait for another client to "pair" with.
