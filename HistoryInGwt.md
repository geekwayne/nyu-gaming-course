Example of how history was done last semester:
[Presenter with History](https://code.google.com/p/nyu-gaming-course-2013/source/browse/trunk/eclipse/src/org/simongellis/hw3/Presenter.java?spec=svn590&r=590). Look at how `History` class was used, and look at the `serializeState` and `unserializeState` methods that change a state into a string and back.

The relevant code:
```
History.newItem(serializeState(state));

        public void initializeHistory() {
                History.addValueChangeHandler(new ValueChangeHandler<String> () {
                        @Override
                        public void onValueChange(ValueChangeEvent<String> event) {
                                String historyToken = event.getValue();
                                setState(unserializeState(historyToken));
                        }
                });
                String startState = History.getToken();
                setState(unserializeState(startState));
                initializedHistory = true;
        }
```