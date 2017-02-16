# abuseLookup

Lookup abuse contact address.

Requires `host`, `whois` and `egrep` to be executable in any of your `PATH`
directories.

Based on [a post from Andreas Klein, to Fail2ban mailing lists](https://sourceforge.net/p/fail2ban/mailman/message/27538211/).

## Usage

```
syn$ ./abuseLookup 82.237.197.209
abuse@proxad.net
syn$ ./abuseLookup 109.190.111.190
abuse@ovh.net
syn$ ./abuseLookup 195.64.190.209
abuse@giknpc.com.ua
syn$ ./abuseLookup 8.8.8.8
security@level3.com
```

## Fail2ban

Sample fail2ban action configuration was not tested yet. Make sure to
properly set your contact address (used as reply-to), ensure that the
binaries we access using their absolute paths (`grep`, `abuseLookup`)
actually exist where we're expecting them to.
