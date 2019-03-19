# emacs-config
This is a copy of my emacs configuration that I use for development, book keeping, notes, organization etc. I hope this can be of use to you. In case of any issues, please feel free to reach out to me, raise an issue or create a pull request.

## Packages
* [Spacemacs: Amazing Emacs distribution based on Evil mode](#spacemacs)
  

# Why Spacemacs?
Original documentation can be found at the [Spacemacs github repo](https://github.com/syl20bnr/spacemacs). For me it provides a perfect combination of power and beauty.

# Installing Configuration
While you might not be interested in installing this directly, but rather use certain parts of the configuration package. Direct installation can be done with the following steps:

Open a terminal or command prompt, paste the following code to it:

`git clone https://github.com/love2dishtech/spacemacs-config ~/.emacs.d`

Press enter to execute the code and the program you installed in the previous step, Git, will download the Spacemacs extension files.

Additionally, following [fonts](https://github.com/adobe-fonts/source-code-pro#font-installation-instructions) are recommended to be installed for Spacemacs.

You can find the complete spacemacs installation instruction [here](https://github.com/syl20bnr/spacemacs/blob/master/doc/BEGINNERS_TUTORIAL.org)

# Keybindings
It is practically not possible to highlight all the bindings here. The intent is to showcase some of the top used keybindings here. Additional contributions are welcome.

## Spacemacs Basic Modifiers

* `SPC = Space`, used as the leader key in Vim editing style.
* `C- = Ctrl`
* `M- (for “meta”) = Alt` or Option in OSX
* `S- = Shift`
* `SPC` - spacemacs commands in Vim editing style.
* `SPC f e d` to access .spacemacs file.
* `SPC h SPC` to access list of documentation and supported layers.

## Modal Editing
* `SPC h T` - Spacesmacs modal editing Tutor - based on Emacs EVil mode(An Emacs VIM emulation)
* `j` to move a line down (usually achieved by down arrow, but saves your wrist to bend)
* `h` to move left (usually achieved by left arrow, but saves your wrist to bend)
* 'l' to move right (usually achieved by left arrow, but saves your wrist to bend)
* `k` to move a line up (usually achieved by up arrow, but saves your wrist to bend)
* `qa! <ENTER>` exiting the Spacemacs without saving any work
* `wqa <ENTER>` exiting the Spacemacs after saving the work
* `x` deleting a character under the cursor
* `dd` deleting the line

### Spacemacs
Spacemacs is an amazing Emacs distribution based on the Evil mode. Bringing in the best of the world of Emacs and Vim, it provides the best ergonomics, mnemonics and consistency. Includes a curated set of included packages for enhanced end user experience. Spacemacs additionally provides a layering abstraction for configuration that allows users to simply switch off a part of the functionality.

Site: http://spacemacs.org
Github: https://github.com/syl20bnr/spacemacs
