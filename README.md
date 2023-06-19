![github-header-image (1)](https://user-images.githubusercontent.com/102983952/227266392-088e5ded-bbc6-4312-9daa-cae451488a75.png)
# AIP Docs

**I just want to state that I don't take any liability and responsibility for the usage of this API.** 

With that going out of the way, **this API has no limits and will be up if 000webhost is up.** *You can see the API for yourself [here](https://carlbot-61041ca.000webhostapp.com/index2.php)*

No headers, it's formatted to run on **most** programming languages and doesn't need to be decoded from JSON.

# Pros

✅ **Unlimited** requests                              

✅ Up for most of the time

# Cons

~~❌ Might glitch while trying to print~~ Fixed the bug with version 2.0

# Code Examples:

`LuaU`

``` lua
local HttpService = game:GetService("HttpService")
local link = "https://carlbot-61041ca.000webhostapp.com/index.php"
local get = HttpService:GetAsync(link)

--the following lines will remove any mistakes in printing

local text = get
text = text:gsub("<html>", "")
text = text:gsub("AIP, The world at one click.", "")
text = text:gsub("<?php", "")
text = text:gsub("<head>", "")
text = text:gsub("<title>", "")
text = text:gsub("</title>", "")
text = text:gsub("</head>", "")
text = text:gsub("<!DOCTYPE html>", "")
text = text:gsub("<br>", " ")

print(text)
```

# Patch-Notes

> 24 / 03 / 2023 (DD/MM/YYYY)

✅ • **Added ISP, Region, City, Timezone, and country.**

✅ • Started working on **JSON Api.**

✅ • Changed the main title to something not childish

> 19 / 06 / 2023 (DD/MM/YYYY) Version 2.0

✅ • **Added private API which you can purchase by sending a dm to me on Discord (Username: 2_swag)** *Version 2.0.1*

✅ • **JSON API is finished and can be found [here](https://carlbot-61041ca.000webhostapp.com/index3.php)** *Version 0.1.1*

✅ • **Added an easteregg**

✅ • **Patched**
