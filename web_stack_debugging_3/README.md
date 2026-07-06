# Web stack debugging #3

Debugging a WordPress site running on a LAMP stack (Ubuntu 14.04).

Using `strace` on the Apache process reveals a failed `open()` call on
`class-wp-locale.phpp` — a typo (`.phpp` instead of `.php`) inside
`/var/www/html/wp-settings.php`, which makes Apache return
`500 Internal Server Error`.

## Files

- `0-strace_is_your_friend.pp` — Puppet manifest that fixes the typo with
  `sed`, restoring the site to `200 OK`.
