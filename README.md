# azure-tooling

List of common pre-requisites tools for developing in Azure.

## Visual Studio Code

https://code.visualstudio.com/

So much more than a text editor yet very lightweight and intuative to use. After installing vscode and cloning this repo (needs Git, see below) install the recommended vscode extentions.

Open your project directories in VS Code.
``` bash
# Navigate to your local working directory
cd repo

# Clone this repo 
git clone https://github.com/axgonz/azure-tooling.git

# Navigate to the cloned directory
cd azure-tooling

# Open with VS Code 
code .
```

## Git

https://git-scm.com/

Git is a source control tool used interact with local and remote repositories (repos). When installing make sure to also install the Credential Manager used to assist authenticating with remote repos.

> Tip: Select VSCode as your editor. 

Comman commands:

- git clone
- git fetch
- git status
- git add --all
- git commit -m "my message"
- git push
- git pull

## posh-git 

https://www.powershellgallery.com/packages/posh-git/1.1.0

Adds information to the Powershell CLI prompt when working in a Git directory. After installing use your Powershell profile to import it.

Run as Administrator

``` powershell
# Install posh-git 
Set-ExecutionPolicy RemoteSigned;
Install-Module -Name posh-git
```

Run as normal user

``` powershell
# Open your Powershell profile using notepad
notepad $profile

# Add the posh-git import statement to your profile
Import-Module -Name posh-git
```

## Azure CLI (and Bicep)

https://learn.microsoft.com/en-us/cli/azure/install-azure-cli

Great to work with Bicep files and to query state from Azure. It is worth investing time to become familiar with the Azure CLI as well as bash espacially if using GitHub Actions or DevOps pipelines. 

Install bicep using azure CLI

``` bash
# Install bicep
az bicep upgrade
```

## Windows Subsytem for Linux (WSL) v2

https://learn.microsoft.com/en-us/windows/wsl/install

If you are using a windows machine WSL v2 is the cleanest way to get a bash shell. 

Run as Administrator

``` powershell
# Install WSL v2
wsl --install
```

> Tip: Use the same version of Ubuntu as your GitHub Actions or DevOps Pipelines.

# Next

Authenticate your GitHub Actions with Azure using OIDC and a Managed Identity. 

https://github.com/axgonz/githubsecrets