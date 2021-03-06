﻿# Projeto de exemplos em PHP 5.5+

O **Projeto de exemplos em PHP 5.5+** mostra como usar o [Rest PKI](../index.md) junto com o [Web PKI](../../web-pki/index.md) em um projeto usando o **PHP 5.5+** (incluindo 7.x). Isto é
hospedado no GitHub em:

https://github.com/LacunaSoftware/RestPkiSamples/tree/master/PHP/standard

> [!NOTE]
> Para projetos destinados a versões anteriores do PHP, [clique aqui](index.md).

## Executando o projeto

1. [Download do projeto](https://github.com/LacunaSoftware/RestPkiSamples/archive/master.zip) ou clonar o [repositório](https://github.com/LacunaSoftware/RestPkiSamples.git)
1. Gere um token de acesso à API no [REST PKI website](https://pki.rest/)
1. Cole seu token de acesso no arquivo [PHP/standard/config.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/config.php#L21-L24)
1. No prompt de comando, navegue até a pasta `PHP/standard` e execute o comando `composer install` e faça o download das dependências (se você não tiver Composer instalado, pegue [aqui](https://getcomposer.org/))
1. Configurar um site no seu servidor HTTP local apontando para à pasta `PHP/standard`
1. Abrir o arquivo index.php no browser a URL correspondente (dependendo do passo anterior)

## Mapa do projeto

Esta seção lista tem onde encontrar as partes relevantes em cada amostra de recurso no projeto.

<a name="auth" />
### Autentificação com certificado digital

* [authentication.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/authentication.php)
  * JavaScript: [signature-form.js](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/content/js/signature-form.js)
* [authentication-action.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/authentication-action.php)

<a name="pades" />
### Assinatura PAdES com arquivo já no servidor

* [pades-signature.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/pades-signature.php)
  * JavaScript: [signature-form.js](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/content/js/signature-form.js)
* [pades-signature-action.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/pades-signature-action.php)

<a name="pades-upload" />
### Assinatura PAdES com arquivo enviado pelo usuário

Após o upload do arquivo (que é grosseiramente implementado apenas para fins de demonstração em [upload.php]
(https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/upload.php)) é feito o fluxo de controle é o mesmo que na amostra [Assinatura PAdES com arquivo já no servidor](#pades),
mas com parâmetro de URL `userfile` preenchidos.

<a name="pades-cosign" />
### Assinatura conjunta PAdES

Após o fluxo de controle da amostra [Assinatura PAdES com arquivo já no servidor](#pades) está concluído e o link *Co-sign with another certificate* é clicado, o mesmo fluxo de controle é 
repetido, mas agora com parâmetro de URL `userfile` preenchidos.

<a name="pdf-marks" />
### Marcas PAdES

Esse recurso é demonstrado como uma configuração opcional no  [Assinatura PAdES com arquivo já no servidor](#pades), amostra que por padrão começa comentada. Para ativá-lo, remova o comentário da linha a seguir [pades-signature.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/pades-signature.php):

```php
array_push($signatureStarter->pdfMarks, getPdfMark(1));
```

> [!TIP]
> Tente mudar o argumento para a função `getPdfMark()`para ver diferentes configurações de marcas PDF.

O código relevante está no arquivo [util-pades.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/util-pades.php), 
função `getPdfMark()`.

<a name="pades-server" />
### Assinatura PAdES usando chave do servidor

 * [pades-signature-server-key.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/pades-signature-server-key.php)

 <a name="pades-wo-client" />
### Assinatura PAdES sem a comunicação com cliente

Ainda não está disponível neste projeto.

<a name="open-pades" />
### Abrir/validar uma assinatura PAdES existente

* [open-pades-signature.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/open-pades-signature.php)

<a name="print" />
### Versão para impressão

Após o fluxo de controle da amostra [Assinatura PAdES com arquivo já no servidor](#pades) está concluído e o link *Download a printer-friendly version of the signed file* é clicado, o fluxo 
vai para o arquivo [printer-friendly-version.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/printer-friendly-version.php), mas com parâmetro de URL `file` preenchidos.

O PDF gerado contém links para o arquivo [check.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/check.php), que 
mostra detalhes das assinaturas.

<a name="cades" />
### Assinatura CAdES com arquivo já no servidor

* [cades-signature.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/cades-signature.php)
  * JavaScript: [signature-form.js](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/content/js/signature-form.js)
* [cades-signature-action.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/cades-signature-action.php)

<a name="cades-upload" />
### Assinatura CAdES com upload do arquivo pelo usuário

Depois que o upload do arquivo (que é grosseiramente implementado apenas para fins de demonstração no [upload.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/upload.php)) é feito 
o fluxo de controle é o mesmo que na amostra [CAdES signature with file already on server](#cades), mas com parâmetro de URL `userfile` preenchidos.

<a name="cades-cosign" />
### Assinatura conjunta CAdES

Após o fluxo de controle da amostra [CAdES signature with file already on server](#cades) está concluído e o link *Co-sign with another certificate* é clicado, o mesmo fluxo de controle é 
repetido, mas agora com parâmetro de URL `cmsfile` preenchidos.

<a name="cades-server" />
### Assinatura CAdES usando chave do servidor

* [cades-signature-server-key.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/cades-signature-server-key.php)

<a name="open-cades" />
### Abrir/validar uma assinatura CAdES existente

* [open-cades-signature.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/open-cades-signature.php)

<a name="xml-full" />
### Assinatura XML do documento inteiro

* [xml-full-signature.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/xml-full-signature.php)
  * JavaScript: [signature-form.js](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/content/js/signature-form.js)
* [xml-full-signature-action.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/xml-full-signature-action.php)

<a name="xml-element" />
### Assinatura XML de um elemento

* [xml-element-signature.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/xml-element-signature.php)
  * JavaScript: [signature-form.js](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/content/js/signature-form.js)
* [xml-element-signature-action.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/xml-element-signature-action.php)

<a name="xades-element" />
### Assinatura XAdES de um elemento

Não está disponível neste projeto.

<a name="open-xml" />
### Abrir/validar assinatura de um arquivo XML existente

* [open-xml-signature.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/open-xml-signature.php)

<a name="batch" />
### Lote de assinatura PAdES 

* [batch-signature.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/batch-signature.php)
  * JavaScript: [batch-signature-form.js](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/content/js/batch-signature-form.js)
  * AJAX handlers: [batch-signature-start.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/batch-signature-start.php)
    and [batch-signature-complete.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/batch-signature-complete.php)

<a name="batch-optimized" />
### Lote otimizado de assinaturas PAdES

Não está disponível neste projeto.

<a name="batch-cades" />
### Lote de assinaturas CAdES

Não está disponível neste projeto.

<a name="batch-xml-element" />
### Lote de assinaturas XML de elementos no mesmo documento

* [batch-xml-element-signature.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/batch-xml-element-signature.php)
  * JavaScript: [batch-xml-element-signature-form.js](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/content/js/batch-xml-element-signature-form.js)
  * AJAX handlers: [batch-xml-element-signature-start.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/batch-xml-element-signature-start.php)
    and [batch-xml-element-signature-complete.php](https://github.com/LacunaSoftware/RestPkiSamples/blob/master/PHP/standard/batch-xml-element-signature-complete.php)
