---
layout: post
title: 换行符
date: 2016-09-02
tags: ["cs"]
---

- windows: \r\n
- unix: \n

```
sed -e 's/$/\r/' inputfile > outputfile                # UNIX to DOS  (adding CRs)
sed -e 's/\r$//' inputfile > outputfile                # DOS  to UNIX (removing CRs)
perl -pe 's/\r\n|\n|\r/\r\n/g' inputfile > outputfile  # Convert to DOS
perl -pe 's/\r\n|\n|\r/\n/g'   inputfile > outputfile  # Convert to UNIX
perl -pe 's/\r\n|\n|\r/\r/g'   inputfile > outputfile  # Convert to old Mac
```

参考： [stackoverflow.com](http://stackoverflow.com/questions/6373888/converting-newline-formatting-from-mac-to-windows)
