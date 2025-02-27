---
title: Microsoft Azure Data Box Disk のクイック スタート | Microsoft Docs
description: このクイック スタートを使用して、Azure portal からすばやく Azure Data Box Disk をデプロイしましょう。
services: databox
author: alkohli
ms.service: databox
ms.subservice: disk
ms.topic: quickstart
ms.date: 08/28/2019
ms.author: alkohli
Customer intent: As an IT admin, I need to quickly deploy Data Box Disk so as to import data into Azure.
ms.openlocfilehash: cbc55433517174c8080b941ca8526e5a4fd3427d
ms.sourcegitcommit: 07700392dd52071f31f0571ec847925e467d6795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/28/2019
ms.locfileid: "70126013"
---
::: zone target="docs"

# <a name="quickstart-deploy-azure-data-box-disk-using-the-azure-portal"></a>クイック スタート:Azure portal を使用して Azure Data Box Disk をデプロイする

::: zone-end

::: zone target="chromeless"

## <a name="get-started-with-azure-data-box-disk"></a>Azure Data Box Disk を使ってみる 

::: zone-end

::: zone target="docs"

このクイック スタートでは、Azure portal を使用して Azure Data Box Disk をデプロイする方法について説明します。 ここでは、すばやく注文を作成する手順や、ディスクを受け取る手順、開梱の手順、接続手順のほか、Azure にアップロードできるようデータをディスクにコピーする手順などについて取り上げています。

デプロイと追跡に関する詳しい手順については、「[チュートリアル: Azure Data Box Disk を注文する](data-box-disk-deploy-ordered.md)」を参照してください。 

Azure サブスクリプションをお持ちでない場合は、[無料アカウント](https://azure.microsoft.com/free/?WT.mc_id=A261C142F)を作成してください。

::: zone-end

::: zone target="chromeless"

このガイドでは、Azure portal で Azure Data Box Disk をデプロイする方法について説明します。 この手順には、前提条件の確認、ディスクのロック解除、Azure へのアップロードのためのデータへの接続とディスクへのコピーが含まれます。

::: zone-end

::: zone target="docs"

## <a name="prerequisites"></a>前提条件

作業を開始する前に、次のことを行います。

- ご利用のサブスクリプションで Azure Data Box サービスが有効になっていることを確認してください。 ご利用のサブスクリプションでこのサービスを有効にするには、[サービスにサインアップ](https://aka.ms/azuredataboxfromdiskdocs)してください。

## <a name="sign-in-to-azure"></a>Azure へのサインイン

Azure Portal ([https://aka.ms/azuredataboxfromdiskdocs](https://aka.ms/azuredataboxfromdiskdocs)) にサインインします。

::: zone-end

::: zone target="chromeless"

### <a name="prerequisites"></a>前提条件

- Data Box Disk を注文済みであること。「[チュートリアル:Azure Data Box Disk を注文する](data-box-disk-deploy-ordered.md)」を参照してください。
- ディスクの受け取りが済んでいて、ポータルでジョブの状態が **[配信済み]** に更新されていること。
- 受け取ったディスクの数と、ディスクごとに 1 つの接続ケーブルがあることを確認しました。
- データのコピー元として使用できるクライアント コンピューターがあること。 クライアント コンピューターの要件は以下のとおりです。

    - [サポート対象のオペレーティング システム](data-box-disk-system-requirements.md#supported-operating-systems-for-clients)が実行されていること。
    - Windows クライアントである場合は、[その他の必須ソフトウェア](data-box-disk-system-requirements.md#other-required-software-for-windows-clients)がインストールされていること。

::: zone-end

::: zone target="docs"

## <a name="order"></a>順序

この手順には約 5 分かかります。

1. Azure portal で新しい Azure Data Box リソースを作成します。 
2. このサービスが有効になったサブスクリプションを選択し、転送の種類として **[インポート]** を選択します。 **[ソースの国]** にデータが存在する場所を、 **[宛先 Azure リージョン]** にデータの転送先を指定します。
3. **[Data Box Disk]** を選択します。 ソリューションの最大容量は 35 TB ですが、それを超えるサイズのデータについては複数のディスク注文を作成することができます。  
4. 注文の詳細と発送情報を入力します。 ご利用のリージョンでこのサービスが提供されている場合、通知メール アドレスを指定し、概要を確認したうえで注文を作成します。

注文が作成されると、ディスクの発送準備が行われます。

## <a name="unpack"></a>開梱

この手順には約 5 分かかります。

Data Box Disk は、UPS Express Box で郵送されます。 開梱して同梱物をチェックしてください。

- エアークッションで包まれた USB ディスク (1 台から 5 台)。
- 接続ケーブル (ディスクごと)。
- 返送用の配送ラベル。

## <a name="connect-and-unlock"></a>接続とロック解除

この手順には約 5 分かかります。

1. 同梱されているケーブルを使用して、サポート対象バージョンの Windows/Linux が実行されているコンピューターにディスクを接続します。 サポート対象 OS バージョンについて詳しくは、「[Azure Data Box Disk system requirements (Azure Data Box Disk のシステム要件)](data-box-disk-system-requirements.md)」を参照してください。 
2. 次の手順に従って、ディスクのロックを解除します。

    1. Azure portal で **[全般] > [デバイスの詳細]** に移動し、パスキーを取得します。
    2. ディスクへのデータのコピーに使用するコンピューターに、オペレーティング システム固有の Data Box Disk のロック解除ツールをダウンロードして展開します。 
    3. Data Box Disk ロック解除ツールを実行して、このパスキーを指定します。 ディスクの再挿入に対応するには、ロック解除ツールをもう一度実行し、パスキーを指定します。 **BitLocker ダイアログまたは BitLocker キーを使用したディスクのロック解除は行わないでください。** ディスクのロック解除方法の詳細については、[Windows クライアントでのディスクのロック解除](data-box-disk-deploy-set-up.md#unlock-disks-on-windows-client)または [Linux クライアントでのディスクのロック解除](data-box-disk-deploy-set-up.md#unlock-disks-on-linux-client)に関するページを参照してください。
    4. ディスクに割り当てられたドライブ文字が、ツールによって表示されます。 ディスクのドライブ文字をメモしておいてください。 以降の手順で使用します。

## <a name="copy-data-and-validate"></a>データをコピーし、検証する

この工程にかかる時間は、実際のデータのサイズによって異なります。

1. ドライブには、*PageBlob*、*BlockBlob*、*AzureFile*、*ManagedDisk*、*DataBoxDiskImport* の各フォルダーが格納されています。 ブロック BLOB としてインポートするデータは、*BlockBlob* フォルダーにドラッグ アンド ドロップでコピーします。 同様に、VHD/VHDX などのデータは、*PageBlob* フォルダーに、適切なデータは *AzureFile* にドラッグ アンド ドロップします。 マネージド ディスクとしてアップロードする VHD を *ManagedDisk* 以下のフォルダーにコピーします。

    Azure Storage アカウントには、*BlockBlob* フォルダー下および *PageBlob* フォルダー下のサブフォルダーごとにコンテナーが 1 つ作成されます。 ファイル共有が *AzureFile* 以下のサブフォルダーに作成されます。

    *BlockBlob* フォルダー下のファイルと *PageBlob* フォルダー下のファイルはすべて、Azure Storage アカウントの既定のコンテナー `$root` にコピーされます。 ファイルを *AzureFile* 内のフォルダーにコピーします。 *AzureFile* フォルダーに直接コピーされたファイルはすべて失敗し、ブロック BLOB としてアップロードされます。

    > [!NOTE]
    > - すべてのコンテナー、BLOB、およびファイルは、[Azure 名前付け規則](data-box-disk-limits.md#azure-block-blob-page-blob-and-file-naming-conventions)に準拠する必要があります。 これらの規則に従っていない場合、Azure へのデータのアップロードに失敗します。
    > - ファイルのサイズが、ブロック BLOB の場合は最大 4.75 TiB、ページ BLOB の場合は最大 8 TiB、Azure Files の場合は最大 1 TiB を超えないようにします。

2. **(省略可能ですが推奨されます)** コピーが完了したら、少なくとも *DataBoxDiskImport* フォルダーにある `DataBoxDiskValidation.cmd` を実行し、オプション 1 を選択してファイルを検証することを強くお勧めします。 時間が許せば、オプション 2 を使用して検証用のチェックサムも生成することをお勧めします (データ サイズによっては時間がかかる場合があります)。 このような手順で、データを Azure にアップロードするときに失敗する可能性が最小限になります。
3. ドライブを安全に取り外す

## <a name="ship-to-azure"></a>Azure への発送

この手順の所要時間は 5 分から 7 分程度です。

1. すべてのディスクを元のパッケージに梱包します。 同梱されている配送先住所ラベルを使用してください。 ラベルを破損または紛失した場合は、ポータルからダウンロードしてください。 **[概要]** に移動し、コマンド バーの **[出荷ラベルをダウンロード]** をクリックします。
2. パッケージに封をし、集荷場所に持ち込みます。  

Data Box Disk サービスからメール通知が送信され、Azure portal で注文の状態が更新されます。

## <a name="verify-your-data"></a>データの検証

この工程にかかる時間は、実際のデータのサイズによって異なります。

1. Data Box ディスクが Azure データセンターのネットワークに接続されると、Azure へのデータのアップロードが自動的に開始されます。
2. Azure Data Box サービスは、データのコピーが完了したことを Azure portal 経由でお客様に通知します。
    
    1. 失敗していないかエラー ログで確認し、適切な措置を講じます。
    2. コピー元からデータを削除する前に、データがストレージ アカウントに存在することを確認します。

## <a name="clean-up-resources"></a>リソースのクリーンアップ

この手順を完了するには、2 分から 3 分かかります。

クリーンアップするには、Data Box の注文をキャンセルしたうえで削除してください。

- Data Box の注文は、注文が処理される前であれば、Azure portal からキャンセルできます。 注文が処理された後は、キャンセルできません。 注文は、完了ステージに到達するまで続行されます。

    注文をキャンセルするには、 **[概要]** に移動し、コマンド バーの **[キャンセル]** をクリックします。  

- Azure portal で **完了済み**または**キャンセル済み**の状態になった注文は削除することができます。

    注文を削除するには、 **[概要]** に移動し、コマンド バーの **[削除]** をクリックします。

## <a name="next-steps"></a>次の手順

このクイック スタートでは、Azure へのデータのインポートを支援する Azure Data Box Disk をデプロイしました。 Azure Data Box Disk の管理について詳しくは、次のチュートリアルをご覧ください。

> [!div class="nextstepaction"]
> [Azure portal を使用して Data Box Disk を管理する](data-box-portal-ui-admin.md)

::: zone-end
