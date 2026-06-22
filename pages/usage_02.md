# 実行

```ruby
# fib.rb
def fib(n)
  if n < 2
    n
  else
    fib(n - 1) + fib(n - 2)
  end
end

puts fib(34)
```

* `spinel`でバイナリが生成出来るので、あとはそれを実行するだけ

```bash
./spinel fib.rb #=> ./ffi.rb -> ffi
./fib  # => 5702887
```
