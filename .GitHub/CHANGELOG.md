Ace Asin — 04/04/2023

- Created a custom Bloodborne package in the Packages folder. This is where Bloodborne version 3.0.0 will reside moving forward. The legacy residence was the Assets folder.

- Added Bloodborne references to VRC asmdef editor files.

Ace Asin — 04/04/2023

- Added the same com.unity.nuget.newtonsoft-json dependency version that the VRChat base package uses to Bloodborne. This will prevent any strong named errors that some encountered in the past.

Ace Asin — 04/11/2023

- Optimized the content manager for your avatars and worlds by removing unnecessary code.

- Improved the auto-updater. It will now check the version instead of the date. It previously caused issues when I made minor patch updates since I don't have to update the date on the library.

- Changed the description of the prompt windows.

Ace Asin — 04/11/2023

- Optimized the code for Discord RPC.

- Fixed a bug that caused the Discord RPC auto-reconnect retry amount to reset every time the control panel was focused.

- Fixed a bug that attempted to auto-reconnect the previously failed pipe when you switched pipes and connected to another. This bug only occurred when connecting to different clients very rapidly during the time it waits to attempt another auto-reconnect. It caused an auto-reconnect loop for the new client, even after it was already connected.

- Changed the number of retries to 20 every 15 seconds for a total duration of 5 minutes. This is especially low and will likely not cause a stack overflow crash error.

- Improved the behavior of auto-reconnect. If rich presence is disabled, it will stop trying to auto-reconnect instantly. If a client is successfully connected, it will reset the number of auto-reconnect retries and attempt to auto-reconnect once again until its capacity is reached. It will also reset the number of auto-reconnect retries if any manual connection is attempted.

- These changes were put in place to prevent and stop the stack overflow crash error caused by auto-reconnect.

Ace Asin — 04/12/2023

- Improved and optimized the placeholder text for all fields. The placeholder text will automatically be removed as soon as you begin typing. Although the placeholder text was automatically highlighted, there's no more need to clear the placeholder text before typing.

- Noticed that it was kind of scuffed on certain fields, but it's not a big issue. I don't have the time to make it better at the moment, so it'll have to wait for a future update.

Ace Asin — 04/12/2023

- Added Discord RPC support for Linux and macOS, hopefully, they work fine. Unable to test Linux, but it should work fine, and macOS seems to run into problems after a while. I had to build a NativeNamedPipe.so and NativeNamedPipe.bundle artifact.

Ace Asin — 04/13/2023

- Patched the original Assets > Export Package... method, and it now supports UPM. It allows creators to export their avatars with Bloodborne included. You'll have to select the main folders from the left side of your Project tab. This will allow you to export from both Assets and Packages.

Ace Asin — 04/13/2023

- Made changes to the remote version file, so expect some things to stop functioning.

Ace Asin — 04/13/2023

- Removed a lot of SDK2 code that wasn't used anymore since it's no longer supported.

- Removed the date from Bloodborne and VRChat at the bottom of the settings.

- Renamed SDK3A to Avatar and SDK3W to World at the bottom of the settings.

- The definitions SDK3A and SDK3W will still be used on the title of the packages, auto-update prompt windows, and rich presences.

Ace Asin — 04/13/2023

- Fixed a small GUI alignment issue on the builder for SDK3W. Forgot to remove a section of VRChat's unaligned code. It had gone unnoticed for 3 releases.

Ace Asin — 04/13/2023

- Hid the warning that tells you that a world is too large to upload. It will only display the warning after attempting to build a large world, and it's gotten its size.

Ace Asin — 04/13/2023

- Removed the developer and secure bool from the Setting.json file. Decided to make these internal instead, and it looks much cleaner. They were only there for development purposes in the early stages.

Ace Asin — 04/13/2023

- Fixed an issue that wasn't properly setting a banner for the splash screen and control panel when detecting changes on the scriptable object.

Ace Asin — 04/13/2023

- Added a new method that will get the year on the signature that is located at the bottom according to your system date.
