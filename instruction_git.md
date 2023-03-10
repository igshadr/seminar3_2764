# Инструкция по работе с системой контроля версий GIT

![Эмблема Git](git.jpg)

GIT- программа, которая фиксирует изменения в файлах. С помощью программы можно сравнивать, анализировать, редактировать, сливать изменения и возвращаться назад к последнемусохранению.это и есть контроль версий. Система контроля версий — программное обеспечение, которое обеспечивает командную работу в рамках одного или нескольких проектов.
## Иницилизация репозитория
Чтобы инициализировать новый репозиторий нужно ввести в терминале команду:

    git init

Это включит приложение и создат скрытую директорию .git, где будет храниться репозитария и настройки.

## Проверка состояния репозитория
Чтобы проверить текущее состояние репозитария вводим в терминале команду:

    git status

что показывает актуальность информации на нем, нет чего нового, что поменялось и т.д.

## Подготовка файлов
В git есть концепция области подготовленных файлов. Можно представить ее как холст, на который наносят изменения, которые нужны в коммите. Сперва он пустой, но затем мы добавляем на него файлы (или части файлов, или даже одиночные строчки). Это делаем набором в терминале команду:

     git add <название файла>

## Сохранение изменений
Для сохранения изменений, их необходимо закоммитить. Ввдим в терминале команду:

    git commit --m

Флажок -m задаст commit message - комментарий разработчика. Он необходим для описания закоммиченных изменений. 
    
## История изменений
Для просмотра все выполненных фиксаций можно воспользоваться историей коммитов. Она содержит сведения о каждом проведенном коммите проекта. Запросить ее можно при помощи команды в терминале:

    git log

В ней содержиться вся информация о каждом отдельном коммите, с указанием его хэша, автора, списка изменений и даты, когда они были сделаны.

Для просмотра изменений с выводом одного коммита в одну строку используется команда

    git log --oneline

Для просмотра всех имеющихся коммитов используется команда

    git log --all

Для просмотра лога с графическим изображением веток используется команда

    git log --graph

Все указанные флаги могут использоваться вместе:

    git log --all --oneline --graph

## Переключение между сохранениями
 Git позволяет вернуть выбранный файл к состоянию на момент определенного коммита. Для этого набираем в терминале команду:

    git checkout

Она также может быть использована для переключения между коммитами.

## Просмотр различий между изменениями
Для просмотра отличий между текущим состоянием репозитория и последним сохраненным изменением используется команда

    git diff
    
Можно также посмотреть разницу между любыми двуми коммитами. Для этого используется команда

    git diff <хэш1> <хэш2>

Чтобы переключиться на нужный коммит используется команда

    git checkout <хэш>

## Исправление коммита
Для более сложных исправлений, например, не в последнем коммите или если вы успели отправить изменения на сервер, нужно использовать вводим в терминале команду :
    
    git revert

Эта команда создаст коммит, отменяющий изменения, совершенные в коммите с заданным идентификатором.

## Работа с ветвями

Основной идеей ветвления является отклонение от основного кода и продолжение работы независимо от него. Под веткой принято понимать независимую последовательность коммитов в хронологическом порядке. 

Чтобы в Git добавить ветку мы используем:
    
    git branch <name of new branch>

Для перехода с основной (master) на другую ветку, в том числе только что созданную, необходимо написать checkout:
    
    git checkout <name of branch>

В каждой ветке можно вносить изменения в файл и создавать коммиты. Изменения в каждой ветке хранятся отдельно как отдельные версии. Для слияния всех версий необходимо перейти в master и выполнить для каждой дочерней ветки команду слияния
    
    git merge <name of merged branch>


## Заключение
 Вот и все! Наше руководство окончено. Я очень старался собрать всю самую важную информацию и изложить ее как можно более сжато и кратко.

 Git довольно сложен, и в нем есть еще много функций и трюков. Об этом можно почитать в полезных ссылках

