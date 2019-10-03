![Microsoft Cloud Workshops](https://github.com/Microsoft/MCW-Template-Cloud-Workshop/raw/master/Media/ms-cloud-workshop.png 'Microsoft Cloud Workshops')

<div class="MCWHeader1">
サーバーレスアーキテクチャ
</div>

<div class="MCWHeader2">
ハンズオンラボ前のセットアップガイド
</div>

<div class="MCWHeader3">
June 2019
</div>

Information in this document, including URL and other Internet Web site references, is subject to change without notice. Unless otherwise noted, the example companies, organizations, products, domain names, e-mail addresses, logos, people, places, and events depicted herein are fictitious, and no association with any real company, organization, product, domain name, e-mail address, logo, person, place or event is intended or should be inferred. Complying with all applicable copyright laws is the responsibility of the user. Without limiting the rights under copyright, no part of this document may be reproduced, stored in or introduced into a retrieval system, or transmitted in any form or by any means (electronic, mechanical, photocopying, recording, or otherwise), or for any purpose, without the express written permission of Microsoft Corporation.

Microsoft may have patents, patent applications, trademarks, copyrights, or other intellectual property rights covering subject matter in this document. Except as expressly provided in any written license agreement from Microsoft, the furnishing of this document does not give you any license to these patents, trademarks, copyrights, or other intellectual property.

The names of manufacturers, products, or URLs are provided for informational purposes only and Microsoft makes no representations and warranties, either expressed, implied, or statutory, regarding these manufacturers or the use of the products with any Microsoft technologies. The inclusion of a manufacturer or product does not imply endorsement of Microsoft of the manufacturer or product. Links may be provided to third party sites. Such sites are not under the control of Microsoft and Microsoft is not responsible for the contents of any linked site or any link contained in a linked site, or any changes or updates to such sites. Microsoft is not responsible for webcasting or any other form of transmission received from any linked site. Microsoft is providing these links to you only as a convenience, and the inclusion of any link does not imply endorsement of Microsoft of the site or the products contained therein.

Â© 2019 Microsoft Corporation. All rights reserved.

**コンテンツ**

- [ハンズオンラボ事前のセットアップガイド](#ハンズオンラボ事前のセットアップガイド)
  - [前提条件](#前提条件)
  - [ハンズオンラボの前に](#ハンズオンラボの前に)
    - [タスク 1: Azure リソースグループの作成](#タスク-1-Azure-リソースグループの作成)
    - [タスク 2: 開発環境の構築](#タスク-2-開発環境の構築)
    - [タスク 3: IE のセキュリティ強化の無効](#タスク-3-ie-のセキュリティ強化の無効)
    - [タスク 4: Google Chrome のインストール](#タスク-4-google-chrome-のインストール)
    - [タスク 5: Azure への接続確認](#タスク-5-azure-への接続確認)
    - [タスク 6: TollBooth starter ソリューションのダウンロード](#タスク-6-TollBooth-starter-ソリューションのダウンロード)

# ハンズオンラボ事前のセットアップガイド

## 前提条件

- Microsoft Azure サブスクリプション
- 以下が構成されたローカルまたは仮想 PC (**ラボの前日までに準備する**):
  - [Visual Studio Community 2019 以降](https://www.visualstudio.com/vs/)
  - [Visual Studio 2019 Azure ワークロード](https://docs.microsoft.com/azure/azure-functions/functions-develop-vs#prerequisites)
  - [.NET Framework ランタイム 4.7 以降](https://www.microsoft.com/net/download/windows)
- Office 365 アカウント: [体験版あり](https://portal.office.com/Signup/MainSignup15.aspx?Dap=False&QuoteId=79a957e9-ad59-4d82-b787-a46955934171&ali=1)
- [GitHub](https://github.com) アカウント

## ハンズオンラボの前に

**所要時間**: 10 分

このセクションではサンプルのダウンロードや Azure リソースグループの作成を行います。

### タスク 1: Azure リソースグループの作成

1.  [Azure ポータル](https://portal.azure.com) にログイン。

1.  左の **リソース グループ** を選択して、**追加**をクリック。

    ![](images/Setup/image9.png 'Azure ポータル')

1.  リソースグループに **ServerlessArchitecture** と入力し、**リージョン**に**東日本**を設定して、**確認および作成**から**作成**をクリック。

    ![](images/Setup/image10.png 'リソースグループの作成')

### タスク 2: 開発環境の構築

Visual Studio Community 2019 の Azure 開発ワークロードがインストールされた PC がない場合、以下手順で仮想マシンを用意します。

このタスクでは `Visual Studio Community 2019 on Windows Server 2019 (x64)` または Windows 10 の仮想マシンを作成します。MSDN サブスクリプションの場合、Visual Studio VM を作成できるバージョンか確認してください。

    ![](images/Setup/image3.png 'Azure ????')

1. **+リソースの作成**をクリック。

1. **Visual Studio 2019** で検索。

1. **Visual Studio 2019 Community (latest release) on Windows Server 2019 (x64)** を選択。

1. **作成**をクリック

1. 作成したリソースグループを選択。

1. 名前を **MainVM** を指定。

1. 可用性オプションは、**インフラストラクチャー冗長性は必要ありません**を選択。
    
1. イメージで **Visual Studio 2019 Community (latest release) on Windows Server 2019 (x64)** を選択。

1. サイズで任意のサイズを選択。

    > **メモ**: DS2 か D2 以上を推奨。

1. 任意のユーザー名とパスワードを入力

1. パブリック受信ポートで **選択したポートを許可する**を選択。

1. **RDP (3389)** を選択。

1. **確認および作成**をクリック。

1. **作成**をクリック。

### タスク 3: IE のセキュリティ強化の無効

> **メモ**: IE のセキュリティ強化は既定で無効の場合もあります。

1.  作成した VM にログイン。

1.  サーバーマネージャーが起動するまで待機。

1.  **Local Server** を選択。

    ![](images/Setup/image5.png 'Server Manager menu')

1.  **IE Enhanced Security Configuration** が **On** の場合、リンクをクリック。**Off** の場合は何もしない。

    ![](images/Setup/image6.png 'IE Enhanced Security Configuration')

    - Administrator 権限で **Off** に変更して **OK** をクリック。

    ![](images/Setup/image7.png 'Internet Explorer Enhanced Security Configuration dialog box')

### タスク 4: Google Chrome のインストール

> **メモ**: ラボで Google Chrome が一部必要になる場合がある。

1.  Internet Explorer を起動して [Google Chrome](https://www.google.com/chrome/) をダウンロード。

1.  ウィザードに従ってインストール。

### タスク 5: Azure への接続確認

1.  VM から Visual Studio を起動して **Sign in** をクリック。自身のマイクロソフトアカウントでサインイン。

1.  **Continue without code** をクリックして Visual Studio を起動。**Server Explorer** より Azure サブスクリプションに接続。

    ![](images/Setup/image8.png 'Server Explorer')

### タスク 6: TollBooth starter ソリューションのダウンロード

1. ブラウザで [MCW サーバーレスアーキテクチャ](https://github.com/Microsoft/MCW-Serverless-architecture) を開き、 **Clone or download** から **Download ZIP** をクリック

   ![](images/Setup/github-download-repo.png)

1. ダウンロード zip を **C:\\ServerlessMCW\\** に解凍。

1. C:\ServerlessMCW\MCW-Serverless-architecture-master\Hands-on lab\starter を開く。

1. **TollBooth** フォルダの **TollBooth.sln** を Visual Studio 2019 で開いて、 2 つのプロジェクトがあることを確認。

    - TollBooth
    - UploadImages

    > **メモ**: UploadImages は車両の写真を大量にアップロードするツール。

1. フォルダエクスプローラーで C:\ServerlessMCW\MCW-Serverless-architecture-master\Hands-on lab\starter にある **license plates** フォルダを確認。ここにはOCR で解析する車両の画像が含まれている。また **copyfrom** フォルダの画像を利用して UploadImages プログラムが大量の写真をアップロードする。
