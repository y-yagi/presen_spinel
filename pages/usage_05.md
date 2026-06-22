# ライブラリ

* Rubyの標準ライブラリはサポートしていないが、`Time`、`File`、`Regexp`など、よく使われそうなライブラリはSpinel内で実装されており、使用出来るようになっている


```bash
$ ./spinel -e 'puts Time.new' -E
2026-06-28 07:48:29 +0900
$ ./spinel -e 'puts "hello".match?(/hello/)' -E
true
```

* Spinel内で再実装されているので、Rubyの機能と完全に同等では無い(使えない機能などがある)

```bash
$ ./spinel -e 'Regexp.timeout = 3' -E
spinel: /tmp/spinel_eval_29556_0.rb:1: unsupported call: node 2 (CallNode `timeout=`) recv=ConstantReadNode/ty37 argc=1 arg0ty3
```
