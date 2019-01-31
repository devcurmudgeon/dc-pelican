layout: post
title: Measuring MAKEFLAGS -j performance
author: devcurmudgeon
date: 2019/01/31

A few years ago, while working on software build tooling, I needed to work out
what was the optimal setting for parallelising make/compile instructions.

Using some 64-core AWS machines I plotted what happened for building some
large projects using different settings for MAKEFLAGS -j. The results were
interesting, for example:

<img src=/images/qtwebkit.png>
<img src=/images/gcc.png>

For machines with up to 8 cores, I concluded that it makes sense to set

```-j = number_of_cores```

Once we're beyond 8-10 cores, though, the law of diminishing returns set in,
so it seemed (and still seems) to me that we'd be better off using the extra
cores for other work.

```
    if 'max-jobs' not in config:
        config['max-jobs'] = cpu_count()

    if 'instances' not in config:
        # based on some testing (mainly on AWS), maximum effective
        # max-jobs value seems to be around 8-10 if we have enough cores
        # users should set values based on workload and build infrastructure
        # FIXME: more testing :)
        if cpu_count() >= 10:
            config['instances'] = 1 + (cpu_count() / 10)
            config['max-jobs'] = cpu_count() / config['instances']
```

For the the general case, I'm told I should have also looked at memory
bandwidth and number of independent memory channels, so ymmv.