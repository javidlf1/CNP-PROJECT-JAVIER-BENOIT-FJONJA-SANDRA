README FROM THE GROUP: BENOIT TROUILLEZ, JAVIER DE LA FUENTE, FJONJA KECI, SANDRA HILLERGREN


--------------------------------------- LIBRARIES AND IMPORTS --------------------------------------
The libraries and imports part is given at the end of this README


---------------------------------------- COMPATIBLITY ISSUES ---------------------------------------
NONE


-------------------------------------- TO RUN THE APPLICATION --------------------------------------
First run ServerRun.java (to instantiate a server)
Then, for each new user, you should run ClientRun.java (to instantiate ONE client) 


When running a client, some instructions will appear, it explained the different things the user can do during its use of the application :

"
First, you must SIGN UP or LOGIN. Follow the steps ...

When you are logged in, you can use all the following commands :
USERS : to know all the connected users.
HISTORY username : loads all the conversation you had with the user USERNAME before.
TALK username : starts (or continue) a conversation with USERNAME (if he is connected).
EXIT : makes you leave the current conversation. You can then go back to another one (or the same one) using 'talkTo USERNAME' again.
FRIENDS : to know all your friends (i.e. the users you already talked with and are not blocked).
PASSWORD : if you want to change your password.
BLOCK username : blocks a user, impossible to you to receive any message from him until you unblock him.
UNBLOCK username : unblocks a user.
QUIT : disconnects you from the server.

"

/!\ NOTE THAT TO RUN COMMANDS MENTIONED ABOVE, YOU SHOULD WRITE THEM CORRECTLY (upper letters included !) /!\ (for example "talk username" can not work => you should use "TALK username")


------------------------------------------------ FEATURES -----------------------------------------------
The features are the following ones :
- Sign in or login
- Conversation between 2 users
- A client can get all the connected users
- A client can get the friends list 
- A client can get the history of a conversation with another client
- A client can change the password
- A client can block and unblock users
- A client can receive notifications

To use some of thos features, look at the section "TO RUN THE APPLICATION" where some commands are given.


---------------------------------------- ACCESS TO THE DATABASES ----------------------------------------
Simply check the following folders : 
- databaseClients, where blacklists and symmetric keys are stored
- databaseServer, where conversations are encrypted in one folder, and in the other there is information about the users
(connexion status and list of signed up users)




-----------------------------------------------------------------------------------------------------------------




--------------------------------------- LIBRARIES AND IMPORTS --------------------------------------

COMPATIBLITY ISSUES: NONE






LIBRAIRIES:   

NO LIBRAIRIES USED


IMPORTS:

CLIENT CLASS:

package model;

import javax.crypto.*;
import javax.crypto.spec.SecretKeySpec;
import java.io.*;
import java.net.Socket;
import java.nio.file.Files;
import java.nio.file.Path;
import java.security.*;
import java.security.spec.InvalidKeySpecException;
import java.security.spec.X509EncodedKeySpec;
import java.util.Base64;
import java.util.Objects;


SERVER CLASS:

package model;

import java.io.*;
import java.net.ServerSocket;
import java.net.Socket;
import java.nio.charset.StandardCharsets;
import java.nio.file.Files;
import java.nio.file.Path;
import java.security.SecureRandom;
import java.sql.Timestamp;
import java.text.SimpleDateFormat;
import java.util.ArrayList;
import java.util.Collections;
import java.util.Date;

import static java.lang.Thread.currentThread;

CLIENTRUN CLASS:

import java.io.IOException;
import model.Client;

SERVERRUN CLASS:

import java.io.IOException;
import model.Server;
