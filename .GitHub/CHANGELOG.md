# Changelog

Ace Asin — 08/12/2021

- The buttons on the asset list were over expanding by 2 pixels, this caused a horizontal scrollbar to appear. I made them smaller by 2 pixels and removed padding on the buttons for both left and right side.

- I had previously increased the width by 2 more pixels, since the text for the download button wasn't showing properly, but removing the padding fixed it and allowed me to make them smaller by 2 pixels once again.

- I made some improvements to the asset directories and files. If an author folder, category folder, or asset folder becomes empty, then the deletion of that specific directory will be handled accordingly, resulting in no empty directories. When you download assets, the correct paths get automatically created in your asset folder, as usual right, and now when you delete files, then the files and folders will get deleted automatically as well.

Ace Asin — 08/14/2021

- Further improved authorization, so that I'm not making too many requests all at once. My private API already had the guild endpoint setup, so I can figure out who's in the server, it also allows me to get the entire user object, and know which roles you have. In case that the main API endpoint or API version changes, it's now more dynamic, as I get them from the dedicated host.

Ace Asin — 08/14/2021

- Fixed a small bug on the asset tab, where there was an event being set, but never used, which prevented everything from loading after compiling many times.

Ace Asin — 08/14/2021

- In second thought the control panel will be completely disabled if you are on an alpha, beta, or private build without the proper authorization from now on.

- The editor application will also exit completely and continue to exit every time, until you change it back to a build that you are authorized to use, such as public. You can also get authorization by becoming a Patreon and use early access, this is just a security measurement.

- A dialog message will popup before exiting, with two options, the first button will take you to Patreon, where you can get early access, the second button simply says okay. No matter what button you click, the editor application will proceed to exit.

Ace Asin — 08/14/2021

- Fixed a bug that would utilize another thread, aside from the main thread to make requests, and a lot of code would not be able to process, this one was very important, should be good moving forward.

Ace Asin — 08/15/2021

- A lot of security measurements and precautions have been put in place, like I have mentioned in the past, alpha and beta will only work for authorized users only, just in case unauthorized users manage to get their hands on one. Early releases will last for a few days, before both the public and private releases go out.

- It's a different story when it comes to both public and private releases, they are technically the same. If you are an authorized user for private and are using a public release, then it will essentially work the same as a private release. If you are an unauthorized user for private and are using a private release, then it will essentially work the same as a public release. It is heavily dynamic in that aspect and open to change.

- The Discord RPC was heavily modified and optimized to handle these changes and display them accordingly.

Ace Asin — 08/15/2021

- Added the ability to change the client pipe, currently supports all 4 clients, Discord, Discord Canary, Discord PTB, and Discord Development. It's very sad to say that the library currently doesn't support users being signed into a web browsers for authorization. If you have an alt account that's authorized or it's getting the wrong client due to the pipe order, then you can easily change them now through a dropdown menu.

- It's still in beta, so there might be some issues here and there, noticed that for Discord Development it takes quite a bit longer to establish a connection when switching between pipes, but it works fine on startup, so just be patient I guess.

- When you first startup Unity, all of your accounts should show up, Username, Discriminator, and Identification, they change dynamically and more accounts will show up on the dropdown menu as you open a new Discord client.

Ace Asin — 08/16/2021

- The client pipe manager is now more stable, added a connect and disconnect button, as well as the previously already implemented dropdown menu to switch between all 4 clients.

Ace Asin — 08/16/2021

- Due to taking forever to establish a connection I removed the discord usernames from appearing on the pipes, there will now only be integers, 0, 1, 2, 3 for all 4 clients. When you first open your editor application the default pipe is set to -1, meaning the lowest integer, which will be 0.

- In order to display the names in advanced next to the pipe integer I had to create temporary clients, this has proved troublesome, buggy, and quite slow, especially when going into play mode.

- The way you want to connect is by starting from the lowest number, then making your way up the chain. You will notice that the connected account will change, depending in the order that you opened your discord clients, those will be the pipe integers.

- If a connection is not successfully established within 15000 ms of hitting the connect button, then it will be marked as failed, since these connection should be instant, unless obviously a discord client is closed, resulting in what I just mentioned.

Ace Asin — 08/16/2021

- If you had previously set a pipe and clicked the connect button, then it will remember the pipe for when you open your editor application again. If you only use 1 discord client, then leaving it at 0 is ideal, but if you have multiple clients, then you're obviously going to have to change it constantly, every time your client pipe order changes.

Ace Asin — 08/16/2021

- Fixed a GUI bug that would throw an argument exception and GUI error when restarting discord. The error would occur because as soon as you restart discord, it looses connection, then the GUI disables certain text fields. It was pushing more GUIClips than it was popping. It was a harmless bug, but I still don't like to see errors being thrown out like that, so did it the proper way by changing some GUI methods.

Ace Asin — 08/16/2021

- A few breaking changes are coming to the auto updater and possibly other methods as well, everything will be fine in version 13.0, so make sure that you stay up-to-date when it releases.

Ace Asin — 08/16/2021

- Since multiple client support has been added, had to change the way authorization was handled. If using an early release, alpha or beta, then you'll have chances to connect to all 4 clients. If all 4 clients fail to properly authorize you, then it means that you don't have the authorization to use an early release and the editor application will proceed to exit after the last client fails.

- This does not happen on public or private, they will dynamically change for users without having to do anything. The reason it only happens on alpha and beta is because it's meant to be early release and users without proper authorization shouldn't be able to use early releases.

Ace Asin — 08/16/2021

- The overall avatar performance spoofer has been locked for server boosters, it was experimental, that's why it was open to everyone during the period of release 12.0. You don't really even need it as all limiters are already bypassed by default.

Ace Asin — 08/17/2021

- The avatar and world prefabs for when uploading, as well as the vrccam prefab won't contain any scripts. The scripts will automatically be added during the upload process, this helps me save a bit of time, by not having to manually add them to the prefabs myself.

Ace Asin — 08/17/2021

- A few optimizations have been done on SDK3 builds that I didn't see present for SDK2, so I also implement those changes to SDK2. Made a lot of changes and improvements to speed up the process, have come to realization of a few things that will also speed up the process of modifying the SDK's.

Ace Asin — 08/17/2021

- Some issues with importing the SDK3 World had to do with me not exporting the required package, so users had to manually import some packages, such as Cinemachine, looking into exporting with the required package.

Ace Asin — 08/17/2021

- There was a problem with the obfuscated class library, since I was using an older version of the obfuscator. It would cause the authorization menu for alpha and beta releases to bug out. The obfuscator has been updated to the latest version and everything is working fine now.

Ace Asin — 08/17/2021

- There should be no more problems with missing packages anymore on SDK3 - World, had to make a custom script to be able to export the com.vrchat.vrcsdk3 custom package that's inside the Packages folder, with the folders and files in Assets. The package in com.vrchat.vrcsdk3 includes the UPMImporter.cs script that will install any packages automatically on initial load.

Ace Asin — 08/17/2021

- The titles have been slightly renamed...

Ace Asin — 08/19/2021

- I'm still somewhat experiencing some issues with the client authorization, added another pipe -1, which will try and find the first available client in the list, should solve issues. The pipe -1 will be recommended so that you don't experience any bugs with the client authorization, only change the pipe to a custom one if you have multiple discord clients open and it's getting the wrong account.

Ace Asin — 08/21/2021

- If the date is different for the release, then the Setting.asset cache file will automatically get overwritten by a new one, which should be able to handle future changes. This should prevent the issue with empty control panels, due to having an older cache file. The changes are happening on the next release, but users won't be able to fully experience it's effects until the next, next release, and future release from that moment on.

Ace Asin — 08/21/2021

- Had forgotten to remove some Remote Config requests from the Quest class component, which caused severe lag on the Setting tab, they were no longer in use, so there was no need for them to be there. The lag problem has been solved and it should now be smooth again, this only really affected early access beta users.

Ace Asin — 08/21/2021

- The -1 pipe will not be implemented for both the public and private releases. The private and public releases will also not dynamically change the build. Ended up not caring about that as much, the lists will continue to be locked as usual if you don't meet the requirements. You need to be in the server to unlock the public asset list, and you need to be a Patron Tier II or higher to unlock the private asset list.

Ace Asin — 08/21/2021

- The names have been slightly changed once again... The endpoints will also change for the auto updater due to these name changes, but hopefully they become permanent from now on, they will affect the beta release of 13.0.

Ace Asin — 08/21/2021

- There was a few bugs with some changes on the Setting.asset cache file, they've been fixed the file is now working better.

Ace Asin — 08/21/2021

- The log text color has been changed due to a small bug. You will now only be able to change the [Bloodborne] text color when certain log messages are sent, not the entire line, as you were previously able to do. The [Bloodborne] text is now also wrapped around brackets for easier identification of the messages being sent.

Ace Asin — 08/21/2021

- The asset section will now be completely disabled on the toolbar if there's to connection to the client. If you were on the asset section upon loosing connection, then it will move you over to the setting section, where you can reconnect or wait for the 15000 auto reconnect interval to kick in.

- This change should also fix the bug that would make the state of fetching last forever when you clicked the fetch button in the asset section. It would stay fetching until a connection was reestablished, since there was no client.

Ace Asin — 08/21/2021

- Certain aspects and terminology for the unique device identification generator have been corrected.

Ace Asin — 08/21/2021

- For the control panel and splash screen, background and foreground colors have been disabled. The primary and secondary colors still remain, which are the important ones that I personally assigned to the menus.

Ace Asin — 08/22/2021

- There are now placeholders for certain text fields, to make it a little easier to understand what to type.

Ace Asin — 08/22/2021

- The internet protocol for private and public networks will now appear as 0.0.0.0 when hidden, instead of an empty null value, by default they're both hidden, meaning that the toggle option is unchecked.

Ace Asin — 08/22/2021

- A few bugs were fixed that had to do with early access authorization, there shouldn't be any more errors thrown out when clicking the fetch button on the asset section. It had to do with the way I disabled the lists when fetching and used the same state to display the authorization window. The authorization window would appear for a short duration and cause a GUI error to be thrown out, they've been separated into different states and will work better now.
