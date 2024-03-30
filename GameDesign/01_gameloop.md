# Game Loop

# Intent

I intent to keep the game fairly true to the style and feel that aims to scratch that 80s BBS dungeon crawler feel. I do want to add some more modern layers of play on top of that base.

## The 80s BBS Dungeon Crawler experience

When I was a kid we had a 8084 and a c64. I'd use them to log into BBSs. This was before there was an internet that everyone could use together. These BBSs tended to be very local, and run by the nerds who were lucky enough to have enough cash to buy systems people could use externally. This typically meant that they would have between one and a few landlines connected to a constellation of modems. You'd dial a number which would connect your computer directly to their computer, they exchange some information, and then you could do a limited set of actions on their machines. 

Usually this meant:

- Play games
- Send intra-BBS messages
- Sometimes send email externally
- WareZ

As an 8 year old, all I was really interested in were the games.

My favorite was a dungeon crawler that you'd log into every day. You would get a few actions that you were allowed to run before you were booted from the game until the next day. 

I'm sure that it was designed that way because physical resources were limited, and they wanted people to connect, do some stuff, disconnect, and allow the next person to play. The unintended side-effect was that it was immensely addictive. You had limited opportunity to do stuff and that meant that if you wanted to progress you had to be smart about how you went about it.

I'd like to reproduce that addictive quality in the game loop for Deep Dark. The scale of the game shouldn't be just daily, it should span the course of months.

## Core Loop

1. Register/login
2. Character creation
3. Home village with access to
   1. Shopkeep for food, weapons, items, etc.
   2. Dungeonforge for dungeon creation
   3. Tavern for rankings, community
   4. Gaping maw, which drops you into a random dungeon
      1. Run the story and dungeons
      2. On exit (success/death), see a stats screen and allow voting

So once the user is in the home village, they must make a smart decision about what they do. There should be no constraints on access to the shopkeep, the dungeonforge, and the tavern. There should be limits on how many runs you can make in the dungeons.

Every day that you log in, you should be granted some valuable asset like gold or food which can be traded either for equipment that you need OR for access to the dungeons. There's some critical balancing that has to happen here, and we can discuss this at length in a separate document.

We want to draw users to come into the game every day to get their free loot, and we want to get them to stay to create content and do dungeon runs.

The Dungeonforge should pay out some incentive for people to create good dungeons. This means that dungeons should be rated after each run, by the players that run them. Since runs are random, sometimes you'll get a great dungeon and sometimes you'll get a meh one. Dungeonforgers are incentivized to create content since highly rate dungeons mean that they themselves receive more loot each day that they log in.