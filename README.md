# emacs-config
This is a copy of my emacs configuration that I use for development, book keeping, notes, organization etc. I hope this can be of use to you. In case of any issues, please feel free to reach out to me, raise an issue or create a pull request.

## Packages
* [Spacemacs: Amazing Emacs distribution based on Evil mode](#spacemacs)
  
# Why Spacemacs?
The configuration is based on using Spacemacs, rather than native Emacs. Original documentation can be found at the [Spacemacs github repo](https://github.com/syl20bnr/spacemacs). For me it provides a perfect combination of power and beauty.

# Installation

## Installing Spacemacs
I would suggest you to pull in the latest spacemacs distribution from Github in your local emacs setup. Spacemacs can be installed using the following [official documentation](https://github.com/syl20bnr/spacemacs/blob/master/doc/BEGINNERS_TUTORIAL.org)

Following are the 2 suggested modes of installing the Spacemacs.
* You can install Spacemacs using the following command in Emacs: `SPC : dotspacemacs/install RET`
* Alternatively installation can be done directly from Github. Open a terminal or command prompt, paste the following code to it:

`git clone https://github.com/love2dishtech/spacemacs-config ~/.emacs.d`

Press enter to execute the code and the program you installed in the previous step, Git, will download the Spacemacs extension files.

Additionally, following [fonts](https://github.com/adobe-fonts/source-code-pro#font-installation-instructions) are recommended to be installed for Spacemacs.

You can find the complete spacemacs installation instruction [here](https://github.com/syl20bnr/spacemacs/blob/master/doc/BEGINNERS_TUTORIAL.org)

## My Custom Configuration/Packages
Following section install the custom packages and configurations that I use. To install my custom configurations, use the following steps:

`TBD`

# Configurations
Spacemacs configurations are managed by the `.spacemacs` file in the home directory. This is the starting point of all the configurations.

## User Config
`dotspacemacs/user-config` is the user configration function that is executed at the end after all the layers configurations are complete. Unless there is an advanced configuration that needs to be defined early in the bootstrap process, most of the user configurations should be done in this section. This is the best place to customize your Spacemacs configuration for any external behaviour.

It is better to use this section to add any configuration that you would typically add in your `init.el` file.

## Configuration Layers


# Keybindings
It is practically not possible to highlight all the bindings here. The intent is to showcase some of the top used keybindings here. Additional contributions are welcome.

## Spacemacs Basic Modifiers

* `SPC = Space`, used as the leader key in Vim editing style.
* `C- = Ctrl`
* `M- (for “meta”) = Alt` or Option in OSX
* `S- = Shift`
* `SPC` - spacemacs commands in Vim editing style.
* `SPC f e d` to access/edit .spacemacs file.
* `SPC h SPC` to access list of documentation and supported layers.
* `SPC t` to toggle default spacemacs buffer functionality. This might include colors, indentation, etc.
* `SPC f e R` to reload spacemacs configurations from file

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

Please refer to following links for detailed information on this package.

* [Spacemacs Home Page](http://spacemacs.org)
* [Install Instructions](https://github.com/syl20bnr/spacemacs)
* [Documentation](https://github.com/syl20bnr/spacemacs/blob/master/doc/DOCUMENTATION.org)
