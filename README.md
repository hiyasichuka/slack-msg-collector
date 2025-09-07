# 前提

- https://api.slack.com/apps/ で、App を作成の上、User Token Scopes を以下のように設定し、OAuth Token を取得しておくこと。

```
# OAuth Scope
channels:history
channels:read
```

![UserTokenScope](/imgs/user-token-scope.png "サンプル")


OAuth & Permissions -> User OAuth Token から取得したものを.env に設定する。


# 利用手順

```
cp .env.sample .env
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```


`slack-msg-collector.ipynb` を開き、`channel id` および取得開始から終了日時を設定する。

```
# --- 設定 ---
CHANNELS = [
    "C", # channel id
]

START_DATE = datetime.datetime(2025, 9, 1, 0, 0, 0, tzinfo=JST)
END_DATE   = datetime.datetime(2025, 9, 7, 23, 59, 59, tzinfo=JST)
```

Jupyterを上から順番に実行していく。

以上。