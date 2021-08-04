---INSTALL---
1) Поместить исходный код модуля в рабочую папку
2) Установить зависимости используя pip3 install для каждой зависимости или pip3 install -r requirements.txt для установки всех зависимостей сразу

---DEPENDENCE---
 - pythonping
 - pysnmp
 - python-ubus

---USING---
1) Отредактировать файлы настроек pingconf, snmpconf

   
    config section '<value>' - ID опроса (любое название/id)

   
    option pollURL '<value>' - URL опроса в данном потоке (url - для ping, url:port - для snmp)
   
    option period '<value>' - период опроса в данном потоке
   
    option size '<value>' - размер пакета в данном потоке опроса (только для ping)
   
    option OID '<value>' - идентификатор объекта (только для snmp)
   
    option community '<value>' - пароль доступа (только для snmp)
   
    option timeout '<value>' - timeout (только для snmp)

2) Запустить файл testpinger.py
3) Завершение скрипта осуществляется нажатием "CTRL + C"
    Скрипт останавливается не мгновенно (не прерывается), а корректно останавливает все потоки
4) Проверить результат работы модуля можно в файле лога log.txt в папке модуля
