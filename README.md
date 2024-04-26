# lab01
лабораторная №1 по ТиМПу
выполнила Шишаева Елизавета ИУ8-223

1. Скачайте библиотеку boost с помощью утилиты wget. Адрес для скачивания
   https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz
```bash
$ wget https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz
```
```bash
Распознаётся sourceforge.net (sourceforge.net)… 104.18.12.149, 104.18.13.149, 2606:4700::6812:d95, ...
Подключение к sourceforge.net (sourceforge.net)|104.18.12.149|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 301 Moved Permanently
Адрес: https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz/ [переход]
--2024-04-24 19:19:43--  https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz/
Повторное использование соединения с sourceforge.net:443.
HTTP-запрос отправлен. Ожидание ответа… 301 Moved Permanently
Адрес: https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz/download [переход]
--2024-04-24 19:19:43--  https://sourceforge.net/projects/boost/files/boost/1.69.0/boost_1_69_0.tar.gz/download
Повторное использование соединения с sourceforge.net:443.
HTTP-запрос отправлен. Ожидание ответа… 302 Found
Адрес: https://downloads.sourceforge.net/project/boost/boost/1.69.0/boost_1_69_0.tar.gz?ts=gAAAAABmKTEf_6t2xddwBFO6N4tMmgSUHVzvGvSul7K4K-RvO_HWRnFykDdLZRB17e9L-4bPQcW1OGH4pwoeZ6grLS4Kk3tAiA%3D%3D&use_mirror=kumisystems&r= [переход]
--2024-04-24 19:19:43--  https://downloads.sourceforge.net/project/boost/boost/1.69.0/boost_1_69_0.tar.gz?ts=gAAAAABmKTEf_6t2xddwBFO6N4tMmgSUHVzvGvSul7K4K-RvO_HWRnFykDdLZRB17e9L-4bPQcW1OGH4pwoeZ6grLS4Kk3tAiA%3D%3D&use_mirror=kumisystems&r=
Распознаётся downloads.sourceforge.net (downloads.sourceforge.net)… 204.68.111.105
Подключение к downloads.sourceforge.net (downloads.sourceforge.net)|204.68.111.105|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 302 Found
Адрес: https://kumisystems.dl.sourceforge.net/project/boost/boost/1.69.0/boost_1_69_0.tar.gz?viasf=1 [переход]
--2024-04-24 19:19:44--  https://kumisystems.dl.sourceforge.net/project/boost/boost/1.69.0/boost_1_69_0.tar.gz?viasf=1
Распознаётся kumisystems.dl.sourceforge.net (kumisystems.dl.sourceforge.net)… 148.251.120.111, 2a01:4f8:210:1057::2
Подключение к kumisystems.dl.sourceforge.net (kumisystems.dl.sourceforge.net)|148.251.120.111|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 302 Moved Temporarily
Адрес: https://downloads.sourceforge.net/project/boost/boost/1.69.0/boost_1_69_0.tar.gz?download&failedmirror=kumisystems.dl.sourceforge.net [переход]
--2024-04-24 19:19:45--  https://downloads.sourceforge.net/project/boost/boost/1.69.0/boost_1_69_0.tar.gz?download&failedmirror=kumisystems.dl.sourceforge.net
Подключение к downloads.sourceforge.net (downloads.sourceforge.net)|204.68.111.105|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 302 Found
Адрес: https://deac-ams.dl.sourceforge.net/project/boost/boost/1.69.0/boost_1_69_0.tar.gz?viasf=1 [переход]
--2024-04-24 19:19:46--  https://deac-ams.dl.sourceforge.net/project/boost/boost/1.69.0/boost_1_69_0.tar.gz?viasf=1
Распознаётся deac-ams.dl.sourceforge.net (deac-ams.dl.sourceforge.net)… 185.34.27.55
Подключение к deac-ams.dl.sourceforge.net (deac-ams.dl.sourceforge.net)|185.34.27.55|:443... соединение установлено.
HTTP-запрос отправлен. Ожидание ответа… 200 OK
Длина: 111710205 (107M) [application/x-gzip]
Сохранение в: ‘boost_1_69_0.tar.gz’

boost_1_69_0.tar.gz 100%[===================>] 106,53M   256KB/s    за 3m 57s  

2024-04-24 19:23:43 (461 KB/s) - ‘boost_1_69_0.tar.gz’ сохранён [111710205/111710205]
```
2. Разархивируйте скаченный файл в директорию ~/boost_1_69_0
```bash
$ tar -xf boost_1_69_0.tar.gz -C ~/
```
3. Подсчитайте количество файлов в директории ~/boost_1_69_0 не включая вложенные директории.
```bash
$ find ~/boost_1_69_0 -maxdepth 1 -type f | wc -l
```
```bash
12
```
4. Подсчитайте количество файлов в директории ~/boost_1_69_0 включая вложенные директории.
```bash
$ find ~/boost_1_69_0 -type f | wc -l
```
```bash
 61191
```
5. Подсчитайте количество заголовочных файлов, файлов с расширением .cpp, сколько остальных файлов (не заголовочных и не .cpp).
```bash
$ find ~/boost_1_69_0 -type f -iname "*.hpp" | wc -l
```
```bash
14912
```
```bash
$ find ~/boost_1_69_0 -type f -iname "*.cpp" | wc -l
```
```bash
13774
```
```bash
$ find ~/boost_1_69_0 -type f ! -name "*.hpp" ! -name "*.cpp" | wc -l
```
```bash
32505
```
6. Найдите полный путь до файла any.hpp внутри библиотеки boost.
```bash
$ find ~/boost_1_69_0 -type f -name "any.hpp"
```
```bash
/home/kaworu/boost_1_69_0/boost/proto/detail/any.hpp
/home/kaworu/boost_1_69_0/boost/hana/any.hpp
/home/kaworu/boost_1_69_0/boost/hana/fwd/any.hpp
/home/kaworu/boost_1_69_0/boost/xpressive/detail/utility/any.hpp
/home/kaworu/boost_1_69_0/boost/any.hpp
/home/kaworu/boost_1_69_0/boost/fusion/include/any.hpp
/home/kaworu/boost_1_69_0/boost/fusion/algorithm/query/any.hpp
/home/kaworu/boost_1_69_0/boost/fusion/algorithm/query/detail/any.hpp
/home/kaworu/boost_1_69_0/boost/spirit/home/support/algorithm/any.hpp
/home/kaworu/boost_1_69_0/boost/type_erasure/any.hpp
```
7.Выведите в консоль все файлы, где упоминается последовательность boost::asio.
```bash
$ grep -r "boost::asio" ~/boost_1_69_0 > ~/boost_1_69_0_files_with_boost_asio.txt
```
этот файл - [boost_1_69_0_files_with_boost_asio.txt](https://github.com/kaworururur/lab01/blob/main/boost_1_69_0_files_with_boost_asio.txt)

8. Скомпилирутйе *boost*.
```bash
$ ./bootstrap.sh --prefix=boost_output
```
```bash
Building Boost.Build engine with toolset gcc... tools/build/src/engine/bin.linuxx86_64/b2
Unicode/ICU support for Boost.Regex?... not found.
Backing up existing Boost.Build configuration in project-config.jam.2
Generating Boost.Build configuration in project-config.jam...

Bootstrapping is done. To build, run:

    ./b2
    
To adjust configuration, edit 'project-config.jam'.
Further information:

   - Command line help:
     ./b2 --help
     
   - Getting started guide: 
     http://www.boost.org/more/getting_started/unix-variants.html
     
   - Boost.Build documentation:
     http://www.boost.org/build/doc/html/index.html
```
```bash
$ ./bootstrap.sh --prefix=boost_output --with-icu= 
```
```bash
Building Boost.Build engine with toolset gcc... tools/build/src/engine/bin.linuxx86_64/b2
Unicode/ICU support for Boost.Regex?... not found.
Backing up existing Boost.Build configuration in project-config.jam.3
Generating Boost.Build configuration in project-config.jam...

Bootstrapping is done. To build, run:

    ./b2
    
To adjust configuration, edit 'project-config.jam'.
Further information:

   - Command line help:
     ./b2 --help
     
   - Getting started guide: 
     http://www.boost.org/more/getting_started/unix-variants.html
     
   - Boost.Build documentation:
     http://www.boost.org/build/doc/html/index.html
```
```bash
$ ./b2 install >> logs.txt
```
logs
