# Overlay de Killer

O overlay de Killer é o conjunto de elementos que ficam **sobre o jogo na sua própria tela** — os temporizadores de habilidade, a detecção automática do resgate do gancho e o duelo 1v1. Ele é transparente, **sempre no topo**, **clique-passante** (o mouse atravessa) e **nunca rouba o foco do jogo**.

## A janela única ("Overlay Unificado")

No uso normal, os seis elementos — os dois temporizadores manuais (**A** e **B**) e os quatro pares automáticos (**J1–J4**) — vivem em **uma única janela transparente** chamada **"DBD Multi Overlays — Overlay Unificado"**.

Para transmitir, basta **uma única fonte de Captura de janela** no OBS apontando para essa janela (o fundo transparente é capturado junto; para compor sobre o jogo, use também uma fonte de captura de tela e ordene as camadas).

> Em monitores com fatores de escala de DPI **diferentes**, a composição se divide automaticamente em uma janela por fator de escala (o título ganha sufixo "(1/2)").

## Temporizadores manuais (A e B)

Cada temporizador exibe: sua **imagem de habilidade**, o **nome**, o **contador** e o **estado** — sempre legível por forma e texto:

| Ícone/forma | Estado |
|---|---|
| ○ Círculo | Contando |
| ▲ Triângulo | Aviso (últimos N segundos) |
| ■ Quadrado | **PRONTO** (aparece por um tempo configurado e some) |
| ‖ Barras | Pausado |

Regras de comportamento:

- Apertar o atalho do temporizador **reinicia a contagem** (comportamento fixo do app).
- Temporizadores **inativos ficam invisíveis** no uso normal (você pode marcar "Mostrar temporizadores inativos").
- O "PRONTO" fica na tela pelo tempo que você configurar ("Segundos de PRONTO").

## Detecção automática do resgate (J1–J4)

Habilidade opcional (**desligada por padrão**) para quem joga de **Killer**: quando um sobrevivente é **desenganchado**, os cartões de **Ataque Decisivo (60 s)** e **Resistência (10 s)** iniciam **automaticamente para aquele sobrevivente** — um par independente por slot (J1…J4, de cima para baixo na ordem do HUD).

Como o app descobre o desenganche:

- **Reconhecimento visual do HUD**: comparação de padrão de imagem do ícone "no gancho" nas quatro áreas fixas do HUD do jogo.
- O app vem com um **gabarito padrão embutido** — funciona de cara na resolução habitual (1080p com HUD 100%).
- **Calibração opcional**: você pode gerar um gabarito com a sua tela e ajustar a **"Escala de HUD (%)"** (70–100%, a faixa real do jogo).
- O detector é conservador: sem confiança suficiente, **nada acontece** (nada é contado por engano).

Extras:

- **Durações e avisos** de DS e Resistência configuráveis por aba Detecção automática.
- **Aparência própria**: J1–J4 têm ícone e cor independentes dos temporizadores manuais (editáveis "Aparência dos automáticos").
- **Atalho de emergência "Cancelar contadores automáticos"** (padrão: **Delete**): zera na hora todos os contadores automáticos, sem tocar nos manuais. Um novo gancho confirmado re-arma o slot.
- **Sacrificado / Memento Mori**: quando um terminal é confirmado, os contadores daquele sobrevivente são cancelados e ocultos.
- **Diagnóstico**: o painel mostra por slot a região, o score e o estado — útil para conferir a detecção na sua resolução.
- **Limite (aviso)**: se você estiver jogando de **sobrevivente**, não ligue a detecção automática — ela observa o HUD e aumenta o consumo de CPU sem necessidade.

## Overlay 1v1

O **duelo** de dois jogadores (ex.: quem sai primeiro do loop) tem janela própria **sobre o jogo** (não vai para o OBS — é a sua tela):

- **Nome, pontos, cor e um cronômetro por lado** — só o cronômetro do **lado ativo** corre.
- **"Cronômetro"** inicia/pausa; pausar de novo **zera** (novo round) ou **retoma**, conforme a opção "retomar em vez de zerar".
- **"Trocar lado"**: congela quem sai e inicia quem entra.
- **Ponto automático** (desligável): quando os DOIS cronômetros pausam acima do mínimo configurável, o **maior tempo vence a rodada** (+1 ponto; empate não pontua).
- **Estados visuais**: verde = vencendo, âmbar = atrás há pouco, vermelho = atrás há mais tempo; a barra do cronômetro do lado ativo pulsa.
- **Fundo semitransparente** (opcional) atrás dos cronômetros para mapas claros.

## Posicionamento e personalização

### Posicionar os elementos

1. Na aba **Temporizadores**, clique em **"Posicionar overlay"** (ou o atalho configurável).
2. Os cartões A/B aparecem mesmo sem contagem; arraste **cada um** para o lugar.
3. Use a **roda do mouse** para mudar o tamanho.
4. **Duplo clique** (ou o atalho/botão "Concluir posicionamento") — as posições de cada elemento são **salvas automaticamente**.

Para os pares automáticos, use **"Posicionar detecção"** na aba Detecção automática (mesmo esquema: arrastar, rodar, concluir). Para o 1v1, **"Posicionar 1v1"** na aba 1v1.

Detalhes:

- **Arraste livre**: o elemento segue o cursor 1:1, sem encaixe forçado; ele pode ficar parcialmente fora do monitor.
- **Recuperação**: se um monitor for desconectado, o elemento reaparece no monitor mais próximo e volta ao lugar salvo quando o monitor retorna — a posição salva **não** é perdida.
- O botão **"Redefinir posição"** recupera uma posição padrão.

### Personalizar a aparência

Na aba **Overlay**:

- **Escala (%)** geral (10–300%) e **opacidade (%)** geral.
- **Fundo do cartão**: *Transparente*, *Semitransparente* (com opacidade do fundo ajustável, 20–95%) ou *Opaco*. Ícone, contador e alertas ficam **sempre 100% visíveis** em qualquer modo.
- Mostrar temporizadores inativos / rótulos; formato da contagem.

Na aba **Temporizadores**:

- **Nome, cor e imagem por temporizador** (a cor que você escolhe nunca é repintada pelo app).
- **Aviso** nos últimos N segundos e **tempo de PRONTO**.

Na aba **Som**:

- Sons de **aviso e término** por temporizador, **gerais** e do **overlay automático**; volume geral e por som; **sons personalizados** (arquivo seu).
