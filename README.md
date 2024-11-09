# Streamfile Worker
File To Link Telegram Bot Using Cloudflare Workers.

<br>

## 🗂 Variables
```javascript
const BOT_TOKEN = "BOT_TOKEN"; // Insert your bot token.
const BOT_WEBHOOK = "/endpoint"; // Let it be as it is.
const BOT_SECRET = "BOT_SECRET"; // Insert a powerful secret text.
const BOT_OWNER = 123456789; // Insert your telegram account id.
const BOT_CHANNEL = -100123456789; // Insert telegram channel id.
const SIA_NUMBER = 1234; // Insert a random integer.
```

### Setup:
- Get `BOT_TOKEN` from [@botfather](https://t.me/botfather).
- Change `BOT_WEBHOOK` with your preferred webhook.
- Change `BOT_SECRET` with a powerful secret text (only `[A-Z, a-z, 0-9, _, -]` are allowed).
- Change `SIA_NUMBER` with a random integer (number).
- Get `BOT_OWNER` from [@idbot](https://t.me/username_to_id_bot).
- Get `BOT_CHANNEL` id by forwarding a message from channel to [@idbot](https://t.me/username_to_id_bot).
  - Channel **ID** must start with `-100`.
  - Bot must be **admin** in channel with **edit rights**.

<br>

## ⚙️Deploy
- Create a [Cloudflare](https://www.cloudflare.com/) **account**.
- Navigate to `Workers & Pages > Create > Create Worker`.
- Deploy the worker by clicking **Deploy**.
- Edit the code by clicking **Edit Code**.
- Upload `worker.js` into **Cloudflare**.
- Modify the [variables](#Variables).
- Finally, **Deploy**.

[![Deploy to Cloudflare Workers](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/Kunani1/filestream-cf)
### Setup:
- Once you deployed the bot on Cloudflare.
- Check `XXX.XXXX.workers.dev/getMe` to verify your bot authorization.
- Open `XXX.XXXX.workers.dev/registerWebhook` to register your bot webhook.
- Then you can start using your bot.

<br>

## 📚 Response
```python
Telegram Link: t.me/usernamebot/?start=ZG9uJ3QgZGVjb2Rl
Download Link: XX.XX.workers.dev/?file=ZG9uJ3QgZGVjb2Rl
Stream Link: XX.XX.workers.dev/?file=ZG9uJ3QgZGVjb2Rl&mode=inline
```

### Limitation:
- Telegram Link: `<4.00GB`
- Download Link: `<20.00MB`
- Stream Link: `<20.00MB`

<br>

## 📷 Screenshot

<a href="#Screenshot"><img src="https://github.com/user-attachments/assets/522ed6a6-3516-421e-aa26-563bb0a96e98" width="300px"></a>
