# pyIRC
pyIRC is a simple to use userfriendly library for creating a very rudimentary ![InternetRelayChat](https://sv.wikipedia.org/wiki/Internet_Relay_Chat)

_Server setup Ex_:
```
>>> import pyIRC
>>> server = pyIRC.Setup(6667)
'Server setup successfull'
>>> server.StartListener()
'Listening on port 10.10.10.10:6667'
```
_Client setup Ex_:
```
>>> import pyIRC
>>> client = pyIRC.Client()
>>> client.connect("TestUsername","10.10.10.10",6667)
'Connected to 10.10.10.10:6667'
>>> print(client.get())
'Server: Hello TestUsername!'
>>> client.send("Testing testiliy test")
1
```

# Installing
Download with ![git](https://git-scm.com/).

```$ git clone https://github.com/mrikea4real/pyIRC```

In the future you will be able to install pyIRC with ![pip](https://pip.pypa.io/en/stable/).

# Documentation
__Server Side__

```Setup(port)``` - Setup server class. (Returns server class)

```ServerClass.StartListener()``` - Set the server to listen for incoming connections and data.

```ServerClass.StopListener()``` - Stop the listener. (Thread can be resumed by running the command listed above)

```ServerClass.Close()``` - Close the server and shut It down safely. (Kicks all clients and deletes server object)

```ServerClass.clients``` - Returns list of all clients connected to the server as objects.

```ServerClass.ip``` - Returns server ip. 

```ServerClass.port``` - Returns server port.

__Client Side__

```Client()``` - Setup client class. (Returns client class)

```ClientClass.Connect(UserAlias,IP,PORT)``` - Connect to server.

```ClientClass.Get()``` - Get data from the server. (Note that this function will cause delay until It gets data from the server)

```ClientClass.Send(data)``` - Send data to server. (returns 1 or a 0 deppending on result, 1 = success, 0 = failure)

```ClientClass.Close()``` - Close connection to server.

```ClientClass.alias``` - Returns client alias.

# Contributing
I happily accpet contributions. They can come in the form of bug fixes,  please send me an email or add me on discord _Mr Ikea#6576_.

# Maintainers
* @mrikea4real (Aaron Gotthardsson)
