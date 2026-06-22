# 主なオプション

```bash
./spinel app.rb -o myapp   # 出力名を指定 (./myapp)
./spinel app.rb -c         # app.c だけ生成
./spinel app.rb -S         # Cを標準出力に出す
./spinel -E app.rb a b c   # コンパイルしてARGV付きで実行、バイナリは捨てる
./spinel -e 'puts 42'      # ソースを直接渡す
```
