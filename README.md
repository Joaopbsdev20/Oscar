# Atividade Banco de dados - Oscar

1- Quantas vezes Natalie Portman foi indicada ao Oscar?

Ela foi indicada três vezes.

Código: select* from movies where `name` = "Natalie Portman"

2- Quantos Oscars Natalie Portman ganhou?

Ela ganhou um Oscar.

Código: select * from movies where `name` = "Natalie Portman" and `winner`='true'

3- Amy Adams já ganhou algum Oscar?

Não ela não ganhou.

Código: select * from movies where `name` = "Amy Adams"

4- A série de filmes Toy Story ganhou um Oscar em quais anos?

Ganhou o Oscar em 2011.

Código: select * from movies where film = "Toy Story 3" and year_ceremony

5- Quem tem mais Oscars: a categoria "Melhor Ator" ou "Melhor Filme"?

Melhor filme no total de 66.

Código: select count(category) from movies where category = "cinematography" and winner="true"

6- O primeiro Oscar para melhor Atriz foi para quem? Em que ano?

Janet Gaynor em 1928.

Código: select * from movies where category="actress"

7- Na coluna/campo Winner, altere todos os valores com "True" para 1 e todos os valores "False" para 0.

Código: update movies set winner=0 where winner="false";

update movies set winner=1 where winner="true";

select * from movies

8- Em qual edição do Oscar "Crash" ganhou o prêmio principal?

Na edição de 2006

Código: select * from movies where film="Crash"

9- Bom... dê um Oscar para um filme que merece muito, mas não ganhou.

O filme 1917

Código: update movies set winner=1 where film="1917";

select * from movies where film="1917"

10- O filme Central do Brasil aparece no Oscar?

Infelizmente não aparece no Oscar

Código select * from movies where film="Central"

11- Inclua no banco 3 filmes que nunca nem foram nomeados ao Oscar, mas que na sua opinião, merecem. 

Código:
INSERT INTO movies (year_film, year_ceremony, ceremony, category, `name`, film, winner) VALUES ('2002', '2003', '1', 'ACTOR', 'Rodrigo Santoro', 'Carandiru', 'True');
INSERT INTO movies (year_film, year_ceremony, ceremony, category, `name`, film, winner) VALUES ('1960', '1961', '1', 'WRITING', 'Dodie Smith, Bill Peet', '101 Dalmatas', 'True');
INSERT INTO movies (year_film, year_ceremony, ceremony, category, `name`, film, winner) VALUES ('2007', '2008', '1', 'ACTOR', 'Brendan Fraser', 'Viagem ao Centro da Terra', 'True');

12- Crie uma nova categoria de premiação. Qualquer prêmio que você queira dar. Agora vamos dar esses prêmios aos filmes que você cadastrou na questão acima.

Código:
INSERT INTO movies (year_film, year_ceremony, ceremony, category, `name`, film, winner) VALUES ('2010', '2024', '95', 'Melhor adaptação de quadrinhos', 'Bryan Lee O'Malley', 'scott pilgrim contra o mundo', 'True');
update movies set category="Melhor adaptação de quadrinhos" where film = 'scott pilgrim contra o mundo';

13- Qual foi o primeiro ano a ter um prêmio do Oscar?

O primeiro ano a ter o Oscar foi em 1927

SELECT MIN(year_film) AS first_year 
FROM movies where winner="true";

14 - Pensando no ano em que você nasceu: Qual foi o Oscar de melhor filme, Melhor Atriz e Melhor Diretor?

Não teve nenhum "Melhor Oscar" desses requisitos em 2002.

15- Agora procure 7 atrizes que não sejam americanas, europeias ou brasileiras.  Vamos cadastrá-los no nosso banco, mas eles ainda não ganharam o Oscar. Só foram nomeados.

Código: update movies set category="actress" where film = 'blue jasmine'; select * from  movies WHERE film="blue jasmine";

16- Agora vamos falar da sua vida. Me diga o nome de uma pessoa que você admira e o que ela fez na sua vida. Agora me diz: Quê prêmio essa pessoa merece? 

Meu pai francisco, ele me forneceu tudo e luta por mim todos o dias, ele merece uma vida de paz e tranquilidade, sem preocupações.














