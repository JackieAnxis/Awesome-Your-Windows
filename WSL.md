# Windows Linux Bash Shell + Cmder + Zsh + oh-my-zsh Configuration

- Cmder Fonts: `Settings->General->Fonts->Main console font`: `Roboto Mono for Powerline`, choose `Bold`

- Linux:

  1. run `sudo apt-get install zsh`

  2. run `which zsh` to see where zsh is installed (usually it is: `/usr/bin/zsh`)

  3. add `bash -c zsh` into the end of `~/.bashrc`

  4. install Ob My ZSH: `sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`

  5. change ZSH Theme: Edit `~/.zshrc`

     ```
     ZSH_THEME="agnoster"
     ```

  6. install `powerline` font

     - `git clone https://github.com/powerline/fonts`

     - `./fonts/.install.sh`

     - The fonts are installed in dict `~/.local/share/fonts`

     - Copy your favorite font: `cp ~/.local/share/fonts/$your_favorite_font$ /mnt/c/Users/$your_window_name$` 
     - Put the font into `C:\\Windows\\Fonts`

  7. Restart cmder

