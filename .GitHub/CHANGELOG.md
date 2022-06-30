**06/20/2022**

- The max amount of expression controls and parameters have been set to the max value of a 32 bit integer, which happens to be 2147483647. This doesn't particularly mean that they'll function in-game when going past 8 controls and 256 parameters. They work on an emulator just fine, but higher values are in fact inaccessible through the in-game menu, unless you somehow figure out how to access them or get them to work through modifications.

**06/20/2022**

- Removed unnecessary logs from the License component. This caused an integer and boolean to appear on your console when the End User License Agreement (EULA) was initialized on load.
- Removed more unnecessary logs from the Quest component. It would previously show the size of the avatar on your console when uploading.
