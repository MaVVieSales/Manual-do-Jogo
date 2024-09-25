# Manual-do-Jogo

# Manual do Jogo Uno Programação

## Objetivo do Jogo
O objetivo do jogo é se livrar de todas as suas cartas antes dos outros jogadores. Utilize as funções de diferentes linguagens de programação para atrapalhar seus oponentes ou facilitar o seu caminho para a vitória!

## Componentes do Jogo
- Cartas divididas em três linguagens: *SQL*, *Python* e *JavaScript*.
- Cartas de troca de linguagem: *Index*.

## Preparação
1. Cada jogador recebe 7 cartas.
2. O baralho é embaralhado e colocado virado para baixo.
3. A primeira carta do topo é virada para iniciar a pilha de descarte.

## Como Jogar
- O jogo segue no sentido horário.
- Em cada turno, um jogador deve:
  1. Jogar uma carta da mesma linguagem ou mudar a linguagem com a carta *Index*.
  2. Caso não tenha uma carta válida, o jogador deve comprar uma do baralho.
  3. Se ainda assim não puder jogar, passa a vez.

### Troca de Linguagem
- Quando a carta *Index* for jogada, o jogador deve escolher qual linguagem será a nova ativa, e o jogo continuará com essa linguagem até que outro *Index* seja jogado.

## Cartas e Funções

### Cartas numeradas
Aqui temos um baralho quase normal. A diferença é que, em vez de naipes, elas são divididas em cores dessa maneira:
  - 19 Cartas Azuis - 0 a 9
  - 19 Cartas Verdes - 0 a 9
  - 19 Cartas Vermelhas - 0 a 9
  - 19 Cartas Amarelas - 0 a 9

### Cartas SQL
1. *INSERT INTO cartas VALUES (X)*
   - *Efeito:* O próximo jogador compra X cartas.
   - *Exemplo:* INSERT INTO cartas VALUES (3);
   - *Descrição:* O próximo jogador deve comprar 3 cartas.

2. *DELETE FROM cartas WHERE language = 'X'*
   - *Efeito:* Descarte quantas cartas quiser de uma linguagem de sua escolha.
   - *Exemplo:* DELETE FROM cartas WHERE language = 'python';
   - *Descrição:* Escolha uma linguagem e descarte quantas cartas dessa linguagem você tiver.

3. *SELECT * FROM próximo_jogador*
   - *Efeito:* Veja todas as cartas do próximo jogador.
   - *Exemplo:* SELECT * FROM próximo_jogador;
   - *Descrição:* Revele todas as cartas da mão do jogador à sua esquerda.

4. *USE jogador_X*
   - *Efeito:* Troque de mão com o jogador X.
   - *Exemplo:* USE jogador_2;
   - *Descrição:* Troque todas as suas cartas com o jogador que você escolher.

5. *DROP próximo_jogador*
   - *Efeito:* Retire o próximo jogador da rodada.
   - *Exemplo:* DROP próximo_jogador;
   - *Descrição:* O jogador à sua esquerda perde a vez.

6. *BACKUP jogador_X*
   - *Efeito:* Restaure o jogador X ao jogo.
   - *Exemplo:* BACKUP jogador_4;
   - *Descrição:* O jogador X, que estava fora do jogo, volta à partida com as cartas que tinha antes.

7. *VARCHAR(X)*
   - *Efeito:* O número X tem um valor, e o próximo jogador só pode jogar uma carta dentro desse valor.
   - *Exemplo:* VARCHAR(5);
   - *Descrição:* O próximo jogador só pode jogar uma carta com valor entre o intervalo permitido.

### Cartas Python
1. *num = X*
   - *Efeito:* Jogue uma carta com valor X.
   - *Exemplo:* num = 7
   - *Descrição:* Jogue uma carta com o número 7.

2. *#Você foi comentado.*
   - *Efeito:* Pula a vez de um jogador.
   - *Descrição:* O próximo jogador perde a vez.

### Cartas JavaScript
1. *let num = X;*
   - *Efeito:* Jogue uma carta com valor X.
   - *Exemplo:* let num = 3;
   - *Descrição:* Jogue uma carta com o número 3.

2. *console.log(jogador_x);*
   - *Efeito:* Revele as cartas do próximo jogador.
   - *Exemplo:* console.log(jogador_x);
   - *Descrição:* Veja todas as cartas do jogador de sua escolha.
     
3. *//Você foi comentado.*
   - *Efeito:* Pula a vez de um jogador.
   - *Descrição:* O próximo jogador perde a vez.


### Carta Especial
1. *Index*
   - *Efeito:* Troca a linguagem ativa no jogo.
   - *Exemplo:* index(languages);
   - *Descrição:* O jogador escolhe a linguagem (SQL, Python, JavaScript) que todos deverão seguir até que outra carta *Index* seja jogada.

## Vencendo o Jogo
- O jogador que descartar todas as suas cartas primeiro, vence.
- Se as cartas do baralho acabarem, embaralhe a pilha de descarte para continuar o jogo.
