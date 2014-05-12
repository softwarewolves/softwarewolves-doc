After the introduction of the organizers, follow the following steps to get started:

## 1. XMPP server

Ensure you have a connection to the xmpp server. Actually, there are several choices:
   * When you are located in the werewolves room, we have a completly independent setup to limit the dependence on the conference wireless. You can connect to the *awtest* wireless network. Password is *prodata123*. The server is pi.software.wolf. 
   * You can also make use of the conference wifi and use a publicaly available server: softwarewolves.org

    $ ping pi.software.wolf
    $ ping softwarewolves.org
  

## 2. Get XMPP accounts

  Make sure you have received 2 accounts for the XMPP server from the organizers. 
  
  One of these is for use by your bot, the other can be used to manually interact with the game and view the activity.
  
  Test them in your xmpp client.
   
## 3. Manually play the game   
A good way to make sure you understand how the game works is to walk through the manual test procedure - see [Acceptance procedure.md](Acceptance procedure.md)

Example clients for manual tests are Pidgin or Adium for Mac. 

## 4. Technology

Choose the technology stack you want to use in this coding contest. 
There are basic bots available for 
  * [*node.js*](https://github.com/JohanPeeters/softwarewolves-nodejs-player)
  * [*C#*](https://github.com/supernelis/softwarewolves-dotnet-player)
  * [*Ruby*](https://github.com/rwestgeest/sww)
  * [*Java*](https://github.com/supernelis/softwarewolves-java-player)
  * [*Scala*](https://github.com/JohanPeeters/basic-softwarewolves-Scala-bot.git)

  But you can also choose to build a bot from the ground up.
  
## 5. Adapt the configuration 

Make sure that your bot uses one of the accounts *you received* on the *correct server*, i.e. on *pi.software.wolf* or *softwarewolves.org*.
