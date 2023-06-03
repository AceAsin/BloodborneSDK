Ace Asin — 05/04/2023

- Removed the NativeNamedPipe.bundle artifact for macOS since further development is still required.

Ace Asin — 05/05/2023

- Added a visibility toggle icon on the password field that allows users to show or hide their password.

Ace Asin — 05/05/2023

- Added a CapsLock notification below the account window that notifies users  when CapsLock is turned on or off, only works for Windows at the moment.

Ace Asin — 05/05/2023

- Removed the function line that has an update/save and remove button on the account window.

- Added  a save icon on the username field that allows users to save and update their preset accounts.

- Added a dialog window with options to create/cancel or update/delete/cancel.

- Added hover tooltip text to both of the save and visibility toggle icons.

Ace Asin — 05/06/2023

- Removed the component section on the settings since it doesn't serve a point anymore.

Ace Asin — 05/06/2023

- Removed the BloodborneAssetBundle script since you can just do the same thing through the settings.

Ace Asin — 05/06/2023

- Fixed a bug that caused the custom image or video to not display on the upload panel.

- Fixed a bug that caused the custom video to not use the volume slider from the settings on the upload panel.

- Made changes and improvements to the BloodborneBackground script.

- Made changes and improvements to internal methods that allow me to modify the VRCSDKAvatar, VRCSDKWorld, and VRCCam prefabs completely. This workflow saves a lot of time by not having to manually modify the prefabs for production.

Ace Asin — 05/07/2023

- Made changes and improvements to the early access auth window. The window is only present on early releases to deny access to unauthorized users.

- Added social buttons on top of the early access auth window that are the same as the ones found on the splash screen.

- Removed early access through the client. This was the old method that granted access through DIscord RPC client pipes. It will still remain present as an alternative method of authorization on official releases, but it will soon be deprecated in the future.

- Added early access through the server. This is the new method that grants access with the utilization of the JSON Web Token system.

- Added a lock icon instead of text for the auth window button that grants access.

- Removed early access internal code related to testers as they have no longer been needed since deprecated.

Ace Asin — 05/07/2023

- Optimized the enter/return keypress detection on the account window that's used to login.

- Added the enter/return keypress detection to the auth window that displays on early releases.

Ace Asin — 05/07/2023

- Made slight changes to the control panel window width. The option toolbar was offset by a bit using the default width.

- Fixed an alignment issue on the account window.

Ace Asin — 05/07/2023

- Added a shortcut that will center the control panel window when pressed. It will be included on the GitHub README.

Ace Asin — 05/08/2023

- Improved the behavior of the remember me toggle. It would only remember the last typed credentials after a successful login. It will now remember the last typed credentials without having to login. These are remembered per session so they won't be remembered after restarting the editor. This is useful after compiling so that it doesn't clear your credentials. It can get quite annoying having to type your credentials every time you compile.

Ace Asin — 05/08/2023

- Redesigned the 2FA window, lots of changes and improvements.

- Removed the help button and description.

- Moved the verify button to where the help button was previously located.

- Added a waiting/loading icon when attempting to login and animated it.

- Added the ability to login by key pressing enter/return. It was already implemented on the main window, but not the secondary 2FA window. I hated not being able to verify the code with enter/return.

- Added a user label and field for the user that's trying to be authenticated.

- Added a code label and field for users to type in their app or email code.

- Added a help icon button on the right side of the code label. It will display a dialog window with an app or email description, along with button options to cancel and link you to the help docs. Hovering over the help icon button will tell you if it's looking for an app or email code in case you don't want to click the button and display the dialog window.

- Added a notification that will display below the window for a short duration if the code entered is valid or invalid.

- Improved the cancel button. It will clear the code if you press the cancel button and go back.

- Improved behavior of the verify button. It will be disabled if an invalid code is entered or when the code is successfully verified.

- Improved behavior of the code field. It will be marked red if an invalid code is entered. It only accepts numbers and they must be 6 digits in length, with the exception of spaces and dashes in the middle, empty spaces at the beginning or end will get trimmed.

- The code text field will be disabled, along with the help button on the right side when it's checking that the code is valid.

Ace Asin — 05/09/2023

- Fixed the width behavior for assets, and made the dropdown menus 50% width at all times, even with responsive window toggled. They were taking up almost 75% of the entire width before.

- Fixed the behavior of the client and asset sections. The width for the path and server labels are now 50%.

- Fixed the behavior of certain elements so that they don't seem glitchy when resizing while the responsive window is toggled.

Ace Asin — 05/10/2023

- Fixed a bug that caused the clear user data warning to show after creating/updating a preset account and resetting the cache.

Ace Asin — 05/10/2023

- Added the ability to dynamically change early access roles from the server. I plan to share the alpha release to patrons that are subscribed to the second tier.

Ace Asin — 05/10/2023

- Removed Config/Setting.json from Bloodborne since it's no longer needed due to the new package.json files.

Ace Asin — 05/10/2023

- Improved the custom export script and made it internal instead of a separate script on my projects. It will definitely improve workflow and speed up the distribution process.

Ace Asin — 05/12/2023

- Changed the style of dropdowns on the asset section.

Ace Asin — 05/13/2023

- Improved the cancel button for the search bar on the manager and asset section.

Ace Asin — 05/21/2023

- Redesigned the content manager section.

- Fixed the image to better fit the button.

- Added a settings icon on the top left of the image to copy, link, update, or delete the avatar/world.

- Removed all previous function buttons, manage avatar/world with the settings cog wheel.

- Added more information such as name, description, along with identification, release, platform(s), and version.

- Changed the list order to avatar, world, test.

Ace Asin — 05/24/2023

- Changed the log text to change color dynamically. It wouldn't change automatically before, only until some sort of compilation occurred.

- Renamed log to accent for the color component, as it's now being used for other things.

- Created a special shader and material for better performance that help in generating a banner/background with custom hue, saturation, and value depending on the accent color.

- Added a new colorize texture toggle that will be used to change the banner/background color. It will be disabled by default, but enabling it once will make the editor remember it on all projects. The banner and background are both changed at an interval of 15000 milliseconds (15 seconds) after detecting accent color changes for better performance.

Ace Asin — 05/24/2023

- Added the hide scrollbar toggle to the default button that resets everything since it was missing.

Ace Asin — 05/25/2023

- Fixed a bug that caused the auto update toggle to not reset back to default.

Ace Asin — 05/25/2023

- Changed the startup behavior for auto update and splash screen. Seeing popups after every compilation can get quite annoying, which only causes the user to disable the startup toggles altogether. This change will now only open startup toggles on the initial startup of your editor application since it's remembering the startup toggles per session.

- Fixed the startup toggles from starting while the application is playing.

Ace Asin — 05/25/2023

- Created a shortcut key to toggle the scrollbar.

- Created a shortcut key to reset settings back to default.

- Created a shortcut key to collapse/expand all settings.

Ace Asin — 05/25/2023

- Changed the accent color to be remembered by the editor since it's the most common. This only affects the accent color, all other colors will continue to be cached per project.
