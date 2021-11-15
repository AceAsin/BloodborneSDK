# Changelog

Ace Asin — 08/30/2021

- Shaders are no longer getting stripped for Quest/Android, should work the same as release version 9.0, these include standard, legacy, rero shaders, and more.

Ace Asin — 08/30/2021

- Fixed a bug where the Discord RPC HH, MM, and SS placeholders were not marked as empty or null.

Ace Asin — 08/30/2021

- When you select a pipe, the username, discriminator, and id of the target account will appear immediately if a client is opened when you launch your editor. It's useful so that you know which pipe belongs to which account. It's dynamic, so the user information should appear and disappear as you open and close a client. You won't be able to connect to an account if the client pipe is considered null, meaning that no client exists for that specific pipe. The text color will also appear gray if a client exists but it's disconnected or unauthorized. If the client exists and it's connected, as well as authorized, then the user text color will appear as white.

- Worked hard to optimize multiple clients to the best best of my ability, since previously they were just too buggy and caused too many problems. That's why I only allowed and worked with one client at a time before, this time around multiple clients seem more stable.

- It might take a while for the user information to show if you just launched or compiled in your editor, or perhaps you just opened a new client, so just wait patiently. It can take up to 15 seconds, sometimes even more, but this usually only happens during development, should be instant for everyone during production. After you've been authorized, then you should be good to go and all custom features will unlock for authorized users.

Ace Asin — 08/30/2021

- The search bars for the manager and asset toolbar sections will now show a little x icon, clicking it will clear what's on the search bar and set the focus control to null.

Ace Asin — 08/31/2021

- The control panel is now completely responsive when the window is docked. I hadn't really ever noticed this, because I never docked the control panel and always had it floating on it's own. The menu looked completely broken when resizing it past it's fixed width. It will now rescale accordingly and everything will look fine. Ended up coding a method to detect when the window is docked, just to fix a few unalignments when docked.

- A lot of the issues had to do with my methods being mixed with VRC's original methods, which have a lot of useless code that can be overly simplified, removed a lot of their garbage in order to make the control panel 100% responsive.

Ace Asin — 08/31/2021

- The Shader System toggle has been removed when targeting Android/Quest, as it was kind of useless, bypass did not work correctly. Now there is no shader stripper by default when it comes to Android/Quest, completely bypassed those limiters, won't be needing that option anymore. It only served as an experimental option and after confirmation it proved to serve no purpose as there were no changes when having it checked or unchecked.

Ace Asin — 08/31/2021

- Previously had changed the clear console hotkey method for testing purposes and never changed it back, so it hasn't been working. Fixed the issue and reverted those changes, working fine once again.

Ace Asin — 08/31/2021

- You are now able to login by pressing the return key, so enter after you type in your credentials on the authentication window. It's mainly a really simple feature that I wanted to implement.

Ace Asin — 08/31/2021

- The authorization window has been slightly improved, such as sign in button being disabled when there's no credentials typed, also setting the focus control to null after a login attempt.

Ace Asin — 09/01/2021

- Added an auto reconnect button toggle for the client component, it's enabled by default. There's also been a few client authorization improvements and bug fixes.

Ace Asin — 09/02/2021

- The GUI initializes less styles and is now more efficient, removed and cleaned up a lot of the GUI styles.

Ace Asin — 09/03/2021

- Added an auto connect button toggle, same as the previously added auto reconnect button toggle. It's recommended that you keep both of these button toggles enabled, so that you don't encounter any authorization issues.

Ace Asin — 09/07/2021

- Changed content for the overall performance spoofer, should allow you to set it back to none now. Depending on your settings the buttons will either be active or inactive, helpful hover messages also dynamically change. It won't allow you to set a new performance option if it's already set to the one you're trying to set.

Ace Asin — 09/08/2021

- Removed unnecessary log from when you delete a package, previously forgot to remove it during development.

Ace Asin — 09/08/2021

- Assets are now more compact when there's more than one asset per author, previously there was a separator in between assets. There's also now a new asset list for the asset store packages that are in your Asset Store-5.x folder. Anything that you download from the Asset Store will show on this new list.

Ace Asin — 09/08/2021

- Quick remote fix, screen freeze shader wasn't properly named on the asset list and had no version tag. The download from the server would always fail due to this mistake on my part. The cache from the load balancer is currently invalidating as I speak, it will properly show after it's completed.

Ace Asin — 09/08/2021

- Styles are now pre-initialized when calling them, they will no longer need to be initialized and assigned their properties, will prevent any potential errors from occurring.

Ace Asin — 09/09/2021

- Splash screen data is now acquired remotely from the dedicated host, which makes it possible to update it whenever and the changes will display for everyone. The splash screen menu has also been optimized by reducing the amount of update calls.

Ace Asin — 09/25/2021

- Your latest build avatar or world size will now constantly be shown by reading the custom.vrca and customscene.vrcw files that are modified after building and compiling. The avatar and world api must be true in order to show the size with the rest of the avatar or world settings on the builder, meaning that you attempted to upload and a blueprint id was created or you attached a valid blueprint id.

Ace Asin — 09/25/2021

- Added a real time toggle option, having it enabled will update your rich presence without having to click the update button in real time. Decided to leave the update button intact when real time is enabled, just in case users might want to reset some settings, such as the elapsed time. Also incremented the end duration by 1000 ms, since previously discord set an offset of 1000 ms by default. It's just to combat that little misconception and equilibrate the elapsed time. The start duration seems to be fine, no offset was detected.

Ace Asin — 09/25/2021

- The toggle buttons for the client, auto connect and auto reconnect will be removed and kept enabled by default for now, because I already know that they will only cause issues for some users. They will be added at a later time, since I need to figure out a way to make them more readable and simpler to use, probably by adding potential warnings or dialogs when attempting to change them.

Ace Asin — 09/30/2021

- Made progress on the new menu to manage everything on your account directly from the SDK, utilizes VRChat's API. The design is complete and open to change in the future.

Ace Asin — 10/07/2021

- Greatly optimized fetching friend list and loading data, toggle to load user images on initial load to help towards performance in slow computers, by default it'll be set to off, since a user might have a large friend list.

Ace Asin — 10/08/2021

- There was a whitelist already implemented for development purposes, but now there is also a blacklist. If you for some reason become blacklisted, then you won't be able to use future software development kits anymore. It's detected by your discord user id and vrchat user id. The unity editor will simply force quit on blacklisted users to prevent further use.

Ace Asin — 10/10/2021

- Decisions have been made regarding exclusive content, some things might get moved around, but nothing has become final. They will also be open to change in the future, please understand and respect any decision that is made.

Ace Asin — 10/10/2021

- Added back the original VRC Check For Updates menu method.

Ace Asin — 10/10/2021

- Fixed a bug on newer software development kits regarding a missing animator, their no error boolean wasn't working properly, would cause the entire builder to break and throw error.

Ace Asin — 10/10/2021

- The wrong unity version message will be hidden on the authentication section, but will still appear as an error on the builder when you attach a descriptor.

Ace Asin — 10/10/2021

- Alpha releases will be on a trial for testers moving forward, since they are only really meant to test features and make sure that they function. Patron's on the other hand will be able to use early releases for as long as they remain a Patron with no trial limit.

Ace Asin — 10/12/2021

- Toggle options on the setting section will now be listed in alphabetical order, new and experimental force fallback option has also been added.

Ace Asin — 10/12/2021

- You are now able to change the skybox material through the setting section for easier accessibility. Also added the sun source selection option just in case anyone needs it.

Ace Asin — 10/14/2021

- There was a bug with the quest limiter, after compiling anything it utilized the default values. This prevented some users from uploading if their avatar was above 10 MB or their world was above 50 MB. It was a simple fix, set the default values to be updated with the custom values on initial load, so that after compiling anything it would utilize the custom values.

Ace Asin — 10/14/2021

- Noticed another bug, the world limiter toggle was using the avatar limiter toggle instead of it's own. It's been fixed and it's now using it's appropriate toggle.

Ace Asin — 10/14/2021

- Small bug with the cached asset bundles when trying to read the most recent avatar or world sizes, will now delete the key if an error is thrown, as well as not display the asset bundle size for the avatar or world when the bool that is returned equals false.

Ace Asin — 10/14/2021

- Fixed the responsiveness of some toolbar buttons when docked that I had forgotten.

Ace Asin — 10/16/2021

- Added 2 new toggles, Bypass Shader and Force Fallback, under a new category named Experimental. These are in development and need to be tested before making them official. The Bypass Shader toggle will definitely work, as it's just a toggle to allow or deny Standard, Legacy, Particle, etc... shaders, but I did some changes, so it still needs to be tested again.

Ace Asin — 10/16/2021

- When the cache default button is clicked, all toggles will also be reset back to normal.

Ace Asin — 10/16/2021

- Fixed a few offset imperfections for the user interface, a new scrollbar style has also been created and slightly modified.

Ace Asin — 10/19/2021

- All 3 builds are finished and have been updated to Unity 2019.4.30f1.

Ace Asin — 10/20/2021

- If you're not authenticated as a patron or tester, then the new experimental toggles, bypass shader and force fallback will be set back to the default false right before uploading as a security feature.

Ace Asin — 10/21/2021

- Now using editor coroutine method to properly run authorization more efficiently after you connect or try to reconnect.

Ace Asin — 10/21/2021

- Texture size limiter toggle has been added for Avatar 3.0, toggle will fix and compress expression parameter menu images.

Ace Asin — 10/21/2021

- There's now infinite parameters, previously forgot to check something which is why I couldn't get them working.
Ace Asin — 10/22/2021

- New custom settings have been added for the infinite expression parameters and controls, after making changes to these settings a dialog window will popup with an option to recompile scripts now or at a later time. Script compilation requests are required and must be done on each project, since PlayerPrefs are being used and the ScriptableObject needs to be enabled again. The new section will only show up if you're working on an Avatar 3.0, since that's the only build that has access to expression parameters and controls. Everything on the editor is responsive and working well, you will also notice that it's very similar to the Quest section, still needs to be tested in-game just to make sure that they work.

Ace Asin — 10/22/2021

- Individual toggles for Discord RPC will now be locked for server boosters only. If you're not a server booster then you won't be able to edit the custom Discord RPC text fields or toggles, only the main Rich Presence toggle that's at the top, which shows and hides Discord RPC.

Ace Asin — 10/26/2021

- The experimental toggle Bypass Shader has been renamed to Force Shader.

Ace Asin — 10/26/2021

- Made some changes and improvements to the responsiveness of the control panel window, everything should be more efficient and should prevent a previous bug from occurring. There's also a new toggle named Responsive Window, which will stretch the width accordingly and make the control panel responsive, having it unchecked will use fixed width sizes in case users run into any issues. The Splash Screen by default is responsive and will stay responsive no matter what, since it's not meant to be docked.

Ace Asin — 10/27/2021

- Fixed alignment issues on content and builder, also moved some stuff around and made improvements to the builder, everything is actually aligned to pure perfection now.
Ace Asin — 10/28/2021

- New cryptography cipher class has been created to encrypt and decrypt credentials, since I'm adding a new account management system. The security feature was created just in case someone with malicious intend gets a hold of your preset key, to prevent them from stealing your information as a precaution. Information in the key will be encrypted, so you won't have to worry even if someone manages to obtain and read it somehow.

Ace Asin — 10/30/2021

- There's a new account management system, so you can add preset accounts, which is pretty poggers, not gonna lie. On the main account window, there will now be a preset dropdown menu with saved accounts. It will be completely disabled if there are no saved accounts. There is also 2 new buttons, save/update and remove which can be used to manage your saved accounts. You can save/update and remove an unlimited amount of accounts whenever you want, whether they will load the preset credentials is another thing entirely. If you are not a Booster or Patron, then you'll only be able to load the credentials for the first account. If you are a Booster, then you'll be able to load the credentials for the first 2 accounts, so that'll be your main and alt. If you are a Patron, then you'll be able to load all saved accounts with no limitations.

Ace Asin — 10/31/2021

- Created a new custom dropdown menu for the saved accounts, since it was required to make it more dynamic. If you are unable to access some saved accounts due to not being a Booster or Patron, then they will be disabled and grayed out. It is extremely responsive and efficient, checking and handling errors, as well as everything else accordingly.

Ace Asin — 11/01/2021

- Added a remember me toggle on the login window, will remember your most recent login credentials if valid and automatically fill them out if they're null when you load the window again.

- It works different than the original credentials loader. For that one when you're already logged in and load the window again, it will automatically fill your credentials and login, but if you logout then it deletes your credentials and doesn't remember them.

- This is why the new remember me toggle is an addition and works hand in hand with the preset account management system.

Ace Asin — 11/01/2021

- More information has been added to the account window once logged in, as well as useful buttons. The buttons will copy to the clipboard and display notifications, open a dialog with the type of upload status, and open an external link to your account. I don't want to add too much on this window, as that is something that will be added to the new menu very soon, but it is open to change in the future.

Ace Asin — 11/03/2021

- The recent new data that has been added will reset back to default settings when you click the default reset button. This will include the entire account management system account list, remember me username and password, as well as newly implemented toggles.

Ace Asin — 11/03/2021

- The bug in which asset lists that are not being targeted were opening has been fixed. This was due to using fixed positions and only working properly when opening one asset list at a time, not multiple asset lists. It's been corrected and shortcut enhancements for the foldout/dropdown menus should work flawlessly with multiple opened, since it is now getting and being based on the last rectangle position.

- If you didn't happen to know, the shortcuts enhancements for asset lists are LEFT/MIDDLE/RIGHT MOUSE BUTTON and ALT + LEFT/MIDDLE/RIGHT MOUSE BUTTON, holding down the ALT key will expand and collapse all asset lists. The shortcut enhancements are similar to the hierarchy and work the same.

Ace Asin — 11/03/2021

- Early releases already cause your editor to exit if all pipes fail, but now there's a retry limit of 4 attempts, equivalent to the number of available pipes, just in case you're trying to connect to the same pipe more than once and continuously fail due to not having access to early releases. Also, when attempting to upload on early releases, authorization will be required or else the upload will fail in case some users manage to get past the first authorization window somehow. You won't be able to access the rest of the control panel without authorization first on early releases anyways.

Ace Asin — 11/03/2021

- Forgot to mention this before, but if your Api Compatibility Level is set to .NET 4.x, then you'll be stuck on it, since Bloodborne SDK is preventing users from switching to .NET Standard 2.0. If you switch, then Bloodborne SDK won't work, so there's no point in allowing users to switch, will be reverted back to prevent any issues.

- It does not work if you're already on .NET Standard 2.0, because Bloodborne SDK is unable to compile its assembly. You will have to manually change your Api Compatibility Level to .NET 4.x.

Ace Asin — 11/03/2021

- ~~Moving forward you will be required to be authenticated before uploading or else an error dialog message will appear. It's for security reasons, so that I prevent blacklisted users from using the software development kit. It won't tell you to connect to a client or user, that only happens on early releases, but it's expected when uploading. This doesn't particularly mean that you have to be on the server, that's just if you want to have access to the public asset list. You simply need to be connected to discord so that the backend server can verify your id and make sure that you're not blacklisted.~~

- In second thought the public and private releases will not be needing authorization, only early releases, since I need to verify if users are a patron or tester. I made some changes and official releases will remain the same, so as everything is at the moment.

Ace Asin — 11/04/2021

- Testers will now also have temporary beta access, since it’s also considered an early release, previously testers only had temporary alpha access.

Ace Asin — 11/04/2021

- The Discord RPC callbacks for detecting when you're building and uploading have been improved, also when changing the active avatar and world variables.

Ace Asin — 11/04/2021

- A retry/delay dropdown menu with 4 options has been added to the client section. The options will be 15/30/45/60, which will mark the amount of seconds to wait before attempting to reconnect in case of a disconnection.

Ace Asin — 11/04/2021

- Created a webhook class that will allow users to create and send custom embed message webhooks after an action is completed or upon request in the future.

Ace Asin — 11/05/2021

- The log type has changed, using logger instead of debug with a prefix type now.

Ace Asin — 11/08/2021

- Fixed focus control coming from the new dropdown menu still remaining after login, it was getting applied to the first button in ascending order.

Ace Asin — 11/08/2021

- The shader blocking system for Android/Quest is now available to everyone, it's also been renamed to Shader Stripper.

Ace Asin — 11/08/2021

- The Spoofer and Android/Quest sections have been disabled and won't show at all anymore, since they will be completely overwritten in-game by the client.

Ace Asin — 11/08/2021

- Forgot to mention that the unlimited expression parameters and controls were temporarily disabled until further notice. I will eventually attempt to get them to work, if not possible then I'll add a different method which doesn't allow unlimited expression parameters and controls to work, but it does allow a lot more.

Ace Asin — 11/08/2021

- The Responsive Window toggle will be disabled by default, due to users having issues getting the correct screen width. I am unsure as to why this happens, might just have to do with the user's monitor and resolution.

Ace Asin — 11/08/2021

- The experimental toggle Force Fallback has been removed on official releases, as having the special fallback tag doesn't seem to affect anything. Shader Stripper is now an official toggle and has been moved from the Experimental section to the Toggle section.

Ace Asin — 11/10/2021

- Fixed a condition bool on the authentication window which shows and hides the advanced setting API and it's dropdown menu. It wasn't able to handle multiple lines of code due to missing the open and close braces. A temporary fix at the moment is to go to Setting > Developer > Extra and enable the toggle.

Ace Asin — 11/11/2021

- The GUI focus control will now be set to null when switching between toolbar options, this will help prevent carrying over the focus control from custom generic menus.
