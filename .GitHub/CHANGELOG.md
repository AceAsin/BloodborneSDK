# **Changelog**

8/5/2021, 8:28:37 AM

- Everything is coming along very well. I'm mainly working on the Unity Editor GUI at the moment, since everything else is done quite fast.

- I had to do a few changes on the Unity Editor GUI, since everything was unaligned on the new Unity 2019 version, but we're back to having everything aligned to perfection.

- If you have dark mode on the new version of Unity, then the previous gray background color for the splash screen and control panel will look extremely dark, changed them back to the normal.

- I allowed a more margin for the manager and asset dropdown labels. You can now click anywhere on the menu with LEFT/RIGHT/MIDDLE mouse buttons and they will expand or collapse. Previously there was 2 pixels worth of margin on the top and bottom of the labels, clicking those areas did not expand or collapse the dropdown menus. They also work with the keybind shortcut that I implemented, just hold down the ALT key while clicking LEFT/RIGHT/MIDDLE mouse buttons and it will expand or collapse all categories for the asset tab section, similar to how it works on the Unity Hierarchy, but covers the entire dropdown label.

- I added back the default margins on all of the buttons, previously they had no margin at all, in Unity 2019, they looked weird without having margins, so just made them go back to default.

8/5/2021, 12:39:26 PM

- I fixed a bug that made your menu disappear when you set the Setting.asset file back to default. It can still occur when a new release generates a different cache file, since I change at least one thing on every new release. It is best to delete the Setting.asset file upon every new release, so that you don't run into any potential problems.

8/6/2021, 1:47:23 AM

- The section for Quest has changed quite a bit. There is no longer a Quest Limiter toggle. You are now going to have to go to the Quest section and type a custom value for Avatar or World. They each have their own text field and toggle on the right.

- If the toggle is checked, then it will use whatever custom size is in the text field. If the toggle is checked and the text field is empty, then it will use the default values, which is 10 MB for avatars and 50 MB for worlds. If the toggle is unchecked, then the upload size will be unlimited, regardless if there is a custom text field or not.

- If you are unable to type a custom Quest limit size, due to not being a server booster, then you will only able to only toggle the limiter, meaning that the limiter will either be set to the default limit or unlimited.

8/6/2021, 3:19:38 AM

- There will be a new toggle option that is only visible when the target build is set to Android. It's to toggle the shader blocking system, which strips all shaders. It's an experimental feature and only there is case people run into issues with their avatars being all dark in game.

8/6/2021, 8:45:50 AM

- I added a developer shortcut to clear the console, but everyone is more than welcome to use it as well, ALT + C.

- I also added 2 more colors, for the control panel, primary and secondary, which are the two that I use, they can now be changed to anything.

- The select text from dropdown menus has been removed, as it was kind of useless and it made it so that you would have to choose something if you wanted to access the toggles for certain sections.

8/6/2021, 4:25:45 PM

- I finally managed to fix a huge memory leak bug that was coming from the thumbnail script. It's now way more optimized and shouldn't break when uploading. It's something that was holding me up quite a bit, since there was no information about it anywhere.

- Previously a long time ago, there was an instance bug, kept spam throwing errors on your console, managed to fix that one, but now I realized resource id out of range error that would break your entire Unity GUI. It's now been fixed and I can proceed to finish with whatever is left.

8/6/2021, 10:24:46 PM

- I fixed the PLAYSTATE.UPLOADING state from getting overwritten by PLAYSTATE.PLAYING when entering the upload panel. It was due to the new subscribed events that I had previously implemented, since they're so good and are always detecting while not causing lag. I added a condition to not go through if the PLAYSTATE was currently set the PLAYSTATE.UPLOADING, which solved it.

8/6/2021, 10:42:37 PM

- I added a shortcut to delete the Setting.asset file in case users don't see the menus due to conflicts with the files if they're from different releases. All of the shortcut keys will be documented on the GitHub repository, right now it's ALT + D. I'll look into making them customizable later, not a priority at the moment.

8/6/2021, 11:59:54 PM

- I fixed the world prefab from showing all white text colors, since it was hard to read the input text, had to filter things out differently, but it looks good now.

8/7/2021, 1:02:56 AM

- The elapsed time will not get reset when switching between play mode and edit mode anymore. It would previously get reset, since everything technically has to re-initialize. I managed to get the timestamp of when the unity editor is opened, then with some basic math we maintain the actual elapsed time.

8/7/2021, 3:07:08 AM

- All of the social links and support links have been moved to the remote and dedicated server, just in case they change. They have a fallback to the original static links, just in case it fails to get anything from the server.

8/7/2021, 4:43:28 AM

- I'm going to be adding a performance spoofer option, so might take me a little longer to release the next update, it works and helps you upload the avatar on whatever performance you might want. If you set it to excellent then you will be able to use the avatar as a fallback avatar. The in-game client re-scans your performance and shows you the actual settings from what they were originally, but it's no issue as it will still let you upload regardless.

- I'm adding all of these things so that Quest users can easily test them and let me know if something works by having a certain setting a certain way. It would also help me easily identify what works and what doesn't.

8/7/2021, 6:01:46 AM

- I finished adding the overall performance spoofer, it's working as intended and nicely. I'll finish modifying both the SDK3 Avatar and SDK3 World now.

8/7/2021, 8:37:50 AM

- I had to use PlayerPrefs instead of EditorPrefs for the avatar performance spoofer, since I'm unable to use EditorPrefs on runtime, so just keep that in mind.

8/7/2021, 1:38:13 PM

- All builds are complete and I'm getting ready to export the unity packages. It took me a while to build and compile the new Bloodborne.dll class library, since the way I had to reference things was different.
