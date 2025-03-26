# Omni-Wipe interactive script

This is an interactive drive-wiping script designed by employees at [Green Star of Interior Alaska](https://iagreenstar.org/reuse-it-programs/).

The intended use of this is as a tool on a Linux-on-a-Stick for easily erasing drives that contain data of previous owners without having to interact with the drive in such a way that one might come directly in contact with customer data.

This script can quickly and less-destructively wipe the drive with wipefs to simply remove the file system for drives that only have shop-installed operating systems as well as a more thorough scrub for actual customer data that overwrites the drive with random data.

This script can be used on both HDDs and SSDs. 

If you're looking to use this yourself, we recommend placing it in `~/.local/bin`, adding that location to `$PATH` if it isn't so already, and running `chmod +x` on it so that it can be invoked directly from the terminal.

*This script can and will destroy all data on a drive. That is its intended purpose. **Use at your own risk.***

I might get around to adding a third branch that uses `shred` for multi-pass erases. Or, I may not. We'll see if I get tired of typing that command manually.

Oh, and this script assumes your Linux-on-a-Stick is using bash as its shell. I'm lazy. And basic.

This script *probably* works with all POSIX-compliant operating systems, but I haven't tested it on anything except Arch, Fedora, and Pop. Have fun!

# Operating Manual

- Invoke the script in your preferred manner.
- Locate the drive you wish to wipe in the list from `lsblk`.
- Type the name of that drive into the prompt.
- Decide whether you want to zap the FS or perform an overwrite of the drive's data
- Go do something else while Linux does all the work for you.
  - Maybe enjoy some tea if the drive is particularly large or slow.

  Happy wiping!
  
  \- GSIA
