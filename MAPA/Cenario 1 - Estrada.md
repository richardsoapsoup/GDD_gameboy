# Mapa: A Estrada

## Conceito Geral
O jogo conta com um único mapa dinâmico: a Rodovia/Estrada sem fim. Diferente de um jogo de aventura que tem telas delimitadas, este cenário é gerado rolando continuamente a imagem de fundo.

## Visuais
- **Sprite Base:** `Sprites/Png/Estrada.png` (ou `Estrada.aseprite`).
  ![[Estrada.png]]
- A arte deve representar faixas de asfalto demarcadas por faixas brancas ou amarelas (que se repetem, como marcações pintadas).
- As margens (bordas laterais) da tela podem ter grama, acostamento de terra ou grades de proteção. Esse limite visual diz ao jogador onde ele não pode encostar o carro.

## Implementação Técnica
- **Tilemap de Background:** 
  O fundo utiliza o sistema nativo do GBC de Tilemaps de Background. O padrão do tilemap terá 32x32 tiles em VRAM. A câmera fará a técnica de *Vertical Scrolling* (ajustando o registrador SCY - Scroll Y) sem parar.
- **Loop Infinito:** Como o tilemap tem loop (wrap-around), ao desenhar uma estrada que casa (seamless tile) tanto na parte inferior quanto superior, a rolagem passará uma sensação contínua sem interrupções.

## Variações Climáticas (Sugestões de Expansão)
Para evitar monotonia, a cada X pontos atingidos:
1. **Dia / Noite:** Alterar suavemente a paleta de cores do background e dos sprites (deixando-os mais escuros, ligando os "faróis" do carro).
2. **Chuva:** Usar os sprites para fazer partículas caindo rápido em diagonal.
