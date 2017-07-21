# Getting Started for Mac

```
// Install Git
brew install git

// Creates a new ssh key, using the provided email as a label
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

// start the ssh-agent in the background
eval "$(ssh-agent -s)"
Agent pid 59566


// Add your SSH key to the ssh-agent.
// If you used an existing SSH key rather than generating a new SSH key, you'll need to replace id_rsa in the command with the name of your existing private key file. 
// Use -K option to add it to Mack Keychain
ssh-add -K ~/.ssh/id_rsa


// Copy the SSH key to your clipboard.
pbcopy < ~/.ssh/id_rsa.pub

```




```
// Set proxy, if you are behind a proxy server
git config --global http.proxy http://webproxy.intra.gsacapital.com:3128

// on windows, to cache credential
git config --global credential.helper wincred

// on windows, convert to CR LF automatically
git config --global core.autocrlf true
```

## Set up p4merge

```
$ git config --global merge.tool p4mergetool
$ git config --global mergetool.p4mergetool.cmd \
"/Applications/p4merge.app/Contents/Resources/launchp4merge \$PWD/\$BASE \$PWD/\$REMOTE \$PWD/\$LOCAL \$PWD/\$MERGED"
$ git config --global mergetool.p4mergetool.trustExitCode false
$ git config --global mergetool.keepBackup false

$ git config --global diff.tool p4mergetool
$ git config --global difftool.p4mergetool.cmd \
"/Applications/p4merge.app/Contents/Resources/launchp4merge \$LOCAL \$REMOTE"
```