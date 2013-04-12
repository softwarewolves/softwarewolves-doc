Werewolves
==========

The game
--------

The game follows a night and day cycle. 
* At night, the wolves pick a villager to kill, while everyone else "sleeps". 
* During the day, the villagers wake up and discover that one of them has died, so they will discuss who might be the werewolf. The villagers lynch their guess, hoping it's a wolf. The villagers win if they kill all the wolves; the wolves win if there are the same number of them as villagers.

The following roles can be distinguished:
* Villager – The villager is the simplest role. In the daytime, you vote on who to kill. You try to narrow down who the wolf(s) is/are. 
* Werewolf – The wolf kills one of the villagers during the night. During the day, the Werewolf acts a villager trying to avoid suspicion. 


Starting a game
---------------

* To start a game, you need to send the following chatmessage to the Game Coordinator (Jabber Id "sww@jabber.org" or "sww@localserver"). The Game Coordinator will react by dispatching you to a chatroom.

        I want to play 
    

* To  indicate you are a candidate to play the werewolf role, send the following _private_ chatmessage to the Master of Ceremonies of the chatroom (Jabber Id "softwarewolf"). Any string containing werewolf will work. The MC will only take into account requests until the game starts.

        werewolf
  
Playing the game
----------------

* During the night, werewolves can use send the following _private_ message to the MC to choose which player to eat:

        I eat <playername>
        
* During the day, a villager can cast a vote to hang the player suspected of being a werewolf by sending the following chatroom message. The player with the majority vote will be lynched. 

        I vote for <playername> 

Narrator output
---------------

The MC outputs information in the chatroom as the game progresses.

Night and day last for a particular time period. To inform all players when the switch between night and day occurs, the MC changes the chatroom subject to _Night_ or _Day_. 
