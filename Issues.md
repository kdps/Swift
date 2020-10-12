# Swift

#### App called -statusBar or -statusBarWindow on UIApplication: this code must be changed as there's no longer a status bar or status bar window. Use the statusBarManager object on the window scene instead.

```Swift
UIApplication.shared.value(forKey: "statusBar") as? UIView
```

to

```Swift
let statusBarFrame = UIApplication.shared.keyWindow?.windowScene?.statusBarManager?.statusBarFrame
let statusBar = UIView(frame: statusBarFrame)
view.addSubView(statusBar)
```

#### Software caused connection abort Code 53

https://www.gitmemory.com/issue/Alamofire/Alamofire/2674/543824622

#### Alamofire Background Network Connection Error

```Swift

func sdelay(_ delay:Double, closure:@escaping ()->()) {
    let when = DispatchTime.now() + delay
    DispatchQueue.main.asyncAfter(deadline: when, execute: closure)
}

sdelay(0.4) {
  Alamofire.request ... {
    request in

    DispatchQueue.main.async {
    }
  }
}
```
