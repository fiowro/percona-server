.. rn:: 5.6.38-83.1

=============================
|Percona Server| 5.6.38-83.1
=============================

Percona is glad to announce the release of |Percona Server| 5.6.38-83.1 on
January 31th, 2018. Downloads are available `here
<http://www.percona.com/downloads/Percona-Server-5.6/Percona-Server-5.6.38-83.1/>`_
and from the :doc:`Percona Software Repositories </installation>`.

Based on `MySQL 5.6.38
<http://dev.mysql.com/doc/relnotes/mysql/5.6/en/news-5-6-38.html>`_, including
all the bug fixes in it, |Percona Server| 5.6.38-83.1 is now the current
stable release in the 5.6 series. All of |Percona|'s software is open-source
and free.

Bugs Fixed
==========

 With ``LIST`` table partitioning, incorrect handling of queries involving
 ``NULL`` was possible. (upstream :mysqlbug:`#76418`)

 With :variable:`innodb_large_prefix` set to ``1``, Blackhole storage engine
 was incompatible with InnoDB table definitions, thus adding new indexes would
 cause replication errors on the slave. Fixed :psbug:`1126` (upstream
 :mysqlbug:`53588`).

 Usage of the SHA2 function with non-ASCII values could cause incorrect
 results or even a server exit for some character sets.

 There was a problem with fulltext search, which could find a word with
 punctuation marks in natural language mode only, but not in boolean mode.
 Bug fixed :psbug:`85876` (upstream :mysqlbug:`85876`).

 |Percona Server| now uses *TraviCI* for additional tests.
 Bug fixed :psbug:`3777`.

Other bugs fixed: :psbug:`257` and :psbug:`1127`.
