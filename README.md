# Issue with tabbed search

While working on a project recently, I encountered an issue where a `UITableViewController` with a `UISearchController` embedded in a `UITabBarController` disappears from the view hierarchy under certain situations, as described here:

* `UITabBarController` embedded in a `UINavigationController`
* `UITableViewController` added to `UITabBarController`
* `UITableViewController` has a `UISearchController` with itself as the search results controller (set to `nil` on instantiation)
* When the `UISearchBar` text field has focus and the tab is changed, next time it is displayed the table view is no longer displayed.

This is shown in the following screens:

* Screen #1: initial table view controller w/ search
* Screen #2: focus on search bar text field
* Screen #3: switch to different tab
* Screen #4: switch back to tab w/search, table view is missing
* Screen #5: tapping cancel on the search bar removes the search bar from the view

Screen #1: Here is the initial table view controller w/ search

![alt text](https://raw.githubusercontent.com/jonstjohn/TabbedSearch/master/img/tab_screen1.png  "Screen 1")

Screen #2: Focus on search

![alt text](https://raw.githubusercontent.com/jonstjohn/TabbedSearch/master/img/tab_screen2.png  "Screen 2")

Screen #3: Tap on first tab

![alt text](https://raw.githubusercontent.com/jonstjohn/TabbedSearch/master/img/tab_screen3.png  "Screen 3")

Screen #4: Tap back on tab with search, note missing view controller

![alt text](https://raw.githubusercontent.com/jonstjohn/TabbedSearch/master/img/tab_screen4.png  "Screen 4")

Screen #5: Tapping cancel removes search controller

![alt text](https://raw.githubusercontent.com/jonstjohn/TabbedSearch/master/img/tab_screen5.png  "Screen 5")

