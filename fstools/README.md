Contains following:

    fs_mark
    dbench
    xfsprogs
    fio (built from github)
    blktrace
    btrfs-progs
    e2fsprogs
    perf

To use these tools on files on host, pass the directory as a volume and then operate on them as usual.

Example:
```
docker run -v /dir/:/dir/ -it –rm –name test ronin/fstools xfs_io -c 'mmap -rw 0 10M' -c 'mmap' -c “mincore” /dir/file
```
