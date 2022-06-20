Ace Asin — 04/22/2022

- Improved the current size on the builder and it's now more persistent. There was also a bug that would mark the current size as unknown when making changes to the limiter from the settings and would only update after attempting to upload.

Ace Asin — 04/22/2022

- The overall avatar performance spoofer section has been disabled due to a few complications, will more than likely enable it again in the future.

Ace Asin — 04/23/2022

- Finally came up with a perfect formula for token authentication and it's fully completed, ended up taking me a while. I had to do major changes, not only to the software development kit, but also to the bot, database, and backend server. The token can be used to unlock exclusive features, alternative method for users who struggle with Discord RPC. It's way more efficient and optimized, access is granted immediately, instead of having to wait a while like Discord RPC. Incorporated token generation and regeneration commands for the bot, simply execute -token once the next update is released and the bot will send the token to your messages, must allow messages from server members temporarily if you have them disabled. The token will only be deleted if it's shared or exposed, so please don't share your newly generated token with other users. You will be penalized and there will be a cooldown of 24 hours before being able to generate a new one. If there are too many incidents of your token getting shared or exposed, then that could blacklist and prevent you from being able to generate a new one in the foreseeable future. I just can't stress this enough, so please don't share them, there's also going to be token status updates for when a token gets shared or exposed. The Discord RPC will still work as usual, it just won't be used for authentication when using a token.

Ace Asin — 04/23/2022

- JSON static files are now being served from the backend server, instead of remote storage. The Content Delivery Network (CDN) will continue to serve assets, since those are large in size and want to continue to offer everyone with the fastest downloads. Taking the opportunity to make these major changes now, since pretty much everyone will be updating after this release. The data that is obtained remotely will no longer show on older releases.

Ace Asin — 04/23/2022

- Once again, users will have to scroll all the way down and read the EULA thoroughly in order to enable the agree button. In the event that a user is unable to unlock the agree button after scrolling all the way down, then there is a 60000 interval or 1 minute timer in place that starts as soon as the window appears. When it's over it will force the agree button to unlock, after it's unlocked then you can go ahead and press it if you agree.

Ace Asin — 04/23/2022

- Made more changes and improvements to the token authentication, mainly it's behavior, so that the authenticated user can be used alongside the Discord RPC connected account without any issues. The User line that displays the current connected for Discord RPC has been relocated from Discord to Client. I separated the Token line, it's now on it's own Server section, along with two buttons used for authentication.

Ace Asin — 04/23/2022

- Updated to the latest live SDK.
