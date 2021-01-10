<h2>Сборки debhelper для ubuntu 16.04 под архитектуру powerpc(ppc)</h2>
<p>ubuntu прекратила поддержку архитектуры powerpc(ppc) на версии ubuntu 16.04, однако это все еще хорошие машины для решения многих задач(например сбор данных zabbix)
Для сборки различных свежих пакетов часто требуется более новая версия debhelper которая официально в ubuntu 16.04 уже не обновляется.
Данный репозиторий содержит инструкции , а также готовые deb пакеты для установки</p> 

<h2>Для самостоятельной сборки</h2>
<p>Качаем исходники со страницы https://launchpad.net/ubuntu/+source/debhelper/12.10ubuntu1
и https://launchpad.net/ubuntu/+source/dh-autoreconf/17

Распаковываем архивы 
tar -xpf ./debhelper_12.10ubuntu1.tar.xz
tar -xpf ./dh-autoreconf_17.tar.xz

Накладываем заплатки
patch -p1 < ppc_debhelper-12.10ubuntu1.patch
patch -p1 < ppc_dh-autoreconf-17.patch

и запускаем сборку
cd debhelper-12.10ubuntu1 && debuild -us -uc
cd dh-autoreconf-17 && debuild -us -uc</p> 



<h2>ДЛя установки готовых пакетов</h2>
<p>dpkg -i /path/dh-systemd_12.10ubuntu1_all.deb
dpkg -i /path/dh-autoreconf_17_all.deb
dpkg -i /path/libdebhelper-perl_12.10ubuntu1_all.deb
dpkg -i /path/debhelper_12.10ubuntu1_all.deb</p>