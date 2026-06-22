# 未サポート

* サポートしていない機能はコンパイル時にエラー or 警告表示


```bash
$ ./spinel -e 'eval("a")'
spinel: /tmp/spinel_eval_13050_0.rb:1: unsupported eval of a runtime string is not supported by AOT compilation (define the code statically): node 2 (CallNode `eval`) recv=-/ty-1 argc=1 arg0ty6

$ ./spinel -e 'require "thread"'
warning: 'thread' is not available in Spinel; the require is ignored and code using it will fail
/tmp/spinel_eval_13316_0.rb -> a

```

