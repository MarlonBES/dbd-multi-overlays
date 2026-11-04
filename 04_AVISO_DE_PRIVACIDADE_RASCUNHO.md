# Aviso de Privacidade — DBD Multi Overlays

**RASCUNHO CONDICIONAL. Não publicar antes de auditar o aplicativo, o emissor de licença e os fluxos de venda/suporte.**

Última atualização: [DATA]
Controlador: [NOME/IDENTIFICAÇÃO DO FORNECEDOR]
Domicílio informado: Barueri/SP
Canal de privacidade: [E-MAIL]
Suporte: Discord — [LINK]

## 1. Quem é responsável

O responsável pelo tratamento será [IDENTIFICAÇÃO DO FORNECEDOR], contato [E-MAIL]. Esta identificação deve ser preenchida sem publicar dados excessivos. O canal para solicitações LGPD deve ser efetivamente monitorado.

## 2. Dados que podem estar envolvidos — confirmar por auditoria

Marque e descreva somente o que realmente for coletado:

- [ ] Nome/apelido do comprador.
- [ ] E-mail para entrega.
- [ ] Nome de usuário/ID do Discord.
- [ ] Identificador de máquina/fingerprint usado na licença offline.
- [ ] ID da licença e estado de emissão.
- [ ] Número interno do pedido, valor e data do Pix.
- [ ] Referência/identificador da transação Pix.
- [ ] Mensagens e anexos enviados voluntariamente ao suporte.
- [ ] Logs e diagnósticos enviados pelo cliente.
- [ ] Dados técnicos salvos localmente pelo aplicativo.
- [ ] Telemetria ou comunicação automática com servidores: [DESCREVER APÓS AUDITORIA].

Não declare ausência de telemetria/rede sem revisar código, dependências, atualizador, crash handler, diagnósticos e conexões feitas pelo aplicativo.

## 3. Finalidades

Descrever apenas finalidades reais: administrar pedidos; confirmar pagamento; emitir, entregar e recuperar licenças; prestar suporte; distribuir atualizações; cumprir obrigações legais/fiscais; prevenir fraude e proteger o sistema de licenciamento.

## 4. Aplicativo e armazenamento local

A licença offline não significa automaticamente que nenhum dado é tratado. O aplicativo pode gerar identificador de máquina e manter configurações/licença/logs localmente; o vendedor pode receber manualmente o identificador para emitir a licença. Descrever com precisão quais dados ficam no computador, quais são transmitidos automaticamente e quais são enviados voluntariamente pelo usuário.

## 5. Compartilhamento e fornecedores

Mapear apenas serviços efetivamente usados: instituição financeira que processa Pix; GitHub que hospeda o instalador; Discord usado para suporte; provedor de e-mail, se houver. Verificar quais dados cada serviço trata segundo seus próprios termos e políticas. Não dizer que esses dados ficam exclusivamente com o vendedor.

## 6. Retenção

- Pedidos/registros fiscais: [PRAZO DEFINIDO COM CONTADOR, CONFORME OBRIGAÇÕES].
- Machine ID/registro de licença: [CRITÉRIO E PRAZO].
- Conversas Discord: [PRAZO/CRITÉRIO].
- Logs e diagnósticos: [PRAZO].

Evitar retenção indefinida. Explicar como pedir exclusão, respeitando retenções legalmente necessárias.

## 7. Segurança

Descrever somente controles existentes: acesso restrito à planilha, armazenamento protegido, backup seguro, chave privada Ed25519 mantida offline, autenticação em dois fatores e descarte seguro. Não afirmar medidas ainda não implementadas.

## 8. Direitos do titular

O titular pode exercer os direitos previstos na LGPD pelo canal [E-MAIL]. Descrever procedimento para confirmar identidade sem exigir dados excessivos e atender solicitações conforme a lei.

## 9. Atualizações deste aviso

Versão: [PREENCHER]. Data: [PREENCHER]. Mudanças relevantes serão comunicadas por [CANAL].

---

## Auditoria obrigatória

1. Conferir como o machine ID é calculado e se algum componente é enviado para fora do PC.
2. Verificar toda conexão de rede do aplicativo: atualização, recursos, diagnósticos, telemetria, crash reports.
3. Identificar logs e seu conteúdo.
4. Mapear dados salvos em `%APPDATA%` e outros diretórios.
5. Conferir dados recebidos em Pix, Discord e e-mail.
6. Definir bases legais, retenção, canal e controles com orientação adequada.
