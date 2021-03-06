﻿# Histórico de versões do Signer

> [!NOTE]
> Este histórico por ora contém informações apenas sobre as atualizações mais recentes ao sistema. Estamos
> trabalhando para documentar as versões mais antigas.

<a name="v1-6-2" />
### 1.6.2 (2020-06-25)

* Correções de bugs
  * [SIG-377] - Erro ao abrir detalhes de documento com observador que não está no fluxo

Atualiza modelo do banco de dados: não

<a name="v1-6-1" />
### 1.6.1 (2020-06-24)

* Melhorias
  * [SIG-374] - Adicionar tema metallic-seaweed-emerald (MSE)

Atualiza modelo do banco de dados: não

<a name="v1-6-0" />
### 1.6.0 (2020-06-24)

* Novas funcionalidades
  * [SIG-349] - Carregar tela de criação de documento com upload já realizado
  * [SIG-360] - Integração com página de Assinatura (Assinatura embutida)

* Melhorias
  * [SIG-227] - Simplificar exemplos no Swagger
  * [SIG-320] - Melhorar tratamento das marcas de assinatura para documentos com muitos assinantes
  * [SIG-327] - Alterar para o singular mensagem de upload de validação
  * [SIG-334] - Adicionar documentação das APIs de validação de documento no Swagger
  * [SIG-335] - Integração com MoviDesk e JivoChat
  * [SIG-339] - Permitir configurar padrão da opção assinaturas ao mesmo tempo

* Correções de bugs
  * [SIG-307] - Corrigir testes no DevOps
  * [SIG-352] - Erro ao consultar eventos de um usuário
  * [SIG-356] - Erro ao submeter documento se assinatura eletronica estiver desabilitada e isAllowedByDefault for true
  * [SIG-357] - Timeout ao buscar documento com muitos participantes
  * [SIG-358] - Faltando traduções no email de fluxo editado
  * [SIG-359] - Assinatura eletronica em lote está exigindo Web PKI instalado

Atualiza modelo do banco de dados: sim

<a name="v1-5-0" />
### 1.5.0 (2020-06-15)

* Novas funcionalidades
  * [SIG-331] - Enviar email para todos participantes do fluxo após a conclusão do documento
  * [SIG-343] - Assinatura eletronica em lote
  * [SIG-344] - Permitir configurar se a assinatura eletronica aparece marcada por padrão

* Melhorias
  * [SIG-311] - Obrigatoriedade de enviar informação de geolocalização
  * [SIG-318] - Permitir que o participante tenha acesso ao documento após assinar/aprovar na área externa
  * [SIG-326] - Testes automatizados de documento escaneado pelo Scanner
  * [SIG-332] - Adicionar nome da aplicação nas propriedades do PDF
  * [SIG-341] - Esconder versão para impressão

* Correções de bugs
  * [SIG-347] - Corrigir traduções na página de validação de documentos

Atualiza modelo do banco de dados: sim

<a name="v1-4-1" />
### 1.4.1 (2020-06-08)

* Correções de bugs
  * [SIG-313] - Internacionalização errada (en) no email de aprovar e assinar

Atualiza modelo do banco de dados: não

<a name="v1-4-0" />
### 1.4.0 (2020-06-08)

* Novas funcionalidades
  * [SIG-216] - Permitir configuração de instância dos detalhes da Versão para impressão

* Melhorias
  * [SIG-249] - Internacionalizar notificações
  * [SIG-285] - Remover digitalização rápida e alterar comportamento da digitalização
  * [SIG-294] - Enviar email para configurar senha ao cadastrar novos usuários
  * [SIG-312] - Adicionada configuração para definir se o texto da representação visual deve começar no meio do retângulo
  * [SIG-314] - Melhorar configuração de integração com Scanner
  * [SIG-323] - Ativar download em lote
  * [SIG-329] - Adicionar mais eventos

* Correções de bugs
  * [SIG-313] - Status de documento na listagem de pastas está "Pendente" quando está concluído

Atualiza modelo do banco de dados: sim


<a name="v1-3-2" />
### 1.3.2 (2020-05-15)

* Correções de bugs
  * [SIG-310] - Exceções lançadas ao logar caracteres especiais gerados pelo PKI SDK

Atualiza modelo do banco de dados: não


<a name="v1-3-1" />
### 1.3.1 (2020-05-05)

* Correções de bugs
  * [SIG-309] - Esconder opção de download em lote até atualização do Web PKI

Atualiza modelo do banco de dados: não

<a name="v1-3-0" />
### 1.3.0 (2020-05-05)

* Novas funcionalidades
  * [SIG-178] - Download em lote
  * [SIG-187] - Permitir selecionar Padrão de assinatura Cades ou Pades na submissão por API
  * [SIG-190] - Permitir administradores visualizaram documentos de usuários/organizações
  * [SIG-287] - Permitir que aplicações possam pegar link para ação externa

* Melhorias
  * [SIG-161] - Permitir alterar dados do usuário na administração
  * [SIG-193] - Adicionar links para PDF de documentação do usuário
  * [SIG-262] - Melhorias na funcionalidade de Autenticação
  * [SIG-293] - Permitir assinar o termo de adesão com assinatura eletronica
  * [SIG-297] - Adicionar listagem de documentos na administração
  * [SIG-301] - Ajustes de responsividade e remoção de scrolls quando loader é exibido
  * [SIG-302] - Validar Assinaturas PDF feitas no Adobe
  * [SIG-305] - Tratar erro PinValidationFailed do Amplia


* Correções de bugs
  * [SIG-304] - Pedidos de certificado que não podem ser emitidos em Cloud deveriam ser ignorados
  * [SIG-306] - Corrigir envio de notificações por email quando o SMS estiver desabilitado

Atualiza modelo do banco de dados: **sim**


<a name="v1-2-0" />
### 1.2.0 (2020-04-29)

* Novas funcionalidades
  * [SIG-284] - Permitir subir um arquivo para ser validado na tela de validação do documento
  * [SIG-296] - Configurar margens da marcação lateral na versão para impressão


* Melhorias
  * [SIG-225] - Melhorar desempenho da Assinatura em Lote


* Correções de bugs
  * [SIG-292] - Uniformizar exibição do nome e apelido de subscriptions entre os componentes da SPA e Signer
  * [SIG-295] - Corrigir assinatura XAdES sem parâmetros
  * [SIG-298] - Erro ao tentar obter o fuso de Brasília no Linux

Atualiza modelo do banco de dados: **sim**

