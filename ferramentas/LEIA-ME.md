# Ferramentas de produção

Nada aqui entra no jogo. São as bancadas usadas pra **criar e avaliar** a arte antes de
ela virar sprite. Todas são HTML solto: abre no navegador e funciona, sem instalar nada.

## `tratador-sprite.html` — a mais importante

Converte imagem de gerador de IA (Leonardo, Midjourney) em pixel art de verdade.
Cola com `Ctrl+V`, arrasta ou escolhe o arquivo.

O que ele faz, em ordem: corta a borda (mata marca d'água de canto) → descobre o tamanho
do bloco de pixel → reduz pegando a cor de cada bloco → tira o fundo por preenchimento a
partir das bordas → corta a paleta → recorta o vazio em volta.

**Controles:**

| Controle | Pra que serve |
|---|---|
| Tamanho final | Resolução do sprite. Ele sugere sozinho, mas quem manda é você |
| Cores | Tamanho da paleta. 14 serve pra maioria; 18-20 se tiver fogo ou gradiente |
| Tolerância do fundo | Sobrou fundo grudado? aumenta. Apareceu buraco no bicho? diminui |
| Cortar borda % | Sobe até a marca d'água sumir |
| Preservar acentos | **Detalhe colorido sumindo?** sobe pra 120-150 |

O último existe porque a primeira versão apagava as rachaduras de lava do dragão: escolher
paleta por frequência descarta justamente o que dá identidade ao personagem, porque acento
é sempre minoria. Hoje a paleta é escolhida por *frequência × o quanto a cor destoa*.

## `prompts-leonardo.html`

Kit de prompts com botão de copiar. Contém o negative prompt, a **âncora de estilo**
(o trecho que nunca muda e é o que mantém todos os dragões parecendo do mesmo jogo),
a linha completa do Dragão Brasa, o molde pra dragões novos e o molde pra objetos.

## Folhas de contato

Bancadas de avaliação, cada uma de um momento do projeto:

- `folha-brasa.html` — a linha do Dragão Brasa gerada pelo PixelLab, 3 estágios, 4 direções
- `folha-dragao.html` — o primeiro dragão gerado, comparando resoluções
- `folha-iniciais.html` — os Pokémon desenhados à mão, com idle animado e o sistema de auras
- `folha-geo.html` — desenho por geometria em 24/32/64
- `folha-charmander.html` — quatro tratamentos do mesmo sprite (foi assim que se
  descobriu que contorno preto muda tudo)
- `folha-perfil.html` — tentativas de perfil que não deram certo, guardadas como registro

## `dragao-teste/`

Os PNGs do Dragão Brasa vindos do PixelLab: filhote, adulto e ancião, quatro direções cada.
