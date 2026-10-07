# Obstáculos

Como este é um jogo de corrida e desvio de tráfego/estrada, não existem "inimigos" dotados de Inteligência Artificial propriamente dita, mas sim obstáculos perigosos que o jogador deve evitar ativamente.

## Pedra (Obstáculo Estático)
- **Sprite:** `Sprites/Png/Pedra.png` (ou `Pedra.aseprite` para edição).
  ![[Pedra.png]]
- **Comportamento:**
  - É spawnada aleatoriamente na parte superior da tela.
  - Seu movimento se resume a descer a tela (no eixo Y) exatamente na mesma velocidade com que a estrada (fundo) está rolando.
  - Não faz curva nem segue o jogador. Fica estática no chão da estrada.
- **Dificuldade e Padrões:**
  - O algoritmo que gera as pedras pode criar "paredes" parciais, obrigando o jogador a ir tudo para a esquerda ou tudo para a direita num movimento rápido.
  - *Regra de Ouro:* Nunca gerar uma linha reta inteira bloqueando 100% da pista na mesma altura. Sempre deixe no mínimo o espaço correspondente à largura do carro livre (garantir que o jogo seja justo e passável).

## Outros Possíveis Obstáculos (Futuros)
- **Manchas de Óleo:** Faz o carro deslizar e perder um pouco de velocidade / pontuação ou prejudica a curva momentaneamente.
- **Outros Carros:** Em atualizações, poderão existir outros veículos mais lentos (movem-se para baixo na tela, mas um pouco mais devagar que o fundo) que exigem ultrapassagem.
