Phync
=====

Simple rsync wrapper in PHP.

Usage
-----

Calls `rsync` with `--dry-run` option by default.

```
$ /path/to/phync file-to-sync
Generated commands:
rsync -avC --dry-run --delete '--exclude-from=exclude.lst' '--rsync-path=/usr/bin/rsync' '--rsh=/usr/bin/ssh' '/home/yuya/dev/php/phync/file-to-sync' 'foo.example.com:/home/yuya/dev/php/phync/file-to-sync'
rsync -avC --dry-run --delete '--exclude-from=exclude.lst' '--rsync-path=/usr/bin/rsync' '--rsh=/usr/bin/ssh' '/home/yuya/dev/php/phync/file-to-sync' 'bar.example.com:/home/yuya/dev/php/phync/file-to-sync'
rsync -avC --dry-run --delete '--exclude-from=exclude.lst' '--rsync-path=/usr/bin/rsync' '--rsh=/usr/bin/ssh' '/home/yuya/dev/php/phync/file-to-sync' 'baz.example.com:/home/yuya/dev/php/phync/file-to-sync'
```

With `--execute` option, synchronizes specified file.

```
Generated commands:
rsync -avC --delete '--exclude-from=exclude.lst' '--rsync-path=/usr/bin/rsync' '--rsh=/usr/bin/ssh' '/home/yuya/dev/php/phync/file-to-sync' 'foo.example.com:/home/yuya/dev/php/phync/file-to-sync'
rsync -avC --delete '--exclude-from=exclude.lst' '--rsync-path=/usr/bin/rsync' '--rsh=/usr/bin/ssh' '/home/yuya/dev/php/phync/file-to-sync' 'bar.example.com:/home/yuya/dev/php/phync/file-to-sync'
rsync -avC --delete '--exclude-from=exclude.lst' '--rsync-path=/usr/bin/rsync' '--rsh=/usr/bin/ssh' '/home/yuya/dev/php/phync/file-to-sync' 'baz.example.com:/home/yuya/dev/php/phync/file-to-sync'
```

Author
------

Yuya Takeyama
