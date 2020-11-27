# The DHIS2 CLI installation guide for Linux operating systems.

## 1. Yarn installation:
```bash
$ curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
$ echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list

$ sudo apt update && sudo apt install yarn

# If you are using nvm you can avoid the node installation by running
$ sudo apt update && sudo apt install --no-install-recommends yarn

# To verify yarn installation, run
$ yarn --version
```

## 2. d2-cli installation:
```bash
$ yarn global add @dhis2/cli

# To verify d2 is installed
$ d2 --help
```
## NOTE: If the &nbsp;<strong>"d2: command not found"</strong>&nbsp; then run the below commands:
```bash
# Check path to yarn packages
$ yarn global bin

# Add yarn installed packages to path
# Example: export PATH=$PATH:/home/dhis/.yarn/bin 
$ export PATH=$PATH:<path_to_yarn_packages>

# Check if yarn is installed
 $ d2 --help
```
