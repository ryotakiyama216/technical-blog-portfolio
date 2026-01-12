# technical-blog-portfolio

## 概要
エンジニア向けの技術記事を投稿・閲覧できるブログプラットフォームです。  
個人開発を想定しつつ、実務で利用される構成・設計を意識して開発しました。

---

## URL
- GitHub: https://github.com/ryotakiyama216/technical-blog-portfolio

---

## 使用技術
### フロントエンド
- Next.js（App Router）
- Tailwind CSS

### バックエンド ※予定
- AWS Lambda（Python）
- API Gateway

### インフラ
- S3
- CloudFront
- Route53

### データベース
- DynamoDB
- S3 ※画像管理

### その他
- Git / GitHub
- Cursor
- CodeRabbit
- Notion

---

## 主な機能
- 記事一覧表示
- 記事詳細表示(Markdown)
- 記事投稿・編集・削除
- 記事投稿・編集・削除（管理者）
- タグ検索
- Markdown対応
- 画像アップロード（S3）

---

## 技術選定理由
### Next.js
- SEOを考慮したSSR/SSGが可能
- コンポーネント設計がしやすい

### DynamoDB
- 小〜中規模サービスを想定
- スキーマレスで開発スピードを優先
- Lambdaとの親和性が高い

### Lambda + API Gateway
- サーバーレス構成で運用コストを抑える
- API単位で責務を分離しやすい

---

## 工夫したポイント
- フロントとAPIを完全に分離した構成
- APIレスポンスの型を意識した設計
- Tailwindでデザインを統一
- 拡張を前提としたディレクトリ構成

---

## 今後の改善予定
- 認証機能 (Cognito)
- コメント機能
- 下書き機能
- ページネーション最適化
- 管理画面のUI改善

---

## セットアップ方法
```bash
git clone git@github.com:ryotakiyama216/technical-blog-portfolio.git
cd teck-blog
node -v
nvm use 20
node -v
npx create-next-app@latest tech-blog
cd tech-blog
npm run dev
