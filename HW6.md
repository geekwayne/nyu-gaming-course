Create a multiplayer version of your game on AppEngine!
You should auto-match the players, i.e., simply match any two waiting players.
The players should pass their moves using [GWT-RPC](https://developers.google.com/web-toolkit/doc/latest/tutorial/RPC) (to AppEngine) and [Channel API](https://developers.google.com/appengine/docs/java/channel/overview) (from AppEngine).
The client should also use RPC at the beginning to get the channel token and to find an auto-match.

You should remove/disable the history support you added in HW3.

You should use this GWT plugin for Channel API: [gwt-gae-channel](https://code.google.com/p/gwt-gae-channel/wiki/HowToUse)
Don't forget to add to your .gwt.xml:
```
<inherits name='com.google.gwt.appengine.channel.Channel'/>
<inherits name='com.google.gwt.inject.Inject'/>
```

Instantiate `Channel` like this:
```
Channel channel = new ChannelFactoryImpl().createChannel(result);
```

The player should be able to [login using his Google account](https://developers.google.com/appengine/docs/java/users/overview), and then the game will display the user name.

As usual, upload your game to AppEngine (don't forget to increment the `version` number!), and test it live in at least two browsers (chrome / firefox / safari / IE).
Add the URL of your game to your commit message.

Here is an [Example](https://code.google.com/p/nyu-gaming-course-2013/source/detail?r=682) from last year.