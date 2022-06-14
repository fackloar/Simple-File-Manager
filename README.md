# File-Manager
###### Простой файловый менеджер.
Умеет: 
- Копировать 
- Удалять 
- Получать информацию о файлах и папках  

Выводит каталог файлов постранично, длинну страницы можно изменить в файле .config.  

![Capture](https://user-images.githubusercontent.com/77644644/115735352-156e4400-a393-11eb-8766-5f7f8793f509.PNG)

### Алгоритм работы
Работает через коммандную строку, в которой принимает команды пользователя и аргументы к ним.  
Доступные команды:  
#### Help  
Выводит все доступные команды и подсказку как их использовать.  
#### GoTo  
Переходит по заданому пути (например `goto C:\Program Files\Example`), либо по названию папки в текущем открытом каталоге (например `goto Example` если открыт каталог C:\Program Files\).  
#### Copy  
Копирует файл в файл или папку в папку. Копирование папок реализованно рекурсивно, что позволяет скопировать также все подпапки. Принимает в качестве аргумента строку "path to path" (например `copy C:\Program Files\Example to C:\Program Files\CopyCatalogue\`). Как и команда GoTo, умеет принимать в качестве копируемого файла или папки только название, если оно находится в открытом каталоге (например `copy Example to C:\Program Files\CopyCatalogue\`). При копировании файла нужно обязательно указать имя нового или существующего файла.  
#### Delete 
Удаляет файл или папку, при вводе пути или названия из активного каталога, как и предыдущие команды (например `delete C:\Program Files\Example` или `delete Example`).  
#### Info
Выводи на экран размер файла, либо размер и количество файлов и подпапок если запрашивается информация о каталоге.
#### Up
Переходит на уровень "выше" в дереве каталогов.  
#### Page  
Так как вывод проводится постранично, с помощью этой команды можно перемещаться между страниц.
#### Exit
Завершает программу.
