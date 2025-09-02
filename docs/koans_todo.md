# KOANS 超具体的 TODO（ロードマップ準拠）

> 目的: 「1 日 30 分」で Python Koans を Day1 から緑化。毎回 2 行メモを残す。

---

## 今日まずやること（5 分）

```powershell
# 仮想環境を起動（必要なら）
# .\.venv\Scripts\Activate

# 1) 依存の動作確認（省略可）
pytest -q

# 2) 最初の 1 ファイルだけ赤を出す
pytest koans/about_asserts.py -x
```

- [ ] `koans/about_asserts.py` を開き、最初の失敗箇所を最小修正
- [ ] `pytest koans/about_asserts.py -x` で緑化を確認
- [ ] `docs/koan_notes.md` に 2 行メモを追記（テンプレ後述）
- [ ] コミット: `git add -A && git commit -m "Koans: asserts green"`
- [ ] プッシュ: `git push`

---

## 進め方テンプレ（毎回コピペで実行）

- [ ] 実行: `pytest {REL_PATH_TO_KOAN} -x`
- [ ] 最小修正で 1 件緑化（複数失敗でも 1 件ずつ）
- [ ] 再実行で緑維持確認
- [ ] `docs/koan_notes.md` に 2 行メモ追加（テンプレ使用）
- [ ] コミット: `git commit -m "Koans: {NAME} green"`

メモ用テンプレ:

```text
- {FILE} のポイント: {何が分かったか 1 行}
- つまずき/境界: {どこで詰まったか・注意点 1 行}
```

---

## 実行順チェックリスト（月次ロードマップ W1-W4）

> 参考: `koans.txt` の順序 + 月次ロードマップの到達目安

### W1（about_asserts / about_none / about_strings）

- [ ] koans/about_asserts.py
  - [ ] 赤を 1 件出す → 最小修正 → 緑化
  - [ ] メモ 2 行 → コミット → プッシュ
- [ ] koans/about_none.py
  - [ ] 赤 → 緑（`None` の等価/同一性/真偽）
  - [ ] メモ 2 行 → コミット
- [ ] koans/about_strings.py
  - [ ] 文字列リテラル/フォーマット/エスケープ
  - [ ] メモ 2 行 → コミット

### W2（about_lists / about_tuples / about_dictionaries）

- [ ] koans/about_lists.py
  - [ ] ミューテーション/スライス/append vs extend
  - [ ] メモ 2 行 → コミット
- [ ] koans/about_tuples.py
  - [ ] 不変/アンパック/一要素タプル
  - [ ] メモ 2 行 → コミット
- [ ] koans/about_dictionaries.py
  - [ ] キー存在/`get`/`setdefault`/順序
  - [ ] メモ 2 行 → コミット

### W3（about_control_statements / about_methods）

- [ ] koans/about_control_statements.py
  - [ ] if/elif/else, while/for, break/continue
  - [ ] メモ 2 行 → コミット
- [ ] koans/about_methods.py
  - [ ] 引数/デフォルト/可変長/キーワード
  - [ ] メモ 2 行 → コミット

### W4（about_classes / about_inheritance）

- [ ] koans/about_classes.py
  - [ ] クラス定義/init/self/属性
  - [ ] メモ 2 行 → コミット
- [ ] koans/about_inheritance.py（余力で OK）
  - [ ] 継承/オーバーライド/super
  - [ ] メモ 2 行 → コミット

---

## 以降のおすすめ順（任意・継続学習）

- about_list_assignments / about_string_manipulation / about_true_and_false / about_sets
- about_exceptions / about_iteration / about_comprehension / about_generators / about_lambdas
- about_with_statements / about_method_bindings / about_decorating_with_functions / about_decorating_with_classes
- about_multiple_inheritance / about_scope / about_modules / about_packages / about_class_attributes / about_attribute_access / about_deleting_objects

プロジェクト系（まとまった時間向け）:

- about_triangle_project / about_triangle_project2 / about_scoring_project / about_dice_project / about_proxy_object_project

---

## 毎朝ルーチン（固定・30 分運用）

```text
1. git pull --rebase
2. pytest -q          # 妥当性確認
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

- 1 つずつ緑にする（`-x` で最初の失敗だけを見る）
- 失敗メッセージの「期待/実際」を 2 行メモしてから修正
- `assert` の左右を `repr()` で確認して差分を把握
