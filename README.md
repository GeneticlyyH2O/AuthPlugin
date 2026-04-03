# AuthPlugin

Discord-based authentication system for PaperMC

Supported: 1.12  
WIP: 1.13 → 1.16, 1.17 → 1.21

---

## What it does

* No `/register`
* One account per Discord user
* Built-in web signup (served by the plugin)
* Players are locked until they log in

---

## Setup

### Discord

Create an application → OAuth2

Redirect URL:

https://your-domain/callback

Enable:

* Message Content Intent
* Server Members Intent

Invite the bot with:

* Manage Roles

Make sure the bot role is above your verified role.

---

## Config

plugins/AuthPlugin/config.yml

web:
  port: 8080 
  public-url: ""

style:
    background: "#0f172a"
    text-color: "#ffffff"
    accent: "#5865F2"
    font: "Arial"
    button-radius: "8px"

discord:
  bot-token: "BOT_TOKEN"
  client-id: "CLIENT_ID"
  client-secret: "CLIENT_SECRET"
  guild-id: "GUILD_ID"
  verified-role-id: "ROLE_ID"

messages:
  login: "&cLogin with: /login <password>"

---

## Usage

1. Join the server  
2. Open the link shown in chat  
3. Login with Discord  
4. Create your account  
5. Use `/login <password>` in-game  

---

## Notes

* `public-url` MUST match your Discord redirect exactly
* Port must be open / accessible
* The bot must be able to assign the verified role

---

## If something breaks

Check:

* redirect URL mismatch  
* `public-url` incorrect  
* bot token / permissions  
* port not exposed / blocked  

---

## Extra

* `/l` works as an alias for `/login`
* Password resets are handled through Discord DMs
* Sessions are stored server-side (not client-side)

---

## Status

Actively being worked on. Expect changes.
