# tmux-sessionizer : Customization

## Configurations
- Edit the tmux-sessionizer script source file
    - Installed
        ```bash
        $EDITOR $PREFIX/bin/shellkit/tmux-sessionizer
        ```
    - Repository
        ```bash
        $EDITOR src/tmux-sessionizer
        ```

- Change the default project workspace directory choices in the array variable 'DEFAULT_TARGET_DIRS'
    ```bash
    DEFAULT_TARGET_DIRS=(~/work/builds ~/projects ~/ ~/work ~/personal)
    ```

## Shell Customization

> Bash

- Add the macro 'ctrl+f' on your .bashrc file
    - Explanation
        - Add a keymapping/keybinding to your bash shell instance, mapping '^f' to the command "tmux-sessionizer\n"
            - where
                + '^f' = 'Ctrl-F'
                + '\n' = Pressing the carriage return/enter key to confirm the command
    ```bash
    bindkey -s ^f "tmux-sessionizer\n"
    ```

> Zsh

- Add the macro 'ctrl+f' on your .zshrc file
    - Explanation
        - Add a keymapping/keybinding to your bash shell instance, mapping '^f' to the command "tmux-sessionizer\n"
            - where
                + '^f' = 'Ctrl-F'
                + '\n' = Pressing the carriage return/enter key to confirm the command
    ```zsh
    bindkey -s ^f "tmux-sessionizer\n"
    ```

> Fish

- Add the macro 'ctrl+f' on your config.fish file
    - Explanation
        - Add a keymapping/keybinding to your bash shell instance, mapping the control 'f' to the command "tmux-sessionizer"
            - where
                + 'f' = 'Ctrl-F'
    ```fish
    bind \cf "tmux-sessionizer"
    ```

## Tmux
- Add a keymap/keybind in '.tmux.conf' 
    - To automatically open the fuzzy finder (fzf) when starting a new tmux session by pressing '<prefix>+f'
        ```bash
        bind-key -r f run-shell "tmux neww ~/.local/bin/binutils/tmux-sessionizer"
        ```
    - To jump directly to your desired project without opening fzf
        - Explanation
            + This will create a new tmux session in the target project directory when you press the mapped keybinding (in this case, <Prefix>+k)
        ```bash
        bind-key -r k run-shell "~/.local/bin/binutils/tmux-sessionizer /path/to/target/directory"
        ```

## Resources

## References

## Remarks
