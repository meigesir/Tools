# Tools
Tools I use most frequently

## Xcode Plug-ins
`Xcode → Plug-ins` I use for development.

#### Invalid bug fixes:
You need to execute command in terminal:
```shell
find ~/Library/Application\ Support/Developer/Shared/Xcode/Plug-ins -name Info.plist -maxdepth 3 | xargs -I{} defaults write {} DVTPlugInCompatibilityUUIDs -array-add `defaults read /Applications/Xcode.app/Contents/Info.plist DVTPlugInCompatibilityUUID`
```
Reference Sources： [XCode升级后插件失效的原理与修复办法](http://joeshang.github.io/2015/04/10/fix-xcode-upgrade-plugin-invalid/)
