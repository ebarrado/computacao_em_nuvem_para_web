# Hospedar um aplicativo Web com o Serviço de Aplicativo do Azure

## Serviço de Aplicativo do Azure

O Azure App Service é um serviço de Plataforma como Serviço (PaaS) utilizado para criar, publicar e hospedar aplicações web, APIs REST e back-ends de aplicativos móveis na nuvem.

A Microsoft administra a infraestrutura, permitindo que o desenvolvedor se concentre no código da aplicação, sem precisar configurar servidores, sistema operacional ou atualizações de segurança.

Principais características
- Hospedagem de aplicações em Windows ou Linux.
- Suporte a linguagens como Python, Java, PHP, Node.js, .NET e Ruby.
- Possibilidade de executar aplicações em contêineres Docker.
- Publicação por GitHub, Azure DevOps, Git, VS Code ou arquivo ZIP.
- Criação de fluxos de CI/CD para implantação automática.
- Certificados HTTPS e domínios personalizados.
Autenticação integrada com o Microsoft Entra ID e outros provedores.
- Integração com bancos de dados e outros serviços do Azure.
- Monitoramento com Azure Monitor e Application Insights.
- Escalabilidade manual ou automática.
- Slots de implantação para testar novas versões antes de colocá-las em produção.

#### Aplicativo × Plano do Serviço de Aplicativo

| Componente                         | Função                                                                       |
| ---------------------------------- | ---------------------------------------------------------------------------- |
| **Aplicativo Web**                 | Contém o código, as configurações e os arquivos da aplicação                 |
| **Plano do Serviço de Aplicativo** | Define os recursos computacionais, a região, o sistema operacional e o preço |


Vários aplicativos podem utilizar o mesmo plano e compartilhar seus recursos.

### Escalabilidade

O serviço oferece duas maneiras principais de aumentar a capacidade:

- **Escala vertical**: aumentar memória, processamento e recursos da instância.
- **Escala horizontal**: adicionar mais instâncias para distribuir os acessos.


### Slots de implantação

Os slots permitem manter ambientes separados, como:

- Produção;
- Homologação;
- Desenvolvimento.

Uma nova versão pode ser publicada no slot de homologação, testada e depois trocada com o ambiente de produção, reduzindo o risco e o tempo de indisponibilidade.

### Segurança

O Azure App Service oferece:

- HTTPS;
- Certificados TLS;
- Identidade gerenciada;
- Controle de acesso com RBAC;
- Restrições de acesso por rede;
- Integração com redes virtuais;
- Armazenamento seguro de configurações e segredos.

### Exemplo de utilização

Uma empresa desenvolve uma API em Python para consultar produtos. Essa API pode ser publicada no Azure App Service e configurada para:

- Conectar-se ao Azure SQL Database.
- Autenticar usuários com o Microsoft Entra ID.
- Aumentar automaticamente o número de instâncias quando houver muitos acessos.
- Registrar erros e desempenho no Application Insights.


## Referências

- [Hospedar um aplicativo Web com o Serviço de Aplicativo do Azure](https://learn.microsoft.com/pt-br/training/modules/host-a-web-app-with-azure-app-service/)