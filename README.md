# Yuri's VS Code Configuration

* [Theme and Font](#theme-and-font)
* [Microprocessor Development](#platformio)
* [C/C++ Development](#cc-development)
* [Using zsh](#zsh)
* [Python Development](#python-development)
* [Web Development](#web)
* [List of All Extensions](#all-extensions)

---
## Theme and Font
* Install my [RageQuit Theme](https://marketplace.visualstudio.com/items?itemName=YuriRage.ragequit)
* Install the [Fira Code Font](https://github.com/tonsky/FiraCode/releases)
    * (on Windows, use the static *.ttf fonts, not the variable one)
    * Set the editor font family to `Fira Code`
* Other `settings.json` entries (or use [my file](https://update-this-link)):

        "editor.fontFamily":  "Fira Code",
        "editor.fontSize": 14,
        "editor.fontLigatures": true,
        "editor.lineHeight": 20,
        "editor.rulers": [80],
        "editor.smoothScrolling": true,
        "editor.cursorBlinking": "phase",
        "editor.cursorSmoothCaretAnimation": true,
        "editor.bracketPairColorization.enabled": true,
        "editor.formatOnSave": true,
        "files.autoSave": "afterDelay",
        "files.autoSaveDelay": 1500,
        "terminal.integrated.cursorBlinking": true,
        "terminal.integrated.cursorStyle": "line",
        "terminal.integrated.cursorWidth": 2,
        "typescript.suggest.paths": false,
        "workbench.colorTheme": "RageQuit",
        "workbench.iconTheme": "material-icon-theme",
        "workbench.list.smoothScrolling": true,
        "C_Cpp.clang_format_fallbackStyle":
            "{ BasedOnStyle: Google, IndentWidth: 4, ColumnLimit: 80}",
        "gitlens.defaultDateFormat": "DD MMM YYYY HH:mm",
        "gitlens.defaultTimeFormat": "HH:mm",
        "gitlens.defaultDateShortFormat": "YYYYMMDD"
        

---
## Microprocessor Development (Arduino/ESP)

* Install the [PlatformIO Extension](https://marketplace.visualstudio.com/items?itemName=platformio.platformio-ide)
* (and never use the Arduino IDE again :-) )

---
## C/C++ Development

* Install the [C/C++ Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)

* [Install MSYS2](https://www.msys2.org/)
* Update the *nix distribution using the MSYS2 bash shell:

        pacman -Syu

* Install git and mingw-64 (C/C++ toolchains):

        pacman -S git
        pacman -S mingw-w64-x86_64-toolchain


---
## Enable zsh in VS Code Terminal
(and make it kind of fancy...)
* Make sure you have [MSYS2](https://www.msys2.org/) installed (see [C/C++ Development](#cc-development) above)
* Install zsh, oh-my-zsh, and [my .zshrc](https://link-here):

        pacman -S zsh
        cd ~
        sh -c "$(wget -O- https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
        wget -O .zshrc https://need-to-update-this-link/.zsrhc

* Put the following into VS Code's `settings.json` file under `"terminal.integrated.profiles.windows"` [(or use mine)](https://link-here):

        "MSYS2 (zsh)": {
            "path": "C:\\msys64\\usr\\bin\\zsh.exe",
            "args": ["--login", "-i"],
            "env": {
                "MSYSTEM": "MINGW64",
                "CHERE_INVOKING": "1",
                "MSYS2_PATH_TYPE": "inherit"
                }
        }

* To make this shell your default, add this to `settings.json` [(or use mine)](https://link-here):

        "terminal.integrated.defaultProfile.windows": "MSYS2 (zsh)",

---
### Python Development:
* Install [Python](https://www.python.org/downloads/)
* Install the [Python Extension](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
* Install the [Jupyter Extension](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)
* Install the [Kite Extension](https://marketplace.visualstudio.com/items?itemName=kiteco.kite) (maybe?)

---
## Web Development
(disclaimer: I don't do much of this)
* Install the [Auto Rename Tag Extension](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag)
* Install the [Live Server Extension](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
* Install the [Prettier Extension](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
* Install the [Quokka.js Extension](https://marketplace.visualstudio.com/items?itemName=WallabyJs.quokka-vscode)

---
## All Extensions:
(that I'm using today)

* [advanced-new-file](https://marketplace.visualstudio.com/items?itemName=patbenatar.advanced-new-file)
    *  Map to Ctrl-N for faster/easier new file creation
* [Auto Rename Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag)
    * if working with HTML/CSS
* [Better Comments](https://marketplace.visualstudio.com/items?itemName=aaron-bond.better-comments)
    * comment/TODO highlighting
* [C/C++](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)
    * language support
* [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)
    * nice for avoiding typos
* [Color Highlight](https://marketplace.visualstudio.com/items?itemName=naumovs.color-highlight)
    * highlight RGB and HEX color codes
* [Git Indicators](https://marketplace.visualstudio.com/items?itemName=lamartire.git-indicators)
    * status bar git info
* [Git Lens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
    * integrated git support - must have!
* [Jupyter](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter)
    * Python (and other) notebooks
* [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
    * development web server (live debugging web apps on localhost) 
* [Material Icon Theme](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)
    * colored icons for files/folders
* [Path Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)
    * file autocompletion
* [PlatformIO IDE](https://marketplace.visualstudio.com/items?itemName=platformio.platformio-ide)
    * if developing for Arduino/microprocessors
* [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
    * auto-formatting aimed at web development
* [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
    * language support
* [Quokka.js](https://marketplace.visualstudio.com/items?itemName=WallabyJs.quokka-vscode)
    * Javascript playground/debugging tool
* [RageQuit Theme](https://marketplace.visualstudio.com/items?itemName=YuriRage.ragequit)
    * my very own color theme (dark) - must have! :-)
* [Kite AutoComplete AI](https://marketplace.visualstudio.com/items?itemName=kiteco.kite)
    * Python AI auto-completion (still on the fence about this one)
* [Tabnine](https://marketplace.visualstudio.com/items?itemName=TabNine.tabnine-vscode)
    * multi-language auto-completion (still on the fence about this one, too)
