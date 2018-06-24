# Sokoban
Trabalho final da cadeira Algoritmos e Programação 2017/01, feito em trio com @juviolato e @birromer.

Estruturas utilizadas:

    - Jogador:
        Armazena o nome, a pontuação, quantos níveis foram concluídos, o tempo de jogo, a quantidade de movimentos realizados por um jogador.
    - Escore:
        Armazena o nome de um jogador e sua pontuação.
    - Posições finais:
        Armazena as coordenadas de uma posição final para um bloco móvel, para fins de comparação na função de movimento.
	- Save:
		Armazena todos os dados necessários para serem salvos. A pontuação, os níveis completos, o tempo passado, os movimentos do jogador, o escore, e o mapa no estado atual.

Funções:

    - ordenaJogadores:
        Lê os 10 primeiros Escores do arquivo highscore.bin, armazenando-os em um vetor de Escores passado como referência.
        Devolve como retorno explícito a quantidade de Escores lidos.
    - leNome:
        Lê o nome de um Jogador e armazena em uma string passada como referência.
    - leMapa:
        Lê a matriz do espaço do jogo no arquivo de texto do nível passado como parâmetro.
    - sorteiaPosicoes:
        Cria posições finais aleatórias no mapa do jogo (matriz passada como referência).
        Armazena as coordenadas sorteadas em um vetor de Posições finais.
    - ampliarMapa:
        Duplica o tamanho do mapa lido pela função leMapa.
    - imprimirMapa:
        Mostra na tela o mapa já duplicado pela função ampliarMapa.
    - calculaEscore:
        Faz os cálculos da pontuação do jogo atual a partir dos níveis completos, quantidade de movimentos, e o tempo decorrido (parâmetros).
    - salvaEstadoAtualTXT:
        Salva o mapa, o tempo decorrido e os movimentos feitos em um arquivo de texto.
    - salvaEscore:
        Salva o nome do jogador e sua pontuação no arquivo binário de highscores.
    - pausaBin:
        Cria um arquivo binário de pausa com o tempo, os movimentos, pontuação e níveis completos pelo jogador e o mapa do jogo.
    - carregaPausa:
        Carrega nas variáveis de tempo, movimentos, pontuação e nível alcançado pelo jogador e restaura o mapa com os valores prévios à pausa.
    - imprimeHighscore:
        Exibe na tela as 10 maiores pontuações registradas, lidar pela ordenaJogadores e passadas como referência em um vetor.
    - menuInicial:
        Exibe na tela as opções do menu inicial do jogo.
    - imprimeMenu:
        Disponibiliza os comandos do menu do jogo.
    - imprimeInfo:
        Mostra, abaixo do menu e acima do mapa do jogo, o nível atual, o nome do jogador e sua pontuação, o tempo restante, os movimentos dados, e a razão entre cubos fixos e cubos totais.
    - movimento:
        Coordena a movimentação do jogador pelo mapa.
        Devolve como retorno explícito a pontuação do jogador.
	- setGameOver:
		Encontra as caixas no mapa e verifica se está num canto, se estiver devolve true, se não, false.
    - novoJogo:
        Inicializa um novo nível, passado como parâmetro.



COMO JOGAR:

    Menu inicial:
        N: Inicializa um novo jogo.
        E: Carrega as 10 maiores pontuações e os nomes dos jogadores.
        Q: Encerra o programa.

    Durante o jogo:
        A tecla TAB disponibiliza os comandos exibidos no menu acima do mapa do jogo (exceto a pausa).
        N: Inicializa um novo jogo.
        S: Salva o escore e o estado atual do jogo.
        P: Pausa o jogo: nenhum outro comando é aceito até que a tecla P seja pressionada novamente.
        E: Carrega as 10 maiores pontuações e os nomes dos jogadores.
        Q: Salva o escore e o estado atual do jogo e encerra o programa.

