# Primeiros passos

Depois de [instalar](installation.md), este guia prepara o essencial em poucos minutos: configurar um temporizador, mostrar e posicionar o overlay e (opcional) ligar o OBS.

## Conheça o painel

A janela principal é o **painel** — todo o app é configurado aqui, antes ou entre partidas. A navegação lateral tem três grupos:

- **Overlays**: Temporizadores · Detecção automática · 1v1 · Winstreak · Placar de Confronto
- **Configurações**: Overlay · Atalhos · Controle (gamepad) · Som
- **Sistema**: Dados (idioma, backup e restauração) · Ajuda

Ao lado de várias opções há um ícone **[?]**: passe o mouse (ou clique para fixar) para ver a explicação daquela opção.

## Passo 1 — Configurar os temporizadores

Na aba **Temporizadores**, escolha **A** ou **B** no seletor e configure:

1. **Nome** — ex.: "DS", "Endurance" (o nome aparece dentro do cartão do overlay).
2. **Duração** (segundos) e **Aviso** nos últimos N segundos (0 = sem aviso).
3. **Imagem**: clique em "Change image…" para usar a sua (PNG, JPG, WebP ou GIF até 2 MB) ou volte ao padrão; também há uma **biblioteca de ícones** com imagens de perks conhecidas.
4. **Cor** personalizada do cartão.
5. **Sons** (aba Som): aviso e fim de contagem por temporizador, com volume próprio; há opção de tocar com o overlay oculto.

Os valores de fábrica (DS 60 s, Endurance 10 s) são apenas exemplos — ajuste para o que quiser medir.

## Passo 2 — Mostrar o overlay e posicionar

Na aba **Temporizadores** (topo), clique em **"Mostrar overlay"**:

- No uso normal, os temporizadores **inativos ficam invisíveis**; o overlay **ignora o mouse** (clique-passante), fica **sempre no topo** e **nunca rouba o foco do jogo**.
- Clique em **"Posicionar overlay"**: os dois cartões aparecem, mesmo inativos.
  1. **Arraste** cada cartão para o lugar desejado (movimento livre, sem encaixe).
  2. Use a **roda do mouse** para ajustar o tamanho.
  3. **Conclua** com duplo clique ou pelo botão "Concluir posicionamento" — as posições ficam salvas.

## Passo 3 — Aparência e fundo do overlay

Na aba **Overlay**:

- **Escala (%)** do cartão e **Opacidade (%)** geral.
- **Fundo do cartão**: *Transparente* (só ícone + número + nome), *Semitransparente* (opacidade ajustável) ou *Opaco*.
- Mostrar temporizadores inativos sempre visíveis, mostrar rótulos A/B, etc.

## Passo 4 — Atalhos

Na aba **Atalhos**, defina as teclas de cada ação — todas funcionam **com o jogo em foco**. No modo padrão, a tecla **continua chegando ao jogo** (use teclas que o DBD não usa); o modo exclusivo, ao contrário, consome a tecla para o app.

Já vêm configurados de fábrica: **End** (zerar tudo) e **Delete** (cancelar contadores automáticos).

Se você usa controle, configure os **botões do gamepad** na aba **Controle (gamepad)** — pressione o botão físico no diálogo de captura e pronto.

## Passo 5 (opcional) — OBS Studio

**Overlay de Killer (temporizador/habilidade):**

1. No painel, deixe o overlay visível.
2. No OBS, crie uma fonte **Captura de janela** e escolha **"DBD Multi Overlays — Overlay Unificado"**.
3. Se a captura ficar preta, marque **"Usar captura de janela para acelerar"** no OBS.
4. O fundo transparente da janela é capturado junto — para compor sobre a imagem do jogo, use também uma fonte de captura de tela e ordene as camadas no OBS.

**Winstreak / Placar de Confronto:** passe o mouse por [Winstreak](winstreak.md) — são fontes **Navegador** com URL local de uma linha.

## Checklist do primeiro teste

- [ ] Jogo em **Tela cheia em janela** (borderless)
- [ ] Overlay visível e posicionado sobre o HUD
- [ ] Durações dos temporizadores ajustadas à sua build
- [ ] Atalhos definidos (evitando teclas que o jogo usa)
- [ ] Sons e volumes conferidos
- [ ] (OBS) Fonte de captura selecionada / widgets pela fonte Navegador

PRONTO — durante a partida, você só usa os atalhos. O painel fica para config antes e entre jogos.
