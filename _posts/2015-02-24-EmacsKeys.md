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

Way back in Visual Studio 2008 many of us rejoiced when
Microsoft released a set of key bindings that mimiced the key
bindings used in [Gnu Emacs](http://www.gnu.org/software/emacs).

## History of Emacs Visual Studio Keybindings

In Visual Studio 2010 the Emacs Keybindings feature was
removed from the main product but the Visual Studio team
released the key bindings as a
[Visual Studio extension](https://msdn.microsoft.com/en-us/library/dd885119.aspx)
available in the online
[Visual Studio Gallery](https://visualstudiogallery.msdn.microsoft.com/) called
"[Emacs Emulation](https://visualstudiogallery.msdn.microsoft.com/09dc58c4-6f47-413a-9176-742be7463f92/)".

This made it so that the bindings were still available for developers, like
myself, who still used our old keyboard shortcuts.  *I cannot begin to count
the number of times that I would pop up the print screen
(Ctrl-P) instead of previous line.*

However after the release of Visual Studio 2012 the extension was
never updated so many of us delayed converting from VS2010 for as long as
we could - waiting for support that never came.  Reluctantly most of us just
started using VS2012 with it's default bindings just to get use of the new
features.

Additionally knowns issues, several bug reports, or just behavioral oddities
were languishing in the online comments section of the extension.

Several folks on the extension comment list suggested ways to
backward engineer the content that would allow it to be
installed in VS2012.  Up to now this has been considered an "acceptable"
workaround.

## Personal Emacs History Digression

I first started using Emacs back when I worked for DEC, on the [TOPS-10](http://en.wikipedia.org/wiki/TOPS-10)
and [TOPS-20](http://en.wikipedia.org/wiki/TOPS-20)
operating systems.  It's programming language at that time was
[TECO](http://en.wikipedia.org/wiki/TECO_%28text_editor%29), and the name was
an acronym for "Editing MACroS".

Later when I started working on VAX/VMS, James Gosling had already released
[Gosling Emacs](http://en.wikipedia.org/wiki/Gosling_Emacs).  So once again I
was able to reuse all those typing skills.   Although now the programming
language was [Mocklisp](http://en.wikipedia.org/wiki/Mocklisp).

Finally (somewhere in the early 90's) I switched over to
[Gnu Emacs](http://www.gnu.org/software/emacs), probably when I was working
on a number different Unix systems, and also some of the early versions of
Linux ([Slackware 3.0](http://en.wikipedia.org/wiki/Slackware#1993.E2.80.932003)).

When I originally joined Microsoft (the first time
in 1996) I started as a Program Manager in the Developer Relations Group and at that time Microsoft
was very deeply involved with the developer community. 
Even during that time I was still using [Gnu Emacs](http://www.gnu.org/software/emacs) fairly extensively. 
For example when C# was first created we did not have any Visual Studio support
for it.  So I created an Emacs C# mode (cc-mode at that time was not yet ready)
so that I could edit my source code and have some basic syntax highlighting.
(For an example of an older C#
project which builds using a Makefile see my
[CsLex Project](http://github.com/zbrad/CsLex))

I left Microsoft in 2006, but continued to work in a mixed Visual Studio /
Emacs mode.  During that time my Emacs skills were still very helpful and
relevant particularly when working on various Linux installations.

I re-joined Microsoft in 2012 working on the Azure team but was still missing
my Emacs key bindings when I had to use Visual Studio.

## New (and exciting) Microsoft

Just this last fall (2014) under Microsoft's new CEO's ([Satya Nadella](http://news.microsoft.com/ceo/index.html))
leadership Microsoft has recently re-engaged with the broader
developer community by open sourcing many of our languages and tools.  Satya
originally joined Microsoft as a [Program Manager in the Developer Relations Group](https://www.crunchbase.com/person/satya-nadella)
and cites that time as strong influencer.

Late last year I changed teams to start with a group called TED (Technical
Evangelism and Development).  When the opportunity to start a new
project came up I asked if we could consider open sourcing
the original VS2010 extension.  It helped when they considered that the VS2010
extension had over 22,000 downloads.

After tracking down the Visual Studio "owners" and getting all the
appropriate legal sign-off this release is finally ready.

## Emacs Keys Project

 I can now present to you the original
[Visual Studio Emacs Emulator extension source](http://github.com/zbrad/EmacsKeys)
open sourced under the [open source MIT License](http://opensource.org/licenses/MIT).

I have renamed the project to "EmacsKeys" to more accurately
reflect that it is primarily about mapping key bindings although it does
support some basic Emacs behaviors (for example kill ring)
that did not exist in Visual Studio.

## New Work

Initially I'm releasing it exactly as I received it, warts and
all.  But I've added some work items to the list to see if we
can actually improve it over time.

If you are interested in working on this project please just:
take a fork, dive in, post an issue, etc...

## Useful Links

- [GitHub EmacsKey Project](http://github.com/zbrad/EmacsKeys)
- [Visual Studio extension](https://msdn.microsoft.com/en-us/library/dd885119.aspx)
- [Visual Studio 2008 Emacs Shortcut Keys](http://msdn.microsoft.com/en-us/library/ms165528%28VS.90%29.aspx)
- [Visual Studio 2010 Blog Entry Accouncing Emacs Emulation](http://blogs.msdn.com/b/visualstudio/archive/2010/09/01/emacs-emulation-extension-now-available.aspx)
- [Visual Studio Gallery](https://visualstudiogallery.msdn.microsoft.com/)
- [Visual Studio Gallery Emacs Emulation extension](https://msdn.microsoft.com/en-us/library/dd885119.aspx)
- [Gnu Emacs](http://www.gnu.org/software/emacs)

