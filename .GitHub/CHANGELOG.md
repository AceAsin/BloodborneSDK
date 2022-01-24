# Changelog

Ace Asin — 11/18/2021

- Fixed the Shader Stripper toggle and some internal changes regarding the the process of data clearance, now it will not only prevent android shader stripping, but also android post processing stripping. The toggle being used was wrong due to being renamed. The reset cache button was also incorrect and not deleting the correct preference key upon button press.

- The errors were made due to rushed changes and modifications, since it was preventing android shader stripping internally, which left no room for testing. It's another reason as to why it needed to remain private for a while, so that it reached a smaller audience, until it was perfected, but users didn't like that and now the previous release is bugged.

- It should be good moving forward nonetheless.

Ace Asin — 11/18/2021

- The Quest section has been readded, since you can now load into worlds that are up to 100 MB in size.

Ace Asin — 11/18/2021

- Behavior for all rich presence text fields have been fixed, recently noticed a small bug that would set values in real-time, but not update, until any sort of compilation occurred. The bug would occur when the Real Time toggle was disabled, when enabled everything behaved accordingly.

Ace Asin — 11/18/2021

- Fixed some stuff from the Environment section, should now use Default-Skybox.mat by default instead of None when a new Setting.asset file is created. It also now actually saves the object properties to the Setting.asset file, so they'll be the same as you left them when you restart your editor.

- Setting the Skybox to None will result in using the fallback Default-Skybox.

- Setting the Sun to None will result in using the fallback Directional Light.

- If you do not want to display any skybox, then simply uncheck the skybox from your scene toggles.

Ace Asin — 11/18/2021

- The overall performance spoofer has been readded, only use if you don't care and wish to ignore the overall performance stats. It is not intended to work in-game, as your stats will get rescanned, since it's not a modification to the client.

Ace Asin — 11/18/2021

- Added a new favorite star icon to the left of assets, clicking on the star will change the icon from being empty to full, meaning that the asset is now favorited. The new icons are fully dynamic, lots of work and time went into not only aligning them to perfection, but also their functionality.

- The favorited assets will not appear on a new list, they will simply be able to be filtered by favorites. The algorithm's time complexity has also been optimized, so assets should be much more efficient.

- Forgot to change a bool on the last release, which caused a bug when trying to expand the public asset list when holding alt and left clicking. The shortcut enhancement would not work, since it was using the original foldout bool, instead of the more advanced and custom one I created.

Ace Asin — 11/19/2021

- Simplified the way that custom generic dropdown menus got the exact static position, no matter the width/height or responsiveness of the window, no more need for complicated mathematical formulas. They're also not using screen width or the window position properties, since previously they relied on those. These more advanced dropdown menus act and look the same as other original menus, but with some extra capabilities.

Ace Asin — 11/19/2021

- The asset lists will not reset back to the default false upon assembly reloading. This means that when you execute any form of compilation or enter and exit play mode, then the toggle states will remain exactly the same. They will only reset back to the default false if you restart your editor or reset all of your settings back to default. I'm not going to lie that it was kind of annoying having the lists constantly reset.

Ace Asin — 11/19/2021

- Your access permissions will now be remembered per session, once again... assembly reloading or any sort of compilation such as entering and exiting play mode will not reset your access permissions. They will however be updated once you reconnect again. If you disconnect, then the permissions will be reset as usual. If a client is required in order to access some features, then those will remain disabled when unauthenticated. This was also quite annoying, having to wait to connect in order to get access to some features after entering and exiting play mode.

Ace Asin — 11/19/2021

- The filter and search for asset lists have been further improved, will not show empty sub foldout menus for categories if the filter or search don't match any items.

Ace Asin — 11/19/2021

- The buttons for assets have been changed to an action dropdown menu with the same functions. The asset functions and package titles will appear grayed out if the target asset is not downloaded.

Ace Asin — 11/22/2021

- The asset section has been heavily modified, spend a lot of time aligning everything to perfection, pixel by pixel, optimizing and creating new methods. Instead of the asset and client path function buttons, there's now a single button with a gear icon. A dropdown menu with options that have the same functionality as the legacy buttons will appear when you click the new gear icon. The fetch button has also been replaced with a refresh button icon when active and a loading button icon when inactive, it becomes inactive when it's fetching data from the servers. There's a favorite icon all the way to the right side of both public and private lists, decided to give each their own. It's the main favorite toggles for the lists that will display only favorite assets when enabled or all assets when disabled. Over on the asset store assets, they still act as a toggle and only display one asset store author and all of their assets at a time, but the style has slightly changed. They now look like button toggles and behave similar to a toolbar, same effects when a button is in the state of normal, hover, focus, and active. The search bar now has a background to complement the rest of the dropdown labels. The author labels now look a bit different to help distinguish them from the dropdown labels.

Ace Asin — 11/22/2021

- Added the major tag to the version in the setting file and server data, currently it's at v2, so next release will be 2.15.0.

Ace Asin — 11/22/2021

- The world default max upload size has been increased and set to 100 MB, it's multiplied and divided by an integer of 1024, not 1000.

Ace Asin — 11/22/2021

- Preset the Bloodborne background to both the avatar and world prefabs, since it takes a second to load when it's not already preset, don't want to hit anyone with a white background for that duration.

Ace Asin — 11/22/2021

- Fixed a bug that didn't allow users to click the Build & Publish for Android button when it came to worlds.

Ace Asin — 11/25/2021

- Only private releases will contain the new menu as soon as it’s done. It helps you manage everything on your vrc account.

- It’s taking quite a bit, but fairly confident that it will be done soon, with full functionality.

Ace Asin — 12/03/2021

- An End User License Agreement (EULA) will now appear at startup before using the Software Development Kit (SDK).

- The EULA is obtained remotely in case it ever needs to be updated. It requires everyone to accept it once and your decision will be saved in your editor preferences. If it does get updated, editor preferences are deleted, or the editor version changes, then users will have to accept it again, since it will be different than before. If it is declined, then use of Bloodborne will be prohibited and the editor will proceed to exit. If the window is closed or any sort of compilation occurs while it's active and the window becomes out of scope, then the editor will also proceed to exit. It's required and nothing on the control panel will load until it's accepted. If a major change happens with or without notice and the way that the EULA is obtained changes, then all other previous releases will become void. You will need to scroll all the way to the bottom of the EULA in order to be able to accept it. If you are a regular user and don't do anything that's very obviously against Ace Asin or Bloodborne, then you should be fine.

Ace Asin — 12/03/2021

- The Setting option on the Control Panel now better compliments the rest of the Software Development Kit, changes to the UI had to be made in order to achieve this. The bold text that separates sections now have a label background and the box background is now behind the scrollbar.

Ace Asin — 12/03/2021

- Toggle sections are now in the form of a custom dropdown menu, since the amount of toggles are rapidly increasing. This change won't give you tooltip information on text hover anymore, they will be documented instead.

Ace Asin — 12/03/2021

- Added support for 2FA, it was already implemented but having the remember toggle enabled caused issues due to the way things were saved. Nonetheless, methods have been improved and optimized, they are now only making one request when attempting to login. Previously had to make 2 requests, one to validate and save/update preset account credentials or save/update remember me credentials, and another one to actually login. Validation of credentials occurs in the actual login attempt through a special method that handles everything, this makes it easier to handle 2FA and doesn't interfere with anything else or require multiple requests. I encountered a small bug on the preset account, would throw errors when deleting all accounts and being on the selection of the last account, it has been fixed. Previously handled the error by catching it, but after these changes it was clear to me that it still persisted.

Ace Asin — 12/03/2021

- Resetting settings back to default will now also clear your saved user data, meaning that cookies, credentials, tokens, and player preferences will be cleared.

Ace Asin — 12/04/2021

- More bug fixes and optimizations have been made on the login window. The preset dropdown menu is now using editor preferences, instead of a value from the scriptable object, it will better remember it's value if changing between projects. All custom and more advanced generic dropdown menus better handle focus control.

Ace Asin — 12/04/2021

- There are 2 new functions at the bottom of the preset dropdown menu, remove enabled and disabled. It will either remove all accounts which display as enabled or all accounts which display as disabled. If there are no enabled or disabled accounts, then the options will be grayed out and disabled themselves. If you have too many accounts and don't have access to an unlimited amount then removing the enabled accounts will make some of the other disabled accounts enabled. It's a bit confusing, but not much to worry about, resetting the settings back to default removes all of them anyways.

Ace Asin — 12/04/2021

- Separated order options from the filter dropdown on the new menu, where your entire friends list is displayed, so there's a search bar, filter dropdown, and order dropdown. The filter and search can be used in combination with each other, they lower the amount of users that are displayed upon what's searched or filtered. The order dropdown on the other hand helps order users in ascending or descending order, order can be done by display name or friend number count at the moment. It's worth mentioning that multiple filter options can be active at the same time, but only one order option can be active at a time.

Ace Asin — 12/05/2021

- Created a popup window class. It is used to display information when a friend, avatar, or world is clicked.

Ace Asin — 12/06/2021

- Added a moderation section on the new menu, they display all player moderation actions against users. Clicking on a moderation that you made against a target will display a small popup window with actions. It contains a search bar, filter and order dropdown as usual. All moderations displayed have a different background depending if the list index is even or odd. The selected moderation will change the background color for easier identification, support for both dark and light theme.

Ace Asin — 12/07/2021

- Added a toolbar at the bottom of the moderation section. It took me a while to get its functionality working perfectly, since I encountered too many adversities. The toolbar displays page numbers and arrows for easier accessibility.

Ace Asin — 12/08/2021

- Further improved algorithms for the moderation section, now displaying current and total pages, as well as current and total amount of items per page. There's also 2 new buttons for skipping to the start or end of the pages. All filter and order options are now using session states, instead of editor prefs, because users might forget to clear them and might be confused as to why not much is showing once they start a new instance.

Ace Asin — 12/11/2021

- Deleting an item from the moderation section will require the user to right click, it will highlight the active item on the list and a small popup window will appear with a delete button action. It makes a put request and removes the item from the cached/fetched list locally as well.

Ace Asin — 12/11/2021

- Switching accounts will clear the previous account data and fetch new data from the new account, so that local data does not retain older data. Temporary cached files and local dictionary data, such as images and instances will be retained in order to more efficiently exercise requests and to put less stress on your processor.

Ace Asin — 12/11/2021

- Created style sheets and extensible markup language files that utilize the new UIElements found in Unity 2019. They allow content customization without limitations. They're also more optimized, only drawn once and do not spam repaint. They're main creation purpose is to style image buttons on the new menu, but they might have other uses in the foreseeable future.

- Dynamic data that changes, such as images will be handled through internal code, static data will remain on style sheets and extensible markups. If I don't really see the need to have the files, then all new styling will be handled internally as well.

Ace Asin — 12/16/2021

- Made changes to the GUI Builder, it's once again possible to Build & Test/Build & Reload worlds when on an Android environment to check your world size. On both the Avatar and World GUI's all Android defines will be ignored. All GUI checkers are turned off and the build buttons will be enabled no matter what, errors if any will only appear once you click a build button.

Ace Asin — 12/21/2021

- Fixed the offset of the favorite icons, for some reason their position was different once the class library was built.

- Not fixed, seems to keep changing , marked as bug for now.

Ace Asin — 12/21/2021

- Changed the assembly's target framework from .NET Standard 2.0 to .NET Framework 4.7.1, since the API Compatibility Level in Unity is set to .NET 4.x. It was confusing and would prevent the assembly from compiling in Unity after powerful protection technology was applied.

- This change should also stop a dialog from appearing that gives you the option to change the API Compatibility Level. If you followed through with it, then it would change the API Compatibility Level to .NET Standard 2.0, which then prevented the assembly from compiling.

- It's not compatible with .NET Standard 2.0, because Bloodborne relies on dynamic types, which are only available in .NET 4.x.

Ace Asin — 12/21/2021

- The managed dependency UnityNamedPipe.dll has also changed its target framework from .NET Standard 2.0 to .NET Framework 4.7.1.

Ace Asin — 12/21/2021

- Forgot to make changes to the toggles found in the settings for the beta release.  The toggles once again look like they used to in the past.

Ace Asin — 12/21/2021

- Fixed the responsive window toggle, it wasn't working after making some static changes. It gets the dynamic window width once again.

Ace Asin — 12/21/2021

- Fixed some discrepancies regarding dynamic width and resizing of the control panel window. The starting and ending points for the vertical scrollbar on the manager and asset sections have changed. They now better resemble the scrollbar on the setting section. This helps keep content in place by adding flexible spaces, since I noticed that when resizing the window up to a certain point it would cause certain offsets to occur.

- There's also a new toggle called Hide Scrollbar, which does exactly what it says, hides both vertical and horizontal scrollbars, so they do not display at all. It's a nice and simple little feature, scrolling on the other hand will still work with your mouse scroll wheel or a touch pad. I would not hide scrollbars if you are unable to use your mouse scroll wheel or scroll on a touch pad.

Ace Asin — 12/22/2021

- The control panel's banner, toolbar, and signature at the very bottom will no longer stretch when responsive window is toggled off.

Ace Asin — 12/22/2021

- The splash screen window is once again a floating utility window and no longer a normal window, meaning that it cannot be docked, only closed.

Ace Asin — 12/24/2021

- A dialog will appear if the server is down or there's a major change that requires updating in order to use the software.

Ace Asin — 12/24/2021

- Fixed mono behavior scripts not showing their name after obfuscation by excluding them.

Ace Asin — 12/24/2021

- Fixed the default client paths, will now look for both Oculus and Steam directories. The edit function is also fixed, if the path is invalid, then it will not try to open from the invalid path, but instead the base file explorer, so that users can set the correct client path.
