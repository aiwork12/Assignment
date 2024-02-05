# 第5回講座課題

## 組み込みサーバーだけでサンプルアプリケーションのデプロイ

- **デプロイした際のログ**  
![サンプルアプリケーションを起動した際のログ](lecture05_images/組み込みサーバーでのデプロイ_実行画面.png)

- **表示されたＷＥＢページ**  
![WEBページ](lecture05_images/組み込みサーバーでのデプロイ_WEBページ.png)

- **RDSへ保存されていることを確認した際のスクショ**  
![RDS](lecture05_images/組み込みサーバーでのデプロイ_RDS.png)

## サンプルアプリケーションを分けてデプロイ

- **Nginxのアクセスログ（画像保存時）**  
![Nginxのアクセスログ](lecture05_images/サーバーアプリケーションを分けてデプロイ_Nginx.png)

- **Unicorn起動時のログ**  
![Unicornのアクセスログ](lecture05_images/サーバーアプリケーションを分けてデプロイ_Unicorn.png)

- **画像保存時のＷＥＢページ**  
![WEBページ](lecture05_images/サーバーアプリケーションを分けてデプロイ_WEBページ.png)

- **S3の追加**  
![S3のオブジェクト一覧](lecture05_images/S3の追加.png)

## ELBの追加

- **ALBの設定**  
![ALBの設定画面](lecture05_images/ALBの設定.png)

## 構成図

- **今回作成した環境の構成図**  
![構成図](lecture05_images/構成図.png)

### 設定ファイル群（証跡）

- **nginx**  
![設定ファイル](lecture05_images/nginx.conf.png)

- **unicorn**  
![設定ファイル](lecture05_images/unicorn.rb.png)

- **Gemfile**  
![設定ファイル](lecture05_images/Gemfile.png)

- **storage**  
![設定ファイル](lecture05_images/storage.yml.png)

- **development**  
![設定ファイル](lecture05_images/development.rb.png)

### 所感

- エラーが何度も発生し、その度にChatGPTに確認しながら作業を行っていました。
- どうしても分からなかった時にメンターの方へ相談し方向性を教えていただきました。

- 今後は時間を決めて、詰まったときは積極的に相談したいと思います。
- 今回は課題提出までに17日間（４０時間程度）掛かってしまいました。
- 次回以降はスピードを上げていきたいです。