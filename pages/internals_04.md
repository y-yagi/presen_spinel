# 型推論

```ruby
def a(val); val * 2; end
puts a(2)
puts a('a')
```

```c
static sp_RbVal sp_a(sp_RbVal lv_val) {
    SP_GC_SAVE();
    SP_GC_ROOT_RBVAL(lv_val);
  return sp_poly_mul(lv_val, sp_box_int(2LL));
  return sp_box_nil();
}

```

* `a`に`String`も指定しているので、型が`sp_RbVal`になる
* `sp_RbVal` はアクセスのたびにタグ確認とunboxが必要で、具体型(例: `mrb_int`)より遅い
* 型推論では「できる限り `sp_RbVal` を避けて具体型に絞り込む」ようになっている
