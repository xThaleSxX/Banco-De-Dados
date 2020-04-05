# Banco-De-Dados
Atividades
===========================================================================================================
/* atividade numero 1 */
/* 0 */show databases;

/* 1 */ use pokedex;
/* 2 */select * from pokemon;
/* 3 */select * from pokemon;
/* 4 */Select numero, nome, cor, altura_m , peso_kg from pokemon;
/* 5 */select numero, nome from pokemon  where geracao = 1; 
/* 6 */select * from pokemon where geracao = 1 and cor = 'amarelo';
/* 7 */select nome from pokemon order by  ataque_especial desc;
/* 8 */select numero, nome, tipo1 from pokemon where geracao = 1 and tipo1 = 'fire';
/* 9 */
/* 10 */select numero, nome, defesa from pokemon order by defesa desc;
/* 11 */select numero, nome from pokemon order by taxa_captura limit 1 ;
/* 12 */select * from pokemon tipo2;
/* 13 */select numero, nome, tipo1, tipo2 from pokemon where peso_kg between 100kg and 500kg;
/* 14 */select numero, nome, velocidade from pokemon order by velocidade desc limit 10;
/* 15 */select numero, nome, tipo1, tipo2, taxa_captura from pokemon where tipo1 and tipo2  is not null and  taxa_captura> 100 order by taxa_captura desc;
/* 16 */select distinct tipo1 from pokemon;
/* 17 */select numero, nome, cor from pokemon where nome like 'd%' ;
/* 18 */select nome from pokemon  order by ataque_especial > geracao desc ;
/* 19 */select numero, nome, defesa, ataque from  pokemon  order by  defesa > 60 and  ataque <= 70 desc ;
/* 20 */select * from pokemon where tipo1 = 'planta' and tipo2 = 'venenoso' and cor <> 'grenn' order by nome asc ;
/* 21 */select nome from  pokemon where  nome like '___y%' order by nome asc;
/* 22 */select ataque_especial from pokemon order by ataque_especial desc limit 1;
/* 23 */select numero, nome, altura_m from  pokemon where altura_m >  '2,10m' ;
/* 24 */select distinct cor from pokemon order by cor asc ;
/* 25 */select nome, velocidade from  pokemon where velocidade between 30 and 70 order by  nome asc ;
/* 25 */select nome, velocidade from  pokemon where velocidade between 30 and 70 order by  nome desc ;
/* 26 */select * from pokemon where lendario = 1 order by total desc ;
/* 27 */select * from pokemon where geracao = 1 and taxa_captura = 255;
/* 28 */select nome from  pokemon where nome in ('Pikachu', 'Squirtle', 'Bulbasaur', 'Charmander') order by  total desc limit 1 ;
/* 29 */select * from  pokemon where nome like 'd%' and tipo2 is null order by taxa_captura asc;
/* 29 */select * from  pokemon where nome like 'd%' and tipo2 is null order by total desc ;
/* 30 */select numero, nome, total, taxa_captura from pokemon where lendario order by taxa_captura desc limit 5;
/* 31 */select numero, nome, peso_kg from pokemon where peso_kg between  2  and  3 ;
/* 32 */select numero, nome, tipo1, tipo2 from pokemon where tipo1 = 'Normal'  and tipo2 is null  and lendario <>  1 ;
/* 33 */select nome, cor, tipo1, tipo2 from pokemon where (tipo1 = 'Water'  or tipo2 = 'Water' ) and cor <>  " azul "  order by nome asc ;
/* 34 */select * from pokemon order by velocidade asc limit 10;
/* 35 */select * from pokemon where nome like 'a%a' ;
/* 36 */select nome, cor, tipo1, tipo2 from  pokemon where (tipo1 = 'fire' or tipo2 = 'fire') and cor <> 'vermelho' order by nome asc;
/* 37 */select distinct peso_kg from pokemon order by peso_kg asc ;
/* 38 */select numero, nome, hp from pokemon where hp between 0 and 100 order by hp and nome asc;
/* 39 */select numero, nome, hp, ataque, defesa, total from pokemon where hp and ataque and defesa >= 100; 
/* 40 */select * from pokemon where (tipo1 ='Water' and tipo2 ='gelo') order by total desc;
===============================================================================================================================
====================================================================================================================================
==============================================================================================================================
/* atividade numero 2 */
/* Função agregada */
/* 0 */show databases;

/* 01 */select max(total) from pokemon;
		select min(total) from pokemon;
		select max(hp) from pokemon;
		select min(hp) from pokemon;
        select max(ataque) from pokemon;
		select min(ataque) from pokemon;
        select max(defesa) from pokemon;
		select min(defesa) from pokemon;
        select max(ataque_especial) from pokemon;
		select min(ataque_especial) from pokemon;
        select max(defesa_especial) from pokemon;
		select min(defesa_especial) from pokemon;
        select max(velocidade) from pokemon;
		select min(velocidade) from pokemon;
        select max(taxa_captura) from pokemon;
		select min(taxa_captura) from pokemon;
/* 02 */select count(distinct cor) from pokemon;
/* 03 */select avg(peso_kg) from pokemon;
/* 04 */select sum(altura_m) from pokemon;
/* 05 */select count(*) from pokemon;
/* 06 */select avg(altura_m) from pokemon;
/* 07 */select std(hp) from pokemon;
/* 08 */select count(distinct tipo2) from  pokemon;
/* 09 */select count(distinct tipo1) from  pokemon;
/* 10 */select sum(peso_kg) from  pokemon;
/* 11 */select count(*) from pokemon where lendario;
/* 11 */select count(*) from pokemon where not lendario ; 
/* 12 */select cor, count(*) from pokemon group by cor order by count(*) desc;
/* 13 */select avg(peso_kg), avg(altura_m) from pokemon group by geracao = 1 order by avg(peso_kg), avg(altura_m) desc;
/* 14 */select cor, avg(taxa_captura) from pokemon group by cor order by lendario;
/* 15 */select tipo1,  geracao = 1, avg(taxa_captura) > 100 from pokemon ;
/* 16 */select cor, avg(total) < 400 from pokemon where not lendario group by nome;
/* 17 */select geracao, total from pokemon  group by geracao ;
/* 18 */select geracao, count(lendario) from pokemon group by geracao;
/* 19 */select geracao, count(tipo1), count(tipo2), avg(taxa_captura) from pokemon group by geracao ;
/* 20 */select geracao, count(distinct cor), count(lendario) from pokemon where lendario  group by geracao ;
============================================================================================================================
