# terraform


## mac OSの場合のset up
```
brew tap hashicorp/tap
brew install hashicorp/tap/terraform
```

### autocompleteの設定
macOSではzshを使用しているため下記のエラー時は~/.zshrcファイルを作成することで解消できる
```bash
% terraform -install-autocomplete
Error executing CLI: Did not find any shells to install
% touch ~/.zshrc
% terraform -install-autocomplete
```


## provider
### docker provider
https://registry.terraform.io/providers/kreuzwerker/docker/latest/docs

provider色々用意されている
https://registry.terraform.io/browse/providers
例えばcloudRunならこれ
https://registry.terraform.io/modules/GoogleCloudPlatform/cloud-run/google/latest


## terraform環境変数優先順位

最終的な優先順位（高い順）
- -var オプション（CLI）
- 環境変数（TF_VAR_変数名）
- terraform.tfvars や *.auto.tfvars
- デフォルト値（variable の default）