# Windowsサポートの経緯

* 以前はMinGW / MSYS2でビルドするようになっていた
  * [Build on Windows (MinGW / MSYS2) #16](https://github.com/matz/spinel/pull/16)
* ただ、やはりサポートが大変という事でサポートは停止し、Windows環境についてWSL推奨になった
  * [ci, docs: drop native Windows (MinGW) support](https://github.com/matz/spinel/commit/38b5a22647cd59493ab118d3ccb3cb3a70aa3539)
* という訳で現在はネイティブWindowsは非対応
