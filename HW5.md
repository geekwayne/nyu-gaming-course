## Group HW ##
Submit version 2.

## Individual HW ##
### Part A: Use an emulator to test your game ###
The GWT emulator team built an awesome emulator, and you all need to convert your game to use `postMessage` and test your game on [GWT emulator site](http://smg-gwt-emulator.appspot.com/).
I converted my cheat game (it only takes 10 minutes), and you can test it in the emulator by going to [emulator](http://smg-gwt-emulator.appspot.com/GwtEmulator.html) and putting in my cheat URL: `http://2-dot-cheat-game.appspot.com/CheatGame.html`.

Follow these instructions:
  1. Include the following line in your GWT xml file:
```
  <add-linker name='xsiframe' />
  <inherits name='com.google.gwt.json.JSON'/>
```
  1. Move your GWT xml file to the `org` directory. We have to do it because I move `GameApi.java` to a common package that will be the same in all games, because the package name appears in the JSNI code:
```
c.@org.game_api.GameApi.ContainerConnector::eventListner(Ljava/lang/String;)(str);
```
  1. You will need to change your source paths in your GWT xml, e.g., for my cheat game I did:
```
  <source path='cheat'/>
  <source path='game_api'/>
```
  1. Download [GameApi.java](https://raw.githubusercontent.com/yoav-zibin/cheat-game/master/eclipse/src/org/game_api/GameApi.java) and put it in package `org.game_api` (obviously delete the old `GameApi.java`). Note that I replaced all `Id`s that were `int` to `String`, so you will need to change your game accordingly and replace some `int` to `String`. After you're done test your game like you did before and only then move to the next steps.
  1. In your `EntryPoint` class, use `GameApi.ContainerConnector` instead of `GameApi.IteratingPlayerContainer`. You only need to call `container.sendGameReady();` method initially, and the rest will be handled by the emulator. Delete any UI that you added to change the current player (that is handled by the emulator).
  1. Upload to AppEngine (increase version number), and test in the [emulator](http://smg-gwt-emulator.appspot.com/GwtEmulator.html). You can also test locally if you want by downloading the emulator (follow the instructions on [GWT emulator site](http://smg-gwt-emulator.appspot.com/)).
  1. When everything works correctly, commit to your github and in your commit message write: `HW7 part A: converted the game to use the emulator in http://smg-gwt-emulator.appspot.com/GwtEmulator.html , enter in the emulator this URL: http://BLABLA.appspot.com/YOURGAME.html`

### Part B: Advanced graphics ###
You need to add to your game: animations for the moves, drag-n-drop the pieces, sounds (for the moves).

Make sure to send the move only after the animations finish.

Do NOT use [GWT drag-n-drop project](https://code.google.com/p/gwt-dnd) (gwt-dnd). They have a [bug](https://code.google.com/p/gwt-dnd/issues/detail?id=179) if you scale the game.


If your can't support drag-n-drop in any reasonable way (e.g., a poker game), then just add drag-n-drop to two labels `drag me` and `drag onto me` and change the size/color of the labels on drag over and drop events.

As usual, upload your game to your AppEngine, and write the URL in the commit message. Make sure to increment the `version` number in your `appengine-web.xml` so the grader could still access the old HW. I recommend setting the `version` number to the HW number.

Make sure that your game will still work even in old browsers that do not support these features.

You should be able to move the pieces using two ways:
  1. Just by clicking - then you should see an animation of the piece moving.
  1. drag-n-drop - then there shouldn't be any animation (the piece should just appear in the destination).

Example from previous year:
  1. [MP3 and WAV sounds](https://code.google.com/p/nyu-gaming-course-2013/source/browse/trunk/eclipse/src/org/simongellis/hw5/)
  1. [Including the sounds using ClientBundle](https://code.google.com/p/nyu-gaming-course-2013/source/browse/trunk/eclipse/src/org/simongellis/hw5/GameSounds.java)
  1. [class extending Animation](https://code.google.com/p/nyu-gaming-course-2013/source/browse/trunk/eclipse/src/org/simongellis/hw5/PieceMovingAnimation.java)
  1. [Graphics using drag-n-drop, sounds, local storage, and the animation class](https://code.google.com/p/nyu-gaming-course-2013/source/browse/trunk/eclipse/src/org/simongellis/hw3/Graphics.java#521)