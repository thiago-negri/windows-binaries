# nvim
- `winget install Neovim.Neovim`

# ripgrep
- required for grepping files with telescope in nvim
- repo: https://github.com/BurntSushi/ripgrep
- downloads: https://github.com/BurntSushi/ripgrep/releases
- latest atm: https://github.com/BurntSushi/ripgrep/releases/download/14.1.1/ripgrep-14.1.1-x86_64-pc-windows-gnu.zip 
- extract and add to path

# wezterm
- https://wezfurlong.org

# msys2 + gcc, required for treesitter in nvim
- https://www.msys2.org/
- install
- open MSYS2 MSYS
- $ pacman -Syu
- it will force close the terminal
- open MSYS2 MSYS again
- $ pacman -Su
- close the terminal
- open MSYS MINGW64
- pacman -S mingw-w64-x86_64-gcc
- add "C:\msys64\mingw64\bin" to path

# sqlite
- https://www.sqlite.org/download.html

# fish
- https://fishshell.com
- on msys2: `pacman -S fish`
- to fix PATH in fish on Windows (MSYS2): `set -U MSYS2_PATH_TYPE inherit`
- to fix CWD when creating new windows, add the following to `~/.config/fish/config.fish`:
    ```fish
    function wezterm_fix_working_directory --on-event fish_prompt
        wezterm set-working-directory
    end
    ```
