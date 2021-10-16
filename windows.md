# Windows terminal setup

## Prerequisites

* [Windows Terminal](https://www.microsoft.com/en-gb/p/windows-terminal/9n0dx20hk701)

* [chocolatey](https://chocolatey.org/)

    * To install open Admin PowerShell
    * do
        ```bash
        Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
        ```
    * close PowerShell

* [gsudo](https://github.com/gerardog/gsudo)

    * To install open Admin PowerShell
    * do
        ```bash
        choco install gsudo
        ```
    * close admin powershell

*  [MesloLGS NF Font](https://github.com/romkatv/powerlevel10k/blob/master/font.md#:~:text=Download%20these%20four%20ttf%20files%3A)

    * Download these four fonts
    * Install them all

## Step by step
* open Windows Terminal

* go to Settings => Windows Powershell and change the font to MesloLGS NF

* do one by one
```bash
gsudo
Install-Module oh-my-posh -Scope AllUsers
Import-Module oh-my-posh
Get-PoshThemes
Get-PoshThemes -list
```

* you will see a list of themes, find a one you like and copy it’s name

* do 

```bash
code $PROFILE
```

* paste this (change "wopian" to the theme name of the theme you like)

```
Set-PoshPrompt -Theme wopian
```

* close the Terminal and open it again

## Done!