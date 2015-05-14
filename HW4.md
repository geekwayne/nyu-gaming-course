Create GWT Graphics for your game: create `YourGameGraphics` that will implement `YourGamePresenter.View`.
For example, see [CheatGraphics.java](https://github.com/yoav-zibin/cheat-game/blob/master/eclipse/src/org/cheat/graphics/CheatGraphics.java).

Use `UiBinder`, i.e., create both `YourGameGraphics.java` and `YourGameGraphics.ui.xml`.

Use `GameApi.IteratingPlayerContainer` to test your graphics (because the emulator is not built yet :))
Upload your game to AppEngine (e.g., [CheatGame.html](http://cheat-game.appspot.com/CheatGame.html)), and give a link to the game in the commit message, e.g., `HW4: Graphics for cheat game, url: http://cheat-game.appspot.com/CheatGame.html`