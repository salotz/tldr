# runit-tools

My personal runit wrappers and other general tips

- Get values of all the runit env vars:

`runit_env`

- Check on runit running from systemd

`sudo systemctl status runit`

- Get status of all running services

`runit_status`

- List all the running services

`runit_ls_active`

- List all the available services

`runit_ls_lib`


- Enable a service in SVLIB

`runit_enable {{service_name}}`

- Disable a service

`runit_disable {{service_name}}`

- View the log for a service

`runit_log {{service_name}}`


- Generate a stub for a new service with logging etc.

`runit_new_service {{service_name}}`


- Completely remove a service from SVLIB and SVLOG dirs

`runit_rm_service {{service_name}}`

- Copy a service from your config dir to SVLIB

`runit_copy_sv_config {{service_name}}`
