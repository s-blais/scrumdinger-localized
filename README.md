# Scrumdinger – Localization Experiment

### Hello! • ¡Hola! • Bonjour!

This repo is my experimentation with localizing an iOS app (this app is created as part of the Apple Developer [Develop Apps for iOS](https://developer.apple.com/tutorials/app-dev-training) tutorial). Note that localization of this app is NOT in any way part of the tutorial; I figured it out how to do it by reading the Xcode documentation and a handful of articles. It's a very simple implementation of localization, nevertheless, success!

Download the project, open the Scrumdinger.xcodeproj with Xcode. Then, either:

* In iOS simulator, Settings > General > Language & Region: change to ES/Español or FR/Français, then hit the Build&Run button in Xcode.
* in Xcode, choose Product > Scheme > Edit Scheme. Select the Run scheme action in the left column, then Options on the right. Choose Spanish or French from the popup menu; Close; hit the Build%Run button.

Some Notes:

* Got ES and FR localizations working (Disclaimer: translation accuracy not guaranteed!)
* The biggest speed bump in this exercise for me was incorporating interpolated values into the localized strings. Although I was able to convert the strings with a *single* interpolated value in DetailView and EditView to an NSLocalizedString to pass the value with the string key, I solicted a hint from the helpful @cambardell to nail down the correct syntax to pass *two* values for the "Speaker [x] of [n]" string in MeetingFooterView.

```swift
// DetailView.swift  
Text(String(format: NSLocalizedString("meetingLength %11d", comment: ""), self.scrum.lengthInMinutes))  
// EditView.swift
Text(String(format: NSLocalizedString("meetingLength %11d", comment: ""), Int(self.scrumData.lengthInMinutes)))
// Localizable.strings EN & FR, ES
"meetingLength %11d" = "%11d minutes";  
"meetingLength %11d" = "%11d minutos";

// MeetingFooterView.swift
let localizedString = NSLocalizedString("speakerXofN", comment: "")
return String.localizedStringWithFormat(localizedString, speakerNumber, speakers.count)
// Localizable.strings EN, ES, FR:
"speakerXofN" = "Speaker %d of %d";
"speakerXofN" = "Orador %d de %d";
"speakerXofN" = "Orateur %d de %d";
```

This is fun, and I'd love to learn how these localizations are implemented on a larger scale.

![Home Screen EN](http://s-blais.com/assets/scrumdinger-localized/Home-EN.png)
![Home Screen ES](http://s-blais.com/assets/scrumdinger-localized/Home-ES.png)
![Home Screen FR](http://s-blais.com/assets/scrumdinger-localized/Home-FR.png)


![Detail Screen EN](http://s-blais.com/assets/scrumdinger-localized/Detail-EN-v3.png)
![Detail Screen ES](http://s-blais.com/assets/scrumdinger-localized/Detail-ES-v3.png)
![Detail Screen FR](http://s-blais.com/assets/scrumdinger-localized/Detail-FR-v3.png)

![Timer Screen EN](http://s-blais.com/assets/scrumdinger-localized/Timer-EN-v2.png)
![Timer Screen ES](http://s-blais.com/assets/scrumdinger-localized/Timer-ES-v2.png)
![Timer Screen FR](http://s-blais.com/assets/scrumdinger-localized/Timer-FR-v2.png)


![Edit Screen EN](http://s-blais.com/assets/scrumdinger-localized/Edit-EN-v3.png)
![Edit Screen ES](http://s-blais.com/assets/scrumdinger-localized/Edit-ES-v3.png)
![Edit Screen FR](http://s-blais.com/assets/scrumdinger-localized/Edit-FR-v3.png)

![History Screen EN](http://s-blais.com/assets/scrumdinger-localized/History-EN.png)
![History Screen ES](http://s-blais.com/assets/scrumdinger-localized/History-ES.png)
![History Screen FR](http://s-blais.com/assets/scrumdinger-localized/History-FR.png)