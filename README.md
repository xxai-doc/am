<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

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

እሱ [i18n.yml](https://github.com/xxai-art/doc/blob/main/i18n.yml) ይተነትናል፣ `i18n.yml` እንደሚከተለው ተዋቅሯል።

en:

zh: ja ko en

`bunx i18n` ለትርጉም ዋናው ኮድ ነው ( `nodejs` ብቻ ከተጫኑ ግን `bun` እና `direnv` ካልተጫኑ ለመተርጎም `npx i18n` ማስኬድ ይችላሉ)።

እሱ [i18n.yml](https://github.com/xxai-art/doc/blob/main/i18n.yml) ይተነትናል፣ `i18n.yml` እንደሚከተለው ተዋቅሯል።



en:

zh: ja ko en

* [ቡና_ፕላስ.ኤምዲ](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` ለትርጉም ዋናው ኮድ ነው ( `nodejs` ብቻ ከተጫኑ ግን `bun` እና `direnv` ካልተጫኑ ለመተርጎም `npx i18n` ማስኬድ ይችላሉ)።

እሱ [i18n.yml](https://github.com/xxai-art/doc/blob/main/i18n.yml) ይተነትናል፣ `i18n.yml` እንደሚከተለው ተዋቅሯል።

en:
zh: ja ko en

`bunx i18n` ለትርጉም ዋናው ኮድ ነው ( `nodejs` ብቻ ከተጫኑ ግን `bun` እና `direnv` ካልተጫኑ ለመተርጎም `npx i18n` ማስኬድ ይችላሉ)።

[i18n.ymlን](https://github.com/xxai-art/doc/blob/main/i18n.yml) ይተነትናል፣ በዚህ ሰነድ ውስጥ የ `i18n.yml` ውቅር እንደሚከተለው ነው።


en:
zh: ja ko en
```

它的含义是 :

中文翻译为日文、韩文、英文，英文翻译为其他所有语种。如果你只想支持中文、英文，可以只写 `zh: en`。

最后是 [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee)，它是提取每个语种 `README.md` 大标题 和 第一个子标题 之间的内容，来生成一个入口的 `README.md` 。代码很简单，可以自己看一下。

最后，因为用到了谷歌 API 来免费翻译，所以如果你不能访问谷歌，请配置并设置代理，比如 :

```
ወደ ውጪ መላክ https://127.0.0.1:7890 http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890