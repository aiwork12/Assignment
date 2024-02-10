# 第6回講座課題

## CloudTrailにて最後に利用した日の記録をピックアップ

- **イベント履歴画面**  
![イベント履歴](lecture06_images/CloudTrail_イベント履歴.png)

- **イベントの中に含まれる情報**  
    - イベント名　　：ConsoleLogin
    - ユーザー名　　：inaba
    - イベント時間　：2月 08, 2024, 20:03:19 (UTC+09:00)
    - イベントソース：signin.amazonaws.com
    ![ConsoleLogin](lecture06_images/CloudTrail_ConsoleLogin.png)

## CloudWatch ALBアラームの設定


- **Amazon SNSの設定詳細**  
    - 指定のGmail宛てにメール通知が来るように設定  
    ![SNS設定画面](lecture06_images/SNS.png)

- **CloudWatch ALBアラームの設定詳細**  
    - メトリクス ：raisetech-alb6（ALB）/UnhealtyHostCount  
    - TargetGroup：raisetech-tg（ALBで設定されたTargetGroup）  
    - しきい値　 ：300秒あたり1以上  
    ![ALBアラーム詳細](lecture06_images/CloudWatch_Healthy.png)  
    - アクション ：OK/アラーム状態時に「raisetech-sns」にメッセージ送信  
    ![アクション内容](lecture06_images/CloudWatch_アクション.png)

- **Nginx/Unicorn起動時の挙動**  
    - ALB配下のEC2のヘルスステータスが「Healthy」に遷移する  
    ![TargetGroup詳細](lecture06_images/TargetGroup_Healthy.png)
    - ALBアラームの状態が「OK」に遷移する  
    ![ALBアラーム詳細](lecture06_images/CloudWatch_Healthy.png)
    - メールに通知  
    ![メール内容](lecture06_images/メール通知_OK.png)

- **Nginx/Unicorn停止時の挙動**  
    - ALB配下のEC2のヘルスステータスが「Unhealthy」に遷移する  
    ![TargetGroup詳細](lecture06_images/TargetGroup_Unhealthy.png)
    - ALBアラームの状態が「アラーム状態」に遷移する  
    ![ALBアラーム詳細](lecture06_images/CloudWatch_Unhealthy.png)
    - メールに通知  
    ![メール内容](lecture06_images/メール通知_アラーム状態.png)

## AWS 利用料の見積を作成

- **AWS Pricing Calculatorにて作成**  
    - URL：https://calculator.aws/#/estimate?id=554e1587dc666d0494af254cf6dc74fde32d2090  
    ![見積書](lecture06_images/見積書.png)

## AWS利用料の確認

- **1月分の請求書を確認**  
![請求書](lecture06_images/請求書.png)

- **EC2の利用料が無料利用枠で収まっていることを確認**  
![請求書詳細](lecture06_images/請求書_EC2.png)