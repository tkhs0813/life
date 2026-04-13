# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## このリポジトリについて

ryoの生活をClaude Codeで支援するためのリポジトリ。コードプロジェクトではなく、日々の情報収集・タスク管理・思考の補助をスキルやツールで自動化・効率化する場所。

## 方針

- 日本語で対応する
- ファイルはMarkdownで管理し、シンプルに保つ
- 新しいスキルやツールを継続的に追加していく前提で設計する

## 構造

- `feeds.yml` — RSSフィード定義（デイリーダイジェスト等で使用）
- `digests/` — 生成されたダイジェスト記事の保存先（`YYYY-MM-DD.md`形式）
- `.claude/skills/` — Claude Codeのカスタムスキル置き場。各スキルは独自ディレクトリに`SKILL.md`を持つ

## スキル開発ガイドライン

新しいスキルを追加する際:

- `.claude/skills/{skill-name}/SKILL.md` に配置する
- SKILL.mdのfrontmatterに `name`, `description`, `user-invocable`, `allowed-tools` を定義する
- `description` はスキル検索に使われるため、日本語・英語の両方のキーワードを含める
- テンプレートや設定ファイルが必要な場合は同ディレクトリ内に置く
- 出力ファイルの保存先はリポジトリルート直下に専用ディレクトリを作る（例: `digests/`）
