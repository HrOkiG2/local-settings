キーの平文おきを避けたいため、 `aws-vault` を使用します。
`aws configure` を実行しないので、`~/.aws/` を自分で作ってね

## command install
```
$ brew install awscli
$ brew install aws-vault
```

## setup aws-vault

```
$ aws-vault add {profile-name}
.
.
.
// setp by step input.
// Access key ID
// Secret access key
// mfa_serial
```

## cli_auto_prompt

| 設定値 | 挙動 | おすすめの人 |
| :--- | :--- | :--- |
| **on** | コマンドを完璧に打ったとしても、実行前に必ずインタラクティブなプロンプト（選択画面）が開く。 | AWS CLIに不慣れな方、実行前に必ずパラメータを再確認したい慎重派の人。 |
| **on-partial** | コマンドが正しく完結している場合はそのまま実行。入力が不完全（タイポや必須引数の不足）な時だけプロンプトが起動する。 | **中〜上級者。** 普段はサクサク打ちたいが、コマンドを忘れた時だけ助けてほしい効率重視の人。 |