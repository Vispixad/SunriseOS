# SunriseOS
## Оборудование
1. ```/reboot``` - моментальная перезагрузка платы ESP32.
2. ```/reboot (ns, nm или nh)``` - перезагрузка черед определенное количество времени (n).
- s - секунд
- m - минут
- h - часов
3. ```/sleep``` - переход в режим сна.
4. ```/wkup``` - выход из режима сна.
## Аккаунты и пользователи
При первом включении системы будет автоматически создан аккаунт с правами **Administrator**, для дальнейших аккаунтов по стандарту будут права **Guest**.

5. ```/createacc``` - создание нового аккаунта.
6. ```/listacc``` - просмотр всех созданых ранее аккаунтов с указанием прав, названия и пароля (временно).
7. ```/rights (admin или guest) (название аккаунта)``` - выдача или изменение прав для конкретного аккаунта,
на выбор **Администратор** или **Гость**.
## Control-read оборудования
8. ```/команда1 $$ /команда2...``` - поочередное выполнения команд слева направо, количествои и скорость упирается в ограничения мощности вашей платы.
9. ```/rominfo``` - показ информации о занятой и свободной постоянной памяти устройства.
10. ```/raminfo``` - показ информации о занятой и свободной оперативной памяти устройства.
11. ```/boardinfo``` - отображение информации о частоте процессора, памяти **(ОЗУ, ПЗУ)** "по паспорту".
12. ```/maxperf``` - режим максимальной производительности, имеется ввиду работа ESP32 на максимальной частоте **(240 МГц)**.
13. ```/balperf``` - режим сбалансированной производительности, снижение частоты устройства до уровня **160 МГц**.
14. ```/enersav``` - режим экономии энергии, снижение частоты до **80 МГц** (ниже 80 не будут доступны **WI-FI** функции).
15. ```/uptime``` - отображение времени работы ESP32 с начала включения.
## Сеть
16. ```/checkwifi``` - простой тест качества соединения платы с роутером через **Wi-fi**.
17. ```/conninf``` - более глубокий тест сети, отображения IPv4, маски подсети, шлюза, MAC адреса, силы сигнала в dBm, SSID и BSSID, а также тип шифрования.
18. ```/listnwork``` - список доступных поблизости WI-FI сетей, а также отображение наличия пароля.
19. ```/connwork (название сети)``` - попытка подключения к выбранной сети, а также анализ защиты для ввода пароля при наличии.
20. ```/ping``` - тест скорости соединения с сайтом google.com.
21. ```/ping (example.com)``` - тест скорости соединения с выбранным вами сайтом.
## Файлы и папки
22. ```/checkfs``` - запускает проверку файлов данных пользователей и целостность файловой системы (SPIFFS).
23. ```/fs``` - просмотр всех доступных файлов на устройстве.
24. ```/makng (название файла)``` - создание текстового файла **(.txt)** с выбранным именем.
25. ```/dellfs (название файла)``` - удаление выбранного вами файла.
26. ```/rdfs (название файла)``` - чтение выбранного файла.
27. ```/rnmfs (старое название) (новое название)``` - переименование выбранного файла.
28. ```/rdction (название файла) (содержимое которое будет храниться)``` - редактирование содержимого выбранного файла **(перезапись содержимого полностью на новое).**
29. ```/conhtml (название файла.txt)``` - конвертация выбранного **.TXT** файла в **.HTML** файл. Выбирать файл только с расширением .**txt.**
30. ```/contxt (название файла.html)``` - конвертация выбранного **.HTML** файла в **.TXT** файл. Выбирать файл только с расширением .**html.**
31. ```/delfold (/название папки) или /delfold (/папка1/папка2...)``` - удаление выбранной папки в корневой директории или по выбранному пути.
32. ```/delfile (название файла.txt)``` - удаление выбранного файла в корневой директории или по выбранному пути.
