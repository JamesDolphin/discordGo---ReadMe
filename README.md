## DiscordGo

DiscordGo is a live production and online league adminstrator discord bot used to streamline the running of CS:GO events specifically using the ESEA platform. The bot can be configured to provide real time status updates directly from a csgo server or simply notify users when a match is complete. The actual repoistory is private.

![alt text](https://cdn.discordapp.com/attachments/546946476836782090/546955027210829825/no_backround.png)

- **GENERAL USERS SHOULD NOT HAVE THE ABILITY TO TYPE IN CHANNELS THE BOT CAN READ** 
- **SET UP YOUR SERVER PERMISSIONS CAREFULLY**

- !help - no arguments - sends you here!

- !broadcastrole - 1 argument - set the role which is notified during match events. eg !broadcastrole @tvrole  
    >The broadcastrole is the role tagged in some broadcastchannel messages

- !broadcastchannel - 1 argument - match status messages will appear this channel. eg !broadcastchannel #thechannel  
    >The broadcastchannel is used for match notifications including match live, pauses and match end

- !gamechannel - 1 argument - end of match postings will appear in this channel eg !gamechannel #thechannel  
     
- !adminchannel - 1 argument - channel which admin messages will appear. eg !adminchannel #adminchannel  
    >The adminchannel is used for printing the server list and displaying player disconnects  
    
- !chatchannel - 1 argument - channel which chat messages will appear. eg !chatchannel #chatchannel  
   
- !servers - no arguments - prints a list of all servers and their internal ID's  
    >Will list IP and port, current team names playing (can be undefined) and if rcon sending is available.    

- !delserver - 1 argument - deletes server (and removes the log address) by ID. eg !delsever 15. Can also use !delserver all  
    >Server ID's can be found using the !servers command  
 
- !usechat - 2 arguments - displays chat of server (only 1 server at a time) in the !chatchannel eg !usechat serverid yes/no  

- !rconpass - 1 argument - sets the global rconpassword for all upcoming server additions eg !rconpassword goodpassword  

 ### The following commands REQUIRE !startrcon to be used first AND correctly ---  

- !startrcon - x arguments - start rcon functionality. eg !startrcon ip1:port1 ip2:port2 ip3:port3 -> !startrcon 1.1.1.1:12345  
    >startrcon will take any number of IP's and start a log connection using the rcon password stored in your .env file.  

- !setlive - 2 arguments  - sets the current status to live (used when bot may be started mid game) eg. !setlive serverid yes/no   
    >If the game is not currently "live" then no notifications will be sent from it (match end postings will continue)    
    >Games are automatically set live if the bot is watching at the start of the map (live = true on the real life start of game)  
    
 - !notif - 2 arguments  - sets the notifications to on or off eg. !notifications serverid yes/no  
    >Notifications refer to broadcast role notifications (live, pause, end match)
    
 - !usercon serverid yes  
    >Enables the command below  

- !setnfl - 7 arguments - sets team names (n), flags (f) and logos (l). eg. !setnfl serverid NiP Astralis SE DK nip_logo ast_logo  
    >Logo names aka nip_logo and ast_logo need to be matches to the observer PC's naming convention.    
    >***Use _ instead of spaces in !setnfl***  !setnfl serverid Team_NiP Team_Astralis SE DK nip_logo ast_logo  

- !hudscore - 4 arguments - sets hud series score. eg !hudscore SCOREMAX CTSCORE TSCORE -> !hudscore serverid 2 1 1  
    >!hudscore serverid 2 1 1 will set the series to a bo3 scoring system with the CT on 1 and the T on 1  

- !rconsend - sends string to server. eg !rconsend serverid sv_cheats 1  
    >sends all text following the serverid. !rconsend 13 mp_pause_match; say The match has been paused  


