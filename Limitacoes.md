# Limitações Técnicas (Game Boy / Game Boy Color)

Este jogo é projetado levando em consideração as limitações de hardware reais do Game Boy Color.

## Resolução e Tela
- **Resolução:** 160x144 pixels (20x18 tiles de 8x8 pixels).
- **Proporção:** 10:9
- **Backgrounds:** Apenas 1 camada de background (usada para a Estrada que irá rolar infinitamente no eixo Y).

## Cores e Paletas
- **Limite de Cores:** O GBC suporta até 56 cores simultâneas na tela (de uma paleta de 32,768).
- **Paletas de Sprites:** Até 8 paletas de 3 cores + 1 transparente por sprite.
- **Paletas de Background:** Até 8 paletas de 4 cores (sem transparência).
- **Sprites e Tiles:** Cada tile possui 8x8 pixels. Personagens maiores (como o carro) são formados por múltiplos tiles agrupados (hardware sprites de 8x8 ou 8x16).

## Limites em Cena (Entidades)
- **Máximo de Sprites na Tela:** 40 sprites (hardware sprites).
- **Máximo de Sprites por Linha:** 10 sprites por scanline (se passar disso, ocorre cintilação / "flickering").
- **Design no Jogo:**
  - O Carro ocupará alguns hardware sprites.
  - As Pedras também ocuparão hardware sprites.
  - Devemos limitar a quantidade máxima de pedras visíveis na tela simultaneamente para evitar cintilação pesada, limitando para no máximo 4 a 6 pedras ao mesmo tempo, bem distribuídas na vertical.

## Controles e Inputs
- O Game Boy conta apenas com: **D-Pad (4 direções), A, B, Select, Start**.

## Áudio
- **Canais:** 4 canais (2 ondas quadradas, 1 onda programável/customizada, 1 canal de ruído "white noise").
- Ideal usar a onda de ruído para o som de batida e motor do carro, e as quadradas para a música tema em loop.