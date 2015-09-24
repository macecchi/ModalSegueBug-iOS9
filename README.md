# ModalSegueBug-iOS9

**Bug that makes the springboard reset on iOS 9 when performing a Modal segue.**

The app contains two view controllers, the root view controller containing a button with a modal segue to a second view controller.

Tapping the button makes the springboard reset on the simulator or device. Only happens with iOS 9.

This happened to me with an existing project on Xcode 7 which somehow broke the view controller on the storyboard, causing this problem. However, I found no way to fix this - as there are no errors or warnings presented, not even during the crash. My only solution was to delete the view controller on Storyboard and recreate it from scratch.
