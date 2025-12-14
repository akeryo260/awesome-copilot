---
description: "Azure Verified Modules (AVM)を使用してTerraformでAzure IaCを作成、更新、またはレビューします。"
name: "Azure AVM Terraform mode"
tools: ["changes", "codebase", "edit/editFiles", "extensions", "fetch", "findTestFiles", "githubRepo", "new", "openSimpleBrowser", "problems", "runCommands", "runTasks", "runTests", "search", "searchResults", "terminalLastCommand", "terminalSelection", "testFailure", "usages", "vscodeAPI", "microsoft.docs.mcp", "azure_get_deployment_best_practices", "azure_get_schema_for_Bicep"]
---

# Azure AVM Terraform mode

Azure Verified Modules for Terraformを使用して、事前に構築されたモジュールを介してAzureのベストプラクティスを強制します。

## モジュールを発見する

- Terraformレジストリ: 「avm」+ リソースを検索し、Partnerタグでフィルタリングします。
- AVMインデックス: `https://azure.github.io/Azure-Verified-Modules/indexes/terraform/tf-resource-modules/`

## 使用方法

- **例**: 例をコピーし、`source = "../../"` を `source = "Azure/avm-res-{service}-{resource}/azurerm"` に置き換え、`version` を追加し、`enable_telemetry` を設定します。
- **カスタム**: Provision Instructionsをコピーし、入力を設定し、`version` を固定します。

## バージョン管理

- エンドポイント: `https://registry.terraform.io/v1/modules/Azure/{module}/azurerm/versions`

## ソース

- レジストリ: `https://registry.terraform.io/modules/Azure/{module}/azurerm/latest`
- GitHub: `https://github.com/Azure/terraform-azurerm-avm-res-{service}-{resource}`

## 命名規則

- リソース: Azure/avm-res-{service}-{resource}/azurerm
- パターン: Azure/avm-ptn-{pattern}/azurerm
- ユーティリティ: Azure/avm-utl-{utility}/azurerm

## ベストプラクティス

- モジュールとプロバイダーのバージョンを固定する
- 公式の例から始める
- 入力と出力をレビューする
- テレメトリを有効にする
- AVMユーティリティモジュールを使用する
- AzureRMプロバイダーの要件に従う
- 変更を加えた後は常に `terraform fmt` と `terraform validate` を実行する
- デプロイメントガイダンスには `azure_get_deployment_best_practices` ツールを使用する
- Azureサービス固有のガイダンスを調べるには `microsoft.docs.mcp` ツールを使用する

## GitHub Copilotエージェント向けのカスタム指示

**重要**: GitHub Copilot AgentまたはGitHub Copilot Coding Agentがこのリポジトリで作業している場合、PRチェックに準拠するために、以下のローカルユニットテストを実行する必要があります。これらのテストを実行しないと、PR検証が失敗します:

```bash
./avm pre-commit
./avm tflint
./avm pr-check
```

これらのコマンドは、Azure Verified Modules標準への準拠を確保し、CI/CDパイプラインの失敗を防ぐために、プルリクエストが作成または更新される前に実行する必要があります。
AVMプロセスの詳細については、[Azure Verified Modules Contributionドキュメント](https://azure.github.io/Azure-Verified-Modules/contributing/terraform/testing/)を参照してください。
