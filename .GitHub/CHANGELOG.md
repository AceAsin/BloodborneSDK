Ace Asin — 01/24/2022

- Included the Bloodborne namespace along with every VRChat class that injects into the Control Panel scripts. This prevents any third party scripts which use VRChat as a namespace from conflicting with Bloodborne.

- The known scripts to cause confliction are crash handler and analytic scripts, which are sometimes located deep inside sub folders, as well as poi scripts. These shouldn't cause anymore problems and users won't have to delete these scripts in order to compile the assembly.

Ace Asin — 01/24/2022

- Fixed a typo on the Responsive Window toggle hover text.

Ace Asin — 01/25/2022

- Finished styling the search section for the new menu, so far users and worlds are incorporated. It includes a search bar with support for the return key, as well as filter and order dropdown menus. You can switch between user, world, and avatar with the toolbar. It supports multiple pages, so it will go on forever, small text will display the current page and total results. At the moment it's set to only load 10 results per page.

Ace Asin — 02/06/2022

- Fixed a bug with the client pipe, wouldn't change to the specified pipe and instead it would always fallback to 0. It's working as intended now, forgot to pass the new pipe after a few changes.

Ace Asin — 02/06/2022

- Corrected behavior on the client pipe, it won't fallback to 0 after any sort of compilation. It starts off at 0 on initial load, but it will remember the new pipe if changed during the session. This mean that any sort of compilation won't affect the pipe order. It will always attempt to connect to the last set pipe.

Ace Asin — 02/06/2022

- Removed shader stripping for Android, since there was still something present that was stripping shaders. There's no longer a toggle and shader stripping is disabled by default.

Ace Asin — 02/07/2022

- Added the ability to remove all illegal components for Android. This will greatly help optimize your Quest compatible avatar. There was a similar function available, but it gets removed after bypassing illegal components, so had to create my own and incorporate it.

Ace Asin — 02/15/2022

- Changed the hover text for all disabled buttons. It now says that you must be a patron or server booster if you want to access those buttons.

Ace Asin — 02/15/2022

- Extended the Bloodborne logger, it will now throw warnings and errors.

Ace Asin — 02/27/2022

- Behavior for the HWID spoofer has been improved. It will now switch to default if no account is connected or if an account that's not authorized is connected. It will switch to the last custom HWID set if an authorized account is connected. It will also not keep resetting after failed authorization attempts due to a new memory backup system that was incorporated.
