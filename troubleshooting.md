# Solução de problemas

Problemas comuns do **DBD Skill Timers** e o que fazer em cada caso.

## O overlay não aparece sobre o jogo

- **Causa mais comum**: o jogo está em **tela cheia exclusiva**. Configure o DBD em **Tela cheia em janela (borderless)** — em tela cheia exclusiva nenhum overlay pode aparecer sobre o jogo.
- Confirme que o overlay está **visível**: no painel, aba Temporizadores, use **"Mostrar overlay"**.
- No uso normal os temporizadores **inativos ficam invisíveis** — isso é o comportamento esperado. Use "Posicionar overlay" para conferir onde estão os cartões.
- Se a posição parece perdida (ex.: trocou de monitor), use **"Redefinir posição"**.
- Se o elemento sumiu de um monitor que foi desconectado, ele reaparece no monitor mais próximo e volta ao lugar salvo quando o monitor retorna.

## A captura no OBS está preta

- No OBS, na fonte **Captura de janela**, marque **"Usar captura de janela para acelerar"**.
- Confirme que a fonte aponta para **"DBD Multi Overlays — Overlay Unificado"** (nome atual da janela; após atualizar do app antigo, reselecione a janela uma única vez).
- Sem nenhum temporizador rodando e com inativos ocultos, **não há nada para capturar** — é o esperado. Use "Posicionar overlay" para ver os cartões.

## Os widgets (Winstreak/Placar) aparecem como "OFFLINE" no OBS

- O widget do OBS se conecta ao app por um servidor **local**. Esse aviso significa que o app **não está aberto** — abra o DBD Skill Timers e a fonte reconecta sozinha.
- Se o app estiver aberto e mesmo assim ficar "OFFLINE":
  1. Veja na aba correspondente (Winstreak ou Placar de Confronto) o **status do servidor** e o **"Copiar URL"**.
  2. Confira se a fonte Navegador do OBS está com **exatamente** o URL exibido no painel (a porta pode ter mudado se a padrão estava ocupada).
  3. Recarregue a fonte (botão de recarga da fonte Navegador no OBS).

## A porta do widget está ocupada

- Se a porta padrão (4000 na Winstreak / 4100 no Placar) estiver em uso, o app tenta automaticamente as seguintes (+1…+9). O **URL exibido no painel já sai correto** — copie de lá.
- Você também pode definir a porta manualmente na aba correspondente.

## O atalho de teclado não funciona (ou dispara junto)

- Atalhos configuráveis funcionam **com o jogo em foco**. Confira na aba **Atalhos** se a ação está com atalho definido (algumas ações nascem **sem** atalho de propósito, como "Desfazer" da Winstreak).
- O painel avisa se a **mesma tecla** estiver em uso por outra ação — resolva conflitos atribuindo teclas diferentes.
- No modo padrão, a tecla **continua indo para o jogo** (evite teclas que o DBD usa). Se necessário, troque o modo para **exclusivo** (a tecla é consumida pelo app).
- Não rode o app junto de **outro overlay** usando as mesmas teclas.

## O controle (gamepad) não é detectado

- Confira o status do controle no cabeçalho do painel e na aba **Controle (gamepad)**.
- A leitura usa o padrão **XInput** do Windows. Controles **DirectInput puros** (alguns DualShock/DualSense sem wrapper) podem não aparecer — use **Steam Input** ou **DS4Windows**, que os expõem como XInput.
- Ao associar, o diálogo captura o **botão físico**: pressione-o com o painel em foco. "Esc" cancela; Backspace limpa.

## O botão do controle dispara errado/repetido

- O disparo acontece na **borda de pressão** (só quando o botão desce): segurar **não** repete.
- Durante o posicionamento de overlays, captura de atalho ou com foco em campo de texto, os botões do controle **não acionam nada** (proteção intencional).
- Qualquer controle conectado dispara as ações — não há associação por controle individual.

## A detecção automática não detecta o desenganche

- Confirme que ela está **ligada** na aba Detecção automática (nasce desligada).
- **Calibre**: gere um gabarito com a sua tela ("Capturar gabarito") e ajuste a **"Escala de HUD (%)"** (70–100%) se o HUD do jogo não estiver no espaçamento padrão.
- O app vem com gabarito padrão validado em 1920×1080 com HUD 100%; resoluções/proporções diferentes podem exigir calibração.
- Use o **diagnóstico** no painel: ele registra por slot a região analisada, o **score** e o estado — se o score não passa do limiar na sua resolução, ajuste o limiar ou recalibre.
- Não é reconhecido **sem confiança**: se o ícone não casar, o app fica em silêncio (não conta nada por engano).
- A captura é do **monitor primário**; o jogo em uma segunda tela não é observado.

## O painel avisa que rejeitou o meu gabarito / usa o modelo padrão

- Se um gabarito incoerente for detectado (as medidas não conferem com o recorte), o painel avisa e o app **assume o gabarito padrão** automaticamente. Para recomeçar do padrão, use "Remover modelo".

## CPU alta durante a partida

- Se você está jogando **de sobrevivente**, desligue a **detecção automática**: ela observa o HUD e aumenta o consumo de CPU sem necessidade.
- A detecção adapta o consumo sozinha: captura rápida só enquanto há alguém no gancho; parado, roda lento.
- Os overlays também se ajustam: quando nada está animando, o consumo cai quase a zero.

## Marquei vitória/derrota sem querer na Winstreak

- Use **"Desfazer"** (botão ou atalho): ele devolve os valores do antes da última alteração por killer e depois esvazia (nível único).
- Atalho de Desfazer nasce **sem tecla de propósito** — só configure se quiser o risco de desfazer por tecla.

## As posições/cores/imagem sumiram

- Elas não são apagadas por atualização: a configuração existente **sempre vence**, e o app nunca regrava nada por cima. Veja [FAQ](faq.md) sobre onde ficam os dados.
- Se `settings.json` ficar ilegível, o app **preserva o original** como `settings.corrupt-*.json` e usa os padrões. Fale com o suporte (Discord: **MarliNNNBr**) para recuperar.
- Na aba **Dados** há **backup e restauração** das suas configurações — use antes de reinstalar o sistema.

## A licença parou de funcionar / troquei de computador

- A licença é vinculada ao computador. **Reinstalação do Windows ou troca de máquina exige re-emissão** — envie o novo **código de solicitação** ao desenvolvedor (Discord: **MarliNNNBr**).

---

Não encontrou seu problema? Fale com o desenvolvedor no Discord: **MarliNNNBr**.
