# Controles do Jogo

O esquema de controles é focado na simplicidade e na resposta rápida necessária para um jogo de arcade.

| Botão         | Ação no Jogo                                     |
| ------------- | ------------------------------------------------ |
| **D-Pad Esquerda** | Move o carro para a faixa / lado esquerdo da estrada. |
| **D-Pad Direita**  | Move o carro para a faixa / lado direito da estrada.  |
| **D-Pad Cima**     | Acelera (aumenta temporariamente a velocidade e a rolagem da tela, gerando mais pontos, porém mais risco). |
| **D-Pad Baixo**    | Freia (diminui temporariamente a velocidade e a rolagem da tela para facilitar o desvio). |
| **Botão [A]**      | (Opcional) Usar item / buzinar.                  |
| **Botão [B]**      | Sem uso no momento (pode ser usado como freio alternativo). |
| **Botão [START]**  | Pausar / Despausar o jogo.                       |
| **Botão [SELECT]** | Sem uso no loop principal de gameplay.           |

## Responsividade
O carro não "vira" rotacionando, mas desliza (strafe) para a esquerda e para a direita, mantendo o sprite voltado para cima, o que facilita o hitbox e mantém a estética arcade clássica.
