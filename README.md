#Направленность:
##Кодинг .net под Mono, весёлое безумие.

#Что сервис делает?
##1. Принимает и хранит клиентские данные
##2. Выдаёт клиентские данные по запросу
##3. Принимает клиентский .cs код и компилирует его в .exe (mono)
##4. Выполняет скомпилированный .exe и отправляет клиенту результаты консольного вывода
#Примечания:
Результаты работы исполняемого файла заменяют содержимое файла данных клиента.

#Взаимодействие клиента и сервера
##1. Клиент посылает свой открытый ключ
##2. Сервер посылает свой открытый ключ
### На основании открытых ключей вырабатывается общий сеансовый ключ, на котором и ведётся дальшейшее взаимодействие
### Далее весь обмен клмандами данными ведется только в зашифрованном виде
##3. Клиент посылает команду
##4. Клиент посылает данные [не обязательно]
##5. Сервер отправляет данные [не обязательно]

# Особенности работы сервиса
##1. Открытый ключ клиента выступает в роли его идентификатора
##2. Для каждого клиента создаётся каталог согласно его идентификатору
##3. В клиентском каталоге хранятся: файл с сеансовым ключом клиента, данные клиента в зашифрованном виде, исполняемый файл программы клиента.

#Как с этим жить?
##1. Народ, этот сервис запускает клиентский .cs код. Этого уже достаточно, дальше догадайтесь сами.
##2. Есть детская проверка на рута, ну чисто ради поржать и усугубить предыдущий пункт. Лол над теми, кто так и запустит.

#Что же делать?
##1. Получился почти dummy. Участникам придётся читать и писать на шарпе, что и требовалось. Ну и плюс я не планирую давать какой-либо клиент, так что участникам волей-неволей придётся продраться через дебри говнокода, чтобы разобраться в том, что и как шифровать и куда отправлять свой код. Т.е. в итоге сервис больше для развлечения, чем для глубокого мыслинга.
##2. Дополнительно  - участники не получат исходного кода. В случае и .net это не имеет никакого практического значения.