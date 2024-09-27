# Manual do Jogo: DEV!
135
## Objetivo do Jogo
O objetivo do jogo é se livrar de todas as suas cartas antes dos outros jogadores. Utilize as funções de diferentes linguagens de programação para atrapalhar seus oponentes ou facilitar o seu caminho para a vitória!

## Componentes do Jogo
- Cartas divididas em três linguagens: *SQL*, *Python* e *JavaScript*.
- Cartas de troca de linguagem: *Index Laranja*.
- Cartas de virada de direção: *Index Rosa*.

## Preparação
1. Cada jogador recebe 7 cartas.
2. O baralho é embaralhado e colocado virado para baixo.
3. A primeira carta do topo é virada para iniciar a pilha de descarte.

## Como Jogar
- O jogo se inicia no sentido horário.
- Em cada turno, um jogador deve:
  1. Jogar uma carta da mesma linguagem, mudar a direção da rodada ou mudar a linguagem com a carta *Index* (OBS: Cartas SQL podem ser usado a qualquer momento).
  2. Caso não tenha uma carta válida, o jogador deve comprar uma do baralho.
  3. Se ainda assim não puder jogar, passa a vez.

### Troca de Linguagem
- Quando a carta *Index* for jogada, o jogador deve escolher qual linguagem será a nova ativa, e o jogo continuará com essa linguagem até que outro *Index* seja jogado.

## Cartas e Funções

### Cartas Numeradas e Funcionais
Aqui temos um baralho quase normal. A diferença é que, em vez de naipes, elas são divididas em cores dessa maneira:
  - 40 Cartas Azuis - 0 a 9
  - 5 Cartas Azuis - Funcionais
  - 40 Cartas Amarelas - 0 a 9
  - 8 Cartas Amarelas - Funcionais
  - 16 Cartas Verdes - Funcionais


### Cartas SQL
1. *INSERT INTO cartas VALUES (X)* - (6)
   - *Efeito:* O próximo jogador compra X cartas.
   - *Exemplo:* INSERT INTO cartas VALUES (3);
   - *Descrição:* O próximo jogador deve comprar a quantidade de cartas indicada.

2. *DELETE* - (4)
   - *Efeito:* Descarte uma carta de sua escolha na jogada.
   - *Exemplo:* DELETE FROM cartas;
   - *Descrição:* Escolha uma carta e descarte na rodada.

3. *SELECT* - (4)
   - *Efeito:* Veja todas as cartas SQL(verdes) do próximo jogador.
   - *Exemplo:* SELECT sql FROM próximo_jogador;
   - *Descrição:* Revele todas as cartas SQL(verdes) da mão do jogador escolhido.

4. *USE* - (𝟚)
   - *Efeito:* Troque de mão com o jogador X.
   - *Exemplo:* USE jogador_X;
   - *Descrição:* Troque todas as suas cartas com o jogador que você escolher.
PS: Caso essa for a sua ultima carta, a pessoa escolhida para trocar de mão ganhará, já que não terá mais nenhuma carta. Já você, continuará jogando com as cartas da pessoa escolhida.

5. *DROP* - (2)
   - *Efeito:* Retire um jogador do jogo.
   - *Exemplo:* DROP próximo_jogador;
   - *Descrição:* O jogador é excluido.

6. *BACKUP* - (𝟙)
   - *Efeito:* Restaure o jogador X ao jogo.
   - *Exemplo:* BACKUP jogador_4;
   - *Descrição:* O jogador X, que estava fora do jogo, volta à partida com as cartas que tinha antes.

7. *VARCHAR(X)* - (𝟜)
   - *Efeito:* O número X tem um valor, e o próximo jogador só pode jogar uma carta dentro desse valor.
   - *Exemplo:* VARCHAR(5);
   - *Descrição:* O próximo jogador só pode jogar uma carta com valor entre o intervalo permitido.

### Cartas Python
1. *num = X* - (𝟜𝟘)
   - *Efeito:* Jogue uma carta com valor X.
   - *Exemplo:* num = 7
   - *Descrição:* Jogue uma carta com o número 7.

2. *#Você foi comentado.* - (𝟝)
   - *Efeito:* Pula a vez de um jogador.
   - *Descrição:* O próximo jogador perde a vez.

2. *print (jogador_x);* - (𝟛)
   - *Efeito:* Revele as cartas Python do jogador de sua escolha.
   - *Exemplo:* print(jogador_x);
   - *Descrição:* Veja todas as cartas do jogador de sua escolha.

### Cartas JavaScript
1. *let num = X;* - (𝟜𝟘)
   - *Efeito:* Jogue uma carta com valor X.
   - *Exemplo:* let num = 3;
   - *Descrição:* Jogue uma carta com o número 3.

2. *console.log(jogador_x);* - (𝟛)
   - *Efeito:* Revele as cartas do próximo jogador.
   - *Exemplo:* console.log(jogador_x);
   - *Descrição:* Veja todas as cartas do jogador de sua escolha.
     
3. *//Você foi comentado.* - (𝟝)
   - *Efeito:* Pula a vez de um jogador.
   - *Descrição:* O próximo jogador perde a vez.


### Cartas Especiais
1. *Replace* - (𝟠)
   - *Efeito:* Troca a linguagem ativa no jogo.
   - *Exemplo:* Replace(X);
   - *Descrição:* O jogador escolhe a linguagem (SQL, Python, JavaScript) que todos deverão seguir até que outra carta *Index* seja jogada ou haja a mesma numeração da atual em outra linguagem.

  1. *Return* - (𝟠)
   - *Efeito:* Altera a direção ativa no jogo.
   - *Exemplo:* Return jogo_inverso;
   - *Descrição:* O jogador escolhe a linguagem (SQL, Python, JavaScript) que todos deverão seguir até que outra carta *Index* seja jogada ou haja a mesma numeração da atual em outra linguagem.


## Vencendo o Jogo
- O jogador que descartar todas as suas cartas primeiro, vence.
- Se as cartas do baralho acabarem, embaralhe a pilha de descarte para continuar o jogo.
