---
layout: post
title: Emacs Keys (Emacs Emulator)
description: "An Emacs key bindings emulator for Visual Studio"
tags: [emacs, visual studio]
modified: 2015-02-24
image:
  feature: abstract-1.jpg
  credit: zbrad
  creditlink: http://zbrad.github.io/

---

Way back in Visual Studio 2008, many of us rejoiced when Microsoft released a set of key bindings, that mimiced the key bindings used in
Emacs.  In Visual Studio 2010, the feature was removed from the main product, but the Visual Studio team released the key bindings 
as an extension "[Emacs Emulation](https://visualstudiogallery.msdn.microsoft.com/09dc58c4-6f47-413a-9176-742be7463f92/)", so that it was still
available for developers, like myself, who still used our old keyboard shortcuts.  I cannot 
begin to count the number of times that I would pop up the print screen (Ctrl-P), instead of previous line.

However, upon release of Visual Studio 2012, the extension was never updated, so many of us delayed converting for as long as we could,
until support was available.   However that update never came.   Several folks on the comment list suggested ways to backward engineer the
content that would allow it to be installed in VS2012, so it was considered an "acceptable" workaround.

I recently re-joined Microsoft and was still missing this capability.  However just this last fall, under Satya Nadella's guidance, Microsoft has
newly embraced the outreach to our developer community.   I asked if we could consider open sourcing 
the original VS2010 extension.  After tracking down the Visual Studio "owners", and getting the legal sign-off, I can now present to you
the [Visual Studio Emacs Emulator extension source](http://github.com/zbrad/EmacsKeys), under the
[open source MIT License](http://opensource.org/licenses/MIT). 

I have renamed the project to "EmacsKeys" to more accurately reflect that it is primarily about mapping key bindings, although it does
support some basic Emacs behaviors (kill ring), that didn't used to exist in Visual Studio.

Initially I'm releasing it exactly as I received it, warts and all.  But I've added some work items to the list, to see if we can actually
improve it over time.

If you are interested in working on this project, please just take a fork, dive in, post an issue, etc...

Useful Links:

- [Visual Studio 2008 Emacs Shortcut Keys](http://msdn.microsoft.com/en-us/library/ms165528%28VS.90%29.aspx)
- [Visual Studio 2010 Blog Entry Accouncing Emacs Emulation](http://blogs.msdn.com/b/visualstudio/archive/2010/09/01/emacs-emulation-extension-now-available.aspx)
- [GitHub EmacsKey Project](http://github.com/zbrad/EmacsKeys)


