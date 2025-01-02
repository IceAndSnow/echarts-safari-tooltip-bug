[Bug] tooltip appendTo body briefly causes scrollbar visible in Safari
=====

This repository makes a small working example of the bug.

To further illustrate the problem, I have configured the chart to be cleared every 500ms.
This is solely to make the problem more apparent as it appears the first time you hover over the bar.
Therefore, by resetting the chart every 500ms it saves you from refreshing the page to get another chance of spotting it.

If you don't use my repo and would like to reproduce the bug, do the following:

1. Make sure the body element takes up exactly 100% of the view height
2. Make a chart with tooltip configured with `appendTo: 'body'`
3. Hover over the graph in Safari browser and look closely for the scrollbar (it will only happen first time hovering the bar, so if you didn't see it, refresh page or clear chart and set option again).

I suggest setting a breakpoint whenever the subtree is modified (on the body-element) to see what happens.
