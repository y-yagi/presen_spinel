# 型推論

```ruby
def a(val)
  val * 2
end
puts a(2)
```

```c
static mrb_int sp_a(mrb_int lv_val) {
    SP_GC_SAVE();
  return sp_int_mul(lv_val, 2LL);
  return 0;
}
```

* `a`に指定しているのが`2`(Integer)だけなので、型が`mrb_int`になる

