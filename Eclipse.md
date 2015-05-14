## Setup ##
  1. Download and install [Eclipse for Java developers](http://www.eclipse.org/downloads/packages/eclipse-ide-java-developers/junosr2)
  1. Install the eclipse plugin for [gwt+appengine](http://code.google.com/appengine/docs/java/tools/eclipse.html) (make sure to select in SDKs: Google App Engine Java and Google Web Toolkit (GWT), and choose at least gwt-2.6)
  1. In `Preferences->General->Editors->Text Editors`, set `Display tab width` to `2`, check `Insert spaces for tabs`, and set `Print margin column` to `100`.
  1. Install [EGit](http://www.eclipse.org/egit/) and clone our repository
```
git clone https://github.com/yoav-zibin/multiplayer-gaming-platform.git
```
  1. On windows, I also recommend [Tortoise Git](https://code.google.com/p/tortoisegit/)
  1. Install eclipse plugin [CheckStyle](http://eclipse-cs.sourceforge.net/downloads.html), download [CheckStyleConfigurationForGamingPlatform.xml](https://raw.github.com/yoav-zibin/multiplayer-gaming-platform/master/eclipse/gaming-platform/documents/CheckStyleConfigurationForGamingPlatform.xml), and in `Preferences->CheckStyle->New...` choose `External Configuration File` and enter for `Name:` the name `CheckStyleConfigurationForGamingPlatform`, and browse to the file you just downloaded, and set the configuration as the default.


<h3>Test Check-Style was installed correctly</h3>
Try to do some style violations and see that they are reported correctly:
  1. `static public int i=3;`
  1. `int[] a={1,2,3};`
  1. Try this:
```
int[] b = {
  1,
  2 + 3,
  4+5,
  6 +
  7,
  8
  + 9};
```


## Tips ##
  * `Ctrl+Shift+O` optimizes all your imports (removes unused imports).
  * `Ctrl+Shift+F` formats your code nicely.
  * `Shift+Alt+UP` selects enclosing element.
  * `Shift+Alt+L` extracts local.
  * `Shift+Alt+Z` surround with XXX.
  * `Ctrl+Space` is smart auto-complete.
  * `Ctrl+F8` to switch perspectives
  * `Ctrl+1, 2, 3`  quick fix, quick assist, quick access
  * `Alt+Shift+R` rename
  * `Ctrl+Shift+G` find usages
  * `Ctrl+Shift+M` makes a static import for a static method call