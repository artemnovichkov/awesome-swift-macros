# Awesome Swift Macros
A hand-curated list of Swift macros. Feel free to contribute!

## WWDC23

- [Discover Observation in SwiftUI](https://developer.apple.com/videos/play/wwdc2023/10149)
- [Expand on Swift macros](https://developer.apple.com/videos/play/wwdc2023/10167)
- [Write Swift macros](https://developer.apple.com/videos/play/wwdc2023/10166)

## Macros

- [Swift Macro Examples](https://github.com/DougGregor/swift-macro-examples)

```swift
// "Stringify" macro turns the expression into a string.
#stringify(x + y)

// "AddBlocker" complains about addition operations. We emit a warning
// so it doesn't block compilation.
#addBlocker(x * y + z)

// "#URL" macro provides compile time checked URL construction. If the URL is
// malformed an error is emitted. Otherwise a non-optional URL is expanded.
#URL("https://swift.org/")
```

- [swift Power Assert](https://github.com/kishikawakatsumi/swift-power-assert)

```swift
#powerAssert(max(a, b) == c)
             |   |  |  |  |
             7   4  7  |  12
                       false
```

- Preview macro (Xcode 15+)
```swift
#Preview {
    Button("SwiftUI") {}
}
```

- [SFSymbolsMacro](https://github.com/lukepistrol/SFSymbolsMacro)

```swift
import SFSymbolsMacro
import SwiftUI

@SFSymbol
enum Symbols: String { ... }
```

## Proposals

* [SE-0382: Expression macros](https://github.com/DougGregor/swift-evolution/blob/se-0382-expression-macros-updates/proposals/0382-expression-macros.md)
* [SE-0389: Attached Macros](https://github.com/apple/swift-evolution/blob/main/proposals/0389-attached-macros.md)
* [SE-0394 Package Manager Support for Custom Macros](https://github.com/apple/swift-evolution/blob/main/proposals/0394-swiftpm-expression-macros.md)
