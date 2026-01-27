## ユースケース
- 複数のプロジェクト扱っている時にテーマを切り替え視認性を上げる
- 同一プロジェクトで環境別にテーマを切り替え視認性を上げる

下記のコードを `~/.zshrc` へ追加するか、ファイルを切り、インポートする形で使用する

```
# iTerm2のプロファイルを切り替える関数
function iterm_set_profile() {
  local profile_name="$1"
  # iTerm2の制御シーケンスを送信
  echo -e "\033]1337;SetProfile=${profile_name}\a"
}

# ディレクトリによってiTerm2のプロファイルを切り替える関数
function precmd_iterm_profile_switcher() {
  if [[ "$PWD" == *"/Users/hoge/fuga"* ]]; then
    iterm_set_profile "HogeProfile" # 特定のディレクトリなHogeプロファイル
  else
    iterm_set_profile "DefaultProfile" # それ以外のディレクトリならDefaultプロファイル
  fi
}

# precmd_functionsに、定義した関数を追加
precmd_functions+=(precmd_iterm_profile_switcher)
```