# Cursor 設定コピー手順（Ubuntu / Windows）

Sublime Text 風の設定を Cursor に適用する手順です。

## 含まれる設定

- **テーマ**: Monokai
- **フォント**: monospace / サイズ 16
- **エディタ**: タブ4、80桁ルーラー、スムーススクロール、括弧の色分けなど
- **キーバインド**: Ctrl+I で Agent

## なる早でやるとき
**CURSORでプロジェクトを読み込んで実行させると全部やってくれるぜ**

## 設定フォルダの場所

| OS | パス |
|----|------|
| **Ubuntu** | `~/.config/Cursor/User/` |
| **Windows** | `%APPDATA%\Cursor\User` または `C:\Users\<ユーザー名>\AppData\Roaming\Cursor\User` |

## コピーするファイル

| コピー元 | コピー先 |
|----------|----------|
| `settings.json` | `.../User/settings.json` |
| `keybindings.json` | `.../User/keybindings.json` |

**Ubuntu ワンライナー**（プロジェクトルートから）:
```bash
cp CURSOR_SETTINGS/settings.json ~/.config/Cursor/User/settings.json
cp CURSOR_SETTINGS/keybindings.json ~/.config/Cursor/User/keybindings.json
```

- **既存設定を残す**: 既存ファイルを開き、必要な項目だけマージ
- **完全置換**: 上書きコピー

## 補足

- **テーマ**: Monokai は標準搭載。反映されない場合は拡張機能で「Monokai」を検索してインストール
- **フォント**: `monospace` は OS の等幅フォント（Ubuntu → Ubuntu Mono、Windows → Consolas など）。別フォントを使う場合は `editor.fontFamily` を変更
- コピー後 **Cursor を再起動**して反映。設定変更は `Ctrl+,` からも可能
