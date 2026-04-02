# AuthPlugin

Discord-based login system for Paper 1.12

---

## What it does

* No `/register`
* One account per Discord
* Web signup (hosted by the plugin)
* Players locked until login

---

## Setup

### Discord

Create an application → OAuth2

Redirect:

```
https://your-domain/callback
```


Enable:

* Server Members Intent

Invite bot with:

* Manage Roles

---

## Config

`plugins/AuthPlugin/config.yml`

```
web:
  port: 8080
  public-url: "https://your-domain"

discord:
  bot-token: "TOKEN"
  client-id: "ID"
  client-secret: "SECRET"
  guild-id: "GUILD_ID"
  verified-role-id: "ROLE_ID"
```

---

## Usage

1. Join server
2. Open link
3. Login with Discord
4. Create account

---

## Notes

* `public-url` must match redirect exactly
* Bot role must be above verified role
* Port must be accessible
* I plan to improve this later
---

## If it breaks

Check:

* redirect URL
* public-url
* bot permissions
