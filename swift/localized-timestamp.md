# Localized Timestamp

If one can't use a predefined date or time style from `DateFormatter` for a user-facing timestamp, it should definitely be using a localized template. Use either `DateFormatter.dateFormat(fromTemplate:options:locale:)` or `DateFormatter.setLocalizedTemplate...(something)`.
A problem with this however is that neither `H` or `h` format strings are adjusted to be locale-specific 24 or 12-hour clocks.

To handle those correctly one needs to use a so called "input skeleton symbol" (the `j` below), which is expanded by the `DateFormatter` to use a locale-specific hour value meaning this turns into `HH` or `h a` (or something else) based on the input locale.

```swift
let templateString = DateFormatter.dateFormat(fromTemplate: "Ejm", options: 0, locale: locale)!
let formatString = DateFormatter.dateFormat(fromTemplate: templateString, options: 0, locale: locale)
let formatter = DateFormatter()
formatter.dateFormat = formatString
```

Just for fun, this will output all available timestamp localization across all available locales.

```swift
import Foundation

Locale.availableIdentifiers
    .map { identifier -> (String, String) in
        let locale = Locale(identifier: identifier)
        let templateString = DateFormatter.dateFormat(fromTemplate: "Ejm", options: 0, locale: locale)!
        let formatString = DateFormatter.dateFormat(fromTemplate: templateString, options: 0, locale: locale)
        let formatter = DateFormatter()
        formatter.dateFormat = formatString
    
        let dateString = formatter.string(from: Date())
        return (identifier, dateString)
    }
    .sorted(by: { $0.0 < $1.0 })
    .forEach { (identifier, dateString) in
        let space = Array(repeating: " ", count: 15-identifier.count).joined()
        print("\(identifier):\(space)\(dateString)")
    }
```
