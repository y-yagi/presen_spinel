# パイプライン

* parse (`src/spinel_parse.c`): libprismでRubyをパースしてテキストASTを出力
  * `require_relative` はパース時にインライン展開
* ASTを読み込みしてin-memoryの`NodeTable`に load する
* analyzeとcodegen は同一プロセスで in-memory モデルを共有する
  * 昔はanalyzeとcodegenが別のCLIだったが、in-memoryで共有する事で高速になった
