---
title: 'О моратории ППК на новые возможности браузеров'
authors:
- bruce-lawson
intro: 'Разработчик ППК призывает к мораторию на новые возможности браузеров. Мы объясняем, почему не согласны.'
tags:
- offline
- service-workers
language: ru
translator: Ilya Streltsyn
source: http://css-live.ru/faq/o-moratorii-na-novye-brauzernye-funkcii-ppk.html
license: cc-by-3.0
---

Знаменитый разработчик и автор множества статей Питер Пол Кох (ППК) недавно призвал к «мораторию на новые возможности браузеров на год или около того». Если вы не читали его статью [«Хватит толкать веб вперед»](http://www.quirksmode.org/blog/archives/2015/07/stop_pushing_th.html) ([в переводе](http://css-live.ru/articles/xvatit-tolkat-veb-vpered.html)), просмотрите ее: он выдвигает интересные тезисы, как всегда.

(Нужно сказать сразу: мы все — большие поклонники таланта ППК: ему достались и [личные нападки](https://twitter.com/ppk/status/626849503321149440) за ту статью — мы собираемся возразить на его главный тезис, но мы по-прежнему замечательно относимся к нему и благодарим его за начало этого обсуждения).

Во многом мы, команда Opera по связям с разработчиками, разделяем его боль. Каждому из нас знакомо чувство, когда по возвращении из отпуска мы не можем понять беседы в Твиттере о спецификации, появившейся в тот недавний вечер, когда мы нежились у бассейна (покоряли сердца зажигательной бачатой, бродили по древним руинам, отрывались в Магалуфе, выражали смайликами-эмодзи в виде какашки своё сожаление об излишке съеденных накануне `U+2F364`) — зачеркните лишнее в зависимости от того, кто вы — Брюс, Шветанк, Матиас, Вадим или Андреас).

Всегда есть чему учиться, и веб-платформа становится всё сложнее. Даже Иэн Хиксон, редактор HTML5, [сказал](http://html5doctor.com/interview-with-ian-hickson-html-editor/):

> Платформа уже слишком сложна, чтобы один человек долго мог понимать ее полностью. Черт, да у веб-платформы есть части, в которые и я даже не пытался вникнуть — например, WebGL или IndexDB — и части, которые постоянно оказываются невероятно сложными для меня, несмотря на все мои старания их понять

…и это сказано два с половиной года назад!

Но не обязательно помнить все нюансы каждой спецификации. Нужно знать то, что можно, и иметь доступ к поисковику, чтобы находить нужные подробности в спецификациях или обучающих материалах. Многие ли из нас знают наизусть синтаксис CSS-градиентов, или помнят все тонкости синтаксиса Web Audio API? Но это не мешает нам пользоваться ими при необходимости.

Но главная жалоба ППК вовсе не на сложность:

> Нам надо бы сосредоточиться на сильных сторонах веба: простоте, ссылках и общедоступности. Машина инноваций на всех парах мчит не туда.

ППК приводит пример:

> Для меня спецификация для переходов между страницами олицетворяют всё то, что сегодня с браузерными функциями не так. Её задача — позволять плавно переходить с одной страницы на другую, вплоть до синхронизации анимаций на исходной и конечной страницах. <…> Мы годами обходились без этого. Что еще важнее, конечные пользователи годами обходились без этого и вполне привыкли к легкой задержке при загрузке новой страницы <…> Но зачем это понадобилось веб-разработчикам? Чтобы имитировать нативные приложения, конечно же. По-моему, этого недостаточно.

Но штука тут в том, что пользователи _хотят_ подобных штук, потому что уже привыкли к возможностям нативных приложений. И мы знаем, что потребителям нравятся возможности приложений — в апреле 2014-го специализирующаяся на мобильной аналитике фирма [Flurry сообщила](http://flurrymobile.tumblr.com/post/115191864580/apps-solidify-leadership-six-years-into-the-mobile):

> Приложения продолжают укреплять свои ведущие позиции и занимают 86% активности среднестатистического американского мобильного пользователя — или 2 часа 19 минут в день. Время, проводимое в мобильном вебе, продолжает сокращаться и в среднем составляет лишь 14% активности американского мобильного пользователя — или 22 минуты в день.

Многие из новых «фич», появляющихся в вебе, вроде [Service Worker](https://jakearchibald.com/2014/service-worker-first-draft/) или [устанавливаемые веб-приложения](https://dev.opera.com/blog/installable-web-apps/), призваны улучшать работу веба для конечных пользователей — улучшать по примеру нативных приложений, которые прежде не были доступны в вебе. Это победа.

Также, при всём уважении, мы не согласны с ППК, что добавление похожего на нативные приложения поведения и защита простоты, ссылок и общедоступности как фундаментальных ценностей веба однозначно противоречат друг другу.

Давайте рассмотрим эти фундаментальные ценности в обратном порядке:

## Общедоступность

Всё ближе момент, когда некоторые организации захотят поступиться доступностью веба, потому что хотят возможностей нативных приложений. Например, это уже делает Myntra — и планирует вот-вот сделать их родительская компания Flipkart; они отключили свой сайт для мобильников и убеждают людей пользоваться приложением (хотя сайтом по-прежнему можно пользоваться на компьютерах).

Служба Uber доступна только через приложение. Может быть, это имеет смысл, потому что API геолокации в вебе порой не слишком точен, а точное определение местоположения критически важно для службы вызова такси. Но это аргумент за улучшение API геолокации, а не за прекращение разработки.

Если мы замедлим разработку веба, мы рискуем, что нативные приложения отберут у нас еще больше сервисов, тем самым уменьшая общедоступные возможности веба.

## Ссылки

Если взять огромную кастрюлю и кипятить в ней веб все выходные напролет, периодически снимая пену из комментариев на YouTube, порнухи и фоточек мерзких котиков (тавтология?), то, заглянув под крышку в воскресенье вечером, вы найдете в остатке лишь ссылки, то есть URL (или URI, или URN… да какая разница?).

Это и называется «вебом», т.е. «паутиной», потому что это сеть, связывающая ресурсы воедино, и к каждому ресурсу можно обратиться по своему индивидуальному адресу.

Современные стандарты разрабатываются для сохранения ссылок. Взять, например, Service Worker — поясняющий документ для контроллера навигации (старое название того, что позже выросло в Service Worker) [говорит](https://github.com/sole/NavigationController/blob/master/explainer.md):

> Это вынуждает вас иметь ссылки! Некоторые современные платформы для приложений поступились этим фундаментальным принципом веба и страдают от этого. Веб никогда не должен повторять той же ошибки.

Аналогично, [спецификация Web Manifest](http://html5doctor.com/web-manifest-specification/) определяет начало и область видимости приложения в терминах старых добрых жизненно важных ссылок. Предложенная [спецификация перезаписи незащищенных запросов](https://w3c.github.io/webappsec/specs/upgrade/) пытается обеспечить непрерывность ссылок при переходе сервера на HTTPS, чтобы сделать пользование сайтом удобнее (безопаснее) для пользователя.

Веб много чему может научиться у нативных приложений (для этого не нужно рабски _имитировать_ их), но возможность ссылаться — это то, в чем нативным приложениям нужно имитировать веб. См. смахивающее на «заумную машину Голдберга» предложение [App Links](https://developers.facebook.com/docs/applinks) — вот как Facebook старается привнести «глубокую связность содержимого в ваше мобильное приложение». У нас есть ссылки; ППК прав, что нам нужно беречь их как зеницу ока, что современные стандарты и стараются делать.

## Простота

У современной веб-платформы есть и более глубинная сложность, чем просто количество функций. Это связано с тем, как писались спецификации, сколько времени заняло их написание, а также с тем фактом, что для некоторых возможностей, на которые мы полагаемся, вообще никогда не было спецификаций.

Один из примеров — парсинг HTML5. Годами разработчикам приходилось иметь дело с разными вариантами DOM, получавшимися в браузерах из невалидной разметки (которая, как мы знаем, составляет основную массу веба). Это допускалось, поскольку HTML 4 никогда не уточнял как быть с неправильной разметкой, так что браузеры были вольны делать что им угодно.

HTML5 это изменил, и теперь все браузеры, достойные пожатия угловой скобки, получают одну и ту же DOM вне зависимости от валидности разметки. Это дало колоссальное улучшение совместимости, что радует потребителей и сберегает мегатонны нервных клеток разработчикам.

Более свежий пример — `XMLHttpRequest`, формальное описание и стандарт для которого появились лишь спустя годы после того, как Microsoft его реализовал, а все остальные разобрали эту реализацию и скопировали ее.

XHR едва ли можно назвать красивым API, и его заменит [стандарт Fetch](https://fetch.spec.whatwg.org/), стремящийся упростить и привести к единому виду сетевые запросы. В его преамбуле сказано:

> Загрузка ресурса на высоком уровне — весьма простая операция. Приходит запрос, возвращается ответ. Но детали этой операции достаточно сложны, не были прежде подробно описаны и различаются между одним API и другим.

> Множество API позволяет загружать ресурсы, напр. элементы `img` и `script` в HTML, `cursor` и `list-style-image` в CSS, `navigator.sendBeacon()` и `self.importScripts()` в JavaScript. Стандарт Fetch предоставляет унифицированную архитектуру для таких функций, чтобы все они стали единообразны в том, что касается различных аспектов загрузки, например, редиректов и протокола CORS.

Все современные стандарты связаны с прояснением работы платформы для упрощения разработки и обеспечивают прочную, понятную основу, на которой можно строить всё.

Всё это строится на философии разработки под названием «Манифест расширяемого веба». Это практически необъятная тема, но глава общественной группы W3C по расширяемому вебу, Брайан Карделл, написал нам статью об этом под названием [«Секс, Гудини и расширяемый веб»](https://dev.opera.com/articles/houdini/).

## Безотлагательность

Центральный столп веба, который ППК не упомянул — то, что я называю «безотлагательностью». Если вы что-то поменяете на сайте, следующий посетитель сразу же получит обновленную версию. С нативными приложениями, которые нужно публиковать через App Store, пользователь лишь получит всплывающее уведомление, что есть свежая версия, и что при подключении к Wi-Fi приложение обновится. Может быть.

Устанавливаемые веб-приложения для пользователя выглядят как приложения: иконки на домашнем экране, потенциально работают даже без подключения к интернету, но сохраняют безотлагательность веба, поскольку само приложение хранится на сервере. Фактически, приложение на самом деле является — приготовьтесь — _сайтом_, с адресом, на который указывает иконка на домашнем экране. Мы объединяем преимущества веба с привычным видом и поведением нативного приложения.

## Заключение

Наши разработчики в Opera много трудятся над тем, чтобы обеспечить доступ к вебу людям, которым он иначе недоступен: [либо с Opera Mini](https://dev.opera.com/articles/making-sites-work-opera-mini/), либо путем [уменьшения потребления памяти в Chromium](https://dev.opera.com/blog/reducing-memory-use/), чтобы он работал даже на бюджетных устройствах, которыми пользуется большинство людей в мире.

Мы знаем, что [самые быстрорастущие рынки мобильных телефонов не пользуются приложениями](http://qz.com/466089/the-fastest-growing-mobile-phone-markets-barely-use-apps/), так что искусственно замедляя темп эволюции веба, мы обрекаем этих людей на онлайн-сервис второго сорта.

Мы считаем, что дальнейшее существование веба немыслимо без добавления новых функций — вроде Service Workers и устанавливаемых веб-приложений, в точности как мы добавили нативное видео, API аудио, элемент `<picture>`, API хранилищ — которые раздвигают границы возможного для веба и дают общедоступность, которой жаждет ППК и которая нужна нам.

Opera приветствует новых разработчиков, делающих веб лучше для пользователей. Мы — единственная разрабатывающая браузер компания, которая не пытается попутно продавать операционную систему или закрытое устройство. Поэтому для нас жизненно важно, чтобы веб и дальше рос и процветал, и мы полагаем, что это важно для всех.

_Это написал Брюс Лоусон, при содействии остальных участников команды Opera по связям с разработчиками. Не согласны? Пожалуйста, напишите свой собственный ответ и пришлите нам [в Твиттере](https://twitter.com/odevrel) ссылку!_

Другие высказывания по теме:

- Одновременно с нашей публикацией, евангелист Google Chrome Джейк Арчибальд опубликовал статью [«Если мы остановимся, мы двинемся вспять»](https://jakearchibald.com/2015/if-we-stand-still-we-go-backwards/) ([ее перевод](http://css-live.ru/articles/esli-my-ostanovimsya-my-dvinemsya-vspyat.html))
- Пол Кинлэн написал статью [«SLICE: the web»](https://paul.kinlan.me/slice-the-web/) о положительных аспектах веба как платформы для пользователей и разработчиков _(прим. перев.: SLICE — аббревиатура, которая обозначает безопасность, возможность ссылаться, индексируемость, возможность быстрой сборки из готовых частей и «эфемерность», т.е. способность не занимать ресурсы постоянно; по-русски, наверное, можно передать как «безопасный, линкуемый, индексируемый, компонуемый, исчезающий» — БЛИКИ)_;
- Николас Беваква написал статью [«Быстрая перемотка веб-платформы»](http://ponyfoo.com/articles/fast-forwarding-the-web-platform);
- Мариано Виола написал статью [«Мобильный веб не сломался… пока»](http://www.marianoviola.com/blog/mobile-web-isnt-broken-yet)
- [Размышления о браузерных новинках, функциональной совместимости, мастерстве и будущем веба](http://www.aaron-gustafson.com/notebook/ramblings-on-new-browser-features-interoperability-craft-and-the-future-of-the-web/) — взгляд на это Аарона Густафсона (Microsoft).