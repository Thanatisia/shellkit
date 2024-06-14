# tmux-sessionizer

## Information
### Description
+ A tmux script that makes your workflow BLAZINGLY FAST written by [ThePrimeagen](https://github.com/ThePrimeagen) by allowing you to select from existing tmux session/buffers and jump around

## Setup
### Dependencies
+ fzf

### Pre-Requisites

## Documentations

### Synopsis/Syntax
- Open up FZF (fuzzy finder) menu with various directories to select
    + Tmux will create a new session with the selected project directory (if session doesnt exist)
    ```bash
    tmux-sessionizer [dir-paths ...]
    ```

- Create a new tmux session in the specified target project directory
    ```bash
    tmux-sessionizer "directory-path-name"
    ```

### Parameters
- Positionals
    - dir-paths : Specify all directories you wish to open the menu with. Please separate all directories with a space delimiter (' ')
        + Type: ArrayList (Variable Length)
        - Notes
            + If you only supply 1, tmux-sessionizer will open up a new session with that specific directory

- Optionals
    - With Arguments
    - Flags

### Usage


## Wiki

## Resources

## References
+ [GitHub - ThePrimeagen/.dotfiles - tmux-sessionizer](https://github.com/ThePrimeagen/.dotfiles/blob/master/bin/.local/scripts/tmux-sessionizer)
+ [GitHub - edr3x/tmux-sessionizer - tmux-sessionizer (Modified)](https://github.com/edr3x/tmux-sessionizer)

## Remarks

