# require / require_relative

* `require_relative`はparse時に対象ファイルをインライン展開して解決してくれる
* `require`もある
  * が、`$LOAD_PATH`は使えない
  * なので、今の所特に使いみちは無い気がする…
  * 後述するSpinel向けのGemfile的な機能が入れば使いそう
* C拡張(ネイティブの`.so`)は読み込めない
