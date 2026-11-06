# Perguntas frequentes

## O que é o DBD Skill Timers?

Um aplicativo para Windows que acompanha sua partida de Dead by Daylight: **dois temporizadores de habilidade** configuráveis, **detecção automática** do resgate do gancho (opcional), **overlay de Killer** sobre o jogo e **widgets para o OBS** (Winstreak, Placar de Confronto) — além de um **overlay 1v1** para duelos. Tudo configurável e com atalhos globais de teclado, mouse e controle.

## O app lê a memória do jogo? Injeta código?

**Não.** O app não lê a memória e não injeta código no jogo. A detecção automática funciona por **reconhecimento visual da tela** (comparação de padrão de imagem no HUD), e o controle é lido pelo XInput padrão do Windows. Ele também não depende de, nem interfere em, nenhum outro overlay que você tenha instalado.

## É seguro usar? O anti-cheat vai me punir?

O app não toca no processo do jogo, mas **não há garantia de compatibilidade com o anti-cheat**. Use por sua conta e risco, teste primeiro nas suas condições, e evite rodá-lo junto de outro overlay usando as mesmas teclas.

## Funciona em tela cheia?

Não em tela **exclusiva** — nenhum overlay aparece sobre ela. Configure o DBD em **Tela cheia em janela (borderless)**.

## Em qual sistema operacional funciona?

**Windows 10 ou 11 (64 bits)**. Não há versão para outros sistemas.

## Preciso de alguma dependência instalada?

Não. O aplicativo vem completo no instalador (fora o OBS Studio, se você quiser usar os widgets na transmissão).

## Como funciona a licença?

A licença é **perpétua e vinculada ao seu computador**, com ativação 100% offline: o app gera um **código de solicitação** (que não contém dados pessoais), você envia ao desenvolvedor (Discord **MarliNNNBr**) e importa o arquivo de licença recebido. Trocar de computador ou reinstalar o Windows exige a re-emissão da licença.

## Onde ficam minhas configurações?

Sempre em `%APPDATA%\DBD Skill Timers` (configurações, imagens, sons e recordes). O aplicativo nunca apaga nem regrava nada por cima de uma configuração existente — atualizações preservam tudo. Há **backup e restauração** completos na aba **Dados**.

## Atualizar apaga as minhas configurações?

**Não.** Como citado no item anterior: posições, cores, imagens, atalhos, sons e recordes sobrevivem a toda atualização. Se algo parecer errado depois de atualizar, veja [Solução de problemas](troubleshooting.md).

## Quais habilidades os temporizadores medem?

Os que você quiser: os temporizadores A e B são genéricos e configuráveis (nome, duração, imagem, som). O padrão de fábrica vem com Ataque Decisivo (60 s) e Resistência (10 s). A detecção automática cobre **Ataque Decisivo** e **Resistência** por sobrevivente (J1–J4).

## A detecção automática funciona na minha resolução?

O app já vem com um gabarito validado em 1920×1080 com HUD em 100%. Resoluções ou escalas de HUD diferentes podem exigir **calibração** (um gabarito feito com a sua tela) e o ajuste da "Escala de HUD (%)" (70–100%). O diagnóstico no painel mostra os scores por slot para você conferir. Sem confiança suficiente, o app **não conta nada** (não há falso positivo por engano).

## A detecção automática funciona quando jogo de sobrevivente?

Não é para isso: o detector observa o **HUD de estado dos sobreviventes** — ele é para quem joga de **Killer**. Se você estiver jogando de sobrevivente, desligue-a (aumenta o consumo de CPU à toa).

## Como registro minhas vitórias na Winstreak?

Pelo painel (botões +1 / Derrota / Desfazer), por **atalhos globais** (padrão: **Ctrl+=** para vitória e **Ctrl+-** para derrota — funcionam com o jogo em foco) ou digitando os valores direto. Cada killer tem a própria sequência, recorde pessoal e recorde mundial. Veja [Winstreak](winstreak.md).

## O que é o campo "Tipo de Streak"?

Um texto **opcional** na Winstreak (ex.: "3 Kills Only", "4K Streak", "No Add-ons") que aparece em cinza **acima do nome do killer** no widget. Vazio, o overlay fica exatamente como antes. Veja [Winstreak — Tipo de Streak](winstreak.md#tipo-de-streak).

## O recorde mundial é calculado pelo app?

Não. O recorde mundial é **sempre o valor que você informa**; sem valor, o widget exibe "—". O app nunca inventa nem valida esse número.

## Os retratos dos killers são oficiais?

Os 45 retratos inclusos — 41 da wiki da comunidade e 4 killers extras com imagens fornecidas por usuários/fãs do app — são material utilitário de fã; os da wiki pertencem a **© Behaviour Interactive** e são removidos a qualquer pedido. Para a **imagem das habilidades**, o app não distribui arte: use as suas (PNG/JPG/WebP/GIF até 2 MB) ou a biblioteca de ícones incluída.

## Posso mover/redimensionar cada elemento do overlay separadamente?

Sim. Cada cartão (A, B, J1–J4) e cada elemento dos widgets tem **posição e/ou escala próprias**, salvas automaticamente. Nos widgets do OBS (Winstreak/Placar), use **"Editar elementos"** para mover a imagem do killer e os grupos de texto como unidades e redimensionar a imagem pelas alças dos cantos.

## Posicionar o overlay atrapalha durante a partida?

Não há risco: o posicionamento é um **modo temporário**, só usado antes/entre partidas. Com ele desligado, o overlay é clique-passante, nunca rouba o foco do jogo e nunca é "arrastado por engano".

## O overlay vai para o OBS ou para a minha tela?

- **Overlay Unificado (A/B + J1–J4)**: janela real sobre o seu jogo — capturada pelo OBS por **Captura de janela**.
- **Winstreak e Placar de Confronto**: servidos localmente para fontes **Navegador** do OBS (não aparecem sobre o jogo por si).
- **Overlay 1v1**: janela sobre o seu jogo (não vai para o OBS).

## Posso usar outro overlay junto?

Tecnicamente sim, mas **não use teclas iguais** às de outro overlay — o painel avisa sobre conflitos entre as próprias ações do app e ajuda a evitar duplicidade.

## Quem mantém o projeto e como falo com o suporte?

O projeto é mantido de forma independente. **Suporte, atualizações e licenças**: Discord **MarliNNNBr**.
