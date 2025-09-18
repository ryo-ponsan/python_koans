# KOANS 学習 TODO（pytest 未経験者向け・ロードマップ準拠）

> ゴール: 「1 日 30 分」で TDD の型を身体化。pytest 未経験でも、最短で RED→GREEN を回せるようになる。各回 2 行メモを残す。

---

## 今日まずやること（5 分）（起動エラー回避込み）

```powershell
# 仮想環境（必要なら）
# .\.venv\Scripts\Activate

# 0) pytest の外部プラグイン自動読込を止めて実行（web3 由来の ImportError 回避）
$env:PYTEST_DISABLE_PLUGIN_AUTOLOAD=1; pytest -q

# 1) 最初の 1 ファイルだけ赤を出す（最初の失敗で止める）
$env:PYTEST_DISABLE_PLUGIN_AUTOLOAD=1; pytest koans/about_asserts.py -x -q
```

- [ ] `koans/about_asserts.py` を開き、最初の失敗箇所を最小修正
- [ ] 実行: `$env:PYTEST_DISABLE_PLUGIN_AUTOLOAD=1; pytest koans/about_asserts.py -x -q` で緑化確認
- [ ] `docs/koan_notes.md` に 2 行メモ（テンプレ下記）
- [ ] `git add -A && git commit -m "Koans: asserts green" && git push`

---

## pytest ミニチートシート（最小セット）

- **実行の粒度**: `pytest path/to/file.py -x -q`
- **最初の失敗で停止**: `-x`
- **静かな出力**: `-q`
- **プラグイン無効（本リポ前提）**: `PYTEST_DISABLE_PLUGIN_AUTOLOAD=1`
- **単一テスト名を部分一致で実行**: `-k substring`
- **デバッグ出力を表示**: `-s`

理解ポイント（今回の Koans 範囲で十分）

- **assert の読み方**（左: 実際、右: 期待 で書くと読みやすい）
- **等価と同一**: `==` と `is` の違い
- **例外の概念**（Koans は `unittest` ベース。pytest では `with pytest.raises(...)` だが今回は概念理解で OK）

---

## 進め方テンプレ（毎回コピペで実行）

- [ ] 実行: `$env:PYTEST_DISABLE_PLUGIN_AUTOLOAD=1; pytest {REL_PATH_TO_KOAN} -x -q`
- [ ] 最小修正で 1 件だけ緑化（複数失敗でも 1 件ずつ）
- [ ] 再実行で緑維持を確認
- [ ] `docs/koan_notes.md` に 2 行メモを追加
- [ ] コミット: `git commit -m "Koans: {NAME} green"`

メモ用テンプレ:

```text
- {FILE} のポイント: {何が分かったか 1 行}
- つまずき/境界: {どこで詰まったか・注意点 1 行}
```

---

## 学習トピック（この順で押さえる）

- **assert / 真偽値**: assert の失敗出力、truthy/falsy
- **None / 等価・同一**: `==` と `is`、`None` の比較
- **文字列**: リテラル、フォーマット、エスケープ
- **リスト**: スライス、ミューテーション、`append` vs `extend`
- **タプル**: 不変、アンパック、一要素タプル
- **辞書**: `in`、`get`、`setdefault`、順序
- **集合**: 積・和・差・対称差
- **制御構文**: if/elif/else、for/while、break/continue
- **関数**: 位置/キーワード/デフォルト/可変長
- **例外**: raise/try/except/else/finally（概念理解）
- **反復**: `for`、イテレータの基本
- **内包表記**: list/dict/set の内包表記
- **ジェネレータ**: `yield` の基本（概念）
- **with 文**: コンテキストマネージャの意義（概念）
- **クラス/継承**: `__init__`、属性、オーバーライド、`super()`

---

## 実行順チェックリスト（W1-W4 ｜厳選 Koans）

> ロードマップ @`docs/Loadmap.md` の「1️⃣ TDD 基礎」内の 3 週間想定。毎日 1 ファイル or 1 セクション。

### W1（基礎・RED→GREEN を身体化）

- [ ] `koans/about_asserts.py`
  - [ ] assert の読み方／比較演算の基礎
- [ ] `koans/about_true_and_false.py`
  - [ ] truthy/falsy、空コレクションと 0 の扱い
- [ ] `koans/about_none.py`
  - [ ] `None` と `==`/`is` の違い
- [ ] `koans/about_strings.py`
  - [ ] 連結・フォーマット・エスケープ

### W2（コレクション）

- [ ] `koans/about_lists.py`
  - [ ] スライス、`append` vs `extend`、コピーの落とし穴
- [ ] `koans/about_list_assignments.py`
  - [ ] 参照 vs 値、シャローコピー
- [ ] `koans/about_tuples.py`
  - [ ] 不変・アンパック・一要素タプル
- [ ] `koans/about_dictionaries.py`
  - [ ] `get`/`setdefault`、存在確認、順序
- [ ] `koans/about_sets.py`
  - [ ] 和/積/差/対称差

### W3（制御・関数・例外）

- [ ] `koans/about_control_statements.py`
  - [ ] if/elif/else、for/while、break/continue
- [ ] `koans/about_methods.py`
  - [ ] 位置/キーワード/デフォルト/可変長
- [ ] `koans/about_exceptions.py`
  - [ ] try/except/else/finally と raise（概念）
- [ ] `koans/about_iteration.py`
  - [ ] イテレーションの基本
- [ ] `koans/about_comprehension.py`
  - [ ] list/dict/set 内包表記

### W4（発展・オブジェクト指向）

- [ ] `koans/about_generators.py`（概念把握を優先）
- [ ] `koans/about_with_statements.py`（概念）
- [ ] `koans/about_classes.py`
- [ ] `koans/about_inheritance.py`
- [ ] 余力: `koans/about_attribute_access.py`

---

## 週末 15 分チェック（任意）

- [ ] 本週の「つまずき 1 点」を `docs/koan_notes.md` で再現メモ
- [ ] 来週の先取り 1 ファイルを開いて RED を 1 回だけ出す

---

## 毎朝ルーチン（固定・30 分運用）

```text
1. git pull --rebase
2. $env:PYTEST_DISABLE_PLUGIN_AUTOLOAD=1; pytest -q  # 妥当性確認
3. 今日の目標を Issue に 1 行で追記
4. 25 分実装（Pomodoro）
5. 学びを 2 行メモ → commit → push
```

---

## コミット規約（短く、行動が分かる）

- Koans: {file} green
- Koans: {file} fix edge case
- Docs: add koan_notes for {file}

---

## トラブル時のヒント

- 最初の失敗だけに集中（`-x`）
- 失敗の「期待/実際」を 2 行でメモ → 修正
- 比較が読みにくいときは `repr()` を挟んで差分把握
