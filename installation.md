# Instalação (Windows)

Este guia cobre a instalação e a ativação do **DBD Skill Timers** no Windows 10 ou 11.

## Antes de começar

| Item | Detalhe |
|---|---|
| Sistema operacional | Windows 10 ou 11 (64 bits) |
| Arquivo de instalação | Instalador fornecido pelo desenvolvedor |
| Jogo | Dead by Daylight (para usar na partida) |
| OBS (opcional) | OBS Studio, se você quiser exibir o overlay/widgets na transmissão |

## Passo 1 — Instalar

1. Execute o instalador recebido e siga as telas (instalação padrão do Windows).
2. Selecione a pasta de instalação que preferir quando o instalador pedir.
3. Conclua a instalação. O aplicativo pode ser iniciado pelo atalho criado no menu Iniciar/área de trabalho.

> O aplicativo se chama **DBD Multi Overlays** na interface do Windows.

## Passo 2 — Primeira inicialização

1. Abra o aplicativo. Na primeira execução, é criada a pasta de dados do usuário em
   `%APPDATA%\DBD Skill Timers` — é lá que ficam, para sempre, as suas configurações, imagens e sons.
2. Uma instalação nova já vem configurada com padrões úteis (durações, imagens e sons de exemplo).
   Você pode ajustar tudo na sequência — veja [Primeiros passos](getting-started.md).
3. A janela principal (painel) abre primeiro. Os overlays aparecem sobre o jogo quando você quiser.

## Passo 3 — Ativar a licença

O aplicativo exige uma licença vinculada ao seu computador, obtida com o desenvolvedor. A ativação é **100% offline**:

1. Abra o app. Sem licença válida, a **janela de ativação** aparece com o seu **código de solicitação** exibido no passo 1.
2. Clique em **Copiar** e **envie o código ao desenvolvedor** (Discord: **MarliNNNBr**). O código identifica apenas o seu computador — não contém dados pessoais nem informações de hardware.
3. Você receberá um **arquivo de licença (.json)**.
4. No passo 2 da mesma janela, clique em **"Selecionar arquivo de licença (.json)…"**, escolha o arquivo recebido e aguarde a confirmação.
5. Com a licença aceita, o aplicativo inicia normalmente e não pede ativação de novo.

### Observações sobre a licença

- A licença é **perpétua e vinculada ao computador** em que foi ativada.
- **Reinstalar o Windows ou trocar de computador** exige a re-emissão da licença — fale com o desenvolvedor pelo Discord.
- Se a sua licença for rejeitada, confira se você recebeu o arquivo para o **código exato** do computador em que o app está instalado.

## Passo 4 — Fechar, atualizar e remover

### Fechar de verdade

O **X no canto da janela do painel** envia o app à bandeja do sistema (os overlays continuam te acompanhando). Para fechar de verdade, use o botão **"Sair do app"** ou o menu da bandeja.

### Atualizar

1. Baixe a nova versão com o desenvolvedor.
2. Instale **por cima**: o instalador substitui o app, e nada da sua configuração é perdido.
3. Em versões após a 0.11.0 o nome da janela no OBS mudou para "DBD Multi Overlays — Overlay Unificado" — se a captura do OBS ficar vazia, **reselecione a janela na fonte de Captura de janela** (uma única vez).
4. Se algo parecer errado após atualizar, a configuração nunca foi tocada — consulte [Solução de problemas](troubleshooting.md).

### Remover

1. Remova o app pelo painel **Configurações > Aplicativos** do Windows (ou pelo desinstalador na pasta de instalação).
2. Se preferir apagar também seus dados e recordes, remova a pasta `%APPDATA%\DBD Skill Timers`.

## Dicas iniciais para o primeiro uso

- Configure o DBD em **Tela cheia em janela (borderless)** — em tela cheia exclusiva nenhum overlay aparece.
- Antes de posicionar os elementos, confira o guia [Primeiros passos](getting-started.md).
- Se você transmite pelo OBS, veja também [Overlay de Killer](killer-overlay.md) (captura única da janela) e [Winstreak](winstreak.md) (fonte de navegador).
