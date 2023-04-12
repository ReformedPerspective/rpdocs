# RP Dreamhost Account

## Cron Jobs

Dreamhost allows us to create cron (Linux timer) jobs in the Dreamhost dashboard. This is awfully useful, since one doesn't have to log in to server via SSH and use the commandline (not that I mind ;-) ).

- Expire Ads - cron job to run the [expire-rpad.sh script](scripts.md#expire-ads).

There are some other cron jobs as well which should, probably be transferred to the Dreamhost dashboard system.

- Create RP Backup - uses `tar` and `mysqldump` to create backups and `rclone` to upload them to [PCloud](../pcloud.md).
    - There are two scripts which run, `create-rpbackup-full.sh` which runs on day *0*, and `create-rpbackup.sh` which runs on days *1* to *6*. I should probably combine them and move them to the Dreamhost system.
