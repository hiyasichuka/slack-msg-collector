# 前提

- https://api.slack.com/apps/ で、App を作成の上、User Token Scopes を以下のように設定し、OAuth Token を取得しておくこと。

```
# OAuth Scope
channels:history
channels:read
emoji:read
groups:history
reactions:read
users:read
```

OAuth & Permissions -> User OAuth Token から取得したものを.env に設定する。

# 利用手順

```
cp .env.sample .env
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```