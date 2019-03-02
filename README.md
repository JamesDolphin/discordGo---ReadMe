# discordGo---ReadMe

Actual repo is private.

How to use discordGo commands.

!help - no arguments - lists all available commands  
!broadcastrole - 1 argument - set the role which is notified during match events. eg !broadcastrole @tvrole  
!broadcastchannel - 1 argument - match status messages will appear this channel. eg !broadcastchannel #thechannel  
!adminchannel - 1 argument - channel which admin messages will appear. eg !adminchannel #adminchannel  
!startrcon - 3 arguments - start rcon functionality. eg !startrcon ip port rcon_password -> !startrcon 1.1.1.1 12345
!servers - no arguments - prints a list of all servers and their internal ID's
!delserver - 1 argument - deletes server (and removes the log address) by ID. eg !delsever 15  Can also use !delserver all to remove all servers

The following commands REQUIRE !startrcon to be used first AND correctly ---

!setlive - 2 arguments  - sets the current status to live (used when bot may be started mid game) eg. !setlive <serverid> yes/no  
!setnfl - 7 arguments - sets team names (n), flags (f) and logos (l). eg. !setnfl <serverid> ctname tname ctflag tflag ctlogo tlogo *
!hudscore - 4 arguments - sets hud series score. eg !hudscore SCOREMAX CTSCORE TSCORE -> !hudscore <serverid> 2 1 1  
!rconsend - sends string to server. eg !rconsend <serverid> sv_cheats 1


*Use _ instead of spaces in !setnfl


![alt text](https://cdn.discordapp.com/attachments/546946476836782090/546955027210829825/no_backround.png)
