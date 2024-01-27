Ace Asin — 09/12/2023 6:50 AM

- The VRChat Base package is now referencing Newtonsoft.Json assembly version 13.0.0.0 instead of 12.0.0.0.

- Bloodborne and all of it's dependencies are also now referencing Newtonsoft.Json assembly version 13.0.0.0 in order to avoid assembly version validation errors.

- Discord RPC has been updated to the latest release. The .NET Framework has been updated to 4.7.1 in order to match all other assemblies.

Ace Asin — 09/13/2023 5:10 PM

- The control panel is rendered using visual elements now. There's no more responsive window toggle at the moment due to this, but this could change in the future.

- Made necessary changes to the toolbar due to the new builder. The signature at the bottom of the control panel has also been removed but it will still remain on the splash screen.

Ace Asin — 09/22/2023 6:24 PM

- All tab sections of the control panel have been rewritten and are now internal, except for the builder.

Ace Asin — 09/23/2023 12:34 AM

- Added AudioDistortionFilter as an illegal script to prevent errors since AudioSource depends on it.

Ace Asin — 09/23/2023 1:27 AM

- Phys Bone components and transform count are validated separately to avoid removing all of them on runtime. This means that you'll have to abide by the Phys Bone limits before being able to build and publish.

Ace Asin — 09/23/2023 2:25 AM

- Removed the ability to change the banner on the control panel. Replace the Banner.png found in Bloodborne > Asset > Image for now.

Ace Asin — 09/23/2023 2:36 AM

- Bloodborne Thumbnail and Background scripts have been removed since they're no longer needed.

Ace Asin — 09/23/2023 2:45 AM

- Removed the upload component from settings since uploading doesn't enter play mode anymore.

- Removed colorize texture, compress texture, and responsive window toggles from settings.

Ace Asin — 09/23/2023 3:05 AM

- Updated Discord RPC to not show a discriminator of #0000 for users with the new username system. It will only show the discriminator for users who haven't updated their username.

Ace Asin — 10/25/2023 2:15 PM

- Fixed alignment of settings due to new control panel render method.

Ace Asin — 10/25/2023 3:35 PM

- Changed the style of the authentication account window due to new scope layout.

Ace Asin — 12/11/2023 5:10 PM

- VRC is now targeting .NET Standard 2.1 for some reason. Bloodborne will continue to target .NET Framework 4.7.1. There shouldn't be any complications, and if there are then simply switch to .NET Framework on Edit > Project Settings > Player > Other Settings > Configuration > Api Compatibility Level*.

Ace Asin — 12/12/2023 10:46 PM

- Removed the entire Discord folder found inside Bloodborne. It was never required for Discord RPC to function and was causing issues on Unity 2022.

Ace Asin — 12/13/2023 1:04 AM

- Removed unnecessary editor tool's invocation from the logout method that is no longer used.

Ace Asin — 12/13/2023 1:23 AM

- Added a debug toggle that will enable all logging, including API for debugging purposes.

Ace Asin — 12/13/2023 4:23 AM

- Fixed alignment for all icons on the control panel. There's still a bug that will sometimes offset the icons if you're on the console tab during compilation, until you click on the project tab.

Ace Asin — 12/15/2023 1:51 AM

- Fixed a bug that was making the control panel appear blank due to internal code that wasn't removed along with the material and shader used to colorize the banner on an older release.

Ace Asin — 12/15/2023 2:00 AM

- Used Unity 2022.3.6f1 dependencies to build the Bloodborne assembly, since I previously forgot to change the dependencies. The Bloodborne assembly was still referencing Unity 2019.4.31f1 dependencies, and although it didn't cause any issues, it was still bad practice.

Ace Asin — 12/26/2023 1:05 PM

- Fixed an issue that prevented validations from loading, which ultimately prevented users from uploading.

Ace Asin — 01/05/2024 8:45 PM

- Bypassed the builder's accept terms toggle due to someone not being able to see it at all.

- Fixed accidental mistake on last patch that prevented users from seeing how many PhysBones they had while targeting Android.
