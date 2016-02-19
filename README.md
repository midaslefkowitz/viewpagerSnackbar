# viewpagerSnackbar
 
Swiping to dismiss a Snackbar in Viewpager doesn't work because the viewpager intercepts the touch events. See, for example, [this stackoverflow question](http://stackoverflow.com/questions/33502094/viewpager-intercepts-snackbar-dismiss).

I first tried to extend Snackbar, but for some unknowable reason the folks at Android made many of the classes final.

Anyway, I copied the relevant classes and layouts and modified Snackbar to work in a viewpager. My modification is based upon [this stackoverflow answer](http://stackoverflow.com/a/8122642/2590478) to a similar issue.

To use, just copy the classes ([ViewPagerSnackbar.java](https://github.com/midaslefkowitz/viewpagerSnackbar/blob/master/app/src/main/java/com/lefkowitz_dev/viewpagersnackbar/ViewPagerSnackbar.java) and [ViewPagerSnackbarManager.java](https://github.com/midaslefkowitz/viewpagerSnackbar/blob/master/app/src/main/java/com/lefkowitz_dev/viewpagersnackbar/ViewPagerSnackbarManager.java)) and the layouts ([snackbar_viewpager.xml](https://github.com/midaslefkowitz/viewpagerSnackbar/blob/master/app/src/main/res/layout/snackbar_viewpager.xml) and [snackbar_viewpager_include.xml](https://github.com/midaslefkowitz/viewpagerSnackbar/blob/master/app/src/main/res/layout/snackbar_viewpager_include.xml)) into your project. Then use as if its a regular snackbar.

NOTE - you will need to modify [the third line of snackbar_viewpager.xml](https://github.com/midaslefkowitz/viewpagerSnackbar/blob/master/app/src/main/res/layout/snackbar_viewpager.xml#L3) to match your package.
