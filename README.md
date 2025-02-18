# Expo Linking API Event Listener Inconsistency

This repository demonstrates an inconsistency in Expo's `Linking` API when handling deep links on Android.  The `Linking.addEventListener` function does not reliably trigger when the app is in the background or has been terminated.  This leads to deep links being missed.

The `linkingBug.js` file shows the problematic implementation, while `linkingSolution.js` illustrates a potential workaround using a combination of `Linking.getInitialURL` and the Android's intent filters.