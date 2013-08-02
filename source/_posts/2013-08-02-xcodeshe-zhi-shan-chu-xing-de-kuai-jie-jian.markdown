---
layout: post
title: "Xcode设置删除行的快捷键"
date: 2013-08-02 20:06
comments: true
categories: 
---
[参考在这里](http://stackoverflow.com/questions/551383/xcode-duplicate-delete-line)
如果你用的是preview版本的xcode, 记得修改路径
	sudo chmod 666 /Applications/Xcode.app/Contents/Frameworks/IDEKit.framework/Resources/IDETextKeyBindingSet.plist
	sudo chmod 777 /Applications/Xcode.app/Contents/Frameworks/IDEKit.framework/Resources/
	open /Applications/Xcode.app/Contents/Frameworks/IDEKit.framework/Resources/IDETextKeyBindingSet.plist
add
	deleteToBeginningOfLine:, moveToEndOfLine:, deleteToBeginningOfLine:, deleteBackward:, moveDown:, moveToBeginningOfLine:

Restart Xcode and open Xcode > Preferences > KeyBindings. Find your macro and define a shortkey :


