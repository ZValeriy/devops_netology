# Выполнение ДЗ
* Найдите полный хеш и комментарий коммита, хеш которого начинается на aefea.
    * Ответ: aefead2207ef7e2aa5dc81a34aedf0cad4c32545
    * Как получил: git rev-parse aefea
* Какому тегу соответствует коммит 85024d3?
    * Ответ: v0.12.23
    * Как получил: git tag --contains 85024d3 и взял самый свежий :)
* Сколько родителей у коммита b8d720? Напишите их хеши.
    * Ответ: Два. 56cd7859e0 и 9ea88f22fc
    * Как получил: git log -1 b8d720
* Перечислите хеши и комментарии всех коммитов которые были сделаны между тегами v0.12.23 и v0.12.24.
    * Ответ: b14b74c4939dcab573326f4e3ee2a62e23e12f89 [Website] vmc provider links
3f235065b9347a758efadc92295b540ee0a5e26e Update CHANGELOG.md
6ae64e247b332925b872447e9ce869657281c2bf registry: Fix panic when server is unreachable
5c619ca1baf2e21a155fcdb4c264cc9e24a2a353 website: Remove links to the getting started guide's old location
06275647e2b53d97d4f0a19a0fec11f6d69820b5 Update CHANGELOG.md
d5f9411f5108260320064349b757f55c09bc4b80 command: Fix bug when using terraform login on Windows
4b6d06cc5dcb78af637bbb19c198faff37a066ed Update CHANGELOG.md
dd01a35078f040ca984cdd349f18d0b67e486c35 Update CHANGELOG.md
225466bc3e5f35baa5d07197bbc079345b77525e Cleanup after v0.12.23 release
    * Как получил: git log --pretty=oneline v0.12.23...v0.12.24
* Найдите коммит в котором была создана функция func providerSource, ее определение в коде выглядит так func providerSource(...) (вместо троеточия перечислены аргументы).
    * Ответ: 8c928e83589d90a031f811fae52a81be7153e82f
    * Как получил: git grep -p 'func providerSource(' и git log -L :providerSource:provider_source.go 
* Найдите все коммиты в которых была изменена функция globalPluginDirs.
    * Ответ: 
        8364383c35
        66ebff90cd
        41ab0aef7a
        52dbf94834
        78b1220558
    * Как получил: git grep -p 'globalPluginDirs' и git log -L :globalPluginDirs:plugins.go

* Кто автор функции synchronizedWriters?
    * Ответ: Martin Atkins <mart@degeneration.co.uk>
    * Как получил: git log -SsynchronizedWriters