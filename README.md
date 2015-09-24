# ModalSegueBug-iOS9

**Bug that makes the springboard reset on iOS 9 when performing a Modal segue.**

The app contains two view controllers, the root view controller containing a button with a modal segue to a second view controller.

## Reproducing the bug
Tap the button. Springboard crashes.
Only happens with iOS 9.

## Cause and fix
This happened to me with an existing project on Xcode 7 which somehow *silently* broke the view controller on Storyboard, causing this problem. The console only shows `Terminating since there is no system app.` when testing on a device and `XPC connection interrupted` when using the simulator.

I found no easy way to fix this, as there are no errors or warnings presented, not even during the crash. My only solution was to delete the view controller on Storyboard and recreate it from scratch.

