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
