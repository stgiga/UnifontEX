# UnifontEX
An extended fork of GNU Unifont with a focus on high compatibility, made from the last TrueType version of GNU Unifont (15.0.06), merged with the last version of Upper that will successfully merge after removing the placeholders (11.0.01 Upper). I then did several compatibility steps to make it work under more environments, such as taking SEVERAL measures to make the font work in environments that only want monospace fonts (which Unifont is closer to than something like Times New Roman), as well as fixing the TeX table (among other structures, including stuff like the Panose and OS/2 stuff, among other things), activating Vertical Metrics to make Inkscape not reject it when dealing with Vertical CJKV text, and making the output TTF work best on ALL OS choices. I also used TTF2PNG by Data Beaver's Domain (plus GIMP to make it true 1bpp) to make an unabridged 1 megabyte PNG of the font, for use in situations where TrueType wouldn't make sense.

## Now, what DOES adding Upper into Unifont offer?

Firstly: You gain the fancy letters intended for math but used online to make social media posts have fancier fonts. This includes Fraktur, which has its own ANSI escape code that is defined but rarely used. Those characters, and their bold versions via the bold flag, now work. 

Secondly: You gain emoji from 2018 and before (nothing newer due to being forced to stick to Unifont 11.0.01 Upper as the Upper version), as well as the rest of the characters in blocks that emoji only uses part of. So yes, you get the whole Playing Cards block, the whole Domino Tiles block, and the whole block allocated to Mahjong tiles. You also get all the symbol characters that didn't get emoji status. Stuff such as U+26FF, which is in the Miscellaneous Symbols block, and just so happens to be equivalent to the Rumpus Parable Agender Pride Flag from 2014. Yes, Unicode has THREE pride flags, not two. Samsung temporarily made the character an Emoji on some Android firmwares of theirs. You get the Alchemical Symbols block, including the Sublimate of Antimony symbol, which has been co-opted by nonbinary people as their gender symbol rather than the traditional male or female symbols (which DO have emoji status). So yes, this build of Unifont features the nonbinary symbol on top of the Plane 0 stuff like the transgender symbol, the symbols for various orientations, the Rumpus Parable flag, and etc. Oh, and unlike MANY Plane 0 fonts, Unifont DOES have U+2B89, something that accidentally resembles a gender symbol in the online LGBTQ+ furry community, one that is rarely used. 

Third: You get many OS symbols not in Plane 0, as well as a full set of Wingdings, Wingdings 2, Wingdings 3, and Webdings, many of which ARE emoji, and many of which are NOT. 

Fourth: You get more geometric symbols and historic scripts.

Fifth: You get both modern and ancient musical notation.

Sixth: You get "Transport and Map Symbols" as part of your emoji set.

Seventh: Having emoji makes you comply with the Shift_JIS extensions made by Japanese telephone carriers. 

Eighth: You can handle more obscure dingbats, as well as the Japanese ARIB captioning character set standard.

Ninth: You have more characters to work with for the purposes of Unicode art, especially when doing animated Unicode art, especially when you are dealing with more than just BW. There's more characters to derive brightness values from. 

Tenth: You can view even the most esoteric Kaomoji (Japanese emoticons that *aren't* emoji, such as the famous table flip one), including the ones that DO use emoji in them.

Eleventh: You gain more types of enclosed letters.

Twelfth: You can pass the current version of the BLNS test (a test file for string handling).

*And that's only the beginning.*

As part of the compatibility focus, the x in the filename "UnifontExMono" is lowercase just in case programs looking for "Mono" to determine monospaced status want a clear distinction. Also, I chose to use no symbols or spaces in the font name to make it work better on picky systems. If your system wants variable fonts, rename the font file to have "--VF" at the end before the extension, which can be .ttf or .otf (yes, TrueType fonts can be made to comply with OpenType too. In FontForge's TTF export, I turned on the "Apple", "OpenType", "Dummy 'DSIG'", "Windows-compatible 'kern'", "TeX Table", "FFTM Table" and ALL the PfaEdit Table checkboxes, so that the font would work on as many systems as possible.) Note that "--" on Linux is what is often used for command-line arguments, so that *could* confuse Linux machines. Also, I chose to make the name of this version of Unifont distinct from the official version, because this is a specialized fork that diverged from non-current versions of Unifont (though not horrifically so by any means). That being said, I `did` take quite a few measures to keep things faithful to the original. Compatibility is key. *That's* why I'm keeping the OS/2 table version identical, not touching the GASP table, and etc. The goal of this project is to build on Unifont to make it even greater than it already is, and to do it one better in many ways. That's why I'm so dedicated to it.

Oh, and by the way: This is a passion project that I have worked on for the last 6 years (maybe 7), in part because I was waiting for new Unicode and Unifont versions to drop so I could see what was in them. This isn't the longest project I have done (that honor goes to two of which I have spent 8 years on), but it certainly was a long haul. I hope that my improvements help you in your endeavors.

In case you wonder why this repo was created a month early, that is so I could write the description to a heightened standard prior to release date, and decide on a name. Expect a Github Pages site for this, among other things.
