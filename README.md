# OnlyCat Developer

## Welcome

This is the developer hub for the OnlyCat smart cat flap:  
https://www.onlycat.com

We’ll be sharing APIs, developer documentation, and featuring community-built projects.

---

## 💬 Discussion

Join the conversation on GitHub Discussions:  
https://github.com/OnlyCatAI/onlycat-developer/discussions

---

## 💬 Discord

Join the OnlyCat community:  
https://discord.gg/Xg3bCgXbZa

---

## 📘 Door Policy Schema

Learn about the OnlyCat Door Policy schema:
https://www.onlycat.com/door-policy-schema/

---

## 🔑 API Keys

Enable **Developer Mode** in the OnlyCat app under **Account**, then open
**API Keys** to create a key for your integration.

API keys have full access to your OnlyCat account. Create a separate key for
each integration, store it securely, and revoke it from the app when it is no
longer needed. A new key is displayed only when it is created.

Use the key as the Socket.IO authentication token:

```python
import asyncio
import socketio

async def main():
    client = socketio.AsyncClient()
    await client.connect(
        "https://gateway.onlycat.com",
        transports=["websocket"],
        auth={"token": "oc_live_..."},
    )
    await client.wait()

asyncio.run(main())
```

API key authentication grants the same account-level Socket.IO access as the
OnlyCat app. REST bearer authentication is not currently supported.

---

## 🏠 Home Assistant Integration

Official community integration:  
https://github.com/OnlyCatAI/onlycat-home-assistant

---

## 🚀 Submit Your Project

Built something with OnlyCat?

Open a GitHub Discussion or pull request to share your project and get featured.
