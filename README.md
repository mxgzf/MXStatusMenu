**Caution! Legacy code. Written in Swift 1.2 and Xcode 6.3.**

MXStatusMenu shows the cpu and network load in the menubar of OS X similar to [iStatMenus](http://bjango.com/mac/istatmenus/). Written in Swift.

<img src=MXStatusMenu.png width=407 height=127 alt="Screenshot of MXStatusMenu"/>

# Details

* Implements the menubar item using `NSStatusBar` and a `NSView` with a dynamic width
* Reads the cpu load using `host_processor_info` / `PROCESSOR_CPU_LOAD_INFO`
* Reads the network load using `sysctl` / `NET_RT_IFLIST2`
* Shows how to alloc and dealloc Swift pointers of type `UnsafePointer` and `UnsafeMutablePointer`
* Includes a timer implementation using Grand Central Dispatch / `DISPATCH_SOURCE_TYPE_TIMER`
* Does not require third-party code to compile. The only dependencies are `import Cocoa` and `import Darwin`.

# Parameters

Visual parameters, update intervals, and the maximum network load can be set in the file [App.swift](./MXStatusMenu/App.swift)

# Compatibility

Tested on OS X 10.10.3 (14D131). Compiles without errors or warnings using Xcode 6.3 (6D570).

# Disclaimer

This is a simple app to test the capabilities of Swift and not intended to be used in production environments. If you are looking for a real app that monitors your Mac, i highly recommend [iStatMenus](http://bjango.com/mac/istatmenus/).

Please notice that i'm not affiliated in any way with [Bjango](http://bjango.com), the developer of [iStatMenus](http://bjango.com/mac/istatmenus/).

# Author

Maximilian Götzfried ([@mgoetzfried](https://twitter.com/mgoetzfried), [maximiliangoetzfried.com](http://www.maximiliangoetzfried.com))

# License

MXStatusMenu is available under the MIT license. See [the LICENSE file](./LICENSE.txt) for more information.
