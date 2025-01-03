This folder contains builds of UnifontEX for Minecraft versions that support TrueType font loading (1.13+), (and legacy PNG builds for 1.5-1.12.2) but pre-date 1.20 adding the official Unifont .hex files. Plane 1 characters work on Minecraft 1.16 and above, but Plane 0 characters are still up-to-date with 1.20 and 1.21. Plane 1 characters in supported versions go up to Unifont Upper 11.0.01 due to the limitations of most TrueType/OpenType renderers (including Minecraft's), so not everything in 1.20+ text works, but the lions' share does, and it's certainly better than stock. 

Now for the version guide:

> The `pf0` in `UnifontEXpf0.zip` means that it's a texture pack (`NOT` a `Resource Pack`), and it's for `1.5-1.5.2`.

> The `pf1` in `UnifontEXpf1.zip` means `Pack Format 1`, which is `1.6.1-1.8.9`

> The `pf2` in `UnifontEXpf2.zip` means `Pack Format 2`, which is `1.9-1.10.2`

> The `pf3` in `UnifontEXpf3.zip` means `Pack Format 3`, which is `1.11-1.12.2`

> The `pf4` in `UnifontEXpf4.zip` means `Pack Format 4`, which is `1.13-1.14.4`

> The `pf5` in `UnifontEXpf5.zip` means `Pack Format 5`, which is `1.15-1.16.1`

> The `pf6` in `UnifontEXpf6.zip` means `Pack Format 6`, which is `1.16.2-1.16.5`

> The `pf7` in `UnifontEXpf7.zip` means `Pack Format 7`, which is `1.17-1.17.1`

> The `pf8` in `UnifontEXpf8.zip` means `Pack Format 8`, which is `1.18-1.18.2`

> The `pf9` in `UnifontEXpf9.zip` means `Pack Format 9`, which is `1.19-1.19.2`

> The `pf12` in `UnifontEXpf12.zip` means `Pack Format 12`, which is `1.19.3`

> The `pf13` in `UnifontEXpf13.zip` means `Pack Format 13`, which is `1.19.4`

WARNING: The Legacy Unicode PNG stuff is derpy, toy around and find out, and do so at your own risk, I used [Mineglyph](https://github.com/Hakdaw/Mineglyph) as the converter, so if you can do better let me know what options to use. 

For usage in a server resource pack config file line in 1.13, you want to do `https://stgiga.github.io/UnifontEX/MCpacks/UnifontEXpf4.zip`, for instance. If you're using something like Viaversion, you'd want it to give the relevant client versions the needed resource pack in an unskippable way. That way, if a 1.20+ player sends an above-Plane0 character, assuming it's in UnifontEX's character set (Unifont-JP 15.0.06+15.1.01 + Unifont 11.0.01 Upper, the highest you can go without HarfBuzz extensions that few apps support, of which Minecraft is *not* among them), it will display in 1.13-1.19.4 clients. I should also mention that font resource packs are not possible in Bedrock, so if you allow Bedrock players to connect, at best they will be forced to the device's native emoji set (on Android phones that support font switching by some means, UnifontEX installed as a UI font will work as one), but other Plane 1 characters will likely be forsaken. I say "at best" because Bedrock has a reputation of not working with higher-plane characters *at all*. 

Viaversion can allow Java clients as early as 1.7 to connect, so players on decade+-old versions like 1.7 and 1.8 (my favorite versions prior to TrueType support) won't see these. It *is* possible to replace and extend the legacy PNGs (and they are devilishly tricky to get right, I'm glad I fixed spacing, but there is still a bit of jank to the whole thing), and I'm not sure how Plane 1 characters would work, let alone the Plane 2 Kanji or the Plane 3 Biang and Taito Han characters, or Plane 14 `Tags` + `Variation Selectors Supplement` characters.

Quick note: Bold characters in TrueType mode appear as double-struck/outline due to Minecraft applying the same bolding method (duplicating and shifting pixels) across the board. This affects ALL versions I've played with it (1.17-1.19). Since the obfuscation text effect cycles through codepoints, I'm unsure of how it would handle 65422 glyphs, but in plugin-using servers I'm in it hasn't broken, and I don't think other formatting codes have either.

Also getting the TrueType font scaling right took about an hour of trial and error/bruteforcing if I remember correctly, and it took months to get the legacy PNG scaling working. TrueType mode visually is still bigger than default `Force Unicode Font`, so if you want heavy Unicode support *and* have bad vision like I do, you may find this appealing.

I know that there are some retrocomputing enthusiasts like Action Retro on YouTube who play older versions or modded older versions on old hardware, and I know a LOT of modpacks target significantly older versions of Minecraft, so there *are* use cases. Also, if one doesn't trust the `No Chat Reports` mod and plugin due to it deliberately not being universal (in my opinion defeating the entire purpose), and you want to armor yourself by playing older versions on *purpose*, but you still want to use emoji, *this* is the answer. Pack Format 4 through Pack Format 8 (and Pack Format 9 if you trust the original 1.19 version, which I don't fully) builds are handy for this. Obviously if you do a Viaversion server going back in time to 1.7-1.8 there is even more safety, though I still would play below 1.19.1 or for further safety 1.18.2, just to be safe. 

My cheap personal server from 2013 has only 512MiB of RAM and is 10-players. It won't even start if made to run anything newer than 1.17.1. It also collapses if given plugins on 1.17.1. So if you're on a shoestring budget, and you want a server to play with your friends on, and you want emoji, you may be able to have that pony. 

If you're like Snoopietek/WindowsG Electronics, and you enjoy making Minecraft and/or its server run on ancient computers, you can *also* use these, since the versions you can reasonably run can fit here. 

I'm a Java veteran (I've owned Minecraft Java since 2013), and it was actually Minecraft that got me into Unifont. And no, I don't have a Minecon 2013 cape `😭` (It's a very wild and sad tale...)
I was very adept at the Redstone and Creative stuff ten years ago. I use the Programmer Art resource pack.

TL;DR: If you support "retro" versions of Minecraft on your server, whether exclusively or inclusively, these files allow display of text supported by very modern Minecraft on quite a few versions not normally able to do so.
