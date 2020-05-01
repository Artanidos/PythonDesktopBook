# Part IV LOB
##Develop of a line of business application

![lob](../images/lob.png "lob")

A LOB is an application where you have got a grahical user interface and where the data is stored in a database.  
In this case we have got a database with clients and we are able to add a new client, filter the list of clients and edit the data for a client.  
We can also store a picture for each client.  

In order to run the sample app you have to install the module tinydb.  

```console
user@machine:/path$ pip3 install tinydb
```

Tinydb is a very small but usefull database implementation written in Python. You don't need a server to store the data on. And you do not need the SQL language at all. Tinydb just simply stores pythonic data in a single file.  

Because of the fact, that this app is a little bit larger then all the others that I have posted here, I do not print all the source code here. You can get the source here on github.