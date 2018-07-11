---
layout: post
title: Shell commands to check data usage
date: 2018-05-29
tags: ["cs"]
---

It’s good to check the status of your own data usage. Here are some commands I find useful. Check `man du`, `man df` or `man find` for more information.


### Use `df` to check disk space usage

The command `df` can be used to report disk space usage.

Below is an example to report the space usage of disk /shares/compbio, which is for our group.


```
$ df -h|grep comp

10.100.136.1@tcp:/compbio
                      100T   93T  2.2T  98% /shares/compbio
```


### Use `du` to check file space usage

The command `du` can be used to report file space usage.

Here is an example to report the file space in my folder, where “--max-depth” is the option to set the level of directory/subdirectory and “--h” is the option to print in human-readable format.

```

$ du --max-depth 1 -h /shares/compbio/Group-Yang/huanwei.wang

76G    ./reference
648M    ./software
658G    ./meQTL
979M    ./learning
1.7T    ./projects
2.4T    .
```

### Use `find` and `wc` to count the file number

The command `find` can be used to walk through all files and folders and we can combine `find` and `wc` to count the file number in your folder.

Here is an example to count the number of files.

```
$  find /gpfs/gpfs01/polaris/Q0286/huanwei.wang -type f | wc -l

68737
```

Another example is to count the number of folders.

```
$  find /gpfs/gpfs01/polaris/Q0286/huanwei.wang -type d | wc -l

1498
```