# ランタイム構成

* ランタイムは ヘッダ + アーカイブ に分かれている
  * `lib/sp_runtime.h`: GC・配列/Hash/Stringの実装・ホットパスのinline定義
  * `lib/sp_*.c` / `lib/regexp/`: bigint・fiber・I/O・正規表現など → `libspinel_rt.a`
