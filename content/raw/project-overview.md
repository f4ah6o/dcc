# CCDCCプロジェクト概要

## 基本情報

- **プロジェクト名**: CCDCC (Claude Code Document Content Control)
- **説明**: Claude Codeを活用したドキュメント管理フレームワーク
- **バージョン**: 0.0.1
- **開発言語**: TypeScript
- **パッケージマネージャー**: pnpm

## ビジョン

「One content, any format」- 一つのコンテンツから、Claude CodeのAI機能を通じて任意の形式のドキュメント、スライド、レポートを生成する。

## 核となるコンセプト

**コンテンツ × スコープ × コンテキスト = 任意のドキュメント形式**

- **コンテンツ**: 生の情報と事実
- **スコープ**: ドキュメントの範囲と深度
- **コンテキスト**: 対象読者、目的、使用シナリオ

## 主要機能

### 実装済み
- 基本的なCLI機能
- Claude Code統合
- テクニカルライティング品質チェック（効果性・効率性・満足度）
- ドキュメント生成機能（README、CLAUDE.md、スライド）

### 開発中
- プロジェクト初期化機能
- メタデータ管理
- 高度なドキュメント生成形式

## 技術スタック

### 開発環境
- Node.js 18+
- TypeScript with ESM modules
- Vite (ビルドツール)
- Biome (コードフォーマッター/リンター)

### 依存関係
- @anthropic-ai/claude-code: Claude Code SDK
- commander: CLI フレームワーク
- chalk: ターミナルカラーリング
- inquirer: インタラクティブプロンプト

## 使用方法

### 基本コマンド
```bash
# 品質チェック
ccdcc lint

# 質問
ccdcc ask -p "質問内容"

# インタラクティブモード
ccdcc interactive

# ドキュメント生成
ccdcc gen readme --scope overview --context user
ccdcc gen claude --scope detailed --context developer
ccdcc gen slides --scope overview --context general
```

### 開発コマンド
```bash
# ビルド
pnpm run build

# 開発モード
pnpm run dev

# コード品質チェック
pnpm run check
```

## 品質フレームワーク

### 効果性 (Effectiveness)
- 明確で曖昧でない表現
- 具体例と詳細
- 誤解の防止
- 事実の正確性

### 効率性 (Efficiency)
- 論理的な構造と階層
- 明確なナビゲーション
- 冗長性のない簡潔な表現
- 重要情報の優先順位付け

### 満足度 (Satisfaction)
- 対象読者に適した語彙
- 一貫性のある丁寧な文体
- 読みやすいプレゼンテーション
- 視覚的な整理

## ロードマップ

### 最優先
- このリポジトリのセルフホスティング
- Source of Truth の確立
- 自動ドキュメント生成

### 今後の展開
- バージョン管理統合
- 図表生成機能
- 意思決定履歴管理
- メタ分析機能

## ISSUES

1. gen実行中の進捗表示
2. gen slidesのフォーマットをmarpにする
   - reference/makeslide を読むこと
3. テスト
   - vitest
