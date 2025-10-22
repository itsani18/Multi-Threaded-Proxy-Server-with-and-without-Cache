This project is implemented using C and Parsing of HTTP referred from Proxy Server.



How to Run:

$ git clone https://github.com/itsani18/Multi-Threaded-Proxy-Server-with-and-without-Cache.git

$ cd Multi-Threaded-Proxy-Server-with-and-without-Cache

$ make all

$ ./proxy <port no.>




Note:

This code can only be run in Linux Machine. Please disable your browser cache.
To run the proxy without cache Change the name of the file (proxy_server_with_cache.c to proxy_server_without_cache.c) MakeFile.


Observation:

When website is opened for the first time (url not found) then cache will be miss.
Then if you again open that website again then Data is retrieved from the cache will be printed.


How did we implement Multi-threading?

Used Semaphore instead of Condition Variables and pthread_join() and pthread_exit() function.
pthread_join() requires us to pass the thread id of the the thread to wait for.
Semaphore’s sem_wait() and sem_post() doesn’t need any parameter. So it is a better option.



Motivation/Need of Project:

To Understand →
The working of requests from our local computer to the server.
The handling of multiple client requests from various clients.
Locking procedure for concurrency.
The concept of cache and its different functions that might be used by browsers.
