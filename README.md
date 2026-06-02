# Asteroids Game

Um projeto Python que implementa um jogo estilo *Asteroids* usando `pygame` e transformações geométricas manuais.

## Sobre

O jogo principal está implementado em `asteroids.ipynb` como um protótipo jogável.
A implementação usa lógica manual para transformar vértices, detectar colisões e controlar a animação.

## Requisitos

- Python 3.9 ou superior
- `pygame>=2.6.1`

## Instalação

Instale as dependências no ambiente virtual:

```bash
python -m pip install pygame>=2.6.1
```

## Uso

Execute o notebook Jupyter `asteroids.ipynb` e rode as células para iniciar o jogo.

> Observação: `main.py` atualmente é apenas um stub e não contém a lógica do jogo.

## Funcionalidades implementadas

- Personagem principal controlável:
  - movimentação com setas esquerda/direita/cima/baixo
  - rotação com teclas `A` e `D`
  - disparo de projéteis com `SPACE`
- Inimigos/obstáculos:
  - asteroides gerados em intervalos regulares
  - movimento linear em direção a um alvo interno da tela
  - colisão com o jogador causa perda de vida
- Sistema de pontuação:
  - destruição de asteroides com tiro soma pontos
  - placar e vidas exibidos em tela
- Condição de fim de jogo:
  - 3 colisões e `GAME OVER`
  - reinício com tecla `R`
- Loop de jogo funcional:
  - atualização de posições e renderização a cada frame
  - controle de FPS com `pygame.time.Clock()`

## Detalhes de implementação

- Transformações geométricas manuais:
  - escala, rotação e translação de vértices em `transformar_vertices()`
  - desenho de nave e asteroides com polígonos e círculos
- Detecção de colisão:
  - colisão circular manual em `colisao_circular()` usando distância euclidiana
- Renderização de primitivas:
  - nave triangular composta por vértices base rotacionados e transladados
  - asteroides desenhados como polígonos irregulares
  - tiros desenhados como círculos simples
- Separação de responsabilidades:
  - `Nave`, `Tiro` e `Asteroide` em classes independentes
  - lógica de atualização e lógica de renderização organizadas no loop principal

## Estrutura do projeto

- `asteroids.ipynb` - implementação principal e protótipo jogável
- `main.py` - stub de ponto de entrada sem lógica de jogo
- `pyproject.toml` - metadados e dependências do projeto
- `README.md` - documentação do projeto
