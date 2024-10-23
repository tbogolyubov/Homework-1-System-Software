# 1 Выбор приложения
Для выполнения домашних работ был выбран проект под названием Caddy – это современный веб-сервер, написанный на языке Go. Ссылка на репозиторий: https://github.com/caddyserver/caddy.
В основной функционал Caddy входит:
1. Работа в качестве HTTP/HTTPS сервера для обслуживания веб-страниц и приложений;
2. Работа в качестве реверс-прокси, принимая запросы от клиентов и перенаправляя их на другие серверы, что может быть полезно для балансировки нагрузки или для маршрутизации запросов к микросервисам;
3. Caddy также может обслуживать статические файлы (HTML, CSS, JavaScript, изображения и видео);
4. Caddy позволяет настраивать сервер с помощью конфигурационных файлов или через API.

Caddy достаточно прост в использовании: легко настраивается и запускается, при этом он обеспечивает достаточную безопасность, так как включена автоматическая поддержка HTTPS.

# 2 Запуск приложения с помощью WSL

Запустим сервер Caddy с помощью WSL – подсистемой Windows для Linux.  Для этого сначала установим среду Ubuntu 24.04.1 LTS с помощью WSL. 
Найдем инструкцию по сборке сервера из исходного кода в файле README репозитория. Для запуска нужно сначала клонировать репозиторий:
git clone "https://github.com/caddyserver/caddy.git"

Далее вводим команду для изменения рабочего каталога (Change Directory) на указанный путь:
cd caddy/cmd/caddy/

Вводим команду, используемую в языке программирования Go для компиляции исходного кода в исполняемый бинарный файл:
go build

С помощью следующей команды запустим исполняемый файл Caddy:
./caddy

На экран будет выведена справочная информация о Caddy с несколькими разделами: