# FFI

* Cの関数を呼ぶための機能(FFI)が組込で提供されている

```ruby
module LibM
  ffi_func :sqrt, [:double], :double
  ffi_func :pow,  [:double, :double], :double
end

module LibC
  ffi_func :strlen, [:str], :size_t
end
```

```ruby
puts LibM.sqrt(16.0).to_i # => 4
puts LibC.strlen("hello, world") # => 12
```
