# Autoremote

Automatically copy config files in `~/.autoremote/` to remote hosts.

# Usage

Add the bundle, create `~/.autoremote/` and populate it with the config files you want to push to all your remote hosts.
From then on, use `s` instead of `ssh` to ssh into a remote host (you are wasting time with the addional `sh` anyway...).

The bundle will remember all hosts it pushed the files to in `~/.known_autoremote`, if you make changes to your config,
just flush the file and the config will be pushed again next time you `s` into the host.

For convenience, there is a bash function `sf` that remove the passed hostname (as well as the IP the hostname resolves to)
from `~./ssh/known_hosts` and `~/.known_autoremote`.
