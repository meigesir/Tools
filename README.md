# Tools
Tools I use most frequently

## Xcode Plug-ins
`Xcode → Plug-ins` I use for development.

Xcode Plug-ins Directory:
```bash
~/Library/Application Support/Developer/Shared/Xcode/Plug-ins
```

#### Invalid bug fixes:
You need to execute command in terminal:
```shell
find ~/Library/Application\ Support/Developer/Shared/Xcode/Plug-ins -name Info.plist -maxdepth 3 | xargs -I{} defaults write {} DVTPlugInCompatibilityUUIDs -array-add `defaults read /Applications/Xcode.app/Contents/Info.plist DVTPlugInCompatibilityUUID`
```
Reference Sources： [XCode升级后插件失效的原理与修复办法](http://joeshang.github.io/2015/04/10/fix-xcode-upgrade-plugin-invalid/)

And from Xcode 6.3, you will be prompt to "Load third party bundle" if you are using a plugin. You should always select "Load bundles" to enable this plugin.

If you happened to skip the bundle loading, you can use this to reset the prompt:

```bash
defaults delete com.apple.dt.Xcode DVTPlugInManagerNonApplePlugIns-Xcode-{your_xcode_version}
```

## Xcode CodeSnippets
`Xcode → CodeSnippets` I use for development.

Xcode CodeSnippets Directory:
```bash
~/Library/Developer/Xcode/UserData/CodeSnippets
```

## OSS
`OSS` I think good

### Crypto
`Swift`  
* [CryptoSwift](https://github.com/krzyzanowskim/CryptoSwift)

### JSON
`Swift`
* [SwiftyJSON](https://github.com/SwiftyJSON/SwiftyJSON)

### Image
 `Swift`
* [Kingfisher](https://github.com/onevcat/Kingfisher)
* [AlamofireImage](https://github.com/Alamofire/AlamofireImage)
* [HanekeSwift](https://github.com/Haneke/HanekeSwift)

### Log
`Swift`
* [XCGLogger](https://github.com/DaveWoodCom/XCGLogger)

## SUBSCRIBE
`site` I think good
* [iOS Dev Weekly](https://iosdevweekly.com/)
* [Swift Sandbox](http://swiftsandbox.io/)

## License

Tools is released under the MIT license. See LICENSE for details.
