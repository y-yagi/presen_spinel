# ざっくりとした仕組み

```text
Ruby (.rb)
  → parse (libprism)
  → analyze (プログラム全体の型推論)
  → codegen (Cコード生成)
  → Cコンパイラでネイティブバイナリ化
```

https://github.com/matz/spinel#how-it-works

* `spinel`という上記処理を全部やる単一バイナリが提供されている
  * シェルスクリプトだったときもあるが、今はバイナリ
