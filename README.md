# Configure terminal with Oh My Zsh and spaceship

### Install Zsh

### Check for existence
```bash
$ zsh --version
```
### If not, install
```bash
$ sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

### Install Spaceship
```bash
$ git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt"
```

### Create a symbolic link
```bash
$ ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"
```

### Set Spaceship Theme

### Enter in ~ / .zshrc
```
$ sudo nano ~ / .zshrc
```

> Within ```~ /.zshrc```, find the line ```ZSH_THEME and change``` it to > ```ZSH_THEME = "spaceship"```

### Additional configurations

### Configure Spaceship

### At the end of the ~ / .zshrc file I add the following content
```
SPACESHIP_PROMPT_ORDER=(
  user          # Username section
  dir           # Current directory section
  host          # Hostname section
  git           # Git section (git_branch + git_status)
  hg            # Mercurial section (hg_branch  + hg_status)
  exec_time     # Execution time
  line_sep      # Line break
  vi_mode       # Vi-mode indicator
  jobs          # Background jobs indicator
  exit_code     # Exit code section
  char          # Prompt character
)
SPACESHIP_USER_SHOW=always
SPACESHIP_PROMPT_ADD_NEWLINE=false
SPACESHIP_CHAR_SYMBOL="❯"
SPACESHIP_CHAR_SUFFIX=" "
```

### Plugins ZSH
```bash
$ sh -c "$(curl -fsSL https://raw.githubusercontent.com/zdharma/zinit/master/doc/install.sh)"
```

### Enter in ~ / .zshrc, after the line ### End of Zinit's installer chunk add
```
zinit light zdharma/fast-syntax-highlighting
zinit light zsh-users/zsh-autosuggestions
zinit light zsh-users/zsh-completions
```

### Description of the plugins installed above
- <b>zdharma / fast-syntax-highlighting</b>: Adds syntax highlighting when writing commands that makes it easier to recognize commands that were typed incorrectly;

- <b>zsh-users / zsh-autosuggestions</b>: Suggests commands based on the execution history as you type;

- <b>zsh-users / zsh-completions</b>: Adds thousands of completitions for common tools like Yarn, Homebrew, NVM, Node, etc., so you only need to press TAB to complete commands;
