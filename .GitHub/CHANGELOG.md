Ace Asin — 12/06/2022

Fixed a bug that prevented more than 2 preset accounts from being selected for patrons.

Improved the preset dropdown menu behavior. If you are unauthorized, then instead of the last preset account staying the same, it will now set the preset account to none.

Ace Asin — 12/06/2022

Changed the visibility icons for settings from off and on to minus and plus.

Ace Asin — 12/06/2022

Made minor improvements to the Asset Bundle Loader.

Ace Asin — 12/06/2022

Fixed a bug that displayed the wrong hover text for the Discord component on the settings.

Ace Asin — 12/06/2022

Changed the accessibility of some dropdown menus. The dropdown menus for both the Discord and Quest components will now be disabled when unauthorized. They will only be enabled when authorized.

Ace Asin — 12/07/2022

Improved the overall behavior of your rich presence. The behavior on the buttons is better, they will be enabled or disabled depending on what you type. You must be connected to Discord RPC and authorized as a server booster, premium member, or patron if you want to change your custom rich presence.

Ace Asin — 12/10/2022

Patched the original Assets > Export Package... method so that it supports UPM. It's not really needed at the moment, but in the future, it will help creators export their avatars with Bloodborne SDK when it's moved to the Packages folder. It is a built-in feature so it will only work when using Bloodborne SDK.

I worked hard on this Unity patch because I know that some creators would like to include an SDK when distributing avatars to Gumroad, Payhip, Booth, etc... I remember seeing a post about creators not being able to include an SDK with their avatars. I hope that this patch lays those concerns to rest.

It's worth noting that you'll have to select the main folders from the left side of your Project tab to be able to export from both Assets and Packages at the same time.

Ace Asin — 12/11/2022

Fixed a bug that prevented Discord RPC from auto-reconnecting after getting disconnected. In the past, after making some changes, the delay couldn't get the integer. It had to be called from the main thread.

Ace Asin — 12/11/2022

Commented out a debug line that message logged content that was deleted since it seemed to spam it.

Ace Asin — 12/18/2022

Updated obtained information from the backend server. Added Gesture Manager to the Asset tab. This was a remote update, and no changes are required.
