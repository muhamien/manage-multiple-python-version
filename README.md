
# Installing pyenv on macOS

## Step 1: Update Homebrew and Install pyenv
```bash
brew update
brew install pyenv
```

### Alternatively, clone the repository to get the latest version of pyenv
```bash
git clone https://github.com/pyenv/pyenv.git ~/.pyenv
```

## Step 2: Define your environment variables
For recent macOS versions, replace `~/.bash_profile` with `~/.zshrc` as the default shell is Zsh.

```bash
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
echo 'eval "$(pyenv init -)"' >> ~/.zshrc
source ~/.zshrc
```

## Step 3: Restart your shell so the path changes take effect
```bash
exec "$SHELL"
```

## Step 4: Verify the installation and check the available Python versions
```bash
pyenv install --list
```

## Step 5: Install the required Python version
```bash
pyenv install 3.10
```

## Step 6: Set it as your global version after installation
```bash
pyenv global 3.10
```

## Step 7: Update pyenv paths and verify your current Python version
```bash
eval "$(pyenv init --path)"
python3 --version
```
