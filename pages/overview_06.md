# 対応していないRubyの機能

* Rubyの全機能はサポートしていない
  * `eval`や、`send`などの動的な処理は完全サポートではない
    * 実行時にパーサが必要な機能は使えない
  * `Thread`も使えない
    * `Fiber`は使える
  * 他にもサポートしていない記法がある
    * multiple assignmentとか
* 詳細は[公式のドキュメント](https://github.com/matz/spinel/blob/master/docs/limitations.md)参照
