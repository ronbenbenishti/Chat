# Python Chat 1.2v (beta) #

The following code was written as a home project as part of a Cyber and Information Security course at HackerU College.
The following code contains:
* Server side (Host) – CLI
*	User side (Client) - GUI

The code uses a socket library to establish a connection between the server side and the client side by using the TCP protocol.
# Features #
* **The user can choose a nickname** that will be displayed to the other chat members when he sends a message
* **The ping button** is used to check for proper communication with the server
* **The Who is here? button:** Because the client does not have a user list, you can click this button to check which chat 
members are connected to the server.
The client side that receives the user list call, responds by sending his username to the other members of the chat.
* **File encryption:** You can encrypt (when you send a message) and decrypt (when you receive a message) by using a private key shared by both sides of the client.
If a third user enters the server and does not share the key of the current users, he will not be able to view their messages.
You can disable or allow the encryption of the message at any time (default is enabled)
* **File traffic:** You can share a file with other chat members. The beta version allows sending files only from the client side to the server side. (Network traffic encryption not yet supported)
You can open received folder by clicking the _‘Received folder’_ button.
Client-side can disable the auto receiving files.
* **Settings file:** Users settings (Server, port, nickname, key, and buffer) will be saved in _'settings.txt'_ when the user sets the value in the fields.
If the settings file will be deleted, default settings will be loaded to a new file.
* **Logs:** All the messages automatically logged by client side to a file named _'logs\%d-%m-%Y.txt'_
You can delete the log file by clicking _'Delete'_ button.
* **MOTD:** (a welcome message) is located in _‘motd.txt’_ file (server side).
* **Highlight:** All messages that include client’s own username, will highlight in blue color.

![Image](https://raw.githubusercontent.com/ronbenbenishti/Python-based-Chat/master/screenshots/pic-client.png)

![Image](https://raw.githubusercontent.com/ronbenbenishti/Python-based-Chat/master/screenshots/pic-server.png)

# Getting Started #
## Prerequisites: ##
* **Python 2.7**
* **Modules in use**:
  * Thread
  * select
  * Queue
  * argparse
  * random
  * socket
  * Tkinter
  * tkFileDialog
  * tkMessageBox
  * signal
  * cs_Freeze

## Installing ##
```sh
git clone https://github.com/ronbenbenishti/Python-based-Chat.git
```

# How to use #
### Server Side: ###

```sh
chmod +x server.py
./server –-ip <SERVER_IP> --port <SERVER_PORT>
```

### Client Side: ###
#### Executable ####

```sh
chmod +x setup.py
./setup build_exe
```
All the relevant files will appear in _‘\build\exe.win-amd64-2.7\’_
Run _‘client.exe’_
After running, python and modules requirements are not relevant for the client side.

#### Python ####
```sh
chmod +x client.py
./client
```
# Acknowledgments #
* Daniel Oz
* Stackoverflow
* Python 2.7 Official Documentation
