## Installation
1. Verify that Package Control is installed
2. Make sure that Sublime Text is not running
3. Clone/Copy this repo over Sublime Text's User Packages folder. Remove any existing contents if starting fresh, otherwise merge as required.
    * Windows -> `%AppData%/Roaming/Sublime Text 3/Packages/User`
    * macOS -> `~/Library/Application\ Support/Sublime Text 3/Packages/User`
    * Can also find this location by going into Sublime Text and choosing to `Browse Packages`. Make sure to close out of Sublime Text after.
4. Verify that this README is at `...Sublime Text 3/Packages/User/README`
4. Start Sublime Text
5. Wait for all the packages to finish installing
6. Restart Sublime Text

### LSP Installation
LSP features require the various language servers to be installed in order for them to actually work. These are not part of Sublime Text and thus can not be automatically installed like the other plugins.

```sh
$ npm install -g bash-language-server
$ npm install -g vue-language-server
$ npm install -g javascript-typescript-langserver
$ npm install -g vscode-html-languageserver-bin
$ npm install -g vscode-css-languageserver-bin
$ pip install python-language-server
$ pip install python-language-server[rope]
$ pip install python-language-server[pyflakes]
$ pip install python-language-server[mccabe]
$ pip install python-language-server[pycodestyle]
$ pip install python-language-server[yapf]
```
##### Java
Will need to follow [these instructions](https://lsp.readthedocs.io/en/latest/#java). Be sure to place the extracted files in ~/lsp/jdt-language-server. Note that the version of the org.eclipse.equinox.launcher_*.jar is likely different. The fuzzy path didn't work so it's currently hard coded.

### Font Ligatures
Ligatures make code look nicer [Fira Code](https://github.com/tonsky/FiraCode) is my ligature font of choice at this time though others do exist.

#### macOS
```sh
$ brew tap homebrew/cask-fonts && brew cask install font-fira-code
```
