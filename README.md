# FazendinhaSombria-GDD
Game Design Document detalhado e manual para o projeto Fazendinha Sombria, incluindo fluxo de produção, sistemas, exemplos e dicas para iniciantes no desenvolvimento de jogos.

# Fazendinha Sombria – Game Design Document (GDD)

---
# Sumário

- [1. Introdução ao Desenvolvimento de Jogos e Fluxo de Produção](#1-introdução-ao-desenvolvimento-de-jogos-e-fluxo-de-produção)
- [2. Resumo do Jogo](#2-resumo-do-jogo)
- [3. Loop de Gameplay Central](#3-loop-de-gameplay-central)
- [4. Sistemas do Jogo](#4-sistemas-do-jogo)
  - [4.1 Sistema de Plantio e Cultivo](#41-sistema-de-plantio-e-cultivo)
  - [4.2 Sistema de Colheita e Evolução de Plantas](#42-sistema-de-colheita-e-evolução-de-plantas)
  - [4.3 Sistema de Progresso e Expansão do Terreno](#43-sistema-de-progresso-e-expansão-do-terreno)
  - [4.4 Sistema de Economia e Recursos](#44-sistema-de-economia-e-recursos)
  - [4.5 Sistema de Escolhas (Luz/Sombra/Equilíbrio)](#45-sistema-de-escolhas-luzsombraequilíbrio)
  - [4.6 Mecânicas Avançadas](#46-mecânicas-avançadas)
  - [4.7 Customização Visual e Atmosfera](#47-customização-visual-e-atmosfera)
  - [4.8 Interface (UI/UX)](#48-interface-uiux)
  - [4.9 Sugestões de Scripts/Classes (Unity/C#)](#49-sugestões-de-scriptsclasses-unityc)
- [5. Dicas para Organização de Projeto](#5-dicas-para-organização-de-projeto)
- [6. Referências e Sugestões de Ferramentas](#6-referências-e-sugestões-de-ferramentas)
- [7. Glossário para Iniciantes](#7-glossário-para-iniciantes)
- [8. Perguntas Frequentes (FAQ)](#8-perguntas-frequentes-faq)
- [9. Observações Finais](#9-observações-finais)
---

## 1. Introdução ao Desenvolvimento de Jogos e Fluxo de Produção

### O que é um GDD?

Um Game Design Document (GDD) é um manual completo do seu jogo. Ele serve para guiar toda a equipe, alinhar expectativas e registrar decisões importantes do projeto, tanto criativas quanto técnicas.

### Por que usar um GDD?

- Para não esquecer ideias e decisões.
- Para quem entrar na equipe rapidamente entender o projeto.
- Para organizar a produção, etapas, tarefas e prioridades.

### Fluxo Básico de Produção de um Jogo

1. **Ideação:** Brainstorm, definição do conceito, referências.
2. **Prototipagem:** Criar uma versão simples para testar as mecânicas principais.
3. **Pré-produção:** Planejar sistemas, arte, som, tech e estrutura do código.
4. **Produção:** Desenvolver o jogo, criar assets, implementar sistemas.
5. **Testes:** Jogar, encontrar e corrigir bugs, ajustar equilíbrio.
6. **Polimento:** Melhorar gráficos, sons, interface, UX e performance.
7. **Lançamento:** Publicar e divulgar.
8. **Pós-lançamento:** Atualizações, correções, feedback da comunidade.

> **Dica:** É normal voltar etapas, revisar ideias e mudar sistemas durante a produção!

---

## 2. Resumo do Jogo

### Nome Provisório
**Fazendinha Sombria** (ou “Fazenda do Crepúsculo”)

### Conceito

Jogo de gerenciamento de fazenda com atmosfera sombria, onde você cultiva plantas mágicas, lida com eventos sobrenaturais e decide o destino da fazenda entre a luz, a sombra e o equilíbrio.

### Lore Resumida

Você herda uma fazenda misteriosa tomada por forças mágicas. Seu objetivo é restaurá-la (ou dominá-la) cultivando espécies raras, enfrentando criaturas, desbloqueando áreas e evoluindo a propriedade conforme suas escolhas.

### Objetivo Principal

- Expandir, melhorar e personalizar a fazenda.
- Desbloquear novas plantas, áreas e mecânicas.
- Evoluir o alinhamento da fazenda (Luz, Sombra, Equilíbrio).
- Sobreviver e prosperar enfrentando desafios sazonais e eventos aleatórios.

---

## 3. Loop de Gameplay Central

O ciclo de jogo é o que o jogador faz de forma repetida, variando e expandindo conforme progride.

### Loop Básico

1. **Preparação:**  
   - Escolher sementes e preparar o solo.

2. **Plantio:**  
   - Plantar sementes de diferentes tipos (luz, sombra, equilíbrio).

3. **Crescimento:**  
   - As plantas evoluem ao longo do tempo, podendo sofrer influências (clima, eventos, criaturas).

4. **Defesa/Eventos:**  
   - Proteger plantas contra criaturas, pragas, eventos mágicos ou desastres.

5. **Colheita:**  
   - Colher plantas maduras e receber recompensas variadas.

6. **Gestão & Expansão:**  
   - Usar recursos para expandir a fazenda, construir, comprar, melhorar.

7. **Crafting & Comércio:**  
   - Criar poções, fertilizantes, vender colheitas, trocar com NPCs.

8. **Progresso & Alinhamento:**  
   - Suas ações alteram o alinhamento (luz/sombra/equilíbrio), desbloqueando conteúdos exclusivos.

#### Representação Visual do Loop


Preparar → Plantar → Crescer → Defender/Eventos → Colher → Gerir/Expandir → Recomeçar
```
```
## 4. Sistemas do Jogo

### 4.1 Sistema de Plantio e Cultivo

- *Seleção de sementes:* Sementes de luz, sombra, equilíbrio e híbridas.
- *Preparação do solo:* Tiles com bônus (fértil, sombrio, mágico, etc).
- *Plantio:* Plantio manual ou múltiplo; feedback visual e sonoro para cada fase.
- *Cuidados:* Rega, adubos, poções e encantamentos. Falta de cuidado gera pragas ou doenças.
- *Crescimento:* Fases visuais (Ex: Broto → Jovem → Adulta → Pronta para Colheita).
- *Eventos durante o crescimento:* Clima, bênçãos, pragas, criaturas.
- *Plantas híbridas:* Misture sementes/fertilizantes para criar espécies únicas.

#### Exemplo de Tabela de Plantas

| Nome                | Tipo      | Tempo | Solo Ideal   | Efeito Especial           |
|---------------------|-----------|-------|--------------|---------------------------|
| Mandrágora Macabra  | Sombra    | Médio | Sombrio      | Usada em poções raras     |
| Girassol Sagrado    | Luz       | Curto | Fértil       | Atrai borboletas          |
| Lírio do Crepúsculo | Equilíbrio| Longo | Mágico       | Imune a pragas            |
| Rosa da Meia-Noite  | Híbrido   | Médio | Sombrio/Mágico| Pode render relíquia      |
| Flor Solar Lunar    | Híbrido   | Longo | Fértil/Mágico| Duas colheitas por ciclo  |

---

### 4.2 Sistema de Colheita e Evolução de Plantas

- *Colheita:* Planta indica quando está pronta; clique/tap para colher.
- *Recompensas:* Frutos, sementes extras, itens raros (chance baseada em upgrades).
- *Grimório Botânico:* Registro de espécies, variantes, bônus e requisitos de evolução.
- *Evolução:* Colha várias vezes para liberar variantes evoluídas.
- *Árvore de Evolução:* Visualize possibilidades de combinações e mutações.

#### Sugestão de Organização Técnica (Unity/C#)

- Plant.cs — Dados e estado da planta.
- PlantGrowthManager.cs — Controle das fases de crescimento.
- HarvestManager.cs — Lógica de colheita e recompensas.
- BotanicalGrimoire.cs — Controle do grimório e evolução.

---

### 4.3 Sistema de Progresso e Expansão do Terreno

- *Desbloqueio de áreas:* Progresso libera novos tiles e biomas (bosque sombrio, lago, etc).
- *Tipos de solo:* Solo fértil, sombrio, mágico, amaldiçoado, cada um com bônus e restrições.
- *Construções e Melhorias:* Estufa, celeiro, laboratório, defesas, armazém.
- *Ferramentas:* Podem ser evoluídas (Ex: regador sagrado, foice sombria).
- *Áreas especiais:* Locais secretos desbloqueados por alinhamento, eventos ou relíquias.

---

### 4.4 Sistema de Economia e Recursos

- *Moedas:* Ganhas por vendas, missões, eventos.
- *Essências:* De luz, sombra, equilíbrio; usadas para crafting, upgrades, desbloqueios.
- *Relíquias:* Itens únicos para avanços especiais.
- *Itens de crafting:* Ingredientes de plantas, drops de criaturas, produtos de eventos.
- *Lojas e NPCs:* Comerciante padrão, mercadores raros (ex: sombrio, curandeiro), feiras.

#### Exemplo de Tabela de Recursos

| Recurso    | Como obter             | Para que serve                 |
|------------|-----------------------|--------------------------------|
| Moeda      | Vendas, missões       | Comprar sementes, ferramentas  |
| Essência L | Colheita de luz       | Crafting, desbloqueio de área  |
| Essência S | Colheita de sombra    | Crafting, poções sombrias      |
| Relíquia   | Eventos, mutações     | Construções raras, evolução    |
| Fertilizante| Crafting, loja       | Acelera crescimento            |

---
### 4.5 Sistema de Escolhas (Luz/Sombra/Equilíbrio)

- *Barra de alinhamento:* Suas ações alteram uma barra (Luz ← Equilíbrio → Sombra).
- *Influência das ações:* Plantio, crafting, defesa, eventos, interações com NPCs.
- *Consequências práticas:* Novas plantas, animais, eventos e visuais exclusivos para cada alinhamento.
- *Ambiente dinâmico:* Mudança de iluminação, trilha sonora, eventos e clima conforme alinhamento.

#### Exemplo de Tabela de Ações e Alinhamento

| Ação                              | Luz | Sombra | Equilíbrio |
|-----------------------------------|-----|--------|------------|
| Plantar semente sagrada           | +3  | 0      | 0          |
| Plantar semente sombria           | 0   | +3     | 0          |
| Plantar híbrido                   | 0   | 0      | +3         |
| Usar fertilizante mágico (luz)    | +2  | 0      | 0          |
| Usar poção sombria                | 0   | +2     | 0          |
| Defender com mascote da luz       | +2  | 0      | 0          |
| Defender com mascote sombrio      | 0   | +2     | 0          |
| Ritual de equilíbrio              | 0   | 0      | +4         |

---

### 4.6 Mecânicas Avançadas

#### Eventos Aleatórios e Sazonais

- *Noites de invasão:* Criaturas atacam plantações.
- *Bênçãos mágicas:* Chuva, luz intensa, neblina fértil.
- *Pragas e doenças:* Insetos, plantas doentes.
- *Festivais:* Bônus de venda, plantas/eventos exclusivos.
- *Eclipses e rituais:* Sementes raras, mutações e desafios.

#### Defesa e Criaturas Noturnas

- *Defesas:* Espantalhos animados, barreiras mágicas, poções defensivas.
- *Mascotes:* Cada animal tem habilidade especial de defesa.
- *Upgrades:* Defesas podem ser melhoradas.
- *Criaturas noturnas:* Podem ser hostis ou domesticáveis, dão bônus raros.

#### Crafting e Ferramentas Especiais

- *Oficina/Laboratório:* Fabricação de poções, fertilizantes, amuletos, armadilhas.
- *Ferramentas evolutivas:* Regador sagrado, foice sombria, varinha de equilíbrio.
- *Sistema de receitas:* Novas receitas desbloqueadas por progressão, alinhamento ou eventos.

---

### 4.7 Customização Visual e Atmosfera

- *Tilemaps e skins:* Diferentes paletas e estilos desbloqueáveis.
- *Customização de casa, mascotes e ferramentas:* Itens cosméticos e upgrades visuais.
- *Mudança dinâmica de clima e iluminação:* Conforme o alinhamento e eventos.

---

### 4.8 Interface (UI/UX)

- *Menu de grimório:* Registro de plantas, evoluções e receitas.
- *Barra de alinhamento:* Feedback visual do progresso de luz/sombra/equilíbrio.
- *Inventário intuitivo:* Separação clara de sementes, itens, recursos e ferramentas.
- *Feedbacks visuais e sonoros:* Efeitos para colheita, evolução, eventos e conquistas.
- *Acessibilidade:* Opções para daltônicos, ajuste de fontes, sons e controles simplificados.

---

### 4.9 Sugestões de Scripts/Classes (Unity/C#)

- AlignmentManager.cs: Gerencia pontos de alinhamento e consequências visuais/jogáveis.
- EventManager.cs: Ativa e controla eventos aleatórios e sazonais.
- DefenseManager.cs: Gerencia defesas, upgrades e mascotes.
- CraftingManager.cs: Sistema de crafting de itens, poções e receitas.
- VisualEffectsManager.cs: Muda clima, iluminação e trilha sonora.
- UIManager.cs: Controla menus, inventário e feedbacks de interface.

---

### 4.10 Customização do Protagonista

- *Opções iniciais:* Escolha de gênero, tom de pele, corte/cor de cabelo, cor da roupa.
- *Sistema modular:* Sprites divididos em corpo, cabelo, roupa, acessórios.
- *Fácil expansão:* Novos visuais podem ser adicionados como recompensas ou eventos no futuro.
- *Sem impacto em gameplay:* Apenas estético (no início), focando na identificação do jogador.

#### Sugestão técnica
- Use um sistema de slots de sprites (ex: playerBody.png, playerHair1.png, playerShirt2.png).
- Scripts para trocar sprites via seleção simples no menu inicial ou em um guarda-roupa dentro do jogo.
---

## 5. Dicas para Organização de Projeto

- *Estrutura de pastas sugerida:*
 /Assets
 /Art
 /Audio
 /Scripts
 /Prefabs
 /Scenes
 /UI
 /Docs

- *Controle de versões (Git):*
  - Sempre crie commits pequenos e descritivos.
  - Use branches para features grandes ou experimentos.
  - Escreva mensagens claras nos commits.

- *Trabalho em equipe:*
  - Defina pequenas tarefas (issues) e acompanhe via projetos/quadros do GitHub.
  - Documente sempre que possível (README, comentários).

- *Prototipação rápida:*
  - Comece simples, valide o divertido antes de polir.
  - Use assets temporários (“placeholders”) sem medo.

---

## 6. Referências e Sugestões de Ferramentas

- *Motores de Jogo:*  
  - [Unity](https://unity.com/) (C#, multiplataforma)
  - [Godot](https://godotengine.org/) (GDScript/C#, gratuito e leve)
  - [Unreal](https://www.unrealengine.com/) (C++/Blueprints, potente)

- *Arte e Animação:*  
  - [Aseprite](https://www.aseprite.org/) (pixel art)
  - [Krita](https://krita.org/) (pintura digital)
  - [Piskel](https://www.piskelapp.com/) (pixel art online)

- *Áudio:*  
  - [Bfxr](https://www.bfxr.net/) (efeitos sonoros simples)
  - [Audacity](https://www.audacityteam.org/) (edição de áudio)

- *Organização:*  
  - [Trello](https://trello.com/), [GitHub Projects](https://github.com/features/project-management)
  - [Notion](https://www.notion.so/) (documentação e tarefas)

- *Referências de jogos:*  
  - Stardew Valley, Graveyard Keeper, Forager, Littlewood, Spiritfarer.

---

## 7. Glossário para Iniciantes

- *Asset:* Qualquer recurso do jogo (imagem, som, script).
- *Tilemap:* Mapa formado por “tiles” (blocos/quadrados) usado em jogos 2D.
- *Prefab:* Objeto/modelo pronto para ser reutilizado em várias partes do jogo.
- *Script:* Código que controla o comportamento dos objetos ou sistemas.
- *Build:* Versão exportada/jogável do seu projeto.
- *Placeholder:* Arte/som temporário, só para testes.
- *Branch:* Linha paralela de desenvolvimento no Git.

---

## 8. Perguntas Frequentes (FAQ)

*1. Nunca fiz um jogo. Por onde começo?*  
> Escolha um motor (Unity ou Godot), siga um tutorial básico, tente prototipar o loop central (plantar, colher, vender). Não tente fazer tudo perfeito de cara.

*2. Preciso saber programar?*  
> Ajuda bastante! Mas hoje existem muitos tutoriais e exemplos. Você pode começar copiando scripts e adaptando.

*3. Como dividir o trabalho em grupo?*  
> Separe tarefas por sistemas (jogabilidade, arte, som, UI). Use issues e quadros do GitHub, comunique sempre.

*4. O que fazer quando travar?*  
> Busque exemplos no YouTube, fóruns, Discord, pergunte para colegas. Às vezes, dar uma pausa e voltar depois ajuda!

*5. Como saber se o jogo está ficando bom?*  
> Peça para amigos testarem. Se se divertirem, você está no caminho certo!

---

## 9. Observações Finais

- Não tenha medo de errar, mudar ideia ou pedir ajuda.
- Um GDD é um guia vivo: adapte conforme aprender e evoluir no projeto.
- Divirta-se no processo!  
- Se quiser expandir, adicionar screenshots, mockups ou fluxogramas, vá em frente!

---

> *Este documento serve como guia prático, técnico e criativo para desenvolver o “Fazendinha Sombria”. Sinta-se livre para adaptar, expandir e compartilhar!*
