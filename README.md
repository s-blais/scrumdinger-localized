# Scrumdinger – Localization Experiment

### Yes, hi, Perry Street Software!

Having some fun with trying to localize a complete iOS app (this app is created as part of the Apple Developer [Develop Apps for iOS](https://developer.apple.com/tutorials/app-dev-training) tutorial.

Some Notes:

* Couldn't quite figure out how to localize the strings that include interpolated values (e.g., "Speaker 3 of 5"). The `%11d` method I found in documentation doesn't seem to apply to interpolations in a direct `return` or in a `Label()`.