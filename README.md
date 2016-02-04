# socket-rusher
Optimized version of Goodstuff's Diablo 2 Rusher. [*Link to Goodstuff's repo*](https://github.com/goodstuff-/test)

## Key changes

* Fixed harem bug - leechers and leader while approaching Jerhyn could go accidently to harem and stay there. Now rusherwill call them when it happens.
* Deleted unnecessary TownManager function calls  in rusher script. It's freed up few minutes per run.
* Made rusher wait for other bots to join the game before doing Andy. It deals with often delays between bots.
* Rusher now checks that leader is in expected act before running each quest script.
* Fixed leechers' problem with joining old games. Now leechers can join games only when leader allows it.
* Ensured that leechers change their character mac once per run.
* Improved few interactions sctipts by doubling amount of approaches npcs.
* Fix a4 travelling error. Leader instead of creating new game joins previous one.

## New ntj files

* AccCreator - bot based on the code from Auromule script. It creates (or logs in) an account and makes 8 characters one by one.
* Gamer - bot based on Goodstuff's RusherLeader script. It simply creates a game and stays there allowing other bots to join it.
* Checker - bot based on Goodstuff's RusherLeader script. It logs in to an account and join gamer's game with every character in the acc, one by one. In game it checks if given character made socket quest correctly. Then it sends output to the manager.
