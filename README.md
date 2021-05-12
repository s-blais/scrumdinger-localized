# Scrumdinger – Localization Experiment

### Hello! • ¡Hola! • Bonjour!

This repo is my experimentation with trying to localize a complete iOS app (this app is created as part of the Apple Developer [Develop Apps for iOS](https://developer.apple.com/tutorials/app-dev-training) tutorial). Note that localization of this app is NOT in any way part of the tutorial; I figured it out how to do it by reading the Xcode documentation and a handful of articles. It's a very simple implementation of localization, nevertheless, success!

Download the project, open the Scrumdinger.xcodeproj with Xcode. Then, either:

* In your running iOS simulator, Settings > General > Language & Region: change to ES/Español or FR/Français, then hit the Build&Run button in Xcode.
* in Xcode, choose Product > Scheme > Edit Scheme. Select the Run scheme action in the left column, then Options on the right. Choose English or French from the popup menu.

Some Notes:

* Got ES and FR working (Disclaimer: translation accuracy not guaranteed!)
* Couldn't quite figure out how to localize the strings that include interpolated values (e.g., "Speaker 3 of 5"). The `%11d` method I found in documentation doesn't seem to apply to interpolations in an explicit `return` or in a `Label()`.
* Don't yet understand how some automatic(?) styled(?) upcasing of string elements in the base language doesn't carry over to the localizations. Seems rather awkward to have to `"Cancel" = "ANNULAR"`

This was fun, and I'd love to learn how these localizations are implemented on a larger scale.

![Home Screen EN](http://s-blais.com/assets/scrumdinger-localized/Home-EN.png)
![Home Screen ES](http://s-blais.com/assets/scrumdinger-localized/Home-ES.png)
![Home Screen FR](http://s-blais.com/assets/scrumdinger-localized/Home-FR.png)


![Detail Screen EN](http://s-blais.com/assets/scrumdinger-localized/Detail-EN.png)
![Detail Screen ES](http://s-blais.com/assets/scrumdinger-localized/Detail-ES.png)
![Detail Screen FR](http://s-blais.com/assets/scrumdinger-localized/Detail-FR.png)

![Timer Screen EN](http://s-blais.com/assets/scrumdinger-localized/Timer-EN.png)
![Timer Screen ES](http://s-blais.com/assets/scrumdinger-localized/Timer-ES.png)
![Timer Screen FR](http://s-blais.com/assets/scrumdinger-localized/Timer-FR.png)


![Edit Screen EN](http://s-blais.com/assets/scrumdinger-localized/Edit-EN.png)
![Edit Screen ES](http://s-blais.com/assets/scrumdinger-localized/Edit-ES.png)
![Edit Screen FR](http://s-blais.com/assets/scrumdinger-localized/Edit-FR.png)