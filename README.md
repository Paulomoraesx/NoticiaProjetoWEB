Finalizando Trabalho de Programação WEB
Para iniciação aterar porta/usuario e senha no persistence.
Caso aconteça algum erro, dar Clean no projeto.


SCRIPTS DE CRIAÇÃO DO BD

CREATE DATABASE "noticiasSI" WITH ENCODING = 'UTF8' TABLESPACE = pg_default CONNECTION LIMIT = -1;

create table editoria ( idEditoria serial PRIMARY KEY, nome varchar(150) NOT NULL )

create table jornalista ( idJornalista serial PRIMARY KEY, nome varchar(150) NOT NULL )

create table noticia ( idNoticia serial PRIMARY KEY, titulo varchar(150) NOT NULL, resumo varchar(250) NOT NULL, dataNoticia Date NOT NULL, texto text NOT NULL, idEditoria integer NOT NULL REFERENCES editoria (idEditoria), idJornalista integer NOT NULL REFERENCES jornalista (idJornalista) )
