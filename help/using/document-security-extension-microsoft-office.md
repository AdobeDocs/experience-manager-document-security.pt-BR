---
title: Introdução ao AEM Document Security Extension para Microsoft® Office
description: Ao usar o Document Security Extension para Microsoft® Office, é possível aplicar configurações de confidencialidade predefinidas a seus arquivos do Microsoft® Office.
uuid: a5428c50-fae3-4823-9e6f-0f5306e7248f
content-type: reference
topic-tags: using
discoiquuid: cf93f9f5-1fb6-4909-815e-0ffb8c6ea6d1
exl-id: 3e07c031-3f88-4bde-bdb3-b136ef5f9527
source-git-commit: 3b6a686966fb8d006bed8cc4a4bf5eebe0dfb030
workflow-type: ht
source-wordcount: '1248'
ht-degree: 100%

---

# Introdução à Extensão de segurança de documentos do AEM para Microsoft® Office{#introduction-to-aem-document-security-extension-for-microsoft-office}

A Extensão de segurança de documentos do Adobe® Experience Manager para Microsoft® Office garante que somente as pessoas autorizadas por você possam usar os arquivos do Word, Excel e PowerPoint que contenham sua propriedade intelectual. Ao usar a Extensão de segurança de documentos para Microsoft® Office, é possível aplicar configurações de confidencialidade predefinidas aos seus arquivos.

O Document Security Extension para Microsoft® Office aprimora o LiveCycle Rights Management e a Segurança de documentos para o Adobe Experience Manager Forms. Ele protege arquivos do Office e habilita o acesso de pessoas autorizadas a arquivos protegidos por política de acordo com as configurações de confidencialidade estabelecidas.

## Como a Segurança de documentos protege a propriedade intelectual {#how-document-security-protects-intellectual-property}

A Segurança de documentos garante que somente as pessoas que você autorizar possam usar arquivos que contenham sua propriedade intelectual. Com a Segurança de documentos, você pode proteger arquivos usando políticas de confidencialidade. Uma *política* é uma coleção de informações que inclui configurações de confidencialidade e uma lista de usuários autorizados. As configurações que você especificar em uma política determinam como um recipient pode usar um arquivo ao qual a política foi aplicada. Por exemplo, você pode especificar se os recipients podem imprimir, copiar textos ou salvar alterações.

Administradores e usuários da Segurança de documentos criam políticas. Os administradores criam políticas organizacionais que são disponibilizadas a todos os usuários autorizados. Os administradores ou coordenadores de definições de políticas também podem criar grupos de políticas chamados *conjuntos de políticas*, que ficam disponíveis para um subconjunto de usuários. Os usuários podem criar suas próprias políticas, que somente eles podem usar. Administradores, coordenadores de conjunto de políticas e usuários criam políticas usando as páginas da Web de Segurança de documentos.

Embora as políticas sejam armazenadas na Segurança de documentos, elas podem ser aplicadas a arquivos por meio do Word, Excel ou PowerPoint. Ao aplicar uma política a um arquivo, a informação que o arquivo contém é protegida pelas configurações de confidencialidade especificadas na política. Ao distribuir o arquivo protegido por política, somente destinatários autorizados podem acessar o seu conteúdo.

Usar uma política para proteger um arquivo garante o controle contínuo sobre ele, mesmo depois de distribuí-lo. Você pode auditar eventos para rastrear quando e como os destinatários usam o seu arquivo. Também é possível fazer alterações na política, impedir que usuários continuem acessando o arquivo e alterar a política anexada a ele.

## Como as políticas funcionam {#how-policies-work}

As políticas contêm informações sobre os usuários autorizados e as configurações de confidencialidade a serem aplicadas à propriedade intelectual. A Segurança de documentos reconhece usuários incluídos em uma lista vinculada do LDAP ou do Active Directory. Os usuários também podem ser pessoas convidadas a se registrar na Segurança de documentos ou para as quais o administrador criou uma conta.

As configurações de confidencialidade em uma política determinam como os recipients podem usar arquivos protegidos pela política. Por exemplo, as políticas especificam se os recipients podem imprimir arquivos, copiar conteúdos para outros arquivos ou salvar alterações em arquivos protegidos. As políticas também podem especificar configurações de confidencialidade diferentes para vários usuários.

Ao aplicar uma política a um arquivo, a informação que o arquivo contém é protegida pelas configurações de confidencialidade especificadas na política. Ao distribuir o arquivo, a Segurança de documentos autentica os recipients que tentarem abrir o arquivo e autoriza o acesso de acordo com os privilégios especificados na política.

Depois que uma política é aplicada a um arquivo, as configurações de confidencialidade da política podem ser alteradas a qualquer momento. É possível adicionar ou remover usuários autorizados, ou alterar seus privilégios após terem recebido o arquivo. A política aplicada ao arquivo pode ser alterada. Além disso, o acesso pode ser revogado para que qualquer pessoa com uma cópia do arquivo não possa mais abri-lo.

Se a política permitir acesso offline, os destinatários também poderão usar arquivos protegidos por política offline (sem uma conexão ativa com a Internet ou com uma rede) pelo período especificado na política.

## Como arquivos protegidos por política funcionam {#how-policy-protected-files-work}

Para que alguém abra e use arquivos do Word, Excel e PowerPoint protegidos por política, essa deve incluir essa pessoa como um destinatário. Ou deve permitir acesso anônimo. E a pessoa deve ter o Document Security Extension para Microsoft® Office instalado. Para fornecer um arquivo protegido por política a uma pessoa que não tenha o Document Security Extension para Microsoft® Office, é possível ceder-lhe uma cópia do software. Ou você pode informar como baixá-lo em seu site. Se você não tiver o instalador, é possível baixá-lo da [página de downloads](https://experienceleague.adobe.com/pt-br/docs/experience-manager-document-security/using/download-installer).

Quando alguém tentar abrir um arquivo protegido por política, o Document Security Extension para Microsoft® Office se conecta à Segurança de documentos para autenticar o usuário. Se a Segurança de documentos estiver configurada para auditar o uso do arquivo, o usuário verá uma notificação indicando que o uso do arquivo está sendo auditado. A Segurança de documentos determina quais permissões de arquivo conceder ao usuário, e o usuário poderá então usar o arquivo de acordo com as configurações de política, sob estas condições:

* Pelo período de validade especificado na política.
* Até que um administrador ou a pessoa que aplicou a política revogue o acesso ao arquivo ou altere a política.

  Se a pessoa que aplicou a política alterar a política ou revogar o acesso ao arquivo, as permissões do usuário para o arquivo serão alteradas ou removidas, mesmo que o usuário já tenha o arquivo. Se o próprio arquivo for revogado, um URL poderá ser fornecido ao usuário para que ele obtenha uma cópia atualizada.

  Se a política permitir acesso offline, usuários poderão abrir arquivos protegidos por política sem uma conexão com a internet ou com uma rede durante o período de concessão offline especificado. Ao término do período de concessão offline, o usuário deverá se conectar à internet e sincronizar com a Segurança de documentos, o que inicia um novo período de concessão.

  Se a política permitir acesso offline, usuários poderão abrir arquivos protegidos por política sem uma conexão com a internet ou com uma rede durante o período de concessão offline especificado. Eventos, como tentativas de abrir o novo arquivo, também são auditados e registrados da mesma maneira que o arquivo original.

## Uso da Segurança de documentos para proteger seus arquivos {#using-document-security-to-protect-your-files}

Você pode usar políticas para proteger seus arquivos em várias situações.

Por exemplo, um fabricante que está aceitando ofertas de fornecedores de peças para um novo produto. O fabricante deve fornecer aos proponentes as informações proprietárias necessárias para finalizar suas propostas. O fabricante usa a Segurança de documentos para proteger os arquivos com uma política que permite aos fornecedores abrir os arquivos e visualizar as informações. No entanto, os fornecedores são impedidos de alterar, imprimir ou copiar os arquivos e qualquer pessoa que não tenha permissão é impedida de abri-los.

Após aceitar uma oferta, o fabricante atualiza a política para conceder a quem a fez as permissões para imprimir, copiar e salvar as alterações localmente. O fabricante também remove os ofertantes vencidos, revogando sua permissão para abrir os arquivos.

Ao trabalhar com o proponente escolhido, os engenheiros do fabricante alteram algumas das especificações de design nos arquivos. Para publicar as novas especificações, o fabricante revoga o acesso a alguns dos arquivos e publica novas versões. Quando os engenheiros do fornecedor escolhido tentarem abrir o arquivo, verão uma mensagem informando que o acesso ao arquivo foi revogado. A mensagem contém um URL no qual eles podem baixar uma nova versão do arquivo.

## Informações adicionais {#additional-information}

Os recursos nesta tabela podem ajudar você a saber mais sobre a Segurança de documentos do AEM:

<table >
 <tbody>
  <tr>
   <th><p>Para obter informações sobre</p> </th>
   <th><p>Consulte</p> </th>
  </tr>
  <tr>
   <td><p>Ajuda do administrador do AEM Forms</p> </td>
   <td><p>Na página <a href="https://experienceleague.adobe.com/pt-br/docs/experience-manager-65/content/forms/administrator-help/get-started/configure-general-aem-forms-settings">Ajuda do administrador</a> ou na página de administração de Segurança de documentos, clique no link Ajuda, no canto superior direito de uma página.</p> </td>
  </tr>
  <tr>
   <td><p>Atualizações de patches, notas técnicas e informações adicionais sobre esta versão do produto</p> </td>
   <td><p><a href="https://experienceleague.adobe.com/pt-br?support-solution=General&amp;support-tab=home&amp;lang=pt-BR#support">Suporte técnico da Experience Cloud</a></p> </td>
  </tr>
 </tbody>
</table>
