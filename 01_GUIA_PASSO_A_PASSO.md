# Guia passo a passo — preparação para vender sem mensalidade

## Seu modelo definido

Venda direta, pessoa física (pretendida), em Barueri/SP; Pix apenas; confirmação manual; licença perpétua para um computador por vez; suporte via Discord; emissão manual de licença offline Ed25519; downloads por GitHub Releases.

**Atenção:** “sem mensalidade” não significa “sem obrigações fiscais”, “sem taxas bancárias” ou “sem custos jurídicos”. Não inicie vendas antes de resolver os bloqueios das etapas 1 e 2.

## Etapa 1 — autorização de propriedade intelectual (bloqueador)

1. Leia a política oficial da Behaviour: https://www.bhvr.com/fan-created-content/.
2. Use `07_CONSULTA_A_BEHAVIOUR.md` para pedir orientação formal.
3. Descreva com precisão que o aplicativo é específico para Dead by Daylight, possui detecção visual de eventos, overlays/widget OBS e inclui retratos/ícones extraídos do jogo.
4. Peça resposta por escrito sobre autorização comercial tanto para a funcionalidade derivada quanto para os assets.
5. Guarde a resposta e os limites da autorização.
6. Se não houver autorização que cubra o produto, não venda a versão atual. Retirar apenas as imagens pode não resolver a questão, pois o próprio aplicativo é construído em torno do jogo.

## Etapa 2 — consultar Barueri e um contador (bloqueador)

A Prefeitura de Barueri indica que o Decreto nº 10.462, de 27/08/2026, é a base legal atual para inscrição no Cadastro Mobiliário. A lista municipal publicada contém o item “Licenciamento ou cessão de direito de uso de programas de computação” como código 01.05.01.220, com alíquota de 2,00% e natureza PJ; a tabela também tem itens de programação para PF. **Não conclua por conta própria que o código de programação PF é o correto para uma licença de uso de software.** Peça enquadramento oficial.

1. Envie `10_CONSULTA_TRIBUTARIA_BARUERI.md` para `cadastro.mobiliario@barueri.sp.gov.br` e `sf.assessoria@barueri.sp.gov.br`.
2. Se não houver resposta, ligue para Tributos Mobiliários: (11) 4199-8050.
3. Pergunte especificamente sobre pessoa física residente em Barueri que pretende licenciar o uso de software próprio, com licença perpétua para um computador, vendas diretas a consumidores e recebimento por Pix.
4. Solicite orientação escrita sobre inscrição municipal, item/código de serviço, ISS/UFIB, emissão de documento fiscal e eventual necessidade de formalização empresarial.
5. Leve a resposta a um contador para analisar Imposto de Renda, tratamento dos recebimentos de pessoa física, habitualidade e obrigações acessórias.
6. Não presuma que MEI seja possível: a ocupação precisa constar da lista permitida e o enquadramento deve corresponder à atividade real.

## Etapa 3 — definir a oferta antes de cobrar

Preencha e aprove:

- Nome comercial que pode ser usado após resolver os direitos de terceiros: [PREENCHER].
- Preço único: R$ [PREENCHER].
- Licença: sem prazo de expiração, para 1 computador ativo por vez.
- Atualizações incluídas: [DECIDIR — não anunciar atualizações vitalícias sem assumir esse compromisso].
- Transferência para outro computador: [DECIDIR — por exemplo, mediante solicitação de suporte e limite razoável].
- Reinstalação após formatação: [DECIDIR].
- Suporte via Discord: servidor/convite [PREENCHER], horários [PREENCHER], prazo de resposta esperado [PREENCHER].
- Requisitos mínimos e limitações: documentar a partir de testes reais.

“Perpétua” deve significar que não há cobrança recorrente nem expiração por calendário para o direito adquirido. Não prometa que todas as versões futuras, novos produtos, suporte ilimitado ou compatibilidade eterna estarão incluídos sem decidir isso expressamente.

## Etapa 4 — preparar Pix

1. Confirme com seu banco se a conta e a chave podem ser usadas para recebimentos relacionados à venda pretendida e se há tarifa.
2. Prefira uma chave aleatória Pix, para não divulgar CPF, telefone ou e-mail em público.
3. Gere a cobrança/QR Code no aplicativo oficial do banco, se disponível.
4. Antes de confirmar, o comprador deve conferir o nome do recebedor apresentado pelo banco.
5. Confira o crédito diretamente no extrato oficial. Comprovante enviado em chat não é confirmação suficiente.
6. Não use conta de terceiros nem envie links de pagamento falsos.

Não é necessário abrir conta em intermediador neste primeiro modelo. Pix direto não elimina obrigações fiscais, consumeristas ou bancárias.

## Etapa 5 — criar Discord de suporte

1. Entre em https://discord.com/ e crie uma conta, caso ainda não tenha.
2. Crie um servidor com nome neutro do produto somente quando o uso comercial estiver autorizado.
3. Crie canais: `#avisos`, `#instalacao-e-ativacao`, `#suporte` e `#bugs-conhecidos`.
4. Em `#avisos`, publique somente versões e links oficiais.
5. Configure um convite permanente ou com prazo adequado e copie o endereço para preencher os documentos.
6. Não peça ao cliente senha, token, chave privada, documento de identidade ou dados bancários.
7. Oriente o cliente a enviar logs apenas quando necessários e após verificar que não expõem dados pessoais.

Não é preciso bot ou automação para começar. Atendimento por mensagem direta também é possível, mas um servidor organizado facilita suporte e avisos.

## Etapa 6 — criar GitHub Releases

Faça isto depois da autorização comercial, para não publicar uma versão comercial não autorizada.

1. Use sua conta atual do GitHub.
2. Crie um repositório separado, por exemplo `dbd-multi-overlays-downloads` somente se o nome/marca estiver liberado.
3. Mantenha esse repositório de distribuição independente do repositório privado de desenvolvimento.
4. Não envie código-fonte privado, `.env`, machine IDs, settings pessoais, logs privados, chaves, certificados ou licenças de clientes.
5. Abra `Releases` → `Create a new release`.
6. Use a versão real do aplicativo e as notas corretas; não invente versão.
7. Anexe somente o instalador validado e um arquivo de hash SHA-256.
8. Publique e baixe o arquivo novamente para testar.
9. Faça instalação limpa em Windows sem Node.js, Visual Studio ou cache dos helpers. Teste a detecção GDI e o foco do DBD.

Para calcular SHA-256 no Windows:

```bat
certutil -hashfile "DBD-Multi-Overlays-Setup.exe" SHA256
```

Cada arquivo anexado a uma Release do GitHub deve ser inferior a 2 GiB. Confira a documentação atual: https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases.

## Etapa 7 — primeira venda manual

1. Envie antes da compra: descrição do produto, preço, requisitos, EULA, aviso de privacidade, política de Pix/reembolso e canal Discord.
2. Registre um número interno de pedido.
3. Envie chave/QR Pix e valor exato.
4. Confirme o crédito no app do banco.
5. Solicite somente os dados estritamente necessários para emitir a licença: e-mail/canal de entrega e machine ID exibido pelo aplicativo, se confirmado como necessário.
6. Gere licença com o emissor existente. Nunca exponha a chave privada Ed25519.
7. Envie instalador oficial, SHA-256, licença e instruções.
8. Registre status e data de entrega na planilha CSV.
9. Dê suporte pelo Discord.

## Etapa 8 — reembolso e pós-venda

- Tenha um canal claro para cancelamento e reembolso.
- Não anuncie “sem reembolso porque é digital”. O CDC prevê direito de arrependimento nas contratações à distância, e a aplicação deve ser tratada com orientação jurídica.
- Se houver reembolso, registre a devolução e trate a licença conforme procedimento tecnicamente possível. Em licença offline, uma revogação remota garantida não existe.
- Guarde registros fiscais pelo prazo indicado pelo contador; não conserve dados de suporte indefinidamente sem necessidade.

## Etapa 9 — segurança operacional

- Chave privada Ed25519: armazenamento criptografado/offline, backup seguro, acesso somente seu.
- Downloads: um único repositório oficial e hash publicado.
- Planilha de pedidos: privada, com acesso restrito; não a coloque em repositório público.
- Discord: habilite 2FA e não compartilhe tokens.
- Nunca envie arquivo de licença de um cliente para outro.
- Nunca solicite senha ou acesso remoto desnecessário ao computador do comprador.
