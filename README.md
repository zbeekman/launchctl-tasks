launchctl-tasks
===============

A set of short and sweet `launchctl` plists I have defined for running boring tasks on macOS

Why?
----

`launchctl` is the preferred means of automating tasks on macOS (over, say, `cron`). I original started
using `launchctl` to perform the following main tasks:

 - Ensuring software updates/maintanence can happen automatically/psuedo-automatically
 - I always had a manifest of installed software that was up-to-date in my time machine backups
   (via [`brew bundle`])
 - Establishing reliable reverse ssh tunnels for NAT busting, so that my macOS boxes are accessible to me
   even if they are behind some NAT on a network I don't control.

I use the [LaunchControl App] for editing and managing the plist files, since it provides some great
functionality. This is non-free software and I have purchased a license for it.

Contents
--------

__[User Agents]__

* [sh.brew.update]: Ensure homebrew's package repository remains up to date; spend less of your life waiting
  for homebrew git transactions to take place
* [sh.brew.outdated]: Keep a list of outdated formulae in /tmp so your dot files can inform you about
  outadted packages when you log in
* [sh.brew.cask.outdated]: Keep a list of outdated casks in /tmp so your dot files can inform you when apps
  installed as casks need updating
* [com.github.mas-cli.mas]: Keep a list of outdated mac App store apps in /tmp so your dot files can remind
  you to update them when you log in
* [sh.brew.bundle.dump]: Ensure you have an up-to-date `.Brewfile` in your home directory. This way, a
  manifest of installed software will always be up-to-date and make it into your TimeMachine backups should
  you need to restore your machine and re-provision it.

[`brew bundle`]: https://github.com/Homebrew/homebrew-bundle
[LaunchControl App]: http://www.soma-zone.com/LaunchControl/
[User Agents]: ./UserAgents
[sh.brew.update]: ./UserAgents/sh.brew.update.plist
[sh.brew.outdated]: ./UserAgents/sh.brew.outdated.plist
[sh.brew.cask.outdated]: ./UserAgents/sh.brew.cask.outdated
[com.github.mas-cli.mas]: ./UserAgents/com.github.mas-cli.mas.plist
[sh.brew.bundle.dump]: ./UserAgents/sh.brew.bundle.dump.plist
