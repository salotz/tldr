# keychain

> A manager for SSH and GPG key agents. Useful for reducing the number
> of times passwords are needed and for running scripts requiring
> passwords in an automated way like cron. More information:
> https://www.funtoo.org/Keychain


- Start ssh agent from default key `~/.ssh/id_rsa`:

`keychain id_rsa`

- Start and get SSH agent variables into shell env:

`eval $(keychain id_rsa)`

- Get SSH agent variables into shell env after starting:

`source ~/.keychain/${HOSTNAME}-{{shell-name}}`

- Stop all agents:

`keychain -k all`

- Use keychain for SSH and GPG keys:

`keychain --agents ssh,gpg {{ssh_key}} {{gpg_key_id}}`

