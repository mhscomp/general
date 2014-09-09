#MHS Robotics Club: Languages#

<b>Objective C</b><br/>
This and Swift are the only ways to write native iOS and OSX apps. It's fast, but difficult to learn, especially for those with no experience with C-based languages.

Most languages would have something like this, for example:

```javascript
self.doNow();
```

With objective c:

```objective-c
[self doNow];
```

<b>Swift</b><br/>
Swift is Apple's alternative to Objective C. It's fast, easy to learn, and is much more familiar to users of other programming languages.

As opposed to:

```objective-c
NSString somevar* = @"something";
```

You write

```swift
var i = "something";
```

To use both Objective C and Swift, you need a computer running OSX and to download Xcode.

<b>Java</b><br/>
Java is used to write Android applications, which has helped to contribute to the popularity of the language. It can be slightly more confusing that making iOS applications, but is useful given the popularity of Android.

<b>Javascript?</b><br/>
If you're really adverse to using any of these languages, you can use a framework like Apache Cordova to embed a small webpage in an iOS or Android application automatically. 

You just write what you want it to display in HTML, Javascript, and CSS, and it is put into a native application. This doesn't look as polished as using the "conventional" method, but can cut down on production time.

```
____________________
| Native application|
| ______________    |
| | web page   |    |
| |____________|    |
|___________________|
```