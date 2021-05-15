# **TydiumCraft Skin API**
### `What does it do?`
The API makes it easier for your Bedrock skin to be rendered and outputted! Usually, you would have to use api.geysermc.org to get your texture ID, then figure out a way to use it in your preferred skin API (we send it to mc-heads). The TydiumCraft Skin API does it automatically for you. It also works with Java skins!

### `Using the API!`

Using the API couldn't be any more simple than what it is! First off, make sure that you have Floodgate 2.0. **This will NOT work without it.** Then by using the UUID of your Bedrock player, you can put it into this link `https://api.tydiumcraft.tk/skin?uuid={UUID}` and this will give you the default output of a body render, which should look something like the image below: 

![Default Output](https://api.tydiumcraft.tk/skin?uuid=00000000-0000-0000-0009-01fa3f915d0a&size=84)

Using the URL above will always give you the default render. There are a few more customization options to choose from. To use them add an ampersand (&) at the end of the URL and use one of the options below to put after it. Repeat that if you want an additional option.

It should look something like this: `https://api.tydiumcraft.tk/skin?uuid={UUID}&{Option}`

### `API Render Options`
### Primary Options
***
  Avatar | type=avatar

![Avatar](https://api.tydiumcraft.tk/skin?uuid=00000000-0000-0000-0009-01fa3f915d0a&type=avatar&size=64)
***
  Head | type=head

![Head](https://api.tydiumcraft.tk/skin?uuid=00000000-0000-0000-0009-01fa3f915d0a&type=head&size=64)
***
  Body | type=body

![Body](https://api.tydiumcraft.tk/skin?uuid=00000000-0000-0000-0009-01fa3f915d0a&type=body&size=64)
***
  Player | type=player

![Player](https://api.tydiumcraft.tk/skin?uuid=00000000-0000-0000-0009-01fa3f915d0a&type=player&size=64)
***
  Combo | type=combo

![Combo](https://api.tydiumcraft.tk/skin?uuid=00000000-0000-0000-0009-01fa3f915d0a&type=combo&size=64)
***
  Cape (Java only) | &type=cape

![Cape](https://api.tydiumcraft.tk/skin?uuid=Junki&type=cape&size=64)
***
  Skin | type=skin           

![Skin](https://api.tydiumcraft.tk/skin?uuid=00000000-0000-0000-0009-01fa3f915d0a&type=skin&size=64)
***
### Additional Options
***
  Size | size=(number)
Changes the image size.

![SizeSmall](https://api.tydiumcraft.tk/skin?uuid=00000000-0000-0000-0009-01fa3f915d0a&type=player&size=32) ![SizeLarge](https://api.tydiumcraft.tk/skin?uuid=00000000-0000-0000-0009-01fa3f915d0a&type=player&size=64)
***
  Flip | direction=(left/right)
Flips the body and head renders.

![RightBody](https://api.tydiumcraft.tk/skin?uuid=00000000-0000-0000-0009-01fa3f915d0a&type=body&size=64&direction=left) ![LeftBody](https://api.tydiumcraft.tk/skin?uuid=00000000-0000-0000-0009-01fa3f915d0a&type=body&size=64&direction=right)

![RightHead](https://api.tydiumcraft.tk/skin?uuid=00000000-0000-0000-0009-01fa3f915d0a&type=head&size=64&direction=left) ![LeftHead](https://api.tydiumcraft.tk/skin?uuid=00000000-0000-0000-0009-01fa3f915d0a&type=head&size=64&direction=right)
***
  Download | download

Instead of redirecting to mc-heads, pipe it through TydiumCraft servers for a direct download. This option will only work with type=skin. Using it on other types will result in a 403 Forbidden error.
***