---
title: How to Set Up a Static Site with Jekyll      # FM must either be COMPLETELY filled out or EMPTY between the lines for site to not break
description: A brief guide of how to get a static site up and running using Jekyll.
date: 2025-06-09 23:41:00 -0400
categories: [Blogging, Guide]
tags: [jekyll]     # TAG names should always be lowercase
image: /assets/img/jekyll.png
---

## Why Learn Jekyll?
Jekyll is a free static site generator that is vastly more simple than other website learning models like HTML and CSS, yet complex enough for recruiters to care about this particular skill. It’s open source, easy to learn, and allows for free hosting on Github. I’m confident that Jekyll will be a great asset to anyone who decides to learn it, especially to those who have never made or learned how to make a traditional website before.

## Prerequisites
This guide will be using the Windows installation and configuration process.

#### Having VS Code installed
I highly recommend using VS Code when dealing with Jekyll sites. It lets you edit the files within your Jekyll site, it has built in version control using Git and Github, and it also has a terminal with various types of shells, such as WSL, Git Bash, Powershell, and more. Some of these you’ll have to download, some are pre-installed. Either way, VS Code is exceptional, I use it for my site and for other things, and I think you should as well.

#### Understanding the CLI
Jekyll sites are created, maintained, and updated using the Command Line Interface terminal and an IDE to manage files. If you’ve never used the Terminal before, I suggest searching up some guides on Youtube to learn it at a basic level. Beyond that isn’t required for Jekyll, but it will be to your benefit.

#### Downloading Ruby
To download Ruby, navigate to Ruby’s website and download the most stable version of the Ruby+Devkit installer, and for the purpose of this guide, it’s the `Ruby+Devkit 3.3.8-1 (x64)` installer. This is due to the Gem file error only being fixable using this version, as far as I'm aware.

![Ruby Installers](https://raw.githubusercontent.com/SalihWarsama/salihwarsama.github.io/34577169f887319d2742e7a882f4618d54565aec/assets/img/ruby-install-jekyll.png)

Run the installer with default settings, unless otherwise desired.

Once the Finish button appears, select the checkbox that says `Run 'ridk install'`. This will open the Terminal for a subsequent installation of the Ruby Devkit once you hit the Finish button.

![Ruby Ridk Checkbox](https://raw.githubusercontent.com/SalihWarsama/salihwarsama.github.io/34577169f887319d2742e7a882f4618d54565aec/assets/img/ruby-ridk-checkbox.png)

Click the Finish button and wait for the Terminal to open.

![Ruby CLI](https://raw.githubusercontent.com/SalihWarsama/salihwarsama.github.io/34577169f887319d2742e7a882f4618d54565aec/assets/img/ruby-ridk-cli.png)

> Note: This is an older screenshot. It should say `“RubyInstaller 3 For Windows”` since we installed version `3.3.8-1`.
{: .prompt-info }

The Terminal will ask for user input beyond this point, and the options given are 1, 2, and 3. You can just hit the Enter key if you’re unsure, but it’s better to be safe and download all the options separately by inputting 1 and hitting enter, then similarly for 2 and 3.

If prompted to enter Y or N at any point when installing these options, always enter Y to continue.

Once all options have been installed, you may close the Terminal.

#### Bonus: Having Git Installed
I highly recommend installing Git because Jekyll works with it very well, so well that Jekyll automatically creates Git related files like the .gitignore file to maximize efficiency. You can download Git here.

#### Double bonus: having a Github account.
I also highly recommend creating a Github account. Just head to Github.com and create one there. It’s free, you get access to many developer benefits such as creating repositories and contributing to others, and when coupled with Jekyll, you can host your website on the cloud for free using Github Pages. You can create an unlimited amount of project sites, but only one if it’s a personal site.

## How to Download Jekyll with Bundler
Now you’re ready to download Jekyll with the Bundler gem.

Open your Terminal, and type in:

```powershell
ruby -v
```

If this doesn’t return an error, then that means Ruby was successfully installed.

Similarly, type in:

```powershell
gem -v
```

If this also doesn’t return an error, you’re ready to move on.

Now, to install Jekyll with Bundler, type in:

```powershell
gem install jekyll bundler
```

If you’re using the WSL terminal, then type in:

```wsl
sudo gem install jekyll bundler
```

This is because the command without `sudo` won’t work in WSL due to permission issues.

> Disclaimer: this is where the gem file error typically appears; if no error shows up, type in `jekyll -v` and if no error shows up, you successfully downloaded Jekyll and can safely skip the next section about the gem file error.
{: .prompt-warning }

Also check to see if bundler is properly installed by typing in `bundler -v`.
