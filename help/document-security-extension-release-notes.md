---
title: AEM Documento Security for Microsoft Office - Notas de versão
description: Leia as notas de versão antes de instalar AEM Documento Security 6.2 Extension for Microsoft Office.
uuid: f6ab73d4-ac4e-4fff-9bb8-917b75401653
content-type: reference
topic-tags: installing
discoiquuid: c9342c28-8289-4831-a613-4bc03431f557
translation-type: tm+mt
source-git-commit: 403b800eab086d131beb65a496836158778954ee
workflow-type: tm+mt
source-wordcount: '1030'
ht-degree: 0%

---


# AEM Documento Security for Microsoft Office - Notas de versão{#aem-document-security-for-microsoft-office-release-notes}

## Novidades do AEM Documento Security para Microsoft Office {#whats-new-in-aem-document-security-for-microsoft-office}

* **Suporte para o Office 2019**: O Documento Security Extension for Microsoft Office adicionou suporte ao Microsoft Office 2019. Também deve funcionar com aplicativos de desktop do Microsoft Office 2019 instalados como parte do Office 365.

>[!NOTE]
>
>O documento usa os termos Adobe Experience Manager Documento Security for Microsoft Office, Adobe Experience Manager Documento Security Extension for Microsoft Office e Documento Security Extension for Microsoft Office de modo intercambiável.

## Instalação e Configuração AEM Extensão de Segurança do Documento para Microsoft Office {#installing-and-configuring-aem-document-security-extension-for-microsoft-office}

Esta versão do Documento Security Extension for Microsoft Office é compatível com o Adobe LiveCycle Rights Management ES2 e posterior e com o complemento Documento Security para formulários AEM.

Examine as informações neste documento antes de instalar AEM Documento Security Extension for Microsoft Office. Para obter instruções detalhadas de instalação, consulte o artigo [Instalação e Configuração AEM Documento Security Extension for Microsoft Office](installing-configuring-aemdsext.md).

## Problemas corrigidos {#fixed-issues}

* As strings são exibidas verticalmente e as quebras de linha incorretas são adicionadas ao conteúdo. (Ref# CQ-4201054)

## Problemas conhecidos {#known-issues}

### Plug-ins de terceiros não suportados {#third-party-plug-ins-not-supported}

AEM Documento Security Extension for Microsoft Office não funciona com plug-ins de terceiros. Desinstale todos os plug-ins de terceiros do Microsoft Office antes de instalar o Documento Security Extension for Microsoft Office.

### Opções de menu desativadas no Microsoft Word, Excel e PowerPoint {#disabled-menu-options-in-microsoft-word-excel-and-powerpoint}

AEM Documento Security Extension for Microsoft Office usa recursos de proteção incorporados para proteger documentos, planilhas e apresentações. Desativa algumas opções de menu do Excel, Word e PowerPoint.

### Restrições para o Microsoft Office 2013, 2016 e 2019 {#restrictions-for-microsoft-office}

No Microsoft Office, as seguintes opções estão indisponíveis durante uma sessão protegida:

* Microsoft Office 2016 ou Microsoft Office 2019

   * Arquivo > Salvar como
   * Arquivo > Histórico
   * Arquivo > Compartilhar
   * Arquivo > Exportar
   * Arquivo > Publicar
   * Arquivo > Conta
   * Arquivo > Informações > Documento/pasta de trabalho/apresentação do Protect > Criptografar com senha
   * Arquivo > Informações > Documento Protect > Adicionar uma assinatura digital
   * Arquivo > Informações > Documento Protect > Marcar como final
   * Opção Compartilhar na parte superior direita

* Microsoft Office 2013

   * Arquivo > Salvar como
   * Arquivo > Compartilhar
   * Arquivo > Exportar
   * Arquivo > Conta
   * Arquivo > Informações > Documento/pasta de trabalho/apresentação do Protect > Criptografar com senha
   * Arquivo > Informações > Documento Protect > Adicionar uma assinatura digital
   * Arquivo > Informações > Documento Protect > Marcar como final

### Abrindo um documento protegido do SharePoint Server {#opening-a-protected-document-from-sharepoint-server}

Abrindo o documento protegido: Se tentar abrir um documento protegido no Documento Security Extension for Microsoft Office a partir do SharePoint Server sem abrir primeiro o programa do Microsoft Office associado ao tipo de arquivo, como Microsoft Word, Microsoft Excel ou Microsoft PowerPoint, o documento pode não abrir. Uma mensagem de erro é exibida indicando que você instalou o plug-in aplicável. Portanto, é recomendável abrir o programa associado do Microsoft Office antes de abrir um documento protegido no Documento Security Extension for Microsoft Office a partir do SharePoint Server.

(Opcional) É recomendável limpar a pasta de cache antes de abrir um documento protegido no Documento Security Extension for Microsoft Office a partir do SharePoint Server.

Quando você abre um documento protegido do SharePoint Server, todas as permissões do documento são desativadas, independentemente da política aplicada.

### Aplicar uma política com uma marca d&#39;água dinâmica ao arquivo Microsoft Excel 2013, Microsoft Excel 2016 e Microsoft Excel 2019 sem impressora instalada {#apply-a-policy-with-a-dynamic-watermark-to-microsoft-excel-microsoft-excel-and-microsoft-excel-file-with-no-printer-installed}

Quando você aplica uma política com marca d&#39;água dinâmica ao arquivo Microsoft Excel 2013, Microsoft Excel 2016 e Microsoft Excel 2019 em um computador que não tem impressoras instaladas e, em seguida, salva o arquivo, o seguinte erro é exibido: &quot;Erro interno ao aplicar a marca d&#39;água dinâmica.&quot; Esse erro também aparece quando você reabre o arquivo protegido. A marca d&#39;água não é aplicada e não é visível em Visualização > Layout de página.

### Desabilitar a Prevenção de Execução de Dados do Windows para aplicativos do Office compatíveis {#disable-windows-data-execution-prevention-for-supported-office-applications}

É recomendável desativar a configuração DEP (Prevenção de Execução de Dados) do Windows ao usar o Documento Security Extension para aplicativos do Microsoft Office.

### Os arquivos compartilhados do Microsoft Office não podem ser protegidos usando o Documento Security Extension {#shared-microsoft-office-files-cannot-be-protected-using-document-security-extension}

Quando você protege qualquer arquivo compartilhado do Microsoft Office usando o Documento Security Extension, ocorre um erro e o arquivo compartilhado não é protegido.

### Iniciar aplicativos do Office em computadores que contenham o Documento Security Extension for Microsoft Office e McAfee VirusScan {#starting-office-applications-on-a-machine-containing-document-security-extension-for-microsoft-office-and-mcafee-virusscan}

Para garantir que os aplicativos do Office sejam start sem problemas em uma máquina com o Documento Security instalado e o McAfee VirusScan com o On-Access Scan ativado, desative a opção Proteção de estouro de buffer no console do McAfee VirusScan.

### Instalação do Documento Security Extension for Microsoft Office em computadores com um idioma não suportado do Microsoft Office {#installing-document-security-extension-for-microsoft-office-on-a-machine-with-an-unsupported-microsoft-office-language}

Antes de instalar o Documento Security Extension for Microsoft Office em um computador que tenha um aplicativo do Microsoft Office com um idioma sem suporte, abra o aplicativo do Office pelo menos uma vez.

### O botão Sincronizar offline é ativado mesmo quando um usuário não tem permissões offline {#synchronize-offline-button-is-enabled-even-when-a-user-does-not-have-offline-permissions}

O botão Sincronizar off-line está disponível mesmo se o usuário não tiver permissões off-line para o documento. No entanto, selecionar o botão não faz nada.

### Não há suporte para versões de avaliação do Microsoft Office {#no-support-for-trial-versions-of-microsoft-office}

A extensão de Segurança do documento para Microsoft Office não suporta versões de trilha do Microsoft Office. Antes de instalar a extensão, verifique se você instalou uma cópia licenciada do Microsoft Office e se ela está ativada.

### Não é possível abrir arquivos protegidos do Microsoft Office {#unable-to-open-a-protected-microsoft-office-files}

Se a visualização protegida do Microsoft Office estiver ativada, o Rights Management Extension não poderá abrir arquivos do Microsoft Excel (XLS, XLSX) protegidos e arquivos do Microsoft PowerPoint (PPT) protegidos de um local remoto.

### As células do documento do Microsoft Excel que contêm uma imagem ou uma cor de plano de fundo aparecem na parte superior da marca d&#39;água {#cells-of-microsoft-excel-document-containing-an-image-or-background-color-appear-on-top-of-watermark}

Se uma célula de um documento do Microsoft Excel contiver uma imagem ou estiver preenchida com a cor do plano de fundo e uma política de marca d&#39;água dinâmica for aplicada ao documento, a imagem ou a cor do plano de fundo preenchida na célula aparecerão na parte superior da marca d&#39;água e cobrirão a marca d&#39;água.

### Problema de usabilidade com vários certificados {#usability-issue-with-multiple-certificates}

Se vários certificados estiverem presentes no computador cliente e o usuário cancelar a caixa de diálogo de seleção de certificado, a caixa de diálogo será exibida novamente e o usuário terá que cancelar a caixa de diálogo duas vezes.

### O Microsoft PowerPoint permite a edição de documentos protegidos {#microsoft-powerpoint-allows-editing-protected-documents}

Ao tentar editar um documento protegido, o Microsoft PowerPoint exibe uma mensagem, &quot;Você não tem permissão para modificar esse documento. Você não poderá salvar suas alterações.&quot; Depois de fechar a mensagem, os usuários podem continuar a adicionar texto ou editar o documento. Mas as mudanças feitas nos documentos protegidos não são salvas.

O comportamento mencionado acima é o esperado no PowerPoint 2013, PowerPoint 2016 e PowerPoint 2019.