# db_wrapper

Public db_wrapper created in javascript

## 🛠️ Setup

- Place the solar_db folder in your resources

- Ensure fxmanifest.lua is included

- Add ensure solar_db to your server.cfg

## 📡 Exports

These functions are available to all server-side resources:

| Function   | Description                              |
| ---------- | ---------------------------------------- |
| `query`    | Run any SQL query (SELECT, INSERT, etc.) |
| `fetchOne` | Get the first row from a query result    |
| `insert`   | Insert a row with a helper wrapper       |
| `update`   | Update a row with a helper wrapper       |

## 📥 Example Usage (JavaScript)

```
const users = await global.exports['db_wrapper'].query('SELECT \* FROM users');
const id = await global.exports['db_wrapper'].insert('users', { name: 'Michael' });
```

## 📥 Example Usage (Lua)

```
local users = exports['db_wrapper']:query('SELECT \* FROM users')
local id = exports['db_wrapper']:insert('users', { name = 'Lily' })
```

## 🔐 Security Notes

Logic is obfuscated for protection and tamper resistance

config.js is the only file that should be edited

## 💬 Need Help?

Join the Discord or open an issue for questions about integration.
