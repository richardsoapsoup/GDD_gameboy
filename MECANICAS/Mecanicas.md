# Mecânicas Principais

## Movimentação e Câmera
- **Rolagem de Tela (Scrolling):** O carro do jogador permanece estático em relação ao eixo Y da câmera (ficando próximo à parte inferior da tela, cerca de 1/3 da altura total a partir do chão). O que se move é o cenário (A Estrada) de cima para baixo, criando a ilusão de avanço rápido.
- **Movimentação Lateral:** O jogador move-se estritamente no eixo X. Há limites rígidos nas bordas da estrada para impedir que o carro saia do asfalto ou bata no acostamento invisível.

## Spawning de Obstáculos
- Obstáculos (Pedras) "nascem" pouco acima da borda superior da câmera (fora da visão do jogador) e descem junto com a velocidade de rolagem do cenário.
- A geração é baseada em "faixas" (lanes) imaginárias para garantir que sempre exista pelo menos uma passagem (um caminho livre) para o jogador não tomar um hit garantido (evitar situações de *softlock* de caminho).

## Aceleração e Dificuldade Progressiva
- **Velocidade Base:** O jogo possui uma velocidade inicial.
- **Progressão de Dificuldade:** A cada X segundos (ou Y pontos acumulados), a velocidade base do jogo aumenta gradativamente, tornando o tempo de reação necessário cada vez menor.
- **Risco e Recompensa:** Se o jogador segurar o D-Pad para cima, ele vai mais rápido (o cenário roda mais rápido). Isso aumenta o multiplicador de pontuação, mas aumenta muito o perigo de colidir com uma pedra.

## Colisão e Hitbox
- **Hitbox "Generoso":** A área de colisão (hitbox) do carro deve ser alguns pixels MENOR do que o sprite visual. Isso evita frustrações onde o jogador sente que "não bateu", mas o sistema contabiliza que sim porque os cantinhos transparentes ou a sombra tocaram no obstáculo.
- **Resultado da Colisão:** Encostar numa pedra resulta em **Game Over instantâneo** (morte por colisão) ou dano (caso haja um sistema de "vidas" ou "HP", sugerimos começar com morte súbita estilo arcade clássico).

## Pontuação (Score)
- Baseia-se primariamente na "distância percorrida".
- O score soma +1 ponto constantemente. A velocidade da soma depende da velocidade do cenário.
- Pode haver itens colecionáveis (como moedas) que dão +100 pontos ao passar por cima.
