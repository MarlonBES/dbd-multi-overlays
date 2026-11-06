# Winstreak

O **Winstreak** é o widget que registra e exibe, ao vivo no OBS, a sua sequência de vitórias por killer: um cartão estilo "placa de esports" com o retrato, **STREAK** + número gigante e os recordes pessoal e mundial.

## Como funciona

1. Abra a aba **Winstreak** no painel.
2. Escolha o **killer** na grade — cada killer tem **registros próprios** (sequência, recorde pessoal e recorde mundial separados).
3. Durante o jogo, registre os resultados:
   - **Vitória (+1)** — soma 1 à sequência; se passar do recorde pessoal, o recorde pessoal **empata ao vivo**;
   - **Derrota** — zera a sequência (o recorde pessoal fica intacto, é histórico);
   - **Desfazer** — devolve os valores do ANTES da última alteração (um nível, por killer, sobrevive a reinícios);
   - **Edição manual** — os três valores (sequência, pessoal, mundial) podem ser digitados direto.
4. O **recorde mundial** é sempre o valor que **você** informa: enquanto você não digitar nada, o widget exibe "—". O app nunca inventa um.

## Atalhos globais

Funcionam **com o jogo em foco** (configuráveis na aba Winstreak):

| Ação | Atalho de fábrica |
|---|---|
| Vitória (+1) | **Ctrl+=** |
| Derrota (zera a sequência) | **Ctrl+-** |
| Desfazer | *(nasce vazio — configure só se quiser)* |

## Tipo de Streak

Na aba Winstreak, grupo **"Personalização do widget"**, há o campo **"Tipo de Streak"** (completamente opcional):

- Escreva a modalidade em que está jogando: `3 Kills Only`, `4K Streak`, `3K Streak`, `No Add-ons`… (até 64 caracteres).
- Com o campo preenchido, o texto aparece em **cinza, menor, acima do nome do killer**:

```
3 KILLS ONLY
The Executioner 43
```

- Com o campo **vazio**, o overlay fica **idêntico ao de sempre** — nenhum espaço fica reservado.
- Apagando o texto, o rótulo some imediatamente.
- O texto acompanha o nome do killer: se você mover o grupo "nome + recordes" no editor de elementos (abaixo), o Tipo de Streak vai junto.

## Ícone exibido e nome

- **Ícone exibido**: escolha qualquer killer da biblioteca (a imagem exibida) ou o **ícone de sobrevivente**. A escolha é **só visual**: os recordes continuam pertencendo ao killer selecionado na grade.
- **"Survivor"**: com o ícone de sobrevivente, o nome exibido é exatamente "Survivor" (imagem e nome sempre coerentes).
- **Título personalizado**: substitui o nome exibido (ex.: "Oblivion Streak", "Nurse No Perks"). Vazio = nome do killer/ícone exibido.
- **Imagem personalizada**: substitui o retrato no widget (e no OBS) por uma imagem sua (PNG/JPG/WEBP/GIF até 2 MB), com botões "Escolher imagem" e "Usar padrão".

## Aparência do widget

Tudo com **prévia ao vivo** logo acima dos controles:

- **Cores independentes** (cada uma com seu seletor, aplicadas em tempo real):
  - **Brilho do número** (glow ao redor do STREAK gigante);
  - **Contorno do retrato** (pedestal/anel);
  - **Troféu** da animação de novo recorde (nasce dourado e não herda a cor de acento).
  - **Cor de acento** geral do cartão.
- **Fundo do retrato totalmente transparente**: a placa atrás do retrato sai de verdade (transparência real pelo canal alfa do OBS), sem nenhum contorno ao redor do retrato.
- **Animações** (ligadas por padrão): a coreografia completa. Desligada, tudo congela — número troca seco e o cartão fixa no recorde pessoal (sem alternar).
- **Mostrar recorde mundial**: com a opção ligada (e animações ligadas), os recordes **alternam a cada 4 s** entre pessoal e mundial.

## Coreografia dos eventos

A animação acontece **só com eventos reais** (vitória/derrota que você marca):

- **Vitória**: pop "+1" e o número novo entra com a queda característica.
- **Recorde pessoal SUPERADO**: estouro dourado — varredura de luz, troféu caindo e brilho no número. **Empate não é recorde**: ganha só um brilho discreto no troféu.
- **Derrota**: nevoeiro vermelho, micro-abalo do cartão e faixa "SEQUÊNCIA ENCERRADA".

**Ensaio na prévia**: os três botões (+1 vitória / recorde / derrota) tocam a coreografia com valores temporários na prévia do painel — **nada é salvo**; o próximo evento real devolve a verdade.

## Editor de elementos (posição e tamanho)

No grupo **"Posição dos elementos"**, ligue **"Editar elementos"** e clique em um bloco da prévia para selecioná-lo:

- **Imagem do killer**: arraste para reposicionar e use as **alças dos cantos** para redimensionar **mantendo a proporção** (20–300%).
- **STREAK + número** e **nome + recordes (inclui o Tipo de Streak)**: cada grupo se move como uma **unidade** — nada se desalinha internamente.
- As bordas do overlay dão um **encaixe suave** (puxão leve, sem trava) para indicar alinhamento.
- O arraste é **preciso**: o elemento não salta para o centro do cursor — ele acompanha o movimento a partir do ponto exato onde você clicou (dá para ajustar 3–5 pixels).
- **"Restaurar layout padrão"** devolve a composição de fábrica a qualquer momento.

> Essas posições afetam **só o que está dentro do widget** — a janela/fonte do OBS nas suas telas nunca é movida.

## Exibindo no OBS (fonte Navegador)

1. Na aba **Winstreak**, confira que o servidor está **ativo** (o status aparece na aba; ele é **local**, só responde na sua máquina).
2. Clique em **"Copiar URL"** — o endereço é do tipo `http://127.0.0.1:4000/obs/winstreak`.
3. No OBS, crie uma fonte **Navegador** com esse URL (ex.: **800×240**) — o cartão é atualizado **ao vivo, sem recarregar**.
4. Se a porta 4000 estiver ocupada, o app usa automaticamente a seguinte (4001…): o URL exibido no painel já sai correto.
5. Com o app fechado, a fonte mostra um aviso "OFFLINE" e reconecta sozinha quando você voltar a abrir o app.
6. A porta pode ser alterada nas opções da aba (a atualização do OBS é instantânea — apenas recarregue a fonte se necessário).
