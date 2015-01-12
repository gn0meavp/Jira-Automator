**Предыстория**

Заметил, что за день часто захожу в Jira, чтобы посмотреть таску номер ХХХХ. Часто это бывает нужно в разговоре с кем-то по телефону или в джаббере. Типичные действия в данной ситуации - открыть браузер, начать вводить jir.. выбрать что-то похожее из выпадающего списка на ХХХХ, но имеющее номер ХХYY, стереть старый номер тикета до ХХ, ввести ХХХХ, нажать энтер.

Захотелось какой-то автоматизации. Желательно с горячими клавишами. Желательно, чтобы горячие клавиши были доступны отовсюду. Короче хотим чего-то такого (спойлер):

![alt tag](https://github.com/gn0meavp/Jira-Automator/blob/master/readme%20images/Screen%20Shot%202013-02-20%20at%202.59.26.png)


**Решение**

В Mac OS X есть замечательная вещь AppleScript, с помощью которого замечательное приложение Automator позволяет создавать системные сервисы, на которые можно вешать горячие клавиши.

В репозитории бандл, которые OS X определяет как сервис:

![alt tag](https://github.com/gn0meavp/Jira-Automator/blob/master/readme%20images/Screen%20Shot%202013-02-20%20at%202.31.45.png)

Первый будет использоваться для открытия тикетов в Jira, второй для открытия страниц в стаффе.

При клике на каждом файле, система предлагает его установить (в папку ~/Library/Services) или открыть в Automator. 

Откроем бандл в Automator и отредактируем первую строчку, чтобы открывался нужный нам проект. 

![alt tag](https://github.com/gn0meavp/Jira-Automator/blob/master/readme%20images/Screen%20Shot%202013-02-20%20at%202.39.33.png)

В примере имя проекта указано MOBDISK, меняем его на нужный нам и сохраняем (можно создать несколько таких сервисов под нужные нам проекты в Jira). 

![alt tag](https://github.com/gn0meavp/Jira-Automator/blob/master/readme%20images/Screen%20Shot%202013-02-20%20at%202.39.42.png)

Теперь сохраняем и ставим щелчком в файндере по бандлу:

![alt tag](https://github.com/gn0meavp/Jira-Automator/blob/master/readme%20images/Screen%20Shot%202013-02-20%20at%202.37.57.png)

Отлично! Осталось настроить горячие клавиши в системных настройках для наших сервисов. Для этого идём в System Preferences **>** Keyboard **>** Keyboard shortcuts:

![alt tag](https://github.com/gn0meavp/Jira-Automator/blob/master/readme%20images/Screen%20Shot%202013-02-20%20at%202.46.00.png) ![alt tag](https://github.com/gn0meavp/Jira-Automator/blob/master/readme%20images/Screen%20Shot%202013-02-20%20at%202.46.39.png)

В левом списке выбираем Services и прокручиваем в правом списке до General. Мы видим наши два сервиса, но они ещё без горячих клавиш. Можем настроить удобные сочетания для себя. Я настроил их как **Ctrl + ⌘ + J** для Jira и **Ctrl + ⌘ + U** (User) для Staff.

![alt tag](https://github.com/gn0meavp/Jira-Automator/blob/master/readme%20images/Screen%20Shot%202013-02-20%20at%202.50.27.png)

Ta-Daa! 
