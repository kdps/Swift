# Swift

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
