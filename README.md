# SHADOMAGI System v0.1

Shadowverseのキャラクター（モノ、テトラ、エンネア、ドライツェーン）をモチーフにした4つのAI人格による、多段階意思決定支援チャットシステムです。

## 🌟 主な機能

- **Phase 1: 質問の論理構造化** (目的・選択肢・制約・判断基準の整理)
- **Phase 2: 3人格による独立した初回判断** (モノ・テトラ・エンネアの並列判断)
- **Phase 3: 相互批評** (合意点・対立点・根拠の強弱の検証)
- **Phase 4: 再検討** (他者の意見を踏まえた維持・変更・保留の判断)
- **Phase 5: ドライツェーンの最終判定** (多数決によらない独自の調停・4種の判定区分)

## 🚀 ローカル起動方法

1. 依存パッケージのインストール:
   `ash
   npm install
   `

2. 開発サーバーの起動:
   `ash
   npm run dev
   `
   ブラウザで http://localhost:3000 を開きます。

## 🔑 OpenAI APIキーの設定 (本番AIモード)

本プロジェクトはAPIキー未設定時でも**モックモード**として安全に動作します。
実際のOpenAIモデルによるリアルタイム審議を実行する場合は、以下の設定を行ってください：

1. .env.example をコピーして .env.local を作成します。
2. .env.local にあなたのOpenAI APIキーを入力します：
   `env
   OPENAI_API_KEY=sk-...
   OPENAI_MODEL=gpt-4o-mini
   `
3. 開発サーバーを起動すると、自動的に「OpenAI API接続中」モードに切り替わります。

## 🌐 Web公開（Vercelへのデプロイ）

1. 本リポジトリをGitHubにプッシュします。
2. [Vercel](https://vercel.com) にログインし、「Add New Project」からリポジトリを選択します。
3. Environment Variables（環境変数）に OPENAI_API_KEY を追加して「Deploy」をクリックします。
