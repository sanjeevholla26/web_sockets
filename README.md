# Team Embedus(by Apoorva Agrawal and Sanjeev Holla S)
## ***Websockets implementation***

<br>
<br>

### **Skills we gained by doing this Project:** *(Its a better way of writing 'Prerequisites', as 'Learn while doing a Project' is better than 'Learn and then do a Project')*

<br>
1. We were introduced to the world of websockets and could apply the concepts of websockets that we researched during the course of making this project
2. We learned about various modules like asyncio, websockets, faker, logging etc that exist in python and about how vast the scope of python application in real life is
3. Increased our knowledge of how connections between client and server in real life would be happening
<br>

### ***A detailed report of the task*** :

<br>

 1. In this project we have created a server and number of clients in which two-way interactive communication between client and the server is enabled
 2. The connection between server and client is enabled by using ***websockets*** and ***async*** libraries.
 3. Once the client is connected to the server, we get random data like name, link, country etc. (in the server) using ***faker*** library and then the server sends       that data to the client.
 4. The client would receive the messages sent by the server and it will select the type of data it wants and timestamps only the selected type of messages.
 5. Then the client will wait till a particular block of data (block sizes for different clients are different) is received and then caculate the time taken to receive     that block of data and then it would Log that block into a text file using ***logging*** module of  python.
 6. Then the client would send a response back to the server ***'client <client_name> received <n> block in <t> time’***, where n has to be the sequence number of the     block that the client received and time t taken for the client to receive the entire message block. Also, the client prints that block with sequence number n is       succcessfully received.
 7. The server would receive and print all of the messages received by the various clients.
 8. The client is also having the feature of ***re-establishing the connection with the sever if server restarts for some reason*** (Here we have used error handling       via try except block)
 9. The server also has a feature of handling multiple concurrent connections such as in our code, the server is handling 8 such clients concurrently as shown in the       screenshots of the outputs and it can send and receive data efficiently to and fro all blocks with any discontinuity in data transfer with any of the clients.
 10. Also, we can see that in all our clients, the block size varies for the clients, i.e. the block size is assigned differently for different clients, and we can         also see the different result of different block sizes via observing the different time taken for each block received, as shown in the output screenshots.
 11. The client has the feature for selecting between different kind of data received from the server.
 
 <br>
 
 ### ***Instructions on how to run the files :***
 <br>
 To run the files of this repository, you have to first fork this repository into your git hub and then by using git clone command in your terminal window. Then first start the server by typing "python3 server.py". Then run the client code by typing out "python3 client1.py" in your terminal window and You can see the interactions happening between the server and the client.
 <br>
 
 ### ***Steps taken in finishing the task :***
 <br>
   Both of us collaborated via this github repository for sharing and working on the code. Sometimes we sat together and made algorithms such as that when we had to   log   data in blocks and not log individual messages and whenever we encountered a bug, we would think over how to resolve it. For all references and help, google remained   our saviour as it guided us to various documentations for various modules and showed us how we can apply and use them as per our requirrements. Finally, we compiled   all our code, produced the required output, and henceforth commited all changes to this repository.
 <br>
 
 ### ***A brief description of the modules used and why they were chosen :***
 
   In our code for server and client, we have used the asyncio, websockets, logging, time, datetime and faker modules. 
 
  While ***Asyncio and websocket*** modules were crucial to be able to establish connection and successfully run the connection between server and client, the other modules were applicable to serve various purposes. 
 
 The ***logging*** module allowed us to store the required data and consequenctly log that data in different block size of each client into it's respective data file.
 
 The  ***time*** module allowed for creating ***timestamps*** for blocks and for each individual message and through timestamps we were able to calculate the time taken by the client to receive each block.
    
The ***datetime*** module was just used to get the current date and time at which each message was received by the client from the server.
    
   The ***faker*** module was used for generating various random data such as name, country, city etc. which was sent from server to client and which was also logged in blocks in the respective client's data file.
    
 
 # ***Screenshots of outputs of program execution :***




