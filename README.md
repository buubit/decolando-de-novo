# Decolando de Novo

Tower defense no molde do **Bloons TD 6**, com Pokémon de Kanto segurando a Equipe Rocket.

Quando um capanga é derrotado ele não morre — ele **decola pro céu** virando um brilho, com o *ding* clássico. O "pop" do balão virou o *blasting off again*. É daí que vem o nome.

**[▶ Jogar](https://buubit.github.io/decolando-de-novo/)**

---

## Como se joga

Você posiciona Pokémon ao longo da rota. Cada grunt que chega no Centro Pokémon **rouba um Pokémon seu** — perdeu 20, acabou.

- Clique num Pokémon da loja, depois no terreno (teclas `1`–`6`)
- `Espaço` inicia a rodada · `P` pausa · `Esc` cancela
- Clique numa unidade já colocada pra evoluir e trocar a mira

## O que faz esse ser diferente de um TD comum

**A tabela de tipos é de verdade.** Todos os 18 tipos, com tipo duplo multiplicando. Isso não é enfeite — é o coração da dificuldade:

| Situação | Resultado |
|---|---|
| Pikachu contra Geodude (Pedra/Terra) | **0** — nem consegue mirar |
| Squirtle contra Geodude | **4x** (Pedra 2 × Terra 2) |
| Qualquer Normal contra Gastly | **0** |
| Machop contra Gastly | **0** |
| Abra contra Rocket das Sombras | **0** |

Encheu a rota de um tipo só? A onda 12 te ensina.

**Camuflagem.** Alguns inimigos só são atingidos por quem enxerga camuflado — Growlithe desde o início, Kadabra, Gengar e Dragonite depois. A tela de montagem de time avisa em vermelho se você esqueceu.

**Só uma forma final de cada em campo.** Pode ter seis Charmander e seis Charmeleon, mas **um** Charizard. A terceira evolução é o ápice, e é escassa.

## Progressão

- **Pokébola** — captura no Safári. Você escolhe o alvo e joga bolas: a chance sobe conforme insiste e no tiro 100 é garantido. Nada é desperdiçado.
- **XP** — cada Pokémon acumula o próprio, jogando. Sobe a árvore de habilidades dele.
- **Pó de Estrela** — gacha de **shiny**. Sem pity, chance baixíssima. É troféu, não poder.
- **Ficha do Cassino** — banner de **TM** que troca toda semana. Shadow Ball num Gengar, Earthquake num Machamp.

Três mapas, liberados em ordem: **Rota 1** → **Floresta de Viridian** (camuflagem) → **Monte Lua** (Pedra/Terra).

## Detalhes técnicos

Um arquivo HTML. Sem build, sem dependências, sem CDN, sem nenhum arquivo externo — nem imagem, nem fonte, nem som.

- Canvas 2D, loop de passo fixo a 60 Hz com acumulador
- Toda a arte é **pixel art escrita como texto** dentro do próprio arquivo e rasterizada uma vez em canvas offscreen
- Os shinies não têm sprite próprio: a paleta base é convertida pra HSL e tem o matiz girado, preservando contorno e olhos
- Som sintetizado em WebAudio na hora
- Progresso salvo em `localStorage`

Dá pra baixar o `index.html` e abrir offline. Funciona igual.

## Créditos

Pokémon e Equipe Rocket são marcas da Nintendo / Creatures / GAME FREAK. Este é um projeto pessoal, sem fins lucrativos, feito por gosto. Todos os sprites foram desenhados pixel a pixel para este projeto — nenhum asset original foi usado.
