# Brainfuck-to-Headsecks
Converts Brainfuck source code to Headsecks code, or vice versa.

## Description  
Takes [Brainfuck](https://esolangs.org/wiki/Brainfuck) source code from a file and outputs valid [Headsecks](https://esolangs.org/wiki/Headsecks) source code to stdout. Can also perform the reverse operation. It should be noted that many unicode characters may or may not be printable, it depends on your system/application. Even if the Headsecks output doesn't display properly, it will still be valid.

## Usage  
```
usage: bf2hs.py [-h] [-d] [-e] [--random] [--trigram] [--chess] [--latin]
                [--chinese] [--cyrillic] [--arabic] [--gothic] [--range RANGE]
                input_file

positional arguments:
  input_file     File containing the source code to convert

optional arguments:
  -h, --help     show this help message and exit
  -d, --decode   Decode source from Headsecks to Brainfuck
  -e, --encode   Encode source from Brainfuck to Headsecks
  --random       Randomly select unicode characters upon encoding (default)
  --trigram      Exclusively use trigram characters to encode
  --chess        Exclusively use chess characters to encode
  --latin        Exclusively use basic Latin characters to encode
  --chinese      Exclusively use Chinese characters to encode
  --cyrillic     Exclusively use Russian alphabet to encode
  --arabic       Exclusively use Arabic characters to encode
  --gothic       Exclusively use Gothic characters to encode
  --range RANGE  User specified unicode characters to use for encoding. Input
                 range of characters in form of a string e.g. '0x1000-0x125D'
```

## Examples
All encoding examples use a source file containing a basic Hello World! program. Encoding Brainfuck to Headsecks can be done like so:  
`./bf2hs.py -e --trigram bf_HelloWorld.txt`. Example outputs are shown below.

**trigram**  
>☰☰☰☰☰☰☰☰☶☳☰☰☰☰☶☳☰☰☳☰☰☰☳☰☰☰☳☰☲☲☲☲☱☷☳☰☳☰☳☱☳☳☰☶☲☷☲☱☷☳☳☴☳☱☱☱☴☰☰☰☰☰☰☰☴☴☰☰☰☴☳☳☴☲☱☴☲☴☰☰☰☴☱☱☱☱☱☱☴☱☱☱☱☱☱☱☱☴☳☳☰☴☳☰☰☴

**chess**  
>♘♘♘♘♘♘♘♘♖♛♘♘♘♘♞♛♘♘♛♘♘♘♛♘♘♘♛♘♚♚♚♚♙♗♛♘♛♘♛♙♛♛♘♖♚♗♚♙♟♛♛♔♛♙♙♙♜♘♘♘♘♘♘♘♜♔♘♘♘♜♛♛♔♚♙♜♚♔♘♘♘♔♙♙♙♙♙♙♔♙♙♙♙♙♙♙♙♜♛♛♘♔♛♘♘♔

**chinese**  
>牰祘駠无茀劈鏸興鉞揓樸锸曘泰抆輳搈嬰笛梨蒸忠耻瞸枈酀晛屠攚毺粚轪燉驗經碘菣司褣襙諓蘣筐圾节鳿灚姙淏磻癛崔繃暹蠁穹资塰預馨篨陈樈筸婜腄驰噸腀惬酃謓暼岺妑伜咚丼激贈婀阔歉菁籩歱蔹篡梼舑镁滙呙玱炑穑雹佴舋臓恰捼垃鰨氠榄

**cyrillic**  
>рААиаШиШЖГииИАжлиШГРРрлаААГРкТТвЩплАЫИЫЙЫуИцвЧкЙпГГФГБСбдШАриШШИмЬаАРДЫЫфЪЩдТдиРрдсЙБЙЙБФсСйСБйЩЙДуГидуАШД

**arabic**  
>ﭰﭸﭸﮘﮘﮈﮈﭐﭖﭓﭨﮈﭐﭨﮖﭻﭨﭐﮋﭐﮈﭠﮛﭘﮀﮐﭓﮘﭒﮒﭒﭪﭩﮇﭻﮐﭓﭰﮋﭑﭓﭳﭸﭖﭺﭟﭒﮙﮏﭛﭫﭬﭓﭹﭡﭱﮄﭐﭐﭸﭰﮘﭸﭠﭼﮄﭸﭐﮈﮜﭳﭫﮄﮒﭡﭤﮚﭴﭨﭸﮘﮌﭑﮁﭑﭑﭹﭩﭴﭑﭩﭩﭡﮁﮁﭙﭑﭤﭫﭳﭐﭴﭛﮀﮈﭜ

**range** (0x2625-0x262C)  
>☪☪☪☪☪☪☪☪☨☥☪☪☪☪☨☥☪☪☥☪☪☪☥☪☪☪☥☪☬☬☬☬☫☩☥☪☥☪☥☫☥☥☪☨☬☩☬☫☩☥☥☦☥☫☫☫☦☪☪☪☪☪☪☪☦☦☪☪☪☦☥☥☦☬☫☦☬☦☪☪☪☦☫☫☫☫☫☫☦☫☫☫☫☫☫☫☫☦☥☥☪☦☥☪☪☦

**random** (uses the full range 0x0000 to 0x10FFFF of unicode characters, will likely result in many unprintable but still valid sequences)  
𴅰򥕈󈾈󨝈󗒠𝛠񙪐󁡮薛⹠񓢸񚪘񥫰󣑦񻛋򜤈򻋸񣕳񪻐񝠘򑍈𲋻󂭀󺰨񅵐󟶛𚒐򘇢񼕒򅫲򑺪󗃑󓌏󬺣ᐘ𛝫𤟈𖛳𪰁񧟻𗐛򀎠󸤶񢍲񭼟󞹊򤁙鹧𘟫󳖓񄽼􋥛󾙱󢁉𵋡󺼼򟎸𫧐𽶐𳛈󁠀埀𱨰򖡜󧬄󀘸󥁈𙶘񗭼𽴓𪳣񛓬򜐚򞖁􀯌𱴊󌌌𛚘𕫨𖑈茌񟣡󢓑𐵑𼌡𥴹󇢩󨱄򻓉􎷱񉭙􌚁󨸹񥟑󋞙󨅩򺴄򔆓񄩋񰆨򥿤󙥻򤆈񠄸򹟼

## Warning
Ranges 0xD800-0xDB7F and 0xDC00-0xDFFF are reserved for [Surrogates](https://en.wikipedia.org/wiki/Universal_Character_Set_characters#Surrogates) and ruin everything in this current implementation. Basic measures have been taken to avoid using them in the *--random* encoding but if you specify a custom range consisting of nothing but surrogates you're going to have a bad time. Adding input validation for this is on the to-do list, or you can do it yourself.

## Useful links
https://jrgraphix.net/r/Unicode/ is a great website for looking through much of the unicode character set and picking a custom range.  
https://copy.sh/brainfuck/text.html to generate a basic brainfuck program that will print your supplied string.  
https://copy.sh/brainfuck/ to run brainfuck code in your browser.
