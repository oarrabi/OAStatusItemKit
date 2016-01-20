# OAStatusItemKit

[![CI Status](http://img.shields.io/travis/Omar Abdelhafith/OAStatusItemKit.svg?style=flat)](https://travis-ci.org/Omar Abdelhafith/OAStatusItemKit)
[![Version](https://img.shields.io/cocoapods/v/OAStatusItemKit.svg?style=flat)](http://cocoapods.org/pods/OAStatusItemKit)
[![License](https://img.shields.io/cocoapods/l/OAStatusItemKit.svg?style=flat)](http://cocoapods.org/pods/OAStatusItemKit)
[![Platform](https://img.shields.io/cocoapods/p/OAStatusItemKit.svg?style=flat)](http://cocoapods.org/pods/OAStatusItemKit)

## Usage

To run the example project, clone the repo, and run `pod install` from the Example directory first.

## Requirements

## Installation

OAStatusItemKit is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod "OAStatusItemKit"
```

## Usage
First, `import OAStatusItemKit`

Then create a `StatusBarItemView` and a `StatusBarWindowController`

```swift
let statusBarItem =
StatusBarItemView(brightStatusImage: NSImage(named: "Icon-bright")!,
darkStatusImage: NSImage(named: "Icon-dark")!)

let statusBarWindow =
StatusBarWindowController(xibName: "xib name", statusItem: statusBarItem)
```

Finally, you need to make your app a mac agent app. to do so open Info.plist. Add a new key "Application is agent (UIElement)" and set it's value to YES.

![image](http://i.imgur.com/DwY0Ffj.png)

Thats it, enjoy.

## Documentation
Bellow is a quick and dirty introduction, check the full documentation [here](http://)

#### StatusBarItemView
[StatusBarItemView](http://) is the class responsible for representing a status bar view.

Example usage:

```
let statusItem = StatusBarItemView(brightStatusImage: BrightImage, 
darkStatusImage: DarkImage)

let statusItem = StatusBarItemView(statusImage: AnyImage)
```

To change the width of the view, use `itemWidth`

```
statusItem.itemWidth = 200
```

The displayed panel will take the size of the view passed, if you want to specify a different size, then set it using `windowSize`

```
controller.windowSize = NSSize...
```

`windowPlacement` property is used to determine the placement of the window in the screen, the values are described [here](http://)

#### StatusBarWindowController
[StatusBarWindowController](http://) is a class responsible for displaying and placing a view on screen.

It can be created with a xib or a view.

```
let controller = StatusBarWindowController(xibName:statusItem:)
let controller = StatusBarWindowController(view:statusItem:)
```

## Tests
To run tests execute `make test`

## Author

Omar Abdelhafith, o.arrabi@me.com

## License

OAStatusItemKit is available under the MIT license. See the LICENSE file for more info.
