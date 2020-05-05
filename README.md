<h2>Сборки debhelper для ubuntu 16.04 под архитектуру powerpc(ppc)</h2>
<p>ubuntu прекратила поддержку архитектуры powerpc(ppc) на версии ubuntu 16.04, однако это все еще хорошие машины для решения многих задач(например сбор данных zabbix)
Для сборки различных свежих пакетов часто требуется более новая версия debhelper которая официально в ubuntu 16.04 уже не обновляется.
Данный репозиторий содержит инструкции , а также готовые deb пакеты для установки</p> 

<h2>Для самостоятельной сборки</h2>
<p>Качаем исходники со страницы https://launchpad.net/ubuntu/+source/debhelper/10.2.2ubuntu1~ubuntu16.04.1
и https://launchpad.net/ubuntu/+source/dh-autoreconf/12~ubuntu16.04.1

Распаковываем архивы 
tar -xpf ./debhelper_10.2.2ubuntu1~ubuntu16.04.1.tar.xz
tar -xpf ./dh-autoreconf_12~ubuntu16.04.1.tar.xz

Ставим зависимости
po4a autoconf automake autopoint

и запускаем сборку
cd debhelper-xenial && debuild -us -uc
cd dh-autoreconf-xenial && debuild -us -uc</p> 



<h2>ДЛя установки готовых пакетов</h2>
<p>dpkg -i /path/dh-systemd_10.2.2ubuntu1~ubuntu16.04.1_all.deb
dpkg -i /path/dh-autoreconf_12~ubuntu16.04.1_all.deb
dpkg -i /path/debhelper_10.2.2ubuntu1~ubuntu16.04.1_all.deb</p>