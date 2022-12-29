# Reading 41

[Back to the table of contents](../../README.md)

## getting started with react native

* Name three Core Components of React Native and describe what they do.
  * <View> is the equivalent of a div, working like a container for other components.
  * <Text> is the equivalent of a p, working as a textbox.
  * <Image> is the equivalent of a img, letting you display images.
* What problem does React Native solve (why call it native)?
  * React Native uses your platform's native APIs to make a framework that works across many devices.
* What are the building blocks of a React Native app? How does that compare to a React app?
  * A <View>, which as above, is the equivalent of a div. They hold things inside themselves, be it text, other components... pretty much anything that is rendered!

## Expo

* What solution does expo provide?
  * Expo brings a host of extra features to React Native, with expo apps. It's like a further developed native.
  * But beyond that, it takes care of all of your services and whatnot, so you're only writing Javascript/TS
* Expo tries to manage as much of the complexity of building apps as possible, which is why we call it the ____ workflow.
  * Managed
* What is the difference between React Native and Expo?
  * Biggest difference is that Managed workflow. You're going to have more ability to do custom things with React Native, but you're also going to be doing more work yourself.

## Expo Snack

* Checkout this tool. What does snack allow you to do?
  * Expo snacks let you write native/expo code in browser, and test it on multiple devices. Great way for demonstrating code or quickly testing if you don't have your emulators set up.

## Expo Eject

* What does “eject” mean within the context of Expo?
  * Ejecting removes your project from Expo's iOS/Android clients, meaning you can write special native capabilities.
* When should you not eject?
  * If you need to export to iTunes or Google Play
  * You don't actually want to write native code, and fair enough
* Why might you choose to eject?
  * If you know what you're doing, and you need to do something the Expo SDK can't offer, it might be time to eject.
