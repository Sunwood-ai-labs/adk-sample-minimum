<div align="center">

# 🤖 Weather & Time AI Agent Implementation

このディレクトリには、天気と時間を教えてくれるAIエージェントの実装が含まれてるよ！✨

</div>

## 📁 ファイル構成

- `agent.py` - メインのエージェント実装
- `.env` - 環境変数設定ファイル
- `__init__.py` - Pythonパッケージ定義

## 💻 実装の詳細

### エージェントの機能

1. 🌤️ **天気情報の取得** (`get_weather`関数)
   - 指定した都市の天気情報を返すよ
   - 現在はニューヨークの情報のみ対応してるの

2. 🕒 **時刻情報の取得** (`get_current_time`関数)
   - 指定した都市の現在時刻を返すよ
   - タイムゾーン情報を使って正確な時刻を計算するの

### 使用モデル

- `gemini-2.0-flash-exp` - Google の最新のAIモデルを使用！
  - 高速なレスポンス
  - 自然な会話が可能

## 🛠️ カスタマイズ方法

### 新しい都市の追加

`get_weather`関数と`get_current_time`関数を修正して、新しい都市を追加できるよ！

```python
# get_weather関数での新都市の追加例
if city.lower() == "tokyo":
    return {
        "status": "success",
        "report": "The weather in Tokyo is..."
    }

# get_current_time関数での新都市の追加例
if city.lower() == "tokyo":
    tz_identifier = "Asia/Tokyo"
```

## 📝 注意点

- APIキーは必ず`.env`ファイルで管理してね！
- カスタマイズする時は、既存のエラーハンドリングを参考にしてね！

## 🔗 関連リンク

- [プロジェクトのトップページ](../README.md)
- [Google ADKドキュメント](https://developers.google.com/adk)
