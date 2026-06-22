# この資料について(記載時点の記録)

Spinelは随時更新されているため、本資料がどの時点・どこまでの内容を元にしているかをここに記録する。

## 参照したソース

- リポジトリ: https://github.com/matz/spinel
- ローカル確認パス: `/home/y-yagi/src/github.com/matz/spinel`
- 参照コミット: `8c5a6d32fc2e9189dcd6e4264f00e7fb284b764b`
  - コミット日時: 2026-06-23 07:28:00 +0900
  - メッセージ: `Merge PR #1518: bind missing block and proc params to nil`
- タグ: なし
- 資料作成日: 2026-06-23
- 主な情報源: リポジトリの `README.md` / `docs/`(`limitations.md`, `FFI.md`, `AST.md`)/ `examples/ffi/`

## 数値(コミット時点)

- テスト: 886件パス
- ベンチマーク: 57本パス
- 性能: CRuby 4.0.4 + `--yjit` 比でジオメトリ平均 約7.8倍
  - ベンチの個別値(mandelbrot 55.8x など)もこのコミット時点の README 記載値

## カバーしている範囲

- 概要(Spinelとは / 何が嬉しいか)
- 仕組み(parse → 型推論 → C生成 → Cコンパイラ のパイプライン)
- 対応OS / 動作環境(Linux・macOS・*BSD・Windows は WSL。README の Platform 表ベース)。概要セクション内で説明
  - 参考: Windowsサポートの経緯(PR #16 / #39、Issue #192、現在はネイティブ非対応で WSL 推奨)
- コンパイラ内部(パイプライン詳細・whole-program型推論の5パス・codegenと最適化・ランタイム構成)
- 使い方(コンパイル/実行・主なオプション・対応しているRubyの機能)
- 型推論の挙動 / 整数オーバーフローの扱い
- FFI(`ffi_func`)
- `require` / `require_relative` の挙動と、RubyGems(Spinelfile + `spinel-gem`, Phase 0 / PR #747)の対応状況
- 性能(ベンチマーク抜粋)
- 制約(できないこと)とユースケース(向き・不向き)

## あえて触れていない範囲

- Cソース各ファイルの行レベルの実装詳細
- 自己ホスティング(C → Ruby → self-host → C)の歴史の詳細
  - 現在の`master`はCの実装で、自己ホスティング版は`legacy/`に回帰テスト用のオラクルとして残っている、という点のみ把握
- `make bootstrap` などビルド/開発フローの細部

## 注意

- Spinelは活発に開発中。本資料は上記コミット時点のスナップショットであり、最新の挙動・対応機能・ベンチ値とは異なる場合がある。
- 最新情報は必ずリポジトリの `README.md` / `docs/` を参照すること。
