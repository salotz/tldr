# mblaze

> Tools for dealing with Maildir mail messages.  Contains a number of
> tools which should be used together.  For more information
> <https://github.com/leahneukirchen/mblaze>.

- Documentation:

`man mblaze`

- Initialize tmp folder:

`mkdir -p $HOME/.mblaze`

- Get number of messages in a Maildir:

`mlist {{maildir_path}} | wc -l`

- List all messages in a Maildir and print a one line summary of each:

`mlist {{maildir_path}} | mscan`

- List unread messages in a Maildir and print those messages:

`mlist -s {{maildir_path}} | mshow`

- Config files:
  - `$HOME/.mblaze/profile`
  - `$HOME/.mblaze/filter`

