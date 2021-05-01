
This Reository contains code for the Data communication and Computer Network Protocol Implementation

Steps to run Project:
	1. Run Server.java  ( Run on Port 8888 ) 
	2. Run HttpClient.java ( To handle HTTP client request)
	3. FTP_Client.java ( To handle FTP client request )


1. Implement HTTP server library

	To Get with query parameters : httpc get 'http://localhost:8888/get?'
	To Get with verbose option   : httpc get -v 'http://localhost:8888/get?course=networking&assignment=1'  
	Post :   httpc post http://localhost: 8888/post? 
	To Post with inline data : httpc post -h Content-Type:application/json -d '{"Assignment":1}' http://localhost:8888/post?
	To Support –o option: httpc get -v 'http://localhost:8888/get?course=networking&assignment=1' -o hello.txt

2. Implement GET /  :   httpfs get/  http://localhost:8888/get?

3. Implement GET /filename:  httpfs get/one.java  http://localhost:8083/get?

4. Implement POST /filename:  httpfs post/helo.txt http://localhost:8889/post?

5.6.  HTTP/1.1 404 FILE NOT FOUND  error message

7. Concurrent Requests: Multiple client can read but can not write at same time.

8. Content-Type and Content-Disposition: 
	
	1. httpfs get/one -h Content-Type:java http://localhost:8081/get
	2. httpfs get/one -h Content-Type:java -h Content-Disposition:inline http://localhost:8081/get
	3. httpfs get/one -h Content-Type:java -h Content-Disposition:attachment http://localhost:8081/get
	
	