# shellkit

## Information
### Description
+ Collection of various shell scripts and libraries in a single package that can be installed easily
+ Note that the scripts here though is labelled as bash scripts and libraries - these can be used by other shells if following the same structure and unless specified

## Setup
### Dependencies

### Pre-Requisites
- Create the required PREFIX (Installation directory)
    - User-space .local directory in your $HOME
        - Binaries/Executable
            ```bash
            mkdir -pv $HOME/.local/bin/
            ```
        - Libraries
            ```bash
            mkdir -pv $HOME/.local/lib
            ```
    - System-level 'build-from-source' installation
        - Notes
            - $PREFIX refers to the installation directory/path
                + Default: /usr/local
        - Binaries/Executable
            ```bash
            mkdir -pv $PREFIX/bin
            ```
        - Libraries
            ```bash
            mkdir -pv $PREFIX/lib
            ```

### Installation
> bash Scripts

- Copy the 'src/scripts' directory to your binary directories
    - User-space .local directory in your $HOME
        ```bash
        cp -r src/scripts $HOME/.local/bin/shellkit
        ```
    - System-level 'build-from-source' installation
        - Notes
            - $PREFIX refers to the installation directory/path
                + Default: /usr/local
        ```bash
        cp -r src/scripts $PREFIX/bin/shellkit
        ```

> Libraries

- Copy the 'src/lib' directory to your library directories
    - User-space .local directory in your $HOME
        ```bash
        cp -r src/lib $HOME/.local/lib/shellkit
        ```
    - System-level 'build-from-source' installation
        - Notes
            - $PREFIX refers to the installation directory/path
                + Default: /usr/local
        ```bash
        cp -r src/lib $PREFIX/lib/shellkit
        ```

### Host System Setup

> System PATH environment variable

- Add the toolbox's directory path into your shell's rc file
    - BashRC
        ```bash
        export PATH=$PATH:"$HOME/.local/bin/shellkit"
        ```

- Change permission modifier of scripts to executable
    ```bash
    chmod u+x $HOME/.local/bin/shellkit
    ```

## Documentations

### Libraries

### Scripts
+ [tmux-sessionizer](docs/man/tmux-sessionizer/README.md) : A tmux script that makes your workflow BLAZINGLY FAST written by ThePrimeagen by allowing you to select from existing tmux session/buffers and jump around

## Customization
+ [tmux-sessionizer](docs/man/tmux-sessionizer/customization.md)

## Wiki

### Notes
- tmux-sessionizer
    - I modified tmux-sessionizer to include
        + Check for the existence of the target directories that will be searched
        + Check for the existence of depedencies (fzf)

## Resources

## References
+ [GitHub - ThePrimeagen/.dotfiles - tmux-sessionizer](https://github.com/ThePrimeagen/.dotfiles/blob/master/bin/.local/scripts/tmux-sessionizer)
+ [GitHub - edr3x/tmux-sessionizer - tmux-sessionizer (Modified)](https://github.com/edr3x/tmux-sessionizer)

## Remarks

