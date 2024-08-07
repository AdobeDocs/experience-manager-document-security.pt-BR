---
title: AEM Document Security for Microsoft Office - Notas de versão
description: Leia as notas de versão antes de instalar o AEM Document Security Extension 6.2 for Microsoft Office.
uuid: f6ab73d4-ac4e-4fff-9bb8-917b75401653
content-type: reference
topic-tags: installing
discoiquuid: c9342c28-8289-4831-a613-4bc03431f557
exl-id: 582f10bb-60d2-46ed-b81d-5818a040edc6
source-git-commit: 3b6a686966fb8d006bed8cc4a4bf5eebe0dfb030
workflow-type: ht
source-wordcount: '1010'
ht-degree: 100%

---

# Segurança de Documentos do AEM para Microsoft Office - Notas de versão{#aem-document-security-for-microsoft-office-release-notes}

## Novidades na Segurança de Documentos do AEM para Microsoft Office {#whats-new-in-aem-document-security-for-microsoft-office}

* **Compatibilidade com o Office 2019**: a extensão Document Security for Microsoft Office agora é compatível com o Microsoft Office 2019. Também deve funcionar com aplicativos de desktop do Microsoft Office 2019 instalados como parte do Office 365.

>[!NOTE]
>
>O documento usa os seguintes termos alternadamente:
>
>* Segurança de documentos do Adobe Experience Manager para Microsoft Office
>* Adobe Experience Manager Document Security Extension para Microsoft Office
>* Document Security Extension para Microsoft Office

## Instalação e configuração da Extensão de Segurança de Documentos do AEM para Microsoft Office {#installing-and-configuring-aem-document-security-extension-for-microsoft-office}

Esta versão do Document Security Extension for Microsoft Office é compatível com o Adobe LiveCycle Rights Management ES2 e posterior, e com o complemento Segurança de documentos do AEM Forms.

Examine as informações neste documento antes de instalar o AEM Document Security Extension for Microsoft Office. Para obter instruções detalhadas de instalação, consulte o artigo [Instalação e configuração do AEM Document Security Extension para Microsoft Office](installing-configuring-aemdsext.md).

## Problemas corrigidos {#fixed-issues}

* As strings são exibidas verticalmente e quebras de linha incorretas são adicionadas ao conteúdo. (CQ-4201054)

## Problemas conhecidos {#known-issues}

### Plug-ins de terceiros incompatíveis {#third-party-plug-ins-not-supported}

O AEM Document Security Extension for Microsoft Office não funciona com plug-ins de terceiros. Desinstale todos os plug-ins de terceiros do Microsoft Office antes de instalar o Document Security Extension para Microsoft Office.

### Opções de menu desabilitadas no Microsoft Word, Excel e PowerPoint {#disabled-menu-options-in-microsoft-word-excel-and-powerpoint}

O AEM Document Security Extension for Microsoft Office usa recursos de proteção incorporados para proteger documentos, planilhas e apresentações. Ele desativa algumas opções de menu do Excel, Word e PowerPoint.

### Restrições para o Microsoft Office 2013, 2016 e 2019 {#restrictions-for-microsoft-office}

No Microsoft Office, as seguintes opções estão indisponíveis durante uma sessão protegida:

* Microsoft Office 2016 ou Microsoft Office 2019

   * Arquivo > Salvar como
   * Arquivo > Histórico
   * Arquivo > Compartilhar
   * Arquivo > Exportar
   * Arquivo > Publicar
   * Arquivo > Conta
   * Arquivo > Informações > Proteger Documento/Pasta de trabalho/Apresentação > Criptografar com senha
   * Arquivo > Informações > Proteger documento > Adicionar uma assinatura digital
   * Arquivo > Informações > Proteger documento > Marcar como final
   * Opção Compartilhar na parte superior direita

* Microsoft Office 2013

   * Arquivo > Salvar como
   * Arquivo > Compartilhar
   * Arquivo > Exportar
   * Arquivo > Conta
   * Arquivo > Informações > Proteger Documento/Pasta de trabalho/Apresentação > Criptografar com senha
   * Arquivo > Informações > Proteger documento > Adicionar uma assinatura digital
   * Arquivo > Informações > Proteger documento > Marcar como final

### Abertura de um documento protegido do SharePoint Server {#opening-a-protected-document-from-sharepoint-server}

Para abrir um documento protegido do SharePoint Server no Document Security Extension para Microsoft Office, primeiro abra o programa associado do Microsoft Office (Word, Excel ou PowerPoint) ou o documento pode não abrir. Uma mensagem de erro é exibida indicando que você deve instalar o plug-in aplicável. Portanto, é recomendável abrir o programa associado do Microsoft Office antes de abrir um documento protegido do SharePoint Server no Document Security Extension for Microsoft Office.

(Opcional) É recomendável limpar a pasta de cache antes de abrir um documento protegido do SharePoint Server no Document Security Extension for Microsoft Office.

Ao abrir um documento protegido do SharePoint Server, todas as permissões do documento são desativadas, independentemente da política aplicada.

### Aplicação de uma política com uma marca d&#39;água dinâmica a um arquivo do Microsoft Excel 2013, 2016 e 2019 sem uma impressora instalada {#apply-a-policy-with-a-dynamic-watermark-to-microsoft-excel-microsoft-excel-and-microsoft-excel-file-with-no-printer-installed}

Aplicar uma política com marca d&#39;água dinâmica a arquivos do Excel 2013, 2016 ou 2019 em um computador sem impressoras instaladas resulta no erro: “Erro interno ao aplicar marca d&#39;água dinâmica”. Esse erro também aparece ao reabrir o arquivo protegido. A marca d&#39;água não é aplicada e não é visível em Visualização > Layout da página.

### Desativação da Prevenção de Execução de Dados do Windows para aplicativos compatíveis do Office {#disable-windows-data-execution-prevention-for-supported-office-applications}

É recomendável desativar a configuração DEP (Prevenção de Execução de Dados) do Windows ao usar o Extensão de Segurança de Documentos para aplicativos do Microsoft Office.

### Os arquivos compartilhados do Microsoft Office não podem ser protegidos com a Extensão de Segurança de Documentos {#shared-microsoft-office-files-cannot-be-protected-using-document-security-extension}

Ao tentar proteger qualquer arquivo compartilhado do Microsoft Office usando a Extensão de Segurança de Documentos, um erro ocorrerá e o arquivo compartilhado não será protegido.

### Inicialização de aplicativos do Office em computadores que contenham a Extensão de Segurança de Documentos para Microsoft Office e McAfee VirusScan {#starting-office-applications-on-a-machine-containing-document-security-extension-for-microsoft-office-and-mcafee-virusscan}

Para garantir que os aplicativos do Office sejam inicializados sem problemas em um computador que contenha a Segurança de documentos e o McAfee VirusScan (com o On-Access Scan habilitado), desabilite a opção Proteção de sobrecarga de buffer no console do McAfee VirusScan.

### Instalação da Extensão de Segurança de Documentos para Microsoft Office em computadores com um idioma não compatível do Microsoft Office {#installing-document-security-extension-for-microsoft-office-on-a-machine-with-an-unsupported-microsoft-office-language}

Antes de instalar a Extensão de Segurança de Documentos do AEM para Microsoft Office em um computador que tenha um aplicativo do Microsoft Office com um idioma não compatível, abra o aplicativo do Office pelo menos uma vez.

### O botão Sincronizar offline fica habilitado mesmo quando o usuário não tem permissões offline {#synchronize-offline-button-is-enabled-even-when-a-user-does-not-have-offline-permissions}

O botão Sincronizar offline está disponível mesmo se o usuário não tiver permissões offline para o documento. No entanto, selecionar o botão não faz nada.

### Não há suporte para versões de avaliação do Microsoft Office {#no-support-for-trial-versions-of-microsoft-office}

O Document Security Extension para Microsoft Office não é compatível com versões de avaliação do Microsoft Office. Antes de instalar a extensão, verifique se você instalou uma cópia licenciada do Microsoft Office e se ela está ativada.

### Não é possível abrir arquivos protegidos do Microsoft Office {#unable-to-open-a-protected-microsoft-office-files}

Se a visualização protegida do Microsoft Office estiver habilitada, a Extensão de Gerenciamento de Direitos não poderá abrir arquivos protegidos do Microsoft Excel (XLS, XLSX) e do Microsoft PowerPoint (PPT) de locais remotos.

### Células com uma imagem ou uma cor de fundo de uma planilha do Microsoft Excel aparecem sobre a marca d&#39;água {#cells-of-microsoft-excel-document-containing-an-image-or-background-color-appear-on-top-of-watermark}

Se uma célula em um documento do Excel tiver uma imagem ou cor de fundo e uma marca d&#39;água dinâmica for aplicada, a imagem ou cor cobrirá a marca d&#39;água. Essa abordagem significa que a marca d&#39;água é coberta pela imagem ou cor de fundo na célula.

### Problema de usabilidade com vários certificados {#usability-issue-with-multiple-certificates}

Se houver vários certificados no computador cliente e a caixa de diálogo de seleção de certificado for cancelada, ela será exibida novamente. A caixa de diálogo precisa ser cancelada duas vezes.

### Microsoft PowerPoint permite a edição de documentos protegidos {#microsoft-powerpoint-allows-editing-protected-documents}

Ao tentar editar um documento protegido, o Microsoft PowerPoint exibe a mensagem: “Você não tem permissão para modificar esse documento. Não é possível salvar as alterações.” Após fechar a mensagem, os usuários podem continuar a adicionar texto ou editar o documento. Mas as mudanças feitas nos documentos protegidos não são salvas.

O comportamento mencionado acima ocorre PowerPoint 2013, PowerPoint 2016 e PowerPoint 2019.
