# Ewidencja �rodk�w trwa�ych

Aplikacja do ewidencji �rodk�w trwa�ych umo�liwia wprowadzanie oraz edycj� �rodk�w trwa�ych oraz mo�liwo�� przypisania sprz�tu do pracownik�w oraz lokalizacji co u�atwia zarz�dzanie tym sprz�tem.
System sk�ada si� z dwych modu�ow www oraz aplikacji mobilnej. Interfejs www umo�liwia wprowadzanie danych do bazy oraz zarz�danie nimi natomiast aplikacja mobilna s�u�y do tworzenia powi�za� pracownika z pomieszczeniami i sprz�tem.
Dane pomi�dzy tymi 2 modu�ami wymieniane s� za pomoca synchronizatora danych Mobeelizer.

![Model systemu.](EwidencjaSrodkowTrwalych/raw/master/model.png)

#�rodowisko pracy

* baza danych MySql
* serwer aplikacyjny jBoss 6.1.0
* eclipse indigo
* android sdk 2.2 

# Uruchomienie aplikacji www

1. Utw�rz baz� danych na serwerze MySql (np. CREATE DATABASE ewidencja;)
2. Uruchom skrypty SQL w utworzonej bazie danych
 * www/ddl.sql.txt
 * www/reports_ddl.sql.txt
3. Zmie� ustawienia pliku dost�pu do �r�d�a danych - www/EwidServerAdmin-ear/resources/EwidServerAdmin-ds.xml tak aby wskazywa� na Twoj� baz� danych.
4. Skopiuj skonfigurowany plik do folderu deploy serwera jBoss.
5. Zaimportuj projekty z katalogu www do �rodowiska pracy eclips'a.
6. Uruchom serwer jBosss u�ywaj�c perspektywy Java EE i okna Servers. 
7. Uruchom projekty na serwerze klikaj�c prawym przyciskiem i wybieraj�� Run>Run on Server lub dodaj�c je do serwera w oknie Servers.
8. Aplikacja zostanie uruchomiona na porcie 8080.

# Uruchomienie aplikacji android

1. Zaimportuj projekt z katalogu AndroidApp do eclipsa.
2. Uruchom projekt w emulatorze lub zbuduj go i zainstaluj na telefonie. (Pami�taj �e aplikacja wymaga sdk w wersji minimum 2.2 oraz �e emulator musi by� skonfigurowany tak aby mia� dost�p do internetu oraz zewnetrznej pami�ci)

# Uruchomienie synchronizacji

Do synchronizacji danych serwera z Mobeelizerem stworzyli�my osobn� aplikacj� konsolow� www/Synchronizator, powodem by�y konflikty na serwerze jBoss. 


# Dokumentacja projektu 

Pe�n� dokumentacje projektu znajdziesz pod adresem: http://ai.ia.agh.edu.pl/wiki/pl:dydaktyka:ztb:2012:projekty:srodki_trwale

# Copyright

Copyright 2012 - Marcin Hajduczek(mhajduczek@wp.pl), Tomasz Landowski(landowskitomasz@gmail.com)

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.