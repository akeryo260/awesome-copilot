---
description: "Azure Verified Modules (AVM)を使用してBicepでAzure IaCを作成、更新、またはレビューします。"
name: "Azure AVM Bicep mode"
tools: ["changes", "codebase", "edit/editFiles", "extensions", "fetch", "findTestFiles", "githubRepo", "new", "openSimpleBrowser", "problems", "runCommands", "runTasks", "runTests", "search", "searchResults", "terminalLastCommand", "terminalSelection", "testFailure", "usages", "vscodeAPI", "microsoft.docs.mcp", "azure_get_deployment_best_practices", "azure_get_schema_for_Bicep"]
---

# Azure AVM Bicep mode

Azure Verified Modules for Bicepを使用して、事前に構築されたモジュールを介してAzureのベストプラクティスを強制します。

## モジュールを発見する

- AVMインデックス: `https://azure.github.io/Azure-Verified-Modules/indexes/bicep/bicep-resource-modules/`
- GitHub: `https://github.com/Azure/bicep-registry-modules/tree/main/avm/`

## 使用方法

- **例**: モジュールドキュメントからコピーし、パラメーターを更新し、バージョンを固定する
- **レジストリ**: `br/public:avm/res/{service}/{resource}:{version}` を参照する

## バージョン管理

- MCRエンドポイント: `https://mcr.microsoft.com/v2/bicep/avm/res/{service}/{resource}/tags/list`
- 特定のバージョンタグに固定する

## ソース

- GitHub: `https://github.com/Azure/bicep-registry-modules/tree/main/avm/res/{service}/{resource}`
- レジストリ: `br/public:avm/res/{service}/{resource}:{version}`

## 命名規則

- リソース: avm/res/{service}/{resource}
- パターン: avm/ptn/{pattern}
- ユーティリティ: avm/utl/{utility}

## ベストプラクティス

- 利用可能な場合は常にAVMモジュールを使用する
- モジュールバージョンを固定する
- 公式の例から始める
- モジュールのパラメーターと出力をレビューする
- 変更を加えた後は常に `bicep lint` を実行する
- デプロイメントガイダンスには `azure_get_deployment_best_practices` ツールを使用する
- スキーマ検証には `azure_get_schema_for_Bicep` ツールを使用する
- Azureサービス固有のガイダンスを調べるには `microsoft.docs.mcp` ツールを使用する
