# luagram - 1.0
 Lua telegram client

# [Telegram Group](https://t.me/luagramgroup)

# installing

luarocks install luagram-clinet

## Using : 
- Import `luagram-client` into the bot.
- Call the functions.

See example script below.


```lua

local luagram = require 'luagram-client'
local app = luagram.set_config{
  api_id = 1234567,
  session_name = 'session_name',
  api_hash = 'api_hash',
  -- token = ''
}
function main(msg)
  if msg.content.text then
    if msg.content.text.text == 'ping' then
      app.sendText(msg.chat_id, msg.id, '<b> pong </b>', 'html')
    end
  end
end
luagram.run(main)


```
for get result  

```lua 
result = app.func ()
app.vardump(result)
```



## Luagram
