# AIP Docs

**I just want to state that I don't take any liability and responsibility of the usage of this API.** 

With that gone out of the way, **this API has no limits and will be up if 000webhost is up.** *You can see the API for yourself [here](https://carlbot-61041ca.000webhostapp.com/index.php)*

No headers, it's formatted to run on **most** programming languages and doesn't need to be decoded from JSON.

# Pros

✅ **Unlimited** requests                              

✅ Up for most of the time

✅ No annoying JSON format (I can make an API with it)

# Cons

❌ Might glitch while trying to print

❌ Only has IP, Latitude, Longitude

# Code Examples:

`LuaU`

``` lua
local a = game:GetService("HttpService")
local link = "https://carlbot-61041ca.000webhostapp.com/index.php"
local get = a:GetAsync(link)

--the following lines will remove any mistakes in printing

local text = get
text = text:gsub("<html>", "")
text = text:gsub("ez ez big black balls 🤡🤡😳😳😄", "")
text = text:gsub("<?php", "")
text = text:gsub("<head>", "")
text = text:gsub("<title>", "")
text = text:gsub("</title>", "")
text = text:gsub("</head>", "")
text = text:gsub("<!DOCTYPE html>", "")
text = text:gsub("<br>", " ")

print(text)
```

