create database escola_ativa
default character set utf8
default collate utf8_general_ci;

use escola_ativa;

create table if not exists usuarios (
	id_usuario int primary key auto_increment,
    nome varchar(60) not null,
    sobrenome varchar(60) not null,
    genero varchar(12),
    perfil varchar(60) not null,
    email varchar(100) not null,
    senha varchar(100) not null
) default character set utf8;

create table if not exists atividades (
	id_atividade int primary key auto_increment,
    disciplina varchar(50) not null,
    metodologia varchar(30) not null,
    titulo varchar(50) not null, 
    descricao text not null,
    links varchar(100) not null,
    termo int not null,
    autor int,
    foreign key (autor) references usuarios (id_usuario)
)default character set utf8;

select * from atividades;
select * from usuarios;
