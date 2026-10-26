# 📘 Atividade: Jogo da Forca

## 🎯 Objetivo

Pratique manipulação de strings, listas, estruturas de repetição, condicionais e entrada de dados em Python. Ao final, você terá criado um jogo da Forca em que o jogador tenta descobrir uma palavra secreta antes de esgotar as tentativas.

## 📝 Tarefas

### 🛠️ Preparar a palavra secreta e o progresso

#### Descrição
Crie a estrutura inicial do jogo: escolha aleatoriamente uma palavra de uma lista predefinida e prepare uma representação que mostre quais letras já foram descobertas.

#### Requisitos
O programa concluído deve:

- Manter uma lista predefinida com pelo menos cinco palavras.
- Selecionar uma palavra aleatoriamente usando um recurso da biblioteca padrão do Python.
- Exibir cada letra ainda não descoberta como um sublinhado, separando as posições para facilitar a leitura. Por exemplo, para a palavra `casa`, exiba `_ _ _ _`.
- Inicializar e exibir a quantidade de tentativas incorretas permitidas.

### 🛠️ Implementar as rodadas e o encerramento do jogo

#### Descrição
Implemente as rodadas para que o jogador informe uma letra por vez. Atualize o progresso após cada palpite e encerre a partida quando a palavra for descoberta ou quando não restarem tentativas.

#### Requisitos
O programa concluído deve:

- Solicitar ao jogador um palpite de uma letra em cada rodada.
- Revelar todas as posições em que a letra aparece na palavra secreta.
- Reduzir as tentativas restantes quando o palpite não estiver na palavra.
- Repetir as rodadas enquanto a palavra não for descoberta e ainda houver tentativas.
- Exibir uma mensagem de vitória quando a palavra for descoberta e uma mensagem de derrota quando as tentativas se esgotarem; na derrota, revelar a palavra secreta.
