---
title: Solução de problemas do AEM Document Security Extension for Microsoft Office
description: Se você tiver problemas ao instalar, configurar ou usar o AEM Document Security Extension for Microsoft Office, siga as instruções listadas neste documento.
uuid: 61001ca8-a25a-4879-98ac-563a6eb126e7
contentOwner: khsingh
content-type: reference
topic-tags: using
discoiquuid: bdc3f174-e417-4d3e-b3af-972cdcc10133
exl-id: 98f24032-0774-47f8-bcc5-1ee37b417833
source-git-commit: 3b6a686966fb8d006bed8cc4a4bf5eebe0dfb030
workflow-type: ht
source-wordcount: '284'
ht-degree: 100%

---

# Solução de problemas da Extensão de Segurança de Documentos do AEM para Microsoft Office{#troubleshooting-aem-document-security-extension-for-microsoft-office}

## Solução de problemas de instalação e configuração {#troubleshootinginstallationandconfiguration}

Se está com problemas para instalar e configurar o AEM Document Security Extension para Microsoft Office, verifique se você seguiu cuidadosamente as instruções listadas na seção “antes de instalar” do artigo de [instalação](installing-configuring-aemdsext.md).

Se você instalou e configurou tudo de acordo com a documentação, analise as seções a seguir para ver problemas semelhantes aos que você está enfrentando.

### O Document Security Extension não consegue carregar aplicativos do Microsoft Office {#document-security-extension-fails-to-load-for-microsoft-office-applications}

A propriedade LoadBehavior no Registro do Windows especifica o comportamento de tempo de execução do plug-in de segurança de documentos. Se a propriedade LoadBehavior estiver definida como 3, todos os plug-ins serão carregados automaticamente. Antes de instalar o Document Security Extension para Microsoft Office, verifique se o valor da propriedade LoadBehavior está definido como 3.

1. Faça o backup do Registro do Windows antes de fazer alterações. Para obter instruções detalhadas, consulte [Como modificar o Registro do Windows](https://learn.microsoft.com/pt-br/troubleshoot/windows-server/performance/windows-registry-advanced-users).
1. No Editor de Registro, vá para HKEY_CURRENT_USER\Software\Microsoft\Office\Word\Addins\Adobe.DRMIntegration.WordAddin ou HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Word\Addins\Adobe.DRM.
1. Defina o valor da propriedade **LoadBehavior** como 3.

1. Feche o Editor de registro.

Para obter informações detalhadas sobre LoadBehavior, consulte o artigo [Entradas de registro para suplementos VSTO](https://learn.microsoft.com/pt-br/visualstudio/vsto/registry-entries-for-vsto-add-ins?view=vs-2022&amp;redirectedfrom=MSDN#LoadBehavior).

## Solução de problemas de tarefas administrativas {#admintasks}

Esta seção discute possíveis problemas com a Extensão de Segurança de Documentos do AEM instalada.

### Os aplicativos do Microsoft Office são inicializados com problemas ao instalar a Extensão de Segurança de Documentos {#microsoft-office-applications-dont-start-smoothly-on-installing-document-security-extension}

Para garantir que os aplicativos do Office sejam inicializados sem problemas com o Document Security Extension instalado e o McAfee VirusScan com On-Access Scan habilitado, desabilite a opção Proteção de sobrecarga de buffer no console do McAfee VirusScan.
