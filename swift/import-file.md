# Importing Interpreted Files in Swift

Say you're writing a bit of swift to be interpreted instead of compiled and you want to split code up across multiple files.

**module.swift**

```swift
public func runFromOtherFile() {
    // ...
}
```

All you have to do is import the filename.

**script.swift**

```swift
import module

runFromOtherFile()
```

For this to work a few flags have to be passed to swift. For ease of use, it makes sense to add this to `script.swift` as a shebang.

`#!/usr/bin/swift -frontend -interpret -enable-source-import -I .`



Credits go to https://forums.swift.org/t/import-swift-file-in-script/9429/9