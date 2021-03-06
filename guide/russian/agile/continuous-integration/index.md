---
title: Continuous Integration
localeTitle: Непрерывная интеграция
---
## Непрерывная интеграция

В своей основной, непрерывной интеграции (CI) - гибкая методология разработки, в которой разработчики регулярно объединяют свой код непосредственно в основной источник, обычно с удаленной `master` ветвью. Для обеспечения того, чтобы никаких изменений нарушения не было введено, полный тестовый пакет запускается на каждой потенциальной сборке для регрессионного тестирования нового кода, т. Е. Тестирует, что новый код не нарушает существующие рабочие функции.

Такой подход требует хорошей проверки базы кода, что означает, что большинство, если не все, кода имеют тесты, которые гарантируют, что его функции полностью функциональны. В идеале непрерывная интеграция будет практиковаться вместе с полным [испытательным развитием](https://guide.freecodecamp.org/agile/test-driven-development) .

### Основные этапы

Следующие основные шаги необходимы для выполнения наиболее стандартного текущего подхода к непрерывной интеграции.

1.  Поддерживайте центральное репо и активную `master` ветвь.

Должен быть репозиторий кода для каждого, чтобы объединиться и извлечь изменения. Это может быть на Github или на любое количество служб хранения кода.

2.  Автоматизация сборки.

Используя сценарии NPM или более сложные инструменты построения, такие как Yarn, Grunt, Webpack или [Gulp](https://guide.freecodecamp.org/developer-tools/gulp) , автоматизируйте сборку, чтобы одна команда могла создать полностью функциональную версию продукта, готовую к развертыванию в рабочей среде. Еще лучше, включите развертывание как часть автоматической сборки!

3.  Сделайте сборку всех тестов.

Чтобы проверить, что ничто в новом коде не нарушает существующие функции, необходимо запустить полный набор тестов, и сборка должна завершиться неудачей, если какие-либо тесты в ней не удались.

4.  Каждый человек должен каждый день сминать изменения в `master` .
    
5.  Каждое слияние с `master` должно быть построено и полностью протестировано.
    

### Лучшие практики

Существуют и другие передовые методы, которые наилучшим образом используют то, что предлагает CI, и проблемы, которые он представляет, например:

1.  Храните сборку быстро, так что много времени на разработку не тратится впустую, ожидая сборки.
    
2.  Протестируйте сборку в полном клоне производственной среды.
    

Если у вас есть, например, приложение, развернутое на чем-то вроде Heroku или Digital Ocean, есть отдельное тестовое развертывание там, где вы можете развернуть тестовые сборки, чтобы убедиться, что они работают не только в тестах, но и в реальной производственной среде. Эта тестовая среда должна быть функционально идентична реальной производственной среде, чтобы обеспечить точность теста.

3.  Успокойтесь, чтобы оставаться в курсе последних событий.

Кодеры должны регулярно вытаскивать из `master` ветки, чтобы продолжать интегрировать свой код с изменениями из своей команды. Репо также должно предоставляться заинтересованным сторонам, таким как менеджеры по продуктам, руководители компаний или иногда ключевые клиенты, чтобы каждый мог легко видеть прогресс.

4.  Сохраняйте записи сборок, чтобы каждый мог видеть результаты любой сборки, независимо от того, удалось ли это или не удалось, и кто или что вносило новые изменения.
    
5.  Автоматизация развертывания.
    

Постоянно обновляйте приложение с любыми новыми изменениями, автоматизируя развертывание в производственной среде как завершающий этап процесса сборки, как только все тесты пройдут, и тестовое развертывание в клоне производственной среды преуспело.

### Услуги CI

Множество служб существует для обработки процесса непрерывной интеграции для вас, что упрощает создание сплошного конвейера CI или процесс сборки. Оценивая их, учитывайте такие факторы, как бюджет, скорость сборки и какой проект вы работаете. Некоторые сервисы, такие как [Travis CI,](https://travis-ci.org) предлагают бесплатные услуги для проектов с открытым исходным кодом, которые могут сделать их легким выбором для таких проектов, но у них могут быть более медленные сборки, чем другие сервисы, такие как [Circle CI](https://circleci.com/) или [Codeship](https://codeship.com/) , и это лишь некоторые из них.

#### Дополнительная информация:

Статья в Википедии о [непрерывной интеграции](https://en.wikipedia.org/wiki/Continuous_integration) .