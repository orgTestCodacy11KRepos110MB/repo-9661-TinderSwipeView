# Tinder Swipe View ![Swift 4.0.x](https://img.shields.io/badge/Swift-4.0.x-orange.svg)

Inspired animation from Tinder and Potluck with random undo feature!

Run in physical device for better animaton!!!!

## Preview

<p align="center">
    <img src="./TinderSwipeView/Screen%20Shot%20.png" alt="Size Limit example"
       width="316" height="550">
    <img src="./playback.gif" alt="Size Limit example"
       width="316" height="550">
</p>

<p align="center">
  
</p>

## Screenshot

<p align="center">
  <img src="./TinderSwipeView/Screen%20Shot%20DIislike.png" alt="Size Limit example"
       width="381" height="662">
  <img src="./TinderSwipeView/Screen%20Shot%20Like.png" alt="Size Limit example"
       width="381" height="662">
</p>

## Installation with CocoaPods

[CocoaPods](http://cocoapods.org) is a dependency manager for Objective-C, which automates and simplifies the process of using 3rd-party libraries like SwiftMultiSelect in your projects. You can install it with the following command:

```bash
$ gem install cocoapods
```

#### Podfile

To integrate GradientSlider into your Xcode project using CocoaPods, specify it in your `Podfile`:

```ruby
source 'https://github.com/CocoaPods/Specs.git'
platform :ios, '8.0'

target 'TargetName' do
use_frameworks!
pod 'TinderSwipeView’
end
```

Then, run the following command:

```bash
$ pod install
```


## Instantiation

Tinder Swipe  can be added to storyboard or instantiated programmatically:

```swift
    let swipeView = TinderSwipeView<UserModel>(frame: viewContainer.bounds, overlayGenerator: overlayGenerator)
    viewContainer.addSubview(swipeView)
    swipeView.showTinderCards(with: userModels)
```
## Animation

```swift

    internal func cardGoesRight()

    internal func cardGoesLeft()

    internal func rightClickAction()

    internal func leftClickAction()

    internal func makeUndoAction()

    internal func rollBackCard()

    internal func shakeAnimationCard(completion: @escaping (Bool) -> ())

```

## Delegate Methods

Here is a list of callbacks you can listen to:

```swift
protocol TinderCardDelegate: NSObjectProtocol {

    func dummyAnimationDone()
    func currentCardStatus(card: Any, distance: CGFloat)
    func cardGoesLeft(_ object: Any)
    func cardGoesRight(_ object: Any)
    func endOfCardsReached()
}
```

## Requirements

```
* Swift 5
* XCode 10
* iOS 8.0 (Min SDK)
```

## Author

Nicky Patson

[HomePage](http://about.me/nickypatson)

<mail.nickypatson@gmail.com>


## License

Tinder Swipe View is available under the MIT license. See the LICENSE file for more info.

