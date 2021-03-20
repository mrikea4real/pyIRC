# pyIRC
pyIRC is a _userfriendly_ TCP client and server for creating your own internet relay chat system.

_Server setup Ex_:
```
>>> import pyIRC
>>> server = pyIRC.SimpleSetup(6667)
'Server setup successfull'
>>> server.StartListener()
'Listening on port 10.10.10.10:6667'
```
_Client setup Ex_:
```
>>> import pyIRC
>>> client = pyIRC.SimpleClient()
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

```SimpleSetup(port)``` - Setup server class

```ServerClass.StartListener()``` - Set the server to listen for incoming connections and data

```ServerClass.StopSistener()``` - Stop the listener. (Thread can be resumed by running the command listed above)

```ServerClass.Close()``` - Close the server and shut It down safely.


__Client Side__

```SimpleClient()``` - Setup client class

```ClientClass.Connect(UserAlias,IP,PORT)``` - Connect to server with TCP Protocol.

```ClientClass.Get()``` - Get data from the server. (Note that this function will delay until It gets data from the server)

```ClientClass.Send(data)``` - Send data to server. (returns 1 or a 0 deppending on result, 1 = success, 0 = failure)

```ClientClass.Close``` - Close connection to server.

# Contributing
I happily accpet contributions. They can come in the form of bug fixes,  Please send me an email or add me on discord _Mr Ikea#6576_.

# Maintainers
* @mrikea4real (Aaron Gotthardsson)
