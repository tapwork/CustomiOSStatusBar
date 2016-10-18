# YourStatusBar
## Customize the statusBar of your iOS app with any text or UIView
[![Build Status](https://api.travis-ci.org/tapwork/YourStatusBar.svg?style=flat)](https://travis-ci.org/tapwork/YourStatusBar)
[![CocoaPods Version](http://img.shields.io/cocoapods/v/YourStatusBar.svg?style=flat)](https://github.com/tapwork/YourStatusBar/blob/master/YourStatusBar.podspec)
[![](http://img.shields.io/cocoapods/l/YourStatusBar.svg?style=flat)](https://github.com/tapwork/YourStatusBar/blob/master/LICENSE.md)
[![CocoaPods Platform](http://img.shields.io/cocoapods/p/YourStatusBar.svg?style=flat)]()

You always asked yourself why you can't change the text in the iOS statusBar for debug reasons? Or custom UIViews? YourStatusBar tweaks the iOS statusBar to add custom text or views. 
In big projects I often have the problem to find the right UIViewController class. So I wanted to see the current class name in the statusBar. That is actually the reason why I built this library here. 

# Features
* Set your text to the iOS statusBar
* Add your custom UIView to the statusBar

# Usage
Please make sure that you use YourStatusBar only for **DEBUG** purposes. Not in production mode, because  `UIStatusBarWindow` is private API.
You could use `YourStatusBar` to display the current class like
```
- (void)viewWillAppear:(BOOL)animated {
    [super viewWillAppear:animated];

    [TWYourStatusBar setCustomText:NSStringFromClass([self class])];
}
```

## CocoaPods Installation
Add it to your Podfile and run `pod install`
```
pod 'YourStatusBar'
```
And use `#import <YourStatusBar/TWYourStatusBar.h>`

## Change text
```
[TWYourStatusBar setCustomText:@"My custom Text"];
```

## Use custom UIView
```
UIView *myView = [[UIView alloc] init];
[TWYourStatusBar setCustomView:myView];
```

# Example project
Like always this library comes with an example project.

# References
* [UIStatusBar](https://github.com/nst/iOS-Runtime-Headers/blob/master/Frameworks/UIKit.framework/UIStatusBar.h) UIKit's private header
* [UIStatusBarWindow](https://github.com/nst/iOS-Runtime-Headers/blob/master/Frameworks/UIKit.framework/UIStatusBarWindow.h) UIKit's private header

# Thanks
* [Piet Brauer](https://twitter.com/pietbrauer) thanks for the clean up

# Author
* [Christian Menschel](http://github.com/tapwork) ([@cmenschel](https://twitter.com/cmenschel))

# License
[MIT](LICENSE.md)
