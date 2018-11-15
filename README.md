# Hoogle [![Hackage version](https://img.shields.io/hackage/v/hoogle.svg?label=Hackage)](https://hackage.haskell.org/package/hoogle) [![Stackage version](https://www.stackage.org/package/hoogle/badge/nightly?label=Stackage)](https://www.stackage.org/package/hoogle) [![Linux Build Status](https://img.shields.io/travis/ndmitchell/hoogle/master.svg?label=Linux%20build)](https://travis-ci.org/ndmitchell/hoogle) [![Windows Build Status](https://img.shields.io/appveyor/ci/ndmitchell/hoogle/master.svg?label=Windows%20build)](https://ci.appveyor.com/project/ndmitchell/hoogle)

## Hoogle 4 vs Hoogle 5






## Other stuff (somewhat outdated)



Hoogle is a Haskell API search engine, which allows you to search many standard Haskell libraries by either function name, or by approximate type signature. To experiment, visit the online version at http://haskell.org/hoogle.

* **Online version:** https://www.haskell.org/hoogle/
* **Hackage page:** https://hackage.haskell.org/package/hoogle
* **Source code:** http://github.com/ndmitchell/hoogle
* **Bug tracker:** https://github.com/ndmitchell/hoogle/issues

## Hoogle Use

Hoogle can be used in several ways:

* **Online**, with the web interface at http://haskell.org/hoogle
* **In [IRC](http://haskell.org/haskellwiki/Haskell_IRC_channel)**, using the [Lambdabot](http://haskell.org/haskellwiki/Lambdabot) plugin with `@hoogle` and `@hoogle+`
* **From `emacs`**, by means of [`engine-mode`](https://github.com/hrs/engine-mode)
* **[Installed locally](https://github.com/ndmitchell/hoogle/blob/master/docs/Install.md)**, with either a command line or in a browser
* **[As a developer](https://github.com/ndmitchell/hoogle/blob/master/docs/API.md)**, through Haskell or JSON APIs.

# Searches

## Searching

Here are some example searches:

* `map` searches as text, finding `map`, `concatMap`, `mapM`
* `con map` searches for the text "map" and "con" finding `concatMap`, but not `map`
* `a -> a` searches by type, finding `id :: a -> a`
* `a` searches for the text "a"
* `:: a` searches for the type "a"
* `id :: a -> a` searches for the text "id" and the type "a -> a"


## Scope

By default, searches look at the [Haskell Platform](http://hackage.haskell.org/platform) and [Haskell keywords](http://haskell.org/haskellwiki/Keywords). However, all [Hackage](http://hackage.haskell.org) packages are available to search. As some examples:

* `mode +cmdargs` searches only the "cmdargs" package
* `file -base` searches the Haskell Platform, excluding the "base" package
* `mode +platform +cmdargs` searches both the Haskell Platform and the "cmdargs" package
* `count +missingh` searches only the "MissingH" package - all packages are written in lower-case

With the set of packages you are searching, you can also restrict the set of modules searched:

* `file -System` excludes results from modules such as `System.IO`, `System.FilePath.Windows` and `Distribution.System`
* `fold +Data.Map` finds results in the `Data.Map` module


## Folders

The folders in the distribution, and their meaning are:

data - tools to generate a hoogle data file

docs - documentation on hoogle

misc - presentations, icons, emacs scripts, logos

src  - source code

web  - additional resources for the web front end (css, jpg etc.)

## Similar Tool

* [Google](http://www.google.com/), the leader in online search
