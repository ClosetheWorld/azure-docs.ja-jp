---
title: チュートリアル:Azure Active Directory と EBSCO の統合 | Microsoft Docs
description: Azure Active Directory と EBSCO の間にシングル サインオンを構成する方法について説明します。
services: active-directory
documentationCenter: na
author: jeevansd
manager: mtillman
ms.reviewer: barbkess
ms.assetid: 144f7f65-69e9-4016-a151-fe1104fd6ba8
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: tutorial
ms.date: 04/01/2019
ms.author: jeedes
ms.openlocfilehash: 35cb408473da8c6397c5034ae20ac0a50b0953ea
ms.sourcegitcommit: 124c3112b94c951535e0be20a751150b79289594
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/10/2019
ms.locfileid: "68944717"
---
# <a name="tutorial-azure-active-directory-integration-with-ebsco"></a>チュートリアル:Azure Active Directory と EBSCO の統合

このチュートリアルでは、EBSCO と Azure Active Directory (Azure AD) を統合する方法について説明します。
EBSCO と Azure AD の統合には、次の利点があります。

* EBSCO にアクセスできる Azure AD ユーザーを制御できます。
* ユーザーが自分の Azure AD アカウントで EBSCO に自動的にサインイン (シングル サインオン) するように設定できます。
* 1 つの中央サイト (Azure Portal) でアカウントを管理できます。

SaaS アプリと Azure AD の統合の詳細については、「 [Azure Active Directory のアプリケーション アクセスとシングル サインオンとは](https://docs.microsoft.com/azure/active-directory/active-directory-appssoaccess-whatis)」を参照してください。
Azure サブスクリプションをお持ちでない場合は、開始する前に[無料アカウントを作成](https://azure.microsoft.com/free/)してください。

## <a name="prerequisites"></a>前提条件

EBSCO と Azure AD の統合を構成するには、次のものが必要です。

* Azure AD サブスクリプション。 Azure AD の環境がない場合は、[無料アカウント](https://azure.microsoft.com/free/)を取得できます
* EBSCO でのシングル サインオンが有効なサブスクリプション

## <a name="scenario-description"></a>シナリオの説明

このチュートリアルでは、テスト環境で Azure AD のシングル サインオンを構成してテストします。

* EBSCO では、**SP** Initiated SSO と **IDP** Initiated SSO がサポートされます

* EBSCO では、**Just-In-Time** ユーザー プロビジョニングがサポートされます

## <a name="adding-ebsco-from-the-gallery"></a>ギャラリーからの EBSCO の追加

Azure AD への EBSCO の統合を構成するには、ギャラリーから管理対象 SaaS アプリの一覧に EBSCO を追加する必要があります。

**ギャラリーから EBSCO を追加するには、次の手順を実行します。**

1. **[Azure portal](https://portal.azure.com)** の左側のナビゲーション パネルで、 **[Azure Active Directory]** アイコンをクリックします。

    ![Azure Active Directory のボタン](common/select-azuread.png)

2. **[エンタープライズ アプリケーション]** に移動し、 **[すべてのアプリケーション]** オプションを選択します。

    ![[エンタープライズ アプリケーション] ブレード](common/enterprise-applications.png)

3. 新しいアプリケーションを追加するには、ダイアログの上部にある **[新しいアプリケーション]** ボタンをクリックします。

    ![[新しいアプリケーション] ボタン](common/add-new-app.png)

4. 検索ボックスに「**EBSCO**」と入力し、結果パネルで **[EBSCO]** を選び、 **[追加]** をクリックして、アプリケーションを追加します。

     ![結果一覧の EBSCO](common/search-new-app.png)

## <a name="configure-and-test-azure-ad-single-sign-on"></a>Azure AD シングル サインオンの構成とテスト

このセクションでは、**Britta Simon** というテスト ユーザーに基づいて、EBSCO で Azure AD のシングル サインオンを構成し、テストします。
シングル サインオンを機能させるには、Azure AD ユーザーと EBSCO 内の関連ユーザー間にリンク関係が確立されている必要があります。

EBSCO で Azure AD のシングル サインオンを構成してテストするには、次の構成要素を完了する必要があります。

1. **[Azure AD シングル サインオンの構成](#configure-azure-ad-single-sign-on)** - ユーザーがこの機能を使用できるようにします。
2. **[EBSCO のシングル サインオンの構成](#configure-ebsco-single-sign-on)** - アプリケーション側でシングル サインオン設定を構成します。
3. **[Azure AD のテスト ユーザーの作成](#create-an-azure-ad-test-user)** - Britta Simon で Azure AD のシングル サインオンをテストします。
4. **[Azure AD テスト ユーザーの割り当て](#assign-the-azure-ad-test-user)** - Britta Simon が Azure AD シングル サインオンを使用できるようにします。
5. **[EBSCO のテスト ユーザーの作成](#create-ebsco-test-user)** - EBSCO で Britta Simon に対応するユーザーを作成し、Azure AD の Britta Simon にリンクさせます。
6. **[シングル サインオンのテスト](#test-single-sign-on)** - 構成が機能するかどうかを確認します。

### <a name="configure-azure-ad-single-sign-on"></a>Azure AD シングル サインオンの構成

このセクションでは、Azure portal 上で Azure AD のシングル サインオンを有効にします。

EBSCO で Azure AD シングル サインオンを構成するには、次の手順に従います。

1. [Azure portal](https://portal.azure.com/) の **EBSCO** アプリケーション統合ページで、 **[シングル サインオン]** を選択します。

    ![シングル サインオン構成のリンク](common/select-sso.png)

2. **[シングル サインオン方式の選択]** ダイアログで、 **[SAML/WS-Fed]** モードを選択して、シングル サインオンを有効にします。

    ![シングル サインオン選択モード](common/select-saml-option.png)

3. **[SAML でシングル サインオンをセットアップします]** ページで、 **[編集]** アイコンをクリックして **[基本的な SAML 構成]** ダイアログを開きます。

    ![基本的な SAML 構成を編集する](common/edit-urls.png)

4. **[基本的な SAML 構成]** セクションで、アプリケーションを **IDP** 開始モードで構成する場合は、次の手順を実行します。

    ![EBSCO のドメインと URL のシングル サインオン情報](common/idp-identifier.png)

    **[識別子]** テキスト ボックスに、`pingsso.ebscohost.com` という URL を入力します。

5. アプリケーションを **SP** 開始モードで構成する場合は、 **[追加の URL を設定します]** をクリックして次の手順を実行します。

    ![image](common/both-preintegrated-signon.png)

    **[サインオン URL]** ボックスに、`https://search.ebscohost.com/login.aspx?authtype=sso&custid=<unique EBSCO customer ID>&profile=<profile ID>` という形式で URL を入力します。

    > [!NOTE]
    > サインオン URL は実際の値ではありません。 実際のサインオン URL でこの値を更新してください。 これらの値を取得するには、[EBSCO クライアント サポート チーム](mailto:sso@ebsco.com)に問い合わせてください。 Azure portal の **[基本的な SAML 構成]** セクションに示されているパターンを参照することもできます。

    o   **一意の要素:**  

    o   **[Custid]** = 一意の EBSCO カスタマー ID を入力 

    o   **[プロファイル]** = クライアントはリンクを調整して、ユーザーを (EBSCO から購入したものに基づいて) 特定のプロファイルに転送できます。 特定のプロファイル ID を入力できます。 メインの ID は eds (EBSCO Discovery Service) と ehost (EBSOCOhost データベース) です。 同じことに関する手順が[こちら](https://help.ebsco.com/interfaces/EBSCOhost/EBSCOhost_FAQs/How_do_I_set_up_direct_links_to_EBSCOhost_profiles_and_or_databases#profile)にあります。

6. EBSCO アプリケーションは、特定の形式の SAML アサーションを使用するため、カスタム属性のマッピングを SAML トークンの属性の構成に追加する必要があります。 次のスクリーンショットには、既定の属性一覧が示されています。 **[編集]** アイコンをクリックして、 **[ユーザー属性]** ダイアログを開きます。

    ![image](common/edit-attribute.png)

     > [!Note]
    > **name** 属性は必須であり、EBSCO アプリケーションの**名前識別子の値**とマッピングされます。 これは既定で追加されるため、手動で追加する必要はありません。

7. その他に、EBSCO アプリケーションでは、いくつかの属性が SAML 応答で返されることが想定されています。 **[ユーザー属性]** ダイアログの **[ユーザー要求]** セクションで、以下の手順を実行して、以下の表のように SAML トークン属性を追加します。 

    | Name | ソース属性|
    | ---------------| --------------- |    
    | FirstName   | User.givenname |
    | LastName   | User.surname |
    | Email   | User.mail |

    a. **[新しい要求の追加]** をクリックして **[ユーザー要求の管理]** ダイアログを開きます。

    ![image](common/new-save-attribute.png)

    ![image](common/new-attribute-details.png)

    b. **[名前]** ボックスに、その行に対して表示される属性名を入力します。

    c. **[名前空間]** は空白のままにします。

    d. [ソース] として **[属性]** を選択します。

    e. **[ソース属性]** の一覧から、その行に表示される属性値を入力します。

    f. **[Save]** をクリックします。

8. **[SAML でシングル サインオンをセットアップします]** ページの **[SAML 署名証明書]** セクションで、 **[ダウンロード]** をクリックして、要件のとおりに指定したオプションから**フェデレーション メタデータ XML** をダウンロードして、お使いのコンピューターに保存します。

    ![証明書のダウンロードのリンク](common/metadataxml.png)

9. **[EBSCO のセットアップ]** セクションで、要件に従って適切な URL をコピーします。

    ![構成 URL のコピー](common/copy-configuration-urls.png)

    a. ログイン URL

    b. Azure AD 識別子

    c. ログアウト URL

### <a name="configure-ebsco-single-sign-on"></a>EBSCO のシングル サインオンの構成

**EBSCO** 側でシングル サインオンを構成するには、ダウンロードした**メタデータ XML** と Azure portal からコピーした適切な URL を [EBSCO サポート チーム](mailto:sso@ebsco.com)に送信する必要があります。 サポート チームはこれを設定して、SAML SSO 接続が両方の側で正しく設定されるようにします。

### <a name="create-an-azure-ad-test-user"></a>Azure AD のテスト ユーザーの作成 

このセクションの目的は、Azure Portal で Britta Simon というテスト ユーザーを作成することです。

1. Azure portal の左側のウィンドウで、 **[Azure Active Directory]** 、 **[ユーザー]** 、 **[すべてのユーザー]** の順に選択します。

    ![[ユーザーとグループ] と [すべてのユーザー] リンク](common/users.png)

2. 画面の上部にある **[新しいユーザー]** を選択します。

    ![[新しいユーザー] ボタン](common/new-user.png)

3. [ユーザーのプロパティ] で、次の手順を実行します。

    ![[ユーザー] ダイアログ ボックス](common/user-properties.png)

    a. **[名前]** フィールドに「**BrittaSimon**」と入力します。
  
    b. **[ユーザー名]** フィールドに「brittasimon@yourcompanydomain.extension」と入力します。 たとえば、BrittaSimon@contoso.com のように指定します。

    c. **[パスワードを表示]** チェック ボックスをオンにし、[パスワード] ボックスに表示された値を書き留めます。

    d. **Create** をクリックしてください。

### <a name="assign-the-azure-ad-test-user"></a>Azure AD テスト ユーザーの割り当て

このセクションでは、Britta Simon に EBSCO へのアクセスを許可することで、このユーザーが Azure シングル サインオンを使用できるようにします。

1. Azure portal 上で **[エンタープライズ アプリケーション]** を選択し、 **[すべてのアプリケーション]** 、 **[EBSCO]** の順に選択します。

    ![[エンタープライズ アプリケーション] ブレード](common/enterprise-applications.png)

2. アプリケーションの一覧で **[EBSCO]** を選択します。

    ![アプリケーションの一覧の [EBSCO] リンク](common/all-applications.png)

3. 左側のメニューで **[ユーザーとグループ]** を選びます。

    ![[ユーザーとグループ] リンク](common/users-groups-blade.png)

4. **[ユーザーの追加]** をクリックし、 **[割り当ての追加]** ダイアログで **[ユーザーとグループ]** を選択します。

    ![[割り当ての追加] ウィンドウ](common/add-assign-user.png)

5. **[ユーザーとグループ]** ダイアログの [ユーザー] の一覧で **[Britta Simon]** を選択し、画面の下部にある **[選択]** ボタンをクリックします。

6. SAML アサーション内に任意のロール値が必要な場合、 **[ロールの選択]** ダイアログでユーザーに適したロールを一覧から選択し、画面の下部にある **[選択]** をクリッします。

7. **[割り当ての追加]** ダイアログで、 **[割り当て]** ボタンをクリックします。

### <a name="create-ebsco-test-user"></a>EBSCO のテスト ユーザーの作成

EBSCO の場合、ユーザー プロビジョニングは自動的に行われます。

**ユーザー アカウントをプロビジョニングするには、次の手順に従います。**

Azure AD によって必要なデータが EBSCO アプリケーションに渡されます。 EBSCO のユーザー プロビジョニングは自動であるか、1 回限りのフォームが要求されます。 これは、個人設定が保存された、多数の既存の EBSCOhost アカウントをクライアントが持っているかどうかによって異なります。 実装中、[EBSCO サポート チーム](mailto:sso@ebsco.com)についても同じことが考えられます。 どちらの場合でも、テスト前にクライアントが EBSCOhost アカウントを作成する必要はありません。

   >[!Note]
   >EBSCOhost ユーザーのプロビジョニング/パーソナル化を自動化できます。 Just-In-Time ユーザー プロビジョニングについて、[EBSCO サポート チーム](mailto:sso@ebsco.com)にお問い合わせください。 

### <a name="test-single-sign-on"></a>シングル サインオンのテスト 

このセクションでは、アクセス パネルを使用して Azure AD のシングル サインオン構成をテストします。

1. アクセス パネルで EBSCO のタイルをクリックすると、EBSCO アプリケーションに自動的にサインオンします。
アクセス パネルの詳細については、[アクセス パネルの概要](../user-help/active-directory-saas-access-panel-introduction.md)に関する記事を参照してください。

2. アプリケーションにログインしたら、右上隅の **[サインイン]** ボタンをクリックします。

    ![アプリケーションの一覧の EBSCO サインイン](./media/ebsco-tutorial/tutorial_ebsco_signin.png)
 
3. 組織ログインまたは SAML ログインを、 **[Link your existing MyEBSCOhost account to your institution account now]\(今すぐ既存の MyEBSCOhost アカウントを組織アカウントにリンクする\)** または **[Create a new MyEBSCOhost account and link it to your institution account]\(新しい MyEBSCOhost アカウントを作成して組織アカウントにリンクする\)** に関連付けることを求める 1 回限りのプロンプトが表示されます。 アカウントは、EBSCOhost アプリケーションのパーソナル化に使用されます。 **[新しいアカウントの作成]** オプションを選択すると、次のスクリーンショットのように、SAML 応答の値が事前入力されたパーソナル化用のフォームが表示されます。 **[続行]** をクリックしてこの選択を保存します。
    
     ![アプリケーションの一覧の EBSCO ユーザー](./media/ebsco-tutorial/tutorial_ebsco_user.png)

1. 以上の設定を完了したら、Cookie/キャッシュをクリアして再びログインします。 これで再び手動でサインインする必要はなくなり、パーソナル化の設定は保持されます。

## <a name="additional-sesources"></a>その他のリソース

- [SaaS アプリと Azure Active Directory を統合する方法に関するチュートリアルの一覧](https://docs.microsoft.com/azure/active-directory/active-directory-saas-tutorial-list)

- [Azure Active Directory のアプリケーション アクセスとシングル サインオンとは](https://docs.microsoft.com/azure/active-directory/active-directory-appssoaccess-whatis)

- [Azure Active Directory の条件付きアクセスとは](https://docs.microsoft.com/azure/active-directory/conditional-access/overview)

