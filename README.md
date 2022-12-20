## Installation
1. Verify that Package Control is installed
2. Make sure that Sublime Text is not running
3. Clone/Copy this repo over Sublime Text's User Packages folder. Remove any existing contents if starting fresh, otherwise merge as required.
    * Windows -> `%AppData%/Roaming/Sublime Text/Packages/User`
    * macOS -> `~/Library/Application\ Support/Sublime Text/Packages/User`
    * Can also find this location by going into Sublime Text and choosing to `Browse Packages`. Make sure to close out of Sublime Text after.
    * `git clone <repo> .`
4. Verify that this README is at `...Sublime Text/Packages/User/README`
4. Start Sublime Text
5. Wait for all the packages to finish installing
6. Restart Sublime Text

### LSP Dependencies
LSP features require the various language servers to be installed in order for them to actually work. These are not part of Sublime Text and thus can not be automatically installed like the other plugins.

```zsh
% npm install -g vue-language-server
% pip install pylsp-rope
% pip install "python-lsp-server[mccabe]"
% pip install "python-lsp-server[pycodestyle]"
```
### Java
Install a version of java and make it available through `$JAVA_HOME`

#### macOS
```zsh
% brew install openjdk@17
% sudo ln -sfn /opt/homebrew/opt/openjdk@17/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk-17.jdk
% echo 'export JAVA_HOME=$(/usr/libexec/java_home -v 17)' >> ~/.zshenv
```

### Font Ligatures
Ligatures make code look nicer [Fira Code](https://github.com/tonsky/FiraCode) is my ligature font of choice at this time, though others do exist.

#### macOS
```zsh
% brew tap homebrew/cask-fonts
% brew install font-fira-code
```

### Python
Install `pyenv` and configure a global python version.

#### macOS
```zsh
% brew install pyenv
% pyenv install -l
# Pick a version from the list
% pyenv install <version>
% pyenv global <version>
% echo 'eval "$(pyenv init -)"' >> ~/.zshrc
% echo 'alias brew="env PATH=${PATH//$(pyenv root)/shims:/} brew"' >> ~/.zshrc
# Check that everything installed correctly. Open a new shell and confirm the version
% python --version
```

`~/.config/pycodestyle`
```
[pycodestyle]
ignore = W191,E261,E302,E305,E401
max-line-length = 160
```

