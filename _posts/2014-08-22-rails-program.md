---
layout: post
title: Rails Programming
date: 2014-08-22 17:56:00
disqus: y
---

## Spork
### uninitialized constant RSpec::Core::CommandLine 

Error happened when working with RSpec 3.0.0:

```
Exception encountered: 
#<NameError: uninitialized constant RSpec::Core::CommandLine>
```

Answer:

[Stackover Flow](http://stackoverflow.com/questions/24030907/spork-0-9-2-and-rspec-3-0-0-uninitialized-constant-rspeccorecommandline-n/24085168#24085168)

[replace CommandLine with Runner for RSpec 3.0.0.rc1](https://github.com/manafire/spork/commit/38c79dcedb246daacbadb9f18d09f50cc837de51#diff-937afaa19ccfee172d722a05112a7c6fR8)