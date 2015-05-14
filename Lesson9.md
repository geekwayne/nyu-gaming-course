# Lesson plan #
  * 30 min: [Presentation](http://www2.kbs.uni-hannover.de/fileadmin/institut/pdf/ki1/lecture/chapter06.pdf): Minmax search, alpha-beta pruning, heuristics (evaluation of states and ordering of moves)
  * 5 min: [Optimal decision tree for player X](http://upload.wikimedia.org/wikipedia/commons/d/de/Tictactoe-X.svg) or [XKCD version](http://xkcd.com/832/)
  * 5 min: [XKCD AI](http://www.xkcd.com/1002/) and [Solved games](http://en.wikipedia.org/wiki/Solved_game)
  * 20 min: Explain [HW9](HW9.md), go over [AlphaBetaPruning.java](http://code.google.com/p/gaming-platform/source/browse/trunk/eclipse/gaming-platform/src/org/gaming/shared/games/ai/AlphaBetaPruning.java)

Recorded talks:
  * [Intro and HW](https://www.youtube.com/watch?v=CN5x4pPLtSw) (3 minutes)
  * [Slides](https://www.youtube.com/watch?v=taJdXE0tfBw) (41 minutes)
  * [XKCD](http://youtu.be/d536XU5kZV4) (5 minutes)

# Links #
  * [Minimax search](http://en.wikipedia.org/wiki/Minimax)
  * [Alpha beta pruning](http://en.wikipedia.org/wiki/Alpha-beta_pruning)
  * Neural networks in [Backgammon](http://en.wikipedia.org/wiki/Backgammon#Software) and in [general](http://en.wikipedia.org/wiki/Neural_network)
  * Other AI techniques: [Genetic algorithms](http://en.wikipedia.org/wiki/Genetic_algorithm)
  * [Doubline in backgammon](http://xfriis.dk/maxfriis/bg/double.html)
  * [Chess](http://kom.aau.dk/~zt/cources/Readings_in_Advanced_Intellimedia/ai_chess_alexandre_gimenez.pdf) - openings and end-game positions.
  * [Monte Carlo methods for poker](http://dendiz.com/blog/wp-content/uploads/2010/06/swe555-dizman-research-report.pdf) and bridge, [poker bots in Java](http://www.ke.tu-darmstadt.de/resources/poker)


## Connect 4 heuristic ##
  1. Odd square: is a square belonging to an odd row (1,3,5)
  1. Even square: is a square belonging to an even row (2,4,6)
  1. Threats: A threat is a group of three tokens of the same color which has the fourth square empty and also the square below the empty square is empty
  1. Odd threat: is a threat in which the empty square is odd
  1. Even threat: is a threat in which the empty square is even
  1. If red (moves first) has an odd threat and black cannot connect four tokens anywhere else red will win.
  1. If black (moves second) has an even threat and black cannot connect four tokens anywhere else black will win.
  1. At the beginning of the game it is advantageous to place tokens in the central columns.