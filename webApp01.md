# 演習 1 : AppService (Web App) へのアプリケーションのデプロイ

GitHub から入手した ASP.NET Core アプリケーションを Azure App Service にデプロイします。

このアプリケーションは .NET7 ベースの MVC フレームワークを使用しており、データベースとして Visual Studio のローカル DB を使用しています。

そのため、このアプリケーションを Azure で正しく動作させるには AppService のほかに Azure SQL Database をデプロイしローカルのデータベースの内容を移行する必要があります。

よって、この演習の手順は以下の 4 つとなります。

1. Azure SQL Database インスタンスの作成
2. Visual Studio のローカル DB の内容を Azure SQL Database に移行
3. AppService インスタンスの作成
4. AppService にアプリケーションをデプロイ

## 1. Azure SQL Database インスタンスの作成

Azure Portal から Azure SQL Database インスタンスを作成します。

具体的な手順は以下の通りです。

1. [Azure Portal](http://portal.azure.com) にログインします。

2. ポータル画面上部の \[**+**\] リソースの作成 アイコンか、表示されていない場合は画面左上のハンバーガーメニューをクリックし、\[**リソースの作成**\] をクリックします

    ![Create Resource](images/23aug_create_AzureResource.png)

3. 多くの場合、遷移した画面に \[**SQL Database**\] がリストされているはずですが、

