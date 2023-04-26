<!-- omit in toc -->
# CloudFormationテンプレート実装覚書

---

<!-- omit in toc -->
# 目次
- [1. Lambda](#1-lambda)
  - [1.1. billing-function](#11-billing-function)


# 1. Lambda
## 1.1. billing-function
- 使ったプロンプト
```
あなたはプロのAWSエンジニアです。
あなたは日次でAWSサービス毎の請求額をSlackに通知する仕組みを実装する必要があります。
以下の用件をもとにCloudFormationテンプレートを作成して下さい。

使用サービス: Lambda, Eventbridge, Slack

システムの流れ:
1. 毎朝午前9時になるとEventBridgeが発動し、Lambda関数「billing-function」を実行
2. トリガーされたLambda関数は実行されると予め関数に組み込まれていたWebhook URLに対してPOSTする。

その他事項:
・Lambda関数はPythonの最新バージョンで実装してください。
・AWSコスト情報はCost Explorerから取得するようにします。
・SlackのWebhook機能を使用してLambda関数を実装して下さい。
・CloudFormationテンプレートはYAML形式にて作成して下さい。
```