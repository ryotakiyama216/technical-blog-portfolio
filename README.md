# technical-blog-portfolio
# Tech Blog Platform

## 概要
エンジニア向けの技術記事を投稿・閲覧できるブログプラットフォームです。  
個人開発を想定しつつ、実務で利用される構成・設計を意識して開発しました。

---

## URL
- Frontend: https://xxxx.cloudfront.net
- GitHub: https://github.com/xxxx/xxxx

---

## 使用技術
### フロントエンド
- Next.js（App Router）
- Tailwind CSS

### バックエンド
- AWS Lambda（Python）
- API Gateway

### インフラ
- S3
- CloudFront

### データベース
- DynamoDB

### その他
- Git / GitHub
- Docker（ローカル開発）

---

## 主な機能
- 記事一覧表示
- 記事詳細表示
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
- 認証機能（Firebase Auth）
- コメント機能
- 下書き機能
- ページネーション最適化
- 管理画面のUI改善

---

## セットアップ方法
```bash
git clone https://github.com/xxxx/xxxx.git
cd xxxx
npm install
npm run dev
