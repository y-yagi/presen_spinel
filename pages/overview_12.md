# サポート環境

* ランタイムはPOSIX前提で、POSIX系OSがターゲット
  * Linux(x86-64 / arm64)
  * macOS(Intel / Apple Silicon)
  * *BSDも多分動く(CIを回しているのはLinuxとmacOSのいｍ)
* Windowsは非対応
  * `<ucontext.h>`(Fiber)や`<sys/mman.h>`など、POSIX前提に依存している機能があるため
