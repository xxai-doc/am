<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

# xxAI.አርት

የድረ-ገጹ ኮድ ክፍል ክፍት ምንጭ ነው፣ ትርጉሙን ለማሻሻል ለማገዝ እንኳን ደህና መጡ።

## የፊት-መጨረሻ ኮድ

* [የፊት-መጨረሻ ኮድ](https://github.com/xxai-art/web)
* [የቋንቋ ጥቅል ለጣቢያው በአጠቃላይ](https://github.com/xxai-art/web/tree/main/i18n)
* [የቋንቋ ጥቅሎች ለመግቢያ ሞጁሎች](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [ድርጣቢያ ባለብዙ ቋንቋ ሰነዶች](https://github.com/xxai-doc)

የፊት-መጨረሻ የፕሮግራም አወጣጥ ቋንቋ [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) ነው, ይህም በቡና ስክሪፕት አገባብ ላይ በመመስረት አንዳንድ ባህሪያትን ይጨምራል, ይመልከቱ [./coffee_plus.md](./coffee_plus.md) .

## የድር ጣቢያዎች እና ሰነዶች አለምአቀፍ

በሚከተሉት 3 ፕሮጀክቶች ላይ ይገንቡ

* [@w5/ኤምዲቲ](https://www.npmjs.com/package/@w5/mdt)

  ቅጥያው `.mdt` ነው፣ ውጫዊ ፋይሎችን ለማመልከት ከ `<+ ./coffee_plus/import.js>` ጋር የሚመሳሰል አገባብ መጠቀም እና ከቅጥያ `.md` ጋር ማርክ ማመንጨት ይችላሉ።

* [@w5/trmd](https://www.npmjs.com/package/@w5/trmd)

  ምልክት ማድረጊያ ትርጉም ኮዶችን እና አገናኞችን አይተረጎምም እና የተተረጎሙ ዓረፍተ ነገሮችን ይሸፍናል። ትርጉሙ ከተቀየረ ነገር ግን ዋናው ጽሑፍ ካልተቀየረ, እንደገና ማስፈጸም የትርጉሙን ማሻሻያ አይተካውም.

* [@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

  `yaml` የተፈጠሩ ድር ጣቢያዎችን ለመተርጎም የቋንቋ ፋይሎች።

### የሰነድ ትርጉም አውቶሜሽን መመሪያዎች

ማከማቻ [xxai-art/doc](https://github.com/xxai-art/doc) ይመልከቱ

በመጀመሪያ nodejs, [direnv](https://direnv.net) እና [bun ን](https://github.com/oven-sh/bun) መጫን እና ከዚያ ወደ ዳይሬክተሩ ከገቡ በኋላ `direnv allow` ማስኬድ ይመከራል.

ከመጠን በላይ ትላልቅ መጋዘኖች በመቶዎች በሚቆጠሩ ቋንቋዎች የተተረጎሙ እንዳይሆኑ ለእያንዳንዱ ቋንቋ የተለየ ኮድ መጋዘን ፈጠርኩ እና ይህን መጋዘን የሚያከማችበት ድርጅት ፈጠርኩ.

የአካባቢ ተለዋዋጭ `GITHUB_ACCESS_TOKEN` ማቀናበር እና መፍጠር [.github.coffee ን](https://github.com/xxai-art/doc/blob/main/create.github.coffee) ማሄድ በራስ-ሰር መጋዘኑን ይፈጥራል።

እርግጥ ነው, በመጋዘን ውስጥ ማስቀመጥም ይችላሉ.

የትርጉም ስክሪፕት ማጣቀሻ [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

የስክሪፕት ኮድ እንደሚከተለው ይተረጎማል።

[bunx](https://bun.sh/docs/cli/bunx) የ npx ምትክ ነው፣ ይህም ፈጣን ነው። በእርግጥ ቡን ካልተጫኑ በምትኩ `npx` መጠቀም ይችላሉ።

`bunx mdt zh` `.mdt` በzh directory ውስጥ እንደ `.md` , ከታች ያሉትን 2 የተገናኙ ፋይሎች ይመልከቱ

* [ቡና_ፕላስ.ኤምዲቲ](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [ቡና_ፕላስ.ኤምዲ](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` ለትርጉም ዋናው ኮድ ነው ( `nodejs` ብቻ ከተጫኑ ግን `bun` እና `direnv` ካልተጫኑ ለመተርጎም `npx i18n` ማስኬድ ይችላሉ)።

[i18n.ymlን](https://github.com/xxai-art/doc/blob/main/i18n.yml) ይተነትናል፣ በዚህ ሰነድ ውስጥ የ `i18n.yml` ውቅር እንደሚከተለው ነው።

```
en:
zh: ja ko en
```

ትርጉሙ፡- የቻይንኛ ትርጉም ወደ ጃፓንኛ፣ ኮሪያኛ፣ እንግሊዝኛ፣ እንግሊዝኛ ወደ ሌሎች ቋንቋዎች ትርጉም ማለት ነው። ቻይንኛ እና እንግሊዝኛን ብቻ መደገፍ ከፈለጉ `zh: en` ብቻ መፃፍ ይችላሉ።

የመጨረሻው [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) ነው፣ ይህም በዋናው ርዕስ እና በእያንዳንዱ ቋንቋ የመጀመሪያ ንዑስ ርዕስ መካከል ያለውን ይዘት `README.md` በማውጣት `README.md` . ኮዱ በጣም ቀላል ነው, እራስዎ ሊመለከቱት ይችላሉ.

ጎግል ኤፒአይ ለነጻ ትርጉም ጥቅም ላይ ይውላል። ጎግልን መድረስ ካልቻልክ፣ እባክህ ፕሮክሲን አዋቅር እና አዘጋጅ፣ ለምሳሌ፡-

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

የትርጉም ስክሪፕቱ በ `.i18n` ማውጫ ውስጥ የትርጉም መሸጎጫ ያመነጫል፣ እባክዎ በ `git status` ያረጋግጡ እና ተደጋጋሚ ትርጉሞችን ለማስቀረት ወደ ኮድ ማከማቻ ያክሉት።
