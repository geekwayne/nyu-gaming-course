AI: support playing against the computer. You can copy the [alpha-beta search algorithm](https://code.google.com/p/gaming-platform/source/browse/trunk/eclipse/gaming-platform/src/org/gaming/shared/games/ai/AlphaBetaPruning.java), and you need to use it with a heuristic for your game.
If your game doesn't fit the AI framework, then just have an opponent that plays randomly.
In any case, you should have a single player version of your game.

The AI is a pure GWT client-side change (you don't need to make any server-side changes).
There is also no need to save the single player games.