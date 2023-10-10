# BDAnimaisDELETEALTERUPDATEDROP

-- CRIANDO A TABELA --
CREATE TABLE Animais (
  ID INT PRIMARY KEY,
  NOME VARCHAR(50),
  NASC DATE,
  PESO DECIMAL(10, 2),
  COR VARCHAR(50),
  Especie_ID INT,
  
  FOREIGN KEY (Especie_ID) REFERENCES Especies(ID)
);

-- CRIANDO A TABELA --
CREATE TABLE Especies (
    ID INT PRIMARY KEY AUTO_INCREMENT,
    Nome VARCHAR(60) NOT NULL,
    Descricao TEXT
);

-- INSERINDO DADOS--
INSERT INTO Especies (Nome, Descricao) VALUES
    ('Felinos', 'Animais tipo gato'),
    ('Caninos', 'Animais tipo cachorros'),
    ('Anfíbios', 'Animais tipo sapos');

--INSERINDO DADOS--

insert into Animais values (01, 'Ágata', date'2016-06-06', 13.9, 'branco', 1);
insert into Animais values (02, 'Félix', date'2016-06-06', 14.3, 'preto', 2);
insert into Animais values (03, 'Tom', date'2013-02-08', 11.2, 'azul', 3);
insert into Animais values (04, 'Garfield', date'2015-07-06', 17.1, 'laranja', 1);
insert into Animais values (05, 'Frajola', date'2013-08-01', 13.7, 'preto', 2);
insert into Animais values (06, 'Manda-chuva', date'2012-02-03', 12.3, 'amarelo', 3);
insert into Animais values (07, 'Snowball', date'2014-04-06', 13.2, 'preto', 1);
insert into Animais values (10, 'Ágata', date'2015-08-03', 11.9, 'azul', 2);
insert into Animais values (11, 'Gato de Botas', date'2012-12-10', 11.6, 'amarelo', 3);
insert into Animais values (12, 'Kitty', date'2020-04-06', 11.6, 'amarelo', 1);
insert into Animais values (13, 'Milu', date'2013-02-04', 17.9, 'branco', 2);
insert into Animais values (14, 'Pluto', date'2012-01-03', 12.3, 'amarelo', 3);
insert into Animais values (15, 'Pateta', date'2015-05-01', 17.7, 'preto', 1);
insert into Animais values (16, 'Snoopy', date'2013-07-02', 18.2, 'branco', 2);
insert into Animais values (17, 'Rex', date'2019-11-03', 19.7, 'bege', 3);
insert into Animais values (20, 'Bidu', date'2012-09-08', 12.4, 'azul', 1);
insert into Animais values (21, 'Dum Dum', date'2015-04-06', 11.2, 'laranja', 2);
insert into Animais values (22, 'Muttley', date'2011-02-03', 14.3, 'laranja', 3);
insert into Animais values (23, 'Scooby', date'2012-01-02', 19.9, 'marrom', 1);
insert into Animais values (24, 'Rufus', date'2014-04-05', 19.7, 'branco', 2);
insert into Animais values (25, 'Rex', date'2021-08-19', 19.7, 'branco', 3);
insert into Animais values (30, 'Cerato', date'2021-08-19', 19.7, 'branco', 1);
insert into Animais values (26, 'Carlos', date'2021-08-19', 19.7, 'marrom', 2);
insert into Animais values (27, 'Roberto', date'2021-08-20', 31.2, 'roxo', 3);
insert into Animais values (28, 'Clayton', date'2021-12-28', 31.2, 'roxo', 1);
insert into Animais values (29, 'Rircardo', date'2021-12-22', 31.2, 'roxo', 2);

-- ATUALIZANDO NOME NA TABELA--
Update Animais set nome = 'Goofy' where id=15;

-- ATUALIZANDO PESO NA TABELA--
Update Animais set Peso = 10.0 where id = 04;

-- ATUALIZANDO A COR DE TODOS OS GATOS NA TABELA--
Update Animais set cor = 'laranja' where Especie_ID = 1;

-- INSERINDO A COLUNA ALTURA NA TABELA--
alter table animais add Altura decimal(9.2)
  
-- INSERINDO A COLUNA ALTURA NA TABELA--
alter table animais add Observacao TEXT;

-- DELETANDO OS ANIMAIS COM PESO MAIOR QUE 200 DA TABELA --
DELETE from Animais where peso > 200.00;

-- DELETANDO OS ANIMAIS QUE COMEÇAM COM A LETRA C DA TABELA--
delete from animais where nome = "c%";

-- DELETANDO A COLUNA DE COR DA TABELA--
alter table animais drop column cor;

-- ALTERANDO A QUANTIDADE DE LETRAS POSSIVEIS DE NOME --
alter table animais modify NOME varchar(80);

-- DELETANDO A COLUNA NASC DA TABELA--
alter table animais drop column NASC;

-- DELETANDO A TABELA ANIMAIS --
delete from animais;

-- DELETANDO A TABELA ESPECIES--
delete from especies;

![1](https://github.com/RodrigoMaMoraes/BDAnimaisDELETEALTERUPDATEDROP/blob/main/img/Fotos1.PNG)
![2](https://github.com/RodrigoMaMoraes/BDAnimaisDELETEALTERUPDATEDROP/blob/main/img/fotos2.PNG)
![3](https://github.com/RodrigoMaMoraes/BDAnimaisDELETEALTERUPDATEDROP/blob/main/img/fotos%203.PNG)
