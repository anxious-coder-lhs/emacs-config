# emacs-config
This is a copy of my emacs configuration that I use for development, book keeping, notes, organization etc. I hope this can be of use to you. In case of any issues, please feel free to reach out to me, raise an issue or create a pull request.

## Packages
* [Spacemacs: Amazing Emacs distribution based on Evil mode](#spacemacs)
* [Markdown](#markdown)
  
# Why Spacemacs?
The configuration is based on using Spacemacs, rather than native Emacs. Original documentation can be found at the [Spacemacs github repo](https://github.com/syl20bnr/spacemacs). For me it provides a perfect combination of power and beauty.

# Installation

## Installing Spacemacs
I would suggest you to pull in the latest spacemacs distribution from Github in your local emacs setup. Spacemacs can be installed using the following [official documentation](https://github.com/syl20bnr/spacemacs/blob/master/doc/BEGINNERS_TUTORIAL.org)

Following are the 2 suggested modes of installing the Spacemacs.
* You can install Spacemacs using the following command in Emacs: `SPC : dotspacemacs/install RET`
* Alternatively installation can be done directly from Github. Open a terminal or command prompt, paste the following code to it:

`git clone https://github.com/syl20bnr/spacemacs ~/.emacs.d`

Press enter to execute the code and the program you installed in the previous step, Git, will download the Spacemacs extension files.

If you are using Windows, the directory might not be available at the same location. Please refer to this [page](https://www.gnu.org/software/emacs/manual/html_node/efaq-w32/Location-of-init-file.html) for more details on how to find the home location on Windows.

For me, it was found in the `AppData/Roaming`

Additionally, following [fonts](https://github.com/adobe-fonts/source-code-pro#font-installation-instructions) are recommended to be installed for Spacemacs.

You can find the complete spacemacs installation instruction [here](https://github.com/syl20bnr/spacemacs/blob/master/doc/BEGINNERS_TUTORIAL.org)

## My Custom Configuration/Packages
Following section install the custom packages and configurations that I use. To install my custom configurations, use the following steps:

Copy the `.spacemacs` file from this git repository to your emacs home directory.
` wget https://raw.githubusercontent.com/love2dishtech/emacs-config/master/.spacemacs -O ~/.spacemacs`

If you are using Windows, the directory might not be available at the same location. Please refer to this [page](https://www.gnu.org/software/emacs/manual/html_node/efaq-w32/Location-of-init-file.html) for more details on how to find the home location on Windows.

For me, it was found in the `AppData/Roaming`

# Configurations
Spacemacs configurations are managed by the `.spacemacs` file in the home directory. This is the starting point of all the configurations.

## User Config
`dotspacemacs/user-config` is the user configration function that is executed at the end after all the layers configurations are complete. Unless there is an advanced configuration that needs to be defined early in the bootstrap process, most of the user configurations should be done in this section. This is the best place to customize your Spacemacs configuration for any external behaviour.

It is better to use this section to add any configuration that you would typically add in your `init.el` file.

## Configuration Layers
Layers are an amazing configuration abstraction provided by Spacemacs for tuning the required configuration/packags for your installation. This allows to easily extend the setup capabilities by just plugging in an external layer for independent configurations like programming languages, external tools, etc.

Layers are publically available by community and you can further extend a layer by custom configurations. Also, not all the layers available by Spacemacs are enabled by default. Users have control on enabling and disabling a given layer.

Configuration layers can be enabled/disabled using the `dotspacemacs-configuration-layers` function in the `.spacemacs` configuration file. At the time I installed it, the only enabled package by default was `helm` and `emacs-lisp`. All the others were disabled.

## Enabling/Disabling Layers
In this repo configuration, I have shared my layering configuration for my setup. Please look into `.spacemacs` and the `dotspacemacs-configuration-layers` and disable/enable the packages you would like. Just uncomment the package that are of interest and press `SPC f e R` in Evil mode or `M-m f e R` to reload.

## Custom Layers
The intent of this repo is to provide my own set of chosen and curated custom layers. But, I will highly motivate you to go ahead and modify the functionality I have configured. Additionally, you may also find yourself in a position to create layers of your own.

If you find yourself in a need of installing a new packages, you shouldn't do it with package manager. If you do that Spacemacs will try to throw away the package upon next restart. Spacemacs does it to make sure, your loading time is low and it only loads the packages, you intent to use.

The way Spacemacs recommends is to define the packages you would like to use in the `.spacemacs` file. However, as you add more and more packages and respective configurations, it will soon get very messy soon. For this it is recommended to create your own layers.

Any layers that you create will by default go to the private directory. This command creates a new layer for you in the private directory. You can also configure a different path to load layers from by configuring the layers path in the `.spacemacs` file. This is what i recommend and have done in this setup. This allows you to differentiate between your custom layers and those that you have pulled. You can pull it from various sources and simply disable from a source any time.

To configure additional layer paths, you can use the `dotspacemacs-configuration-layer-path` function in the `.spacemacs` file. I have updated it to use `additional-layer` folder available with this repo.

To create your own layer, use `SPC SPC configuration-layer/create-layer RET`. Note that the search is fuzzy, so you do not have to type in the exact command in the window. 

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
* `cw` change word
* `dw` delete word
* `gg` move to first line of file
* `G` move to last line of file
* `A` move to end of line

### Project operations
`SPC SPC neotree-dir` - Open a directory in neotree
`SPC f t` - Toggle the neotree view
`SPC p` - Projectile menu
`SPC p p` - Switch to a recent project
`SPC p f` - Open a file in the project view

### Markdown
* [Markdown documentation](https://github.com/syl20bnr/spacemacs/tree/master/layers/%2Blang/markdown)

### Git/Magit
* `SPC g s` - Git Status Magit
  * `s` - Stage on the Git Status Maggit
  * `n` - Unstage on the Git Status Maggit
  * `TAB` - To expand the status of the Git Status
  * `C-SPC` - Select some part of the section, `s` - Stage part of the section
  * `c` - Commit
  * `p` - Push
  * [External References - Maggit Page](https://magit.vc/manual/magit.html#Status-buffer)
  * [Spacemacs Git Bindings Manual](https://github.com/syl20bnr/spacemacs/tree/master/layers/%2Bsource-control/git)

### Spacemacs
Spacemacs is an amazing Emacs distribution based on the Evil mode. Bringing in the best of the world of Emacs and Vim, it provides the best ergonomics, mnemonics and consistency. Includes a curated set of included packages for enhanced end user experience. Spacemacs additionally provides a layering abstraction for configuration that allows users to simply switch off a part of the functionality.

Please refer to following links for detailed information on this package.

* [Spacemacs Home Page](http://spacemacs.org)
* [Install Instructions](https://github.com/syl20bnr/spacemacs)
* [Documentation](https://github.com/syl20bnr/spacemacs/blob/master/doc/DOCUMENTATION.org)

### Markdown
Default spacemacs package for markdown. Detailed documentation is available [here](https://github.com/syl20bnr/spacemacs/tree/master/layers/%2Blang/markdown).

In this package, I have configured the vmd mode of markdown preview. It is faster and mimics Github markdown renderer. Please check the spacemacs [documentation](https://github.com/syl20bnr/spacemacs/tree/master/layers/%2Blang/markdown) for markdown layer. Also check the documentation for [Markdown vmd mode](https://github.com/blak3mill3r/vmd-mode)

### Projectile
Projectile provides the default implementation for managing and handling projects. It automatically detects VCS projects and directories with build tools like Git, mercurial, Maven etc. You can also enable any folder to be treated as a project by adding a `.projectile` file. Detailed documentation can be found [here](https://github.com/bbatsov/projectile). Also, do check the [project website](https://projectile.readthedocs.io/en/latest/)

### Noetree
[Neotree](http://develop.spacemacs.org/layers/+filetree/neotree/README.html) provides a different better looking implementation of the directory structure as compared to the default, [Treemacs](http://develop.spacemacs.org/layers/+filetree/treemacs/README.html) 

Spacemacs bundles a set of visual packages for the UI and Neotree directory. You can find the details on the documentation [here](https://github.com/syl20bnr/spacemacs/blob/c7a103a772d808101d7635ec10f292ab9202d9ee/layers/%2Bspacemacs/spacemacs-ui-visual/packages.el)

### Spell Check
[Spell Check](https://github.com/syl20bnr/spacemacs/tree/master/layers/%2Bcheckers/spell-checking) provides an inbuilt implementation of word spell checks and corrections. It also provides an auto-correct mode which is pretty neat out of the box.

Projectile provides the default implementation for managing and handling projects. It automatically detects VCS projects and directories with build tools like Git, mercurial, Maven etc. You can also enable any folder to be treated as a project by adding a `.projectile` file. Detailed documentation can be found [here](https://github.com/bbatsov/projectile). Also, do check the [project website](https://projectile.readthedocs.io/en/latest/)
