# Web stack debugging #4

Debugging an Nginx server that fails under load (Ubuntu 14.04).

Benchmarking with `ab -c 100 -n 2000 localhost/` produces hundreds of failed
requests. The Nginx error log shows `Too many open files`: the startup
defaults file `/etc/default/nginx` sets `ULIMIT="-n 15"`, far too low for
100 concurrent connections.

## Files

- `0-the_sky_is_the_limit_not.pp` — Puppet manifest that raises the ULIMIT
  to 4096 and restarts Nginx, bringing failed requests down to 0.
