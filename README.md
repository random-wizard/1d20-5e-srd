# 1d20-5e-srd

Moved to https://codeberg.org/random-wizard/1d20-5e-srd



Example of using the csv files

    sqlite3 monsters_traits_base.db
    .mode csv
    .import monsters_traits_base.csv monsters_traits_base
    .mode list
    SELECT name, str, dex, con, int, wis, cha, alignment, challenge
    FROM monsters_traits_base
    WHERE challenge > 10 AND challenge < 13;
    .exit
    
    sqlite3 monsters_traits_special.db
    .mode csv
    .import monsters_traits_special.csv monsters_traits_special
    .mode list
    SELECT name, description
    FROM monsters_traits_special
    WHERE monster_name = 'Ghost';
    .exit
    
    sqlite3 spells.db
    .mode csv
    .import spells.csv spells
    .mode list
    SELECT name, range, level, school
    FROM spells
    WHERE school = 'necromancy' AND level = '4th-level';
    .exit
