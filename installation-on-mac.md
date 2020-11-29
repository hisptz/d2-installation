# The DHIS2 CLI installation guide for MacOS.

## 1. Installing d2-app-scripts
```bash
$ yarn global add @dhis2/cli-app-scripts

# To verify d2-app-scripts is installed
$ d2 --help

# Add yarn installed packages to path
# Example: export PATH=$PATH:/home/dhis/.yarn/bin 
$ export PATH=$PATH:<path_to_yarn_packages>

```

## 2. Bootstrapping
To create a new template application (or upgrade and existing React app), use the d2-app-scripts init command. 

```bash
$ d2-app-scripts init app-name
$ cd app-name

#To start app
$ yarn start
```
## 3. Proxying to remote server
Local server should whitelist 
localhost:3000 in system settings
<br>
<br>
Chrome
```bash
As of mid-July 2020, the Chrome (and Chromium) stable release channel has started to disable cross-site cookies by default. Mozilla Firefox has pushed this change to their beta channel and will likely release it to the stable channel soon.

# To enable proxying to remote server developer needs to edit SameSite Cookie Attribute when debugging app or developing app

1. Open chrome browser
2. Paste chrome://flags/#same-site-by-default-cookies in address bar
3. Set SameSite Flag to disabled
```

Mozilla
<br>
```bash
Firefox stable channel does not yet enforce this cookie policy, so for the moment everything should continue to work. Currently there doesn’t appear to be an easy way to disable the policy in Firefox Beta.
```

Safari
```bash
To disable SameSite Cookie in Safari:
1. Open Safari 
2. Go to Preferences
3. Navigate to privacy
4. Uncheck “Prevent cross-site tracking” option
```