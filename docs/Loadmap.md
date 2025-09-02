## 🌱 なぜ "その順番" なのか ―― 成長ストーリーを先に整理します

> **ゴール像**
>
> - フロントエンド実装を高品質にこなせる
> - 生成  AI を"部下"のように扱い、出力を吟味・修正できる
> - 設計・テスト・アルゴリズムを語れるシニアエンジニア

### 1️⃣ テスト駆動 (TDD) ―― _「守」：正しい作法を身体で覚える_

- **理由**: 今後どんな技術を学んでも「壊れないコードを書く」姿勢が土台。
- **効果**:

  - コードを書く前に"期待する振る舞い"を言語化 → AI にも正確に指示できる。
  - エラー原因を筋道立てて追えるので、生成  AI の提案を検証する目が養われる。

### 2️⃣ オブジェクト指向 & デザインパターン ―― _「破」：設計を意識して壊せる_

- **理由**: TDD で守りを固めたら、次は**拡張しやすい設計**へ。
- **効果**:

  - React／Vue のコンポーネント設計や状態管理にも OOP 原則が生きる。
  - AI が生成した冗長コードを"パターン"で整理し直せる。

### 3️⃣ アルゴリズム & データ構造 ―― _「破その２」：問題解決の筋力_

- **理由**: 基本アルゴリズムはパフォーマンスとバグ低減の源泉。
- **効果**:

  - 画像処理・ロボティクス経験を抽象化し、最適化案を自力で検証。
  - AI が出した計算量の見積もりを自分でチェックできる。

### 4️⃣ システム設計 ―― _「離」：全体を俯瞰し、技術を組み合わせる_

- **理由**: Front‑end × 生成  AI × API × DB をスケールさせる力が不可欠。
- **効果**:

  - "どこまでフロントで処理し、どこからバックエンド＋ AI 推論に渡すか"の判断軸が持てる。
  - 面接で必ず聞かれる「スケーラビリティ」「キャッシュ戦略」を語れる。

### 5️⃣ Capstone ―― _「実戦」：学んだ全要素を 1 本のプロダクトに_

- **理由**: 理論とハンズオンの往復だけでは"統合力"がつかない。
- **効果**:

  - GitHub に\*\*CI 付き・テスト 100 %\*\*の実プロダクトを公開 → ポートフォリオ。
  - 生成  AI との協調ワークフロー（プロンプト → 生成 → TDD で検証）を完成形として見せられる。

---

## 🧭 学びの軸：深く学ぶ vs ざっと学ぶ（AI 時代の最適配分）

- **深く学ぶ（長期で効く汎用スキル）**

  - **TDD**（仕様化 → 検証 → 回帰の循環）
  - **OOP/デザインパターン**（変更に強い設計思考）
  - **アルゴリズム/データ構造**（計算量とメモリ感覚）
  - **システム設計**（スケーラビリティ/キャッシュ/整合性）
  - **プロンプト/コンテキスト設計**（AI を道具にする前処理力）
  - **デバッグ/プロファイリング**（計測 → 仮説 → 改善）

- **ざっと学ぶ（必要十分・プロジェクトで磨く）**
  - **フレームワーク/ツール**：FastAPI, Playwright, ccxt などは課題達成に必要な範囲で素早く着手 →TDD で固める
  - **クラウド個別機能**：必要時にドキュメント駆動で都度インクリメンタルに習得
  - **UI ライブラリ**：既存コンポーネントの活用とアクセシビリティ基礎に集中

> 方針：本ロードマップの 1–4 は「深く学ぶ」。フレームワークは Capstone と各トラックの中で「ざっと」身に付ける。

## 🛤️ もう一度：一本道プランを時系列で

| 期間           | ステージ                                  | 毎日の主タスク (30  分)                   | 週末タスク (任意)     | 主要アウトプット              |
| -------------- | ----------------------------------------- | ----------------------------------------- | --------------------- | ----------------------------- |
| **Day 1‑2**    | 0. 環境セット                             | VS Code, `pytest`, `black`, GitHub 初期化 | ―                     | 緑テスト 0 件                 |
| **Week 1‑3**   | 1. TDD 基礎<br>`python_koans`             | Koan 1 ファイルを RED→GREEN→Commit        | 振り返りメモ          | Koans 完走                    |
| **Week 4‑6**   | 2. TDD 実戦<br>`TDD‑Katas‑Python`         | 1 Kata を分割実装                         | README に設計メモ     | Bowling 等 3 Kata + GitHub CI |
| **Week 7‑10**  | 3. OOP／パターン<br>`python-patterns`     | パターン 2 件写経＋自作例＋テスト         | Zenn 記事             | 主要 8 パターン実装集         |
| **Week 11‑18** | 4. アルゴリズム<br>`TheAlgorithms/Python` | 1 アルゴリズム写経 → 自力実装 → 速度比較  | LeetCode Easy 週 2 題 | ソート・木・DP 等 完自作      |
| **Week 19‑22** | 5. システム設計<br>`system-design-primer` | 1 章読破 → Notion 要約                    | draw\.io で図作成     | URL ルーティング例など        |
| **Week 23‑24** | 6. Capstone                               | AI 利用 + TDD + OOP で小プロダクト開発    | OSS に Issue／PR      | 公開ポートフォリオ            |

---

### 🎯 成長のチェックポイント

1. **TDD 期**: テストがないコードに違和感を覚える → _品質フィルター_ 形成
2. **OOP 期**: "責務"でクラスを分割できる → React コンポーネント設計も楽に
3. **アルゴリズム期**: Big‑O を暗算できる → フロントのパフォーマンス相談に強く
4. **設計期**: キャッシュ戦略・キュー選定を説明できる → フルスタック視点獲得
5. **Capstone**: "AI にコードを書かせ、自分は設計とテストに集中"が自然体に

---

これが **「なぜその順番か」→「どう成長していくか」→「具体的に何をするか」** の全体像です。
この流れで進めれば、**生成  AI を賢く操りつつ、設計〜実装〜テストを自律的に回せるエンジニア** へ最短距離で近づけます。
さあ、Koan の一行目を直すところから始めましょう。Happy hacking!

---

以下はロードマップの **「具体的な作業手順」** を、朝の 30 分 × 平日 5 日を前提に細分化したものです。  
週末は **振り返り＋発展課題** のみ ―― 平日は “作業指示書” のように淡々と進められる形にしました。

---

## 💼 3 トラック（並走可・毎日 30 分の運用）

> 目的別に小さく回し、週末に検証と公開までを含める。

### A. キャリア（メガベンチャー/外資 IT）

- **目的**: 面接通過力（コーディング + システム設計 + 実績）
- **KPI**
  - 週: LeetCode Easy/Medium 3 題、設計要約 1 本、PR 2 本
  - 月: 模擬面接 2 回、公開記事 1 本、OSS 1 貢献
- **平日 30 分（例）**
  - 月: アルゴリズム 1 題（最適/境界ケースの口頭説明をメモ）
  - 火: コードリーディング or 既存実装のリファクタ（TDD 前提）
  - 水: ミニ設計（URL Shortener 等）を 2 段落で要約
  - 木: パターン 1 件を before/after で実装＋テスト
  - 金: 面接想定 Q&A を 3 問メモ
- **週末**: 45 分模擬面接（設計 1 テーマ）→ 改善点を Issue 化

### B. 個人収益（自動化/生成で小さく稼ぐ）

- **目的**: 小さな収益ストリームを積み上げる
- **KPI**
  - 週: 機能 1 リリース（FastAPI/CLI/自動化スクリプト）、E2E 安定率 > 95%
  - 月: 試作 1→ 検証 1→ 継続 1（MRR > 0 のストリームを 1 本）
- **平日 30 分（例）**
  - 月: 問題定義 2 行＋テスト雛形（Playwright または pytest）
  - 火: 実装（FastAPI/CLI）→ 単体テスト緑化
  - 水: E2E（Playwright）で回帰セット追加
  - 木: 計測（ログ/メトリクス）と小さな改善 1 点
  - 金: リリースノート 3 行＋ SNS/README 更新
- **週末**: 小規模ユーザー検証（友人/自分運用）→ 改善案を 3 点 Issue 化

### C. クリプト Bot 実践（研究 → 紙トレ → 本番）

- **目的**: 安全に検証 → 自動運用へ段階的に移行
- **KPI**
  - 週: 戦略 1 つのバックテスト（Sharpe≥1.0 目標）、DD≤10% を維持
  - 月: 4 週間の紙トレで安定 → 低リスクで小額本番へ
- **平日 30 分（例）**
  - 月: データ取得/前処理（ccxt + pandas）
  - 火: エントリー/エグジットの 1 ルールを実装
  - 水: 手数料/スリッページを含めて再検証
  - 木: リスク管理（ポジションサイズ/損切り）を TDD で関数化
  - 金: 監視/通知（DRYRUN）を追加
- **週末**: 1 週間の結果レビュー → 改善仮説を 1 つだけ採用

> 注意: 取引はリスクがあります。必ず紙トレ/小額/自己責任で段階的に。

## 0️⃣ 環境セット（Day 1-2）

| 手順 | コマンド／操作                                                      | 終了判定                           |
| ---- | ------------------------------------------------------------------- | ---------------------------------- |
| 1    | `pyenv install 3.12.3 && pyenv virtualenv 3.12.3 tdd-env`           | `python -V` が 3.12.\*             |
| 2    | `pip install pytest pytest-cov pytest-watch black isort pre-commit` | `pytest -q` が 0 Passed            |
| 3    | VS Code 拡張: **Python**, **GitLens**, **Error Lens** を有効化      | エラーがインラインで赤線表示される |
| 4    | `.pre-commit-config.yaml` 生成 → `pre-commit install`               | `git commit` で Black が走る       |
| 5    | GitHub 新規リポジトリ → `main` 保護ブランチ & PR 必須設定           | `git push -u origin main` が成功   |

---

## 1️⃣ TDD 基礎：Python Koans（Week 1-3）

- **平日ループ（30 分）**
  1. `pytest python_koans/about_asserts.py -x` ← 1 つだけ “赤”
  2. 該当行を修正 → テスト緑化 → `git commit -m "Fix asserts koan"`
  3. **AI に質問**: 「なぜこのアサーションが通るのか 2 行で」
  4. チャット内容を `docs/koan_notes.md` に貼付
- **週末タスク**
  - `git log --oneline --stat` を眺めて **コミット粒度** を自己レビュー
  - 気付きは GitHub Discussion にメモ（後で面接ネタになる）

---

## 2️⃣ TDD 実戦：Kata（Week 4-6）

| 分    | 行動                                                  | TIP                                               |
| ----- | ----------------------------------------------------- | ------------------------------------------------- |
| 0-5   | 課題仕様を _日本語 2 行_ で要約し `README` 冒頭に追記 | “AI に指示” しやすくする                          |
| 5-10  | `pytest --maxfail=1 -q` → RED を確認                  | 落ちるテストを 1 つずつ                           |
| 10-25 | 実装を書き、緑化 → コミット                           | コミットメッセージは “テスト名: 振る舞いを満たす” |
| 25-30 | `pytest --cov` でカバレッジ確認 (>95%)                | 足りなければテスト追加                            |

- **Bowling / FizzBuzz / Roman Numerals** の順で 3 つ完了したら：
  - GitHub Actions で `pytest` + `black --check` ワークフローを設定
  - README に **AI から得た学び TOP3** を追記

---

## 3️⃣ OOP & デザインパターン（Week 7-10）

| 週  | 平日タスク                                      | 週末タスク                                      |
| --- | ----------------------------------------------- | ----------------------------------------------- |
| 7   | **Strategy** & **Observer** を写経 → テスト追加 | “もし React コンポーネントなら？”を Zenn 記事に |
| 8   | **Factory** & **Singleton**                     | 過剰 Singleton のアンチパターン例をまとめる     |
| 9   | **Decorator** & **Adapter**                     | Python デコレータ機能と比較し図解               |
| 10  | **Command** & **Template Method**               | 8 パターンを **1 画面図** に整理                |

- **AI 活用ルール**
  - 「X パターンを使って冗長コードを 30 行以内にリファクタ」→ AI に提案させ、**自分でテストを通す**
  - 差分レビューで **”before / after”** コメントを書き、理解を可視化

---

## 4️⃣ アルゴリズム & データ構造（Week 11-18）

1. **平日 1 アルゴリズム**

   - 写経 → 自力実装 → `timeit` で比較 → README に **ms 単位** 記録
   - 難易度順：配列 → 連結リスト → 木 → グラフ → DP

2. **火・木：LeetCode Easy**

   - “AI に初期解を生成させ → 自分で最適化” フロー実験
   - Big-O をコメントで明示

3. **週末**

   - `pytest-benchmark` で週次レポート → `docs/benchmarks/W12.md` など

---

## 5️⃣ システム設計（Week 19-22）

- **平日**
  1. `system-design-primer/README.md` 1 章読破 → 2 段落要約を Notion
  2. 例題（URL Shortener など）の **スケーリングポイント** を draw.io で矢印付け
  3. “AI に質問”：「この構成で QPS 10→10k のボトルネックは？」→ 返答を検証
- **週末**
  - 1 つ選び **スライド 5 枚** を作成（設計面接シミュ）
  - Zenn に公開 → SNS でアウトプット習慣

---

## 6️⃣ Capstone（Week 23-24）

| 日程      | 内容                                                     |
| --------- | -------------------------------------------------------- |
| Day 1     | **Problem Pitch**: 自分 or 友人の課題を 2 行で定義       |
| Day 2     | 技術選定：React + FastAPI + PG + OpenAI / Ollama etc.    |
| Day 3     | GitHub Project で Issue 化（**ユーザーストーリー形式**） |
| Day 4     | Skeleton & CI（lint/pytest）セット                       |
| Day 5-10  | **TDD→ 実装 →AI レビュー** を 1 機能ずつ回す             |
| Day 11    | e2e テスト（Playwright）追加                             |
| Day 12-13 | README 充実：**技術選定理由・AI ワークフロー図**         |
| Day 14    | デプロイ（Fly.io / Render 等）& SNS 公開                 |

---

## 🔖 毎朝のルーチン（テンプレ）

```text
1. git pull --rebase
2. pytest -q          # 妥当性確認
3. 今日の目標を GitHub Issue にチェックリストで追記
4. Pomodoro 25分 ×1 で実装 / 学習
5. Issue コメントに学びを1行メモ → commit → push
6. KPI を Notion に1行記録（Career/Indie/Crypto）
```

> **⚠️ 重要**  
> コードを書く前に _必ず_ 「AI に要件を自然言語で説明 → テスト雛形生成」を行う。  
> 生成結果をそのまま信じず、**テストが先・実装は後** を徹底。

---

## 🎓 修了時に得られるもの

- ✔ **GitHub**：100+ コミット／8 パターン実装／CI ＋ CD 完備プロダクト
- ✔ **Notion／Zenn**：設計・アルゴリズム解説記事 10 本
- ✔ **面接回答集**：キャッシュ戦略・Queue 選定・AI 活用フロー
- ✔ **日々の習慣**：30 分 × 120 日の“積み上げログ”

---

### 🚀 次のアクション

1. **今日**: Python Koans リポジトリを Fork → Day 1 ブランチを作成
2. **明日朝**: `about_asserts.py` 1 つ目のテストを緑化
3. **金曜夜**: 1 週目の所感を GitHub Discussion に投稿（公開ログ化）

これで **“生成 AI × TDD”** の歯車が回り始めます。  
小さな緑化を積み重ね、**AI を部下にする習慣** を身体に刻み込みましょう。Happy hacking!

---

### 📦 まず `git clone` しておくリポジトリ一覧

| ステージ            | 学習フェーズで使う主リポジトリ                                      | Clone コマンド                                                                                                                                                                                                                |
| ------------------- | ------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1. Koans**        | **python_koans** – インタラクティブにテストを緑化するチュートリアル | `git clone https://github.com/gregmalcolm/python_koans.git` ([GitHub](https://github.com/gregmalcolm/python_koans?utm_source=chatgpt.com "gregmalcolm/python_koans: Python Koans"))                                           |
| **2. TDD-Katas**    | **TDD-Katas-Python** – Bowling など代表的 Kata を Python で練習     | `git clone https://github.com/garora/TDD-Katas-Python.git` ([GitHub](https://github.com/garora/TDD-Katas-Python?utm_source=chatgpt.com "garora/TDD-Katas-Python: This repository contains Hands ..."))                        |
| **3. パターン**     | **python-patterns** – GoF デザインパターンの実装集                  | `git clone https://github.com/faif/python-patterns.git` ([GitHub](https://github.com/faif/python-patterns?utm_source=chatgpt.com "A collection of design patterns/idioms in Python"))                                         |
| **4. アルゴリズム** | **TheAlgorithms/Python** – ソート・グラフ・DP など網羅実装          | `git clone https://github.com/TheAlgorithms/Python.git` ([GitHub](https://github.com/TheAlgorithms/Python?utm_source=chatgpt.com "TheAlgorithms/Python: All Algorithms implemented in Python"))                               |
| **5. システム設計** | **system-design-primer** – 大規模システム設計のベストプラクティス   | `git clone https://github.com/donnemartin/system-design-primer.git` ([GitHub](https://github.com/donnemartin/system-design-primer?utm_source=chatgpt.com "donnemartin/system-design-primer: Learn how to design large- ...")) |

#### 追加（トラック向け）

| 目的             | 学習/実装で使う主リポジトリ                    | Clone コマンド                                                                                                                                                                 |
| ---------------- | ---------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| バックエンド     | **FastAPI** – 高速な Python API フレームワーク | `git clone https://github.com/tiangolo/fastapi.git` ([GitHub](https://github.com/tiangolo/fastapi?utm_source=chatgpt.com "tiangolo/fastapi: FastAPI framework"))               |
| E2E/自動化       | **playwright-python** – E2E/自動操作           | `git clone https://github.com/microsoft/playwright-python.git` ([GitHub](https://github.com/microsoft/playwright-python?utm_source=chatgpt.com "microsoft/playwright-python")) |
| クリプト取引 API | **ccxt** – 取引所横断 API クライアント         | `git clone https://github.com/ccxt/ccxt.git` ([GitHub](https://github.com/ccxt/ccxt?utm_source=chatgpt.com "ccxt/ccxt: Crypto trading library"))                               |

> 💡 **使い方のヒント**
>
> - 各フェーズ開始時に `git remote rename origin upstream` → 自分の GitHub に **fork → origin** を追加しておくと PR 練習がしやすくなります。
> - `pre-commit install` をリポジトリごとに仕込むと Black/Isort が自動で走り、TDD に集中できます。

これでロードマップ各段階の教材は揃いました。次は **python_koans** を Fork → Day-1 ブランチを切り、最初のテストを緑にしてみましょう。Happy cloning!
