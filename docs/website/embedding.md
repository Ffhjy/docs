---
slug: /embedding
hide_table_of_contents: true
---

# Embedding

TurboWarp can be embedded with a standard iframe:

```html
<iframe src="https://turbowarp.org/414716080/embed" width="482" height="412" allowtransparency="true" frameborder="0" scrolling="no" allowfullscreen></iframe>
```

Replace `414716080` with the ID of your project. You can change the width and height of the iframe and the player will automatically resize to fit (482x412 will result in the stage rendering at an undistorted 480x360).

TurboWarp's embeds will have a transparent background if the iframe is allowed to be transparent. TurboWarp's embeds will have a fullscreen button if the iframe is allowed to become fullscreen. The example code above enables both of these feature.

## Unshared projects can't be embedded {#unshared-projects}

Unshared projects [can not be shown in embeds](unshared-projects). Make sure the projects you embed are shared or use the [TurboWarp Packager](https://packager.turbowarp.org/) instead.

## URL parameters {#url-parameters}

All [standard URL Parameters](url-parameters.md) are still available. You can use these to control usernames and other things.

There are also some special parameters only available in embeds:

### Autoplay {#autoplay}

Embeds support the `autoplay` parameter, which will automatically hit the green flag when the project loads. For example: https://turbowarp.org/15832807/embed?autoplay

Note that sound blocks may not work until the user interacts with the project (for example, by clicking). This is a restriction imposed by browsers. There is nothing TurboWarp can do to work around this.

### Settings button {#settings-button}

You can optionally enable a settings button in embeds with the `settings-button` parameter that opens a similar menu to the "Advanced settings" menu found in the website and editor. For example: https://turbowarp.org/15832807/embed?autoplay&settings-button

### Fullscreen background color {#fullscreen-background}

Outside of fullscreen mode, the embed is transparent so you can style the parent element if you want to change the background color.

In fullscreen mode, the embed will either use a white or an almost black color depending on whether the user's computer is configured to dark mode or not.

To override this behavior, set the `fullscreen-background` parameter to a CSS color value like `black` or `rgb(50,90,100)`. For example: https://turbowarp.org/15832807/embed?fullscreen-background=yellow

You can also use hex colors if you escape the `#` with percent encoding: `%23abc123`.

### Addons {#addons}

By default, embeds have no addons enabled. This can be overridden with the `addons` parameter, which is a comma separated list of addon IDs to enable. For example: https://turbowarp.org/15832807/embed?addons=pause,gamepad,mute-project

Useful addons and their IDs:

 - "Pause button" is `pause`
 - "Muted project player mode" is `mute-project`
 - "Remove curved stage border" is `remove-curved-stage-border`
 - "File drag and drop" is `drag-drop`
 - "Gamepad support" is `gamepad`
 - "Reverse order of project controls" is `editor-buttons-reverse-order`
 - "Clone counter" is `clones`

Other addons will have no effect on the embed.

## Security considerations {#security}

If you use user-supplied information to generate embed links, you should sanitize any arguments to make sure users can't supply arbitrary URL parameters as some can lead to unexpected behaviors.

## Need more control? {#packager}

Use the [TurboWarp Packager](https://packager.turbowarp.org/) for more control over the loading screen, accent colors, controls, and more. You can also [embed the output of the packager](/packager/embedding) very easily.

## Donations {#donations}

If you use a TurboWarp embed in a commercial website, it is in your best interest to [donate to us and the projects we rely upon](/donate) to ensure the embed continues to function smoothly. ❤️

## License {#license}

TurboWarp is licensed under the [GPLv3.0](https://github.com/TurboWarp/scratch-gui/blob/develop/LICENSE). We believe that an `<iframe>` of a GPLv3.0 work doesn't create a derivative work under the GPLv3.0, rather it creates an "aggregate work" which is not subject to the same requirements as derivative works. However, we are not lawyers and this is not legal advice. Talk to a lawyer if this matters to you.




русский

Замените "414716080" на идентификатор вашего проекта. Вы можете изменить ширину и высоту iframe, и проигрыватель автоматически изменит размер по размеру (482x412 приведет к рендерингу сцены с неискаженным разрешением 480x360).

Вставки TurboWarp будут иметь прозрачный фон, если iframe разрешено быть прозрачным. Вставки TurboWarp будут иметь полноэкранную кнопку, если iframe разрешено становиться полноэкранным. Приведенный выше пример кода включает обе эти функции.

## Неразделенные проекты не могут быть внедрены {#неразделенные проекты}

Неразделенные проекты [не могут отображаться во встроенных файлах] (неразделенные проекты). Убедитесь, что проекты, которые вы внедряете, являются общими, или вместо этого используйте [TurboWarp Packager](https://packager.turbowarp.org/).

## Параметры URL {#url-параметры}

Все [стандартные параметры URL](url-parameters.md) по-прежнему доступны. Вы можете использовать их для управления именами пользователей и другими вещами.

Также есть некоторые специальные параметры, доступные только во встроенных приложениях:

### Автозапуск {#автозапуск}

Встроенные модули поддерживают параметр `автозапуск`, который автоматически устанавливает зеленый флажок при загрузке проекта. Например: https://turbowarp.org/15832807/embed?autoplay

Обратите внимание, что звуковые блоки могут не работать до тех пор, пока пользователь не начнет взаимодействовать с проектом (например, щелкнув). Это ограничение, налагаемое браузерами. TurboWarp ничего не может сделать, чтобы обойти это.

### Кнопка настроек {#кнопка настроек}

Вы можете дополнительно включить кнопку настроек во встроенных приложениях с параметром "кнопка настроек", который открывает меню, аналогичное меню "Дополнительные настройки", которое можно найти на веб-сайте и в редакторе. Например: https://turbowarp.org/15832807/embed?autoplay&settings-button

### Цвет фона в полноэкранном режиме {#fullscreen-background}

За пределами полноэкранного режима вставка прозрачна, поэтому вы можете стилизовать родительский элемент, если хотите изменить цвет фона.

В полноэкранном режиме для встраивания будет использоваться либо белый, либо почти черный цвет, в зависимости от того, настроен ли компьютер пользователя на темный режим или нет.

Чтобы переопределить это поведение, установите для параметра "полноэкранный фон" значение цвета CSS, например "черный" или "rgb(50,90,100)". Например: https://turbowarp.org/15832807/embed?полноэкранный фон=желтый

Вы также можете использовать шестнадцатеричные цвета, если вы экранируете `#` с помощью процентной кодировки: `%23abc123`.

### Дополнения {#addons}

По умолчанию для встраиваний не включены дополнения. Это можно переопределить параметром `addons`, который представляет собой список идентификаторов включаемых дополнений, разделенных запятыми. Например: https://turbowarp.org/15832807/embed?addons=pause,gamepad,mute-project

Полезные дополнения и их идентификаторы:

 - "Кнопка паузы" - это "пауза"
 - "Отключенный режим проигрывателя проекта" - это "отключение звука в проекте"
 - "Удалить изогнутую границу сцены" - это "удалить изогнутую границу сцены"
 - "Перетаскивание файла" - это `перетаскивание`
 - "Поддержка геймпада" - это "геймпад"
 - "Обратный порядок элементов управления проектом" - это "редактор-кнопки-обратный порядок"
 - "Счетчик клонов" - это `клоны`

Другие дополнения никак не повлияют на встраивание.

## Соображения безопасности {#security}

Если вы используете предоставленную пользователем информацию для создания встраиваемых ссылок, вам следует очистить все аргументы, чтобы убедиться, что пользователи не могут указывать произвольные параметры URL, поскольку некоторые из них могут привести к неожиданному поведению.

## Нужно больше контроля? {#packager}

Используйте [TurboWarp Packager](https://packager.turbowarp.org/) для большего контроля над экраном загрузки, цветами акцентов, элементами управления и многим другим. Вы также можете [встроить выходные данные упаковщика](/packager/embedding) очень легко.

## Пожертвования {#пожертвования}

Если вы используете встраиваемый модуль TurboWarp на коммерческом веб-сайте, в ваших интересах [пожертвовать нам и проектам, на которые мы полагаемся] (/donate), чтобы обеспечить бесперебойную работу встраиваемого модуля. ❤️

## Лицензия {#лицензия}

TurboWarp лицензирован в соответствии с [GPLv3.0](https://github.com/TurboWarp/scratch-gui/blob/develop/LICENSE). Мы считаем, что "<iframe>" работы GPLv3.0 не создает производную работу в соответствии с GPLv3.0, скорее это создает "совокупную работу", которая не подпадает под те же требования, что и производные работы. Однако мы не юристы, и это не юридическая консультация. Поговорите с юристом, если это важно для вас.
