# RP Support Scripts

---

## Manna Publish

For more details about this script, see the [Manna page](../manna.md#podcast-publishing-automation).

## Expire Ads

This script uses the *wp-cli* command (i.e. `wp ...`) to get the currently-published Ad (there should only be one) with the 'Ad-New' Category. Since the [PublishPress *Future*](https://en-ca.wordpress.org/plugins/post-expirator/) plugin is being used to set an expiry date for these Ad posts, the *_expiration-date* metadata is set with the Unix timestamp of that date.

This timestamp is compared with today's date (i.e. the timestamp of the date the script is being run) and the post is expired, all using the `wp` command.

Here is what this looks like:

```bash
id=$(wp post list --category_name=ad-new --post_status=publish --format=csv|grep -v 'ID'|cut -d ',' -f '1')

today=$(date +%s)

expiry=$(wp post meta get $id _expiration-date)

[ $today -ge $expiry ] && echo "EXPIRING POST ${id}" ; wp post update $id --post_status=draft || exit
```
