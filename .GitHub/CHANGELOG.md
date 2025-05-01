Ace Asin — 9/12/2023 6:50

- The VRChat Base package is now referencing Newtonsoft.Json assembly version 13.0.0.0 instead of 12.0.0.0.

- Bloodborne and all of it's dependencies are also now referencing Newtonsoft.Json assembly version 13.0.0.0 in order to avoid assembly version validation errors.

- Discord RPC has been updated to the latest release. The .NET Framework has been updated to 4.7.1 in order to match all other assemblies.

Ace Asin — 9/13/2023 17:10

- The control panel is rendered using visual elements now. There's no more responsive window toggle at the moment due to this, but this could change in the future.

- Made necessary changes to the toolbar due to the new builder. The signature at the bottom of the control panel has also been removed but it will still remain on the splash screen.

Ace Asin — 9/22/2023 18:24

- All tab sections of the control panel have been rewritten and are now internal, except for the builder.

Ace Asin — 9/23/2023 12:34

- Added AudioDistortionFilter as an illegal script to prevent errors since AudioSource depends on it.

Ace Asin — 9/23/2023 1:27

- Phys Bone components and transform count are validated separately to avoid removing all of them on runtime. This means that you'll have to abide by the Phys Bone limits before being able to build and publish.

Ace Asin — 9/23/2023 2:25

- Removed the ability to change the banner on the control panel. Replace the Banner.png found in Bloodborne > Asset > Image for now.

Ace Asin — 9/23/2023 2:36

- Bloodborne Thumbnail and Background scripts have been removed since they're no longer needed.

Ace Asin — 9/23/2023 2:45

- Removed the upload component from settings since uploading doesn't enter play mode anymore.

- Removed colorize texture, compress texture, and responsive window toggles from settings.

Ace Asin — 9/23/2023 3:05

- Updated Discord RPC to not show a discriminator of #0000 for users with the new username system. It will only show the discriminator for users who haven't updated their username.

Ace Asin — 10/25/2023 14:15

- Fixed alignment of settings due to new control panel render method.

Ace Asin — 10/25/2023 15:35

- Changed the style of the authentication account window due to new scope layout.

Ace Asin — 12/11/2023 17:10

- VRC is now targeting .NET Standard 2.1 for some reason. Bloodborne will continue to target .NET Framework 4.7.1. There shouldn't be any complications, and if there are then simply switch to .NET Framework on Edit > Project Settings > Player > Other Settings > Configuration > Api Compatibility Level*.

Ace Asin — 12/12/2023 22:46

- Removed the entire Discord folder found inside Bloodborne. It was never required for Discord RPC to function and was causing issues on Unity 2022.

Ace Asin — 12/13/2023 1:04

- Removed unnecessary editor tool's invocation from the logout method that is no longer used.

Ace Asin — 12/13/2023 1:23

- Added a debug toggle that will enable all logging, including API for debugging purposes.

Ace Asin — 12/13/2023 4:23

- Fixed alignment for all icons on the control panel. There's still a bug that will sometimes offset the icons if you're on the console tab during compilation, until you click on the project tab.

Ace Asin — 12/15/2023 1:51

- Fixed a bug that was making the control panel appear blank due to internal code that wasn't removed along with the material and shader used to colorize the banner on an older release.

Ace Asin — 12/15/2023 2:00

- Used Unity 2022.3.6f1 dependencies to build the Bloodborne assembly, since I previously forgot to change the dependencies. The Bloodborne assembly was still referencing Unity 2019.4.31f1 dependencies, and although it didn't cause any issues, it was still bad practice.

Ace Asin — 12/26/2023 13:05

- Fixed an issue that prevented validations from loading, which ultimately prevented users from uploading.

Ace Asin — 1/5/2024 20:45

- Bypassed the builder's accept terms toggle due to someone not being able to see it at all.

- Fixed accidental mistake on last patch that prevented users from seeing how many PhysBones they had while targeting Android.

Ace Asin — 2/14/2024 11:25

- Fixed a bug that failed to find entry points on initial load due to assembly obfuscation. The error was being thrown by Burst due to their ruling, and could safely be ignored. Unity requires specific entry point methods, so an advanced rule was created to exclude those methods from obfuscation.

Ace Asin — 4/14/2024 10:32

- Fixed the height limiter bypass not working on newer releases.

Ace Asin — 4/14/2024 23:32

- Added 2 different toggles, Log for API level logging and Debug for All level logging.

Ace Asin — 4/15/2024 12:50

- Fixed a bug that showed 2 avatar performance options on the settings.

Ace Asin — 4/17/2024 4:11

- Allowed to upload with textures bigger than 8192.

Ace Asin — 4/25/2024 11:07

- Added a new toggle named Experimental Identifier.  This toggle will use Bloodborne's unique device identifier instead of Unity's unique device identifier when authenticating tokens.

Ace Asin — 5/8/2024 2:25

- Set both of the avatar's compressed size and uncompressed size to unlimited for PC.

- Live SDK (3.5.2) avatars have a compressed limit of 500 MB and an uncompressed limit of roughly a bit over 1.2 GB for PC.

Ace Asin — 5/14/2024 20:47

- Removed the original Unity version update message because it looked ugly. It's been added to the account window once logged-in, along with a button that will take users to the exact download page. The software will mark 2022.3.6f1 ➜ 2022.3.22f1 if there's an update. The software will mark the current version 2022.3.22f1 if it's up-to-date. These version numbers are dynamic and will change accordingly, as well as the update button, it'll either be active or inactive.

Ace Asin — 5/15/2024 5:37

- Added a dialog popup window for the Experimental Identifier toggle, warning users of the risks of enabling/disabling the toggle.

- Added the device hash that's being used when communicating with the backend server above the token field. This changes to Unity's unique device identifier or Bloodborne's unique device identifier when enabling/disabling the Experimental Identifier toggle.

- Renamed Experimental Identifier to Persistent Identifier.

Ace Asin — 5/15/2024 9:03

- Moved toggles from Startup to Toggle. The Toggle section is also now able to be minimized.

Ace Asin — 5/15/2024 9:47

- Added a System section with system information. Also created 5 new variables that can be used for Discord RPC ({OS} | {GPU} | {CPU} | {RAM} | {RES}).

Ace Asin — 5/16/2024 5:11

- Fixed the export hotkey that I use for development purposes not working.

- Moved all folders out of the Bloodborne folder and into com.aceasin.bloodborne instead. Although, they have different names, the com.aceasin.bloodborne folder is named Bloodborne in Unity. This made it weird having to go into 2 folders named Bloodborne back to back.

Ace Asin — 5/16/2024 5:37

- Added the ability to change the control panel banner from the settings once again. This option was previously removed when the new builder was introduced, but I found a way to add it back.

Ace Asin — 5/16/2024 6:39

- Removed the Background image asset, it's too large and has no longer been in use.

- Added the Colorize Texture toggle back. This will change the banner image color based on the accent color.

- Improved the behavior of image colorization. The Colorized Texture toggle will colorize both default and custom images if it's been enabled.

- Fixed a slight performance issue when changing the color accent and colorizing the banner, no more need for a delay either that was used to combat this issue.

Ace Asin — 5/16/2024 7:42

- Fixed VRC packages that were marking 3.5.0 instead of 3.5.2 in the package.json file.

Ace Asin — 5/17/2024 7:00

- Changed the style of the toggles to represent an active or inactive button, 4 toggles per row across the width of the settings. I made this change because there were a lot of toggles and they took up a large vertical portion of the settings. It's also better since users are likelier to notice the hover text when hovering over the button-styled toggle.

- Changed the labels in settings to take up 1/4 of the width of the settings.

Ace Asin — 5/17/2024 8:42

- Renamed Generator functions generate and default to create and delete.

- Ace Asin — 5/17/2024 9:33

- Set the default Quest type to Megabytes instead of Bytes.

Ace Asin — 5/17/2024 10:37

- Moved sections Bloodborne and VRChat to a new Release section that's collapsible.

- Created a single field and merged Build and Version into a single string. Moved the cloud icon that executes the update function when clicked on the right side of each field.

Ace Asin — 5/17/2024 13:31

- Moved the Show Avatar Performance Details toggle that's broken on the Live SDK to the Developer section instead of its own Avatar section.

Ace Asin — 5/19/2024 14:34

- Changed the Developer toggles to match Bloodborne's new style toggles and you can now collapse/expand the section.

Ace Asin — 5/19/2024 17:25

- Fixed a bug that caused the Quest type converter from properly changing bytes to megabytes.

- Improved the Quest type converter algorithm to better make changes.

Ace Asin — 5/19/2024 23:56

- Merged sections Color and Control into a new Interface section.

Ace Asin — 5/20/2024 12:42

- Made changes to how assets are fetched. It will no longer try to authenticate the user if they are not authenticated when fetching assets. The user will have to authenticate from the settings before being able to fetch assets, fetch button will be disabled when not authenticated.

- Improved the fetching button state to be realistic to how long it takes to fetch assets by utilizing an editor coroutine.

Ace Asin — 5/20/2024 12:58

- Renamed all button labels to Function in settings.

Ace Asin — 5/20/2024 1:17

- Fixed the user interface text color not working.

- Removed text color picker for now, some styles use custom text colors.

Ace Asin — 5/20/2024 2:50

- Removed the Internet Protocol toggle, each network row has its own visibility icon toggle on the right side.

- Improved the way the numbers are hidden, instead of marking 0.0.0.0, it will not show the exact address number length but replaced with zeros.

Ace Asin — 5/20/2024 2:59

- Improved the persistent identifier algorithm even further, more properties are considered. This will change anyone's current experimental identifier on the next release.

Ace Asin — 5/20/2024 3:37

- Increased clickable icon margin. The clickable area is now 20 x 20 px.

- Fixed margin on other clickable icons that were offset.

Ace Asin — 5/21/2024 1:38

- Improved the upload limiter bypass behavior. It will now be persistent throughout compilation and authorization. It would previously not set the values after compilation or authorization, forcing users to set the values again.

- Updated the information on the builder for the upload limiter warning. It will now also display what the current upload size limiter is set to when the toggle is enabled. It will tell you that it's set to unlimited if the toggle is disabled.

Ace Asin — 5/21/2024 8:17

- Updated the compressed upload size limiter for PC and Quest to automatically be set to unlimited when authorized and limited when unauthorized.

Ace Asin — 9/3/24 4:04

- Removed the upload limiter bypass since it stopped working and all uploaded avatars that are above the limit will stop working in the future.

Ace Asin — 2/21/25 7:23

- Fixed and improved illegal scripts on the builder. The illegal scripts counter will now display the correct number. The select and auto fix buttons will not log multiple times anymore and are both warning log messages now that will display the correct information.

Ace Asin — 2/21/25 8:06

- Changed and improved missing scripts on the builder.

Ace Asin — 4/26/25 6:29

- Fixed the performance button on the developer section to reset avatar issues on button click. It would previously require users to recompile in order to reset the avatar issues on the builder.

Ace Asin — 4/26/25 9:54

- Added new buttons to the Developer section, Detail-Preserving Image Downscaling (BETA), DPID Conservative, and Execute Constraints In Edit Mode. Excluded Dry Run, as there's really no point in users enabling that option.
