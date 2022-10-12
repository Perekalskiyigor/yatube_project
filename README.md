# yatube_project
 «Социальная сеть блогеров»
### Технологии
Python 3.7
Django 2.2.19
### Запуск проекта в dev-режиме
- Установите и активируйте виртуальное окружение:

 source venv/bin/activate
``` 
- В папке с файлом manage.py выполните команду:
```
python3 manage.py runserver
  
  после сделать git add, git commit -m 'с комментарием' и git push
  
### Настройка gitignore

Важно убедиться, что на GitHub не будут отправлены файлы и папки, которые не нужно отслеживать. Всё, что не нужно отправлять в Git, должно быть перечислено в файле .gitignore.
Что должно быть внесено в файл .gitignore в проекте Yatube:

-Файлы виртуального окружения. Их много, они тяжёлые, их проще установить через pip, чем гонять через Git(/venv).
-Служебные файлы IDE(/.vscode).

### Сохранение зависимостей
-Установите зависимости из файла requirements.txt
```
pip install -r requirements.txt

-В  linux есть ошибка которая добавляет в список лишнюю библиотеку pkg_resources==0.0.0. Эту строчку можно смело удалить и формировать файл с зависимостями такой командой: 

pip freeze | grep -v "pkg_resources" > requirements.txt)

-При развёртывании проекта на новой машине нужно из папки, содержащей requirements.txt, при активированном виртуальном окружении выполнить команду:

pip install -r requirements.txt

-после сделать git add, git commit -m 'с комментарием' и git push

### Создание первого приложения

-для создания преложения достаточно использовать в директории с manage.py. команду: 

python3 manage.py startapp <название файла> (другие команды для создания преложения: django-admin startapp <имя файла> или python3 -m django startapp <имя файла>)

При создании приложения в директории создаётся базовая структура файлов, которая, по мнению разработчиков Джанго, пригодится для любого приложения. Её можно дополнять и улучшать.

### Регистрируем приложение

-В каждом приложении автоматически создаётся файл apps.py, в нём описываются настройки приложения. В этом файле автоматически создаётся класс, конфигурирующий приложение; по умолчанию в нём создаётся лишь одно поле, name:

from django.apps import AppConfig

class IceCreamConfig(AppConfig):
    name = 'posts'

-Чтобы Django-проект узнал о том, что в нем есть приложение, нужно это приложение зарегистрировать: добавить его конфиг в список установленных приложений INSTALLED_APPS в файле settings.py:
# yatube/settings.py

INSTALLED_APPS = [
    'posts.apps.IceCreamConfig',  # Добавленная запись

###  Роутинг запросов в urls.py и проектирование структуры адресов








### Авторы
Перекальский Игорь 89667041010
