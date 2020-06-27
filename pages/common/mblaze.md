# mblaze

> Tools for dealing with Maildir mail messages.  Contains a number of
> tools which should be used together.  For more information
> <https://github.com/leahneukirchen/mblaze>.

- Documentation:

`man mblaze`

- Get number of messages in a Maildir:

`mlist {{maildir_path}} | wc -l`

- List all messages in a Maildir and print a one line summary of each:

`mlist {{maildir_path}} | mscan`

- List unread messages in a Maildir and print those messages:

`mlist -s {{maildir_path}} | mshow`

- List messages sorted by date with newest on top:

`mlist {{maildir_path}} | msort -dr | mscan`

- List messages to a specific adress and display:

`mlist {{maildir_path}} | mpick -t 'to = "{{to_address}}"' | msort -dr | mscan`

- List messages from a specific address:

`mlist {{maildir_path}} | mpick -t 'from = "{{from_address}}"' | msort -dr | mscan`

- List messages filtering based on a regex and then display those lines:

`mlist {{maildir_path}} | magrep *:{{regex}} | mshow | grep {{regex}}`

<!-- - Copy messages according to an `mpick` pattern from one maildir to a newly created maildir: -->

<!-- `mmkdir {{maildir_B}} && mlist {{maildir_A}} | mpick -t '{{pattern}}' | xargs -I _ cp _ {{maildir_B}}/new/` -->

- Render the MIME parts of matching emails:

`mlist {{mailder_path}} | {{filter_pipeline}} | mshow -t`

- Render the 'text/plain' MIME part of a message:

`mlist {{maildir_path}} | {{filter_pipeline}} | xargs mshow _ 'text/plain'`

- Move mail from one maildir to another:

`mlist {{maildir_A}} | xargs -I _ cat _ | mdeliver {{mailbox_B}}`

- Initialize tmp folder:

`mkdir -p $HOME/.mblaze`

- Config files:
`less $HOME/.mblaze/profile`
`less $HOME/.mblaze/filter`

