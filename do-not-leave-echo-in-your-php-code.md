---
title: DO NOT LEAVE ECHO IN YOUR PHP CODE
date: 2017-04-24 22:41:57
tags:
---

### Codes
```php
<?php

# test-echo.php

fclose(STDOUT);
$STDOUT = fopen('./output', 'wb');
$i = 0;

while ($i < 10000000) {
    $i += 1;
    echo 'hello world';
}
```

```php
<?php

# test.php

$i = 0;

while ($i < 10000000) {
    $i += 1;
    $x = rand(1000000, 9999999);
}
```

### Benchmark

```
$ time php test-echo.php

real    0m10.693s
user    0m2.111s
sys     0m8.436s

```

```
$ time php test.php

real    0m5.613s
user    0m4.908s
sys     0m0.686s

```

### CPU Info
```
processor       : 0
vendor_id       : GenuineIntel
cpu family      : 6
model           : 42
model name      : Intel Xeon E312xx (Sandy Bridge)
stepping        : 1
microcode       : 0x1
cpu MHz         : 3292.518
cache size      : 4096 KB
siblings        : 4

```
