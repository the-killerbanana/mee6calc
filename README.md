# mee6calc _(For [mee6.xyz](https://mee6.xyz)-powered servers)_
![screenshot](http://i.imgur.com/nHu5NZF.png)
Calculate how many more messages you need to send (for every minute) in order to reach a specific level!

### Usage
1. Send `!rank` in a server where a Mee6 bot is present.
1. Get your TOTAL XP (example output: ` LEVEL 14 | XP 766/1780 | TOTAL XP 10811 | Rank 21/1089`)
    - Note that the total XP will be one message behind due to mee6 not accounting for the `!rank` message.  If you are in the top 100 of the server, use `!levels` and check it on the leaderboard
1. Go to mee6calc
1. Enter the level you want to reach
1. Enter your total XP
1. Press _Calculate_

### But how does it work...?
The leveling system follows a pattern, which can be explained with this mathematical function: ![function](https://latex.codecogs.com/gif.latex?f(x)%20%3D%20\frac{5}{6}x(2x^2%20&plus;%2027x%20&plus;%2091)), where `x` is the level desired, and `f(x)` is the XP required for specified level. Subtract your current XP from the required XP, and what is left is how much more is needed until that level is reached. Since every message (per minute) gives [between 15 and 25 XP](https://github.com/cookkkie/mee6/blob/5da379573c06eddec8ffad455c5b10681da429c3/chat-bot/plugins/levels.py#L173), it is averaged to about 20 XP per message.

##### Disclaimer
I am not part of the [mee6.xyz](https://mee6.xyz) development team. This project is entirely made for fun.
