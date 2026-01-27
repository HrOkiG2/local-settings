使用しているプラグイン
```
plugins=(
  git 
  aws 
  fzf 
  zsh-autosuggestions 
  zsh-syntax-highlighting
)
```

zsh-syntax-highlighting:

```Bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

zsh-autosuggestions:
```Bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

| プラグイン名 | 役割 | 主なメリット・機能 |
| :--- | :--- | :--- |
| **git** | Git操作の効率化 | `ga`(add), `gcmsg`(commit) 等、100種以上のエイリアスを提供。ブランチ名の表示もサポート。 |
| **aws** | AWS操作の補完 | サブコマンドのTab補完を強力に。`asp`コマンドでプロファイルをインタラクティブに切り替え可能。 |
| **fzf** | あいまい検索 | `Ctrl+r`での履歴検索が爆速に。「うろ覚え」のコマンドをリストから一瞬で探し出せる。 |
| **zsh-autosuggestions** | 入力予測 | 過去の履歴から「続き」をグレーで表示。`→`キー一発で長いコマンド（aws-vault等）を完成。 |
| **zsh-syntax-highlighting** | 構文色分け | 正しいコマンドは**緑**、ミスは**赤**で表示。実行前にスペルミスに気づける視覚的ガイド。 |