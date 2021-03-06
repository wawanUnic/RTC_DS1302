# RTC_DS1302
Hardware RTC on DS1302 for RaspberryPi

Гэты праект дапаможа мець рэальны час на поплатках Raspberry Pi, якія працуюць у лакальных сетках без сеткі Інтэрнэт. Неабходна правільна наладзіць гадзінны пояс у сістэме (sudo raspi-config, timezone)

Файл RTC_DS1302 - асноўны файл абмену з мікрасхемай RTC1302. У ім задаюцца ножкі для сувязі.

Файл demo - для праверкі запісу ў мікрасхему. Калі яна непадключаная будуць вернуты ўсе нулі/пустаты.

Файл set - запісвае ў мікрасхему бягучы час Linux і часавую пазнаку аб гэтай падзеі. Запускаецца ўручную адзін раз пры правільным сістэмным часе.

Файл get - чытае з мікрасхемы час і ўсталёўвае яго як сістэмнае ў Linux. Неабходна прапісаць аўтазапуск у etc/rc/local (sudo puthon ../home/pi/get_RTC.py).

Запуск толькі ў Python2:

sudo python set.py - пры ўсталёўцы ўручную трэба перыядычна выклікаць, каб у мікрасхеме таксама абнаўляўся час. Для пачатку ўсталяваць "сінхрон часу": sudo apt-get install ntpdate. Сінхранізаваць час: sudo ntpdate -u ntp.ubuntu.com. Упэўніцца ў правільнасці часу: date. Толькі потым выклікаць sudo python set.py

sudo pytojn get.py - кожны раз пры старце сістэмы

----------------------------------------------------------------------------------------------------

Цей проект допоможе мати реальний час на платах Raspberry Pi, що працюють у локальних мережах без Інтернету. Необхідно правильно налаштувати часовий пояс у системі (sudo raspi-config, timezone)

Файл RTC_DS1302 – основний файл обміну з мікросхемою RTC1302. У ньому задаються ніжки зв'язку.

Файл demo – для перевірки запису в мікросхему. Якщо вона не підключена, будуть повернуті всі нулі/порожнечі.

Файл set - записує в мікросхему поточний час Linux та тимчасову мітку про цю подію. Запускається вручну один раз за правильного системного часу.

Файл get - читає з мікросхеми час і встановлює його як системний Linux. Необхідно прописати автозапуск etc/rc/local (sudo puthon ../home/pi/get_RTC.py).

Запуск тільки в Python2:

sudo python set.py - при встановленні вручну потрібно періодично викликати, щоб у мікросхемі теж оновлювався час. Спершу встановити "синхрон часу": sudo apt-get install ntpdate. Синхронізувати час: sudo ntpdate -u ntp.ubuntu.com. Переконатись у правильності часу: date. Тільки потім викликати sudo python set.py

sudo pytojn get.py - щоразу при старті системи
