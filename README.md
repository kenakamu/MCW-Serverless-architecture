# サーバーレス アーキテクチャ

コントソ有限会社では、大規模な料金所の管理サービスビジネスが急速に伸びています。現在、料金所を通過する車両のナンバープレートを自動で解析するという機能の要望が高まっています。大量の車両のナンバープレート写真を高速に処理して保存するソリューションの開発は、本業のオンライン決済ビジネスとは性質が異なるため、苦慮しています。現在はアウトソースによる手動の写真解析を行っており、解析結果は CSV ファイルとしてコントソ社に送られ、そこからオンライン処理システムに都度アップロードしています。コントソはこれらのプロセスをスケーラブルで費用効果の高い方法で、自動化したいと考えており、サーバレス技術が候補に挙がっていますが、詳しいエンジニアがいないため、実装できないでいます。

June 2019

## 対象者

アプリケーション開発者

## 概要

### ワークショップ

このワークショップでは、チームの一員としてサーバレスアーキテクチャで利用する Azure Functions、Logic Apps、Event Grid、Cosmos DB、Azure ストレージなど Azure　の様々なサービスを作成、構成します。目的はサーバーの管理を無くし、ソリューションを、モジュール単位でスケールやデプロイができるよう細かく分解することであり、使用した分だけ支払う Pay-as-you-go モデルに適用させることです。

ワークショップを通じて、例えばビジネスロジックの一部であるナンバープレートの解析を、Azure Cognitive Service の 1 つである Computer Vision OCR を使って処理する Azure Functions 単体でスケールさせたり、高可用性を兼ね備えた NoSQL ソリューションである Cosmos DB を作成してデータを処理したり、Logic Apps により解析されたナンバープレートのデータをエクスポートしたり、または状況によってメールでのアラートを通知する方法を学びます。システムの監視には Application Insights を活用する方法を学べるほか、継続的なデプロイを GitHub から構成する方法も学びます。

### ホワイトボード デザインセッション

In this whiteboard design session, you will work with a group to design a solution for processing vehicle photos as they are uploaded to a storage account, using serverless technologies on Azure. The license plate data needs to be extracted and stored in a highly available NoSQL data store for exporting. The data export process will be orchestrated by a serverless Azure component that coordinates exporting new license plate data to file storage and sending notifications as needed. You will also configure a Continuous Deployment process to automatically publish new changes to Function Apps. Finally, the entire processing pipeline will need to be monitored, with particular attention paid to components scaling to meet processing demand.

At the end of this whiteboard design session, you will have gained insight on how best to take advantage of the new serverless wave by designing a highly scalable and cost-effective solution that requires very little code and virtually no infrastructure, compared to traditional hosted web applications and services.

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

## Help & Support

We welcome feedback and comments from Microsoft SMEs & learning partners who deliver MCWs.  

***Having trouble?***
- First, verify you have followed all written lab instructions (including the Before the Hands-on lab document).
- Next, submit an issue with a detailed description of the problem.
- Do not submit pull requests. Our content authors will make all changes and submit pull requests for approval.   

If you are planning to present a workshop, *review and test the materials early*! We recommend at least two weeks prior.

### Please allow 5 - 10 business days for review and resolution of issues.
