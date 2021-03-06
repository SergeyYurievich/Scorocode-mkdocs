## Общая информация

Серверный код – это скрипты на JavaScript, выполняемые на сервере с помощью движка Google V8. Разработанный серверный код выполняется по расписанию (плану) или одноразово по вызову через метод API.Для создания нового скрипта нажмите кнопку "Создать".

![Серверный код](../img/scripts.png)

![Серверный код](../img/scriptcreate.png)

Введите серверный код в отведенном для этого окне. Для сохранения введенного описания нажмите на ссылку «Сохранить». Для допуска запуска кода анонимному пользователю (без авторизации) установите соответствующий флаг на закладке «ACL». Для настройки плана запуска серверного кода перейдите на закладку «Запланировать запуск». Задайте опцию «Включить таймер» для выполнения созданного серверного кода по расписанию. Далее настройте расписание и укажите дату начала его действия.

![Серверный код](../img/scriptacl.png)

Возможны следующие варианты расписания:

* Единожды;
* Произвольно через заданное время (дни, часы, минуты);
* Ежедневно (по заданным дням недели и в заданное время);
* Ежемесячно (по заданным месяцам, дням месяца и в заданное время).

![Серверный код](../img/scriptschedule.png)

Серверный код запускается в отдельном контексте, и при запуске в нем доступны следующие объекты:

`pool` – произвольный объект, переданный при вызове метода выполнения скрипта через API, содержащий переданные данные.

## Поддержка NPM модулей

Для того чтобы подключить сторонние модули в вашем скрипте, необходимо описать все имеющиеся зависимости. Для этого перейдите в раздел Настройки приложения и выберите пункт NPM зависимости.

![Серверный код](../img/scriptacl.png)

В секции `dependencies` опишите все модули, которые вы собираетесь использовать, где свойство - это название модуля, а значение - необходимая версия (вы можете оставить значение версии пустым, в этом случае будет установлена последняя версия модуля).

Пример:

```
    {
        "dependencies": {
            "scorocode": ""
        }
    }
```
    
Использовать подключенный SDK Scorocode можно, подключив его в серверный код с помощью `var scorocode = require('scorocode')`