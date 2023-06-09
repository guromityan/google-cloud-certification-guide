> 2023-04-10 [Professional Cloud DevOps Engineer 試験ガイド | Google Cloud](https://cloud.google.com/certification/guides/cloud-devops-engineer?hl=ja)

# Professional Cloud DevOps Engineer

認定試験ガイド

Professional Cloud DevOps Engineer は、Google 推奨の手法とツールを使用して、システム開発ライフサイクル全体にプロセスを実装します。また、ソフトウェアとインフラストラクチャのデリバリー パイプラインを構築してデプロイし、本番環境のシステムとサービスを最適化して保守し、サービスの信頼性と配信速度の調整を行います。

## セクション 1: サイト信頼性エンジニアリングの原則のサービスへの適用

### 1.1 サービスの変更、速度、信頼性確保の調整

- SLI を検出する（例: 可用性、レイテンシ）
- SLO を定義し、SLA を理解する
- エラー バジェットを満たさないことによる結果を受け入れる
- 次に構築するものを決定するためのフィードバック ループを作成する
- 自動化により手間を省く

### 1.2 サービス ライフサイクルの管理

- サービスを管理する（例: 新しいサービスの導入、デプロイ、保守、廃止）
- キャパシティを計画する（例: 割り当てと上限の管理）

### 1.3 運用のための健全なコミュニケーションとコラボレーションの確保

- 心身の疲労を防ぐ（例: 心身の疲労を防ぐための自動化プロセスを設定する）
- 学習する文化を育む
- 誰かのせいにしない文化を育む

## セクション 2: サービスの CI/CD パイプラインの構築と実装

### 2.1 CI / CD パイプラインの設計

- Artifact Registry を使用した不変のアーティファクトの作成と保存
- Cloud Build、Spinnaker を使用したデプロイ戦略
- Anthos、Spinnaker、Kubernetes を使用したハイブリッドおよびマルチクラウド環境へのデプロイ
- Cloud Build、Artifact Registry を使用したアーティファクトのバージョニング戦略
- Cloud Source Repositories、外部 SCM、Pub/Sub を使用した CI / CD パイプライン トリガー
- Spinnaker を使用した新しいバージョンのテスト
- デプロイ プロセスの構成（例: 承認フロー）

### 2.2 CI / CD パイプラインの実装

- Cloud Build を使用した CI
- Cloud Build を使用した CD
- オープンソース ツール（例: Jenkins、Spinnaker、GitLab、Concourse）
- デプロイの監査および追跡（例: CSR、Artifact Registry、Cloud Build、Cloud Audit Logs）

### 2.3 構成とシークレットの管理

- 安全なストレージ方式
- シークレットのローテーションと構成変更

### 2.4 infrastructure as code の管理

- Terraform
- インフラストラクチャ コードのバージョニング
- インフラストラクチャ変更の安全化
- 不変のアーキテクチャ

### 2.5 CI / CD ツールのデプロイ

- 一元管理されたツールと複数のツール（単一テナントとマルチテナント）
- CI / CD ツールのセキュリティ

### 2.6 さまざまな開発環境の管理（例: ステージング環境、本番環境）

- 環境の数とその目的の決定
- GKE を使用した機能ブランチごとの動的な環境作成
- Docker、Cloud Code、Skaffold を使用したローカル開発環境

### 2.7 デプロイ パイプラインの保護

- Artifact Registry を使用した脆弱性分析
- Binary Authorization
- 環境ごとの IAM ポリシー

## セクション 3: サービス モニタリング戦略の実装

### 3.1 アプリケーション ログの管理

- Cloud Logging、Fluentd を使用して Compute Engine、GKE からログを収集する
- Cloud Logging、Fluentd を使用してサードパーティのログおよび構造化ログを収集する
- Cloud Logging API にアプリケーション ログを直接送信する

### 3.2 Cloud Monitoring を使用したアプリケーション指標の管理

- Compute Engine から指標を収集する
- GKE や Kubernetes の指標を収集する
- アドホック指標分析に Metric Explorer を使用する

### 3.3 Cloud Monitoring プラットフォームの管理

- Monitoring のダッシュボードを作成する
- ダッシュボードをフィルタおよび共有する
- Cloud Monitoring を使用してサードパーティのアラートを構成する（例: PagerDuty、Slack）
- Cloud Monitoring を使用して SLI に基づいてアラート ポリシーを定義する
- Terraform を使用してアラート ポリシー定義を自動化する
- Cloud Monitoring を使用して SLO モニタリングとアラートを実装する
- Cloud Monitoring との統合を理解する（例: Grafana、BigQuery）
- SIEM ツールを使用して監査ログとフローログを分析する（例: Splunk、Datadog）
- Cloud Monitoring の指標スコープを設計する

### 3.4 Cloud Logging プラットフォームの管理

- データアクセス ログを有効化する（例: Cloud Audit Logs）
- VPC フローログを有効化する
- Google Cloud Console にログを表示する
- 基本ロギング フィルタと高度なロギング フィルタを使用する
- ログベースの指標を実装する
- ロギング除外とロギング エクスポートを理解する
- ロギング エクスポートのオプションを選択する
- プロジェクト レベルや組織レベルのエクスポートを実装する
- Cloud Storage と BigQuery でエクスポート ログを表示する
- 外部ロギング プラットフォームへログを送信する

### 3.5 ロギングとモニタリングのアクセス制御の実装

- IAM、Cloud Logging を使用して監査ログへのアクセスを制限する ACL を設定する
- IAM、Cloud Logging を使用してエクスポート構成を制限する ACL を設定する
- IAM、Cloud Monitoring を使用してカスタム指標の指標書き込みを許可する ACL を設定する

## セクション 4: サービス パフォーマンスの最適化

### 4.1 サービス パフォーマンスの問題の特定

- ユーザーへの影響を評価および把握する
- Google Cloud のオペレーション スイートを使用してクラウド リソースの使用率を特定する
- Cloud Trace と Cloud Profiler を使用してパフォーマンス特性をプロファイルする
- サービス メッシュ テレメトリーを解釈する
- イメージや OS に関する問題をトラブルシューティングする
- ネットワークの問題をトラブルシューティングする（VPC フローログ、ファイアウォール ログ、レイテンシ、ネットワークの詳細の表示など）

### 4.2 アプリケーション コードのデバッグ

- アプリケーション インストルメンテーション
- Cloud デバッガ
- Cloud Logging
- Cloud Trace
- 分散アプリケーションのデバッグ
- App Engine ローカル開発用サーバー
- Error Reporting
- Cloud Profiler

### 4.3 リソース使用率の最適化

- リソース費用を特定する
- リソース使用率レベルを特定する
- 費用が増大している領域または使用率が低い領域を最適化するための計画を策定する
- プリエンプティブル VM を管理する
- 確約利用割引を利用する（該当する場合）
- TCO について検討する（例: セキュリティ、ロギング、ネットワーキング）
- ネットワークの料金を考慮する

## セクション 5: サービス インシデントの管理

### 5.1 サービス インシデント時の職務の調整と通信チャネルの実装

- 職務を定義する（インシデント コマンダー、コミュニケーション リード、オペレーション リード）
- 影響評価のリクエストを処理する
- 内部および外部で定期的なステータス更新を提供する
- インシデント状態の主要な変化を記録する（軽減されたのはいつか、 問題が解決したのはいつかなど）
- 通信チャネルを確立する（例: メール、IRC、ハングアウト、Slack、スマートフォン）
- 対応チームを選定して委任する
- 極度の疲労や燃え尽きを避ける
- 職務のローテーションや引き継ぎを行う
- ステークホルダー間の関係を管理する

### 5.2 ユーザーに影響を与えるインシデントの症状の調査

- サービス障害の考えられる原因を特定する
- 考えられる原因に対する症状を評価する（実際の動作に基づいた原因の可能性のランク付け）
- 最も可能性が高い原因を突き止めるための調査を実施する
- 問題を軽減するための代替案を特定する

### 5.3 ユーザーに対するインシデントの影響の軽減

- リリースをロールバック
- トラフィックをドレイン / リダイレクトする
- テストをオフにする
- 容量を追加する

### 5.4 デプロイの問題の解決（例: Cloud Build、Jenkins）

- コード変更、バグ修正を行う
- 修正を確認する
- 問題解決を宣言する

### 5.5 事後調査で問題をドキュメント化する

- 根本原因をドキュメント化する
- アクション アイテムを作成して優先順位を付ける
- 事後調査の結果をステークホルダーに伝える
