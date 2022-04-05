# RTC_DS1302
Hardware RTC on DS1302 for RaspberryPi

Этот проект поможет иметь реальное время на платах Raspberry Pi, работающих в локальных сетях без сети Интернет. Необходимо правильно настроить часовой пояс в системе (sudo raspi-config, timezone)

Файл RTC_DS1302 - основной файл обмена с микросхемой RTC1302. В нем задаются ножки для связи.

Файл demo - для проверки записи в микросхему. Если она неподключена будут возвращены все нули/пустоты.

Файл set - записывает в микросхему текущее время Linux и временную метку об этом событии. Запускается вручную один раз при правильном системном времени.

Файл get - читает из микросхемы время и устанавливает его как системное в Linux. Необходимо прописать автозапуск в etc/rc/local.

Запуск только в Python2:

sudo python set.py - при установке вручную

sudo pytojn get.py - каждый раз при старте системы
