# サーバーレス ハンズオン ワークショップ

コントソ有限会社では、大規模な料金所の管理サービスビジネスが急速に伸びています。現在、料金所を通過する車両のナンバープレートを自動で解析するという機能の要望が高まっています。大量の車両のナンバープレート写真を高速に処理して保存するソリューションの開発は、本業のオンライン決済ビジネスとは性質が異なるため、苦慮しています。現在はアウトソースによる手動の写真解析を行っており、解析結果は CSV ファイルとしてコントソ社に送られ、そこからオンライン処理システムに都度アップロードしています。コントソはこれらのプロセスをスケーラブルで費用効果の高い方法で、自動化したいと考えており、サーバレス技術が候補に挙がっていますが、詳しいエンジニアがいないため、実装できないでいます。

2019 年 6 月

## 対象者

アプリケーション開発者

## 概要

### ワークショップ

このワークショップでは、チームの一員としてサーバレスアーキテクチャで利用する Azure Functions、Logic Apps、Event Grid、Cosmos DB、Azure ストレージなど Azure　の様々なサービスを作成、構成します。目的はサーバーの管理を無くし、ソリューションを、モジュール単位でスケールやデプロイができるよう細かく分解することであり、使用した分だけ支払う Pay-as-you-go モデルに適用させることです。

ワークショップを通じて、例えばビジネスロジックの一部であるナンバープレートの解析を、Azure Cognitive Service の 1 つである Computer Vision OCR を使って処理する Azure Functions 単体でスケールさせたり、高可用性を兼ね備えた NoSQL ソリューションである Cosmos DB を作成してデータを処理したり、Logic Apps により解析されたナンバープレートのデータをエクスポートしたり、または状況によってメールでのアラートを通知する方法を学びます。システムの監視には Application Insights を活用する方法を学べるほか、継続的なデプロイを GitHub から構成する方法も学びます。

### ハンズオン ラボ

ハンズオンラボでは、Microsoft Azure Functions、Azure Cosmos DB、Event Grid および関連サービスを利用した、エンドツーエンドのソリューション構築にチャレンジします。シナリオは、コンピュート、ストレージ、ワークフローや監視など、様々な Microsoft Azure のサービスを利用します。このハンズオンラボは一人でも実施できますが、実際の状況に近くなるよう、複数人での作業を強く推奨します。お互いの専門性を活用して学びあうことができます。

ハンズオンラボを完了する頃には、回復性が高くスケールし、コスト効果の高いサーバーレスソリューションの設計や構築、監視の実装に自信が持てることでしょう。

## Azure サービスおよび関連製品

- Azure Functions
- Azure Cognitive Services
- Azure Event Grid
- Application Insights
- Azure Cosmos DB
- Logic Apps

## Azure ソリューション

クラウドネイティブアプリケーション

## 参考情報およびマテリアル

- [Azure 上のサーバーレス Web アプリケーション](https://docs.microsoft.com/ja-jp/azure/architecture/reference-architectures/serverless/web-app)
- [Azure Functions を使用したサーバーレスなイベント処理](https://docs.microsoft.com/ja-jp/azure/architecture/reference-architectures/serverless/event-processing)
- [Microsoft Cloud Workshop (MCW)](https://github.com/Microsoft/MCW) 

## ヘルプとサポート

内容についてヘルプが必要な場合やフィードバックがある場合は、Microsoft メンバーまで声をかけてください。

***トラブルシューティング***
- 事前の準備を含め、ラボの手順をすべて行っているか再度確認してください。
- 問題の詳細を含めて Issue を登録してください。
