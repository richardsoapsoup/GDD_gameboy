# O Carro (Personagem do Jogador)

## Papel
O único personagem e veículo controlado pelo jogador. Trata-se de um carro de corrida com vista superior (top-down).

## Visual e Sprites
- **Sprite Utilizado:** `Sprites/Png/Carro.png` (ou `Sprites/Asesprite/Carro.aseprite` para edição).
  ![[Carro.png]]
- **Design:** Deve ser de fácil leitura e contraste alto com o fundo para que em velocidades altas no GBC o jogador não perca o controle visual de onde está.
- **Animações Sugeridas:**
  - **Idle / Acelerando:** O carro apenas treme sutilmente (1 ou 2 pixels de offset Y de vez em quando) para simular o motor roncando e os solavancos do asfalto, ou não possui animação, confiando inteiramente na rolagem do cenário para transmitir a sensação de velocidade.
  - **Virando:** Inclinação leve (tilt) ou pneus virando levemente (se o limite de sprites permitir).
  - **Explosão / Batida:** Uma animação de 3 frames (poeira, fogo ou amassando) ao atingir uma Pedra.

## Atributos
- **Velocidade Lateral (Maneabilidade):** O quão rápido o carro muda de faixa.
- **Vidas / Hit Points:** Por ser um arcade clássico, inicia com apenas 1 "vida" (bater = morre).

## Feedback Visual e Sonoro
- Ao acelerar com tudo (D-pad Cima), pode soltar partículas de escapamento (pixels brancos/cinzas soltos atrás do carro) usando hardware sprites extras.
