![Capa do Projeto](./assets/Z.jpg)

# Linux - Infraestrutura como Código (IaC)

Este projeto contém um script bash que automatiza a criação de usuários, grupos, diretórios e permissões no Linux. O objetivo é fornecer uma maneira fácil de configurar a estrutura de uma máquina Linux com as permissões corretas de maneira rápida e reutilizável.

## Funcionalidades

- Criação de diretórios essenciais: `/publico`, `/adm`, `/ven`, `/sec`
- Criação de grupos: `GRP_ADM`, `GRP_VEN`, `GRP_SEC`
- Criação de usuários com permissões específicas:
  - Grupo `GRP_ADM`: Acesso aos diretórios administrativos
  - Grupo `GRP_VEN`: Acesso aos diretórios de vendas
  - Grupo `GRP_SEC`: Acesso aos diretórios de segurança
- Definição de permissões:
  - `770` para os diretórios administrativos, vendas e segurança
  - `777` para o diretório público, acessível a todos

## Como Usar

Siga estas etapas para executar o script em uma máquina Linux:

1. **Clone o repositório**:
   Abra o terminal e execute o seguinte comando para clonar o repositório.
   ```bash
   git clone https://github.com/Fabisgb/linux-projeto1-iac.git

2. **Acesse a pasta do repositório**:
   ```bash
   cd linux-projeto1-iac

3. **Torne o script executável**: Dê permissão de execução ao arquivo criar_estrutura.sh.
    ```bash
    chmod +x criar_estrutura.sh
  
4. Execute o script: Agora, execute o script para criar a infraestrutura de usuários, grupos, diretórios e permissões:
   ```bash
   ./criar_estrutura.sh

## Detalhes do Script

O script cria os seguintes recursos no Linux:

1. **Diretórios**:
- /publico: Acesso para todos os usuários.
- /adm: Acesso para o grupo GRP_ADM.
- /ven: Acesso para o grupo GRP_VEN.
- /sec: Acesso para o grupo GRP_SEC.

2. **Grupos**:
- GRP_ADM: Grupo para administradores.
- GRP_VEN: Grupo para vendas.
- GRP_SEC: Grupo para segurança.

3. **Usuários**:
Criados com as permissões adequadas para cada grupo.

5. **Permissões**:
- Diretórios /adm, /ven, e /sec:
    Permissões 770 (leitura, escrita e execução para o dono e o grupo, nenhum acesso para outros).

- Diretório /publico:
    Permissões 777 (leitura, escrita e execução para todos).

## Contribuindo

Sinta-se à vontade para contribuir com melhorias ou sugestões. Para isso:

1. Faça um fork deste repositório.
2. Faça suas alterações e melhorias.
3. Envie um pull request com suas mudanças.

## Demonstração

![Demonstração do Script](./assets/demonstracao.gif)

## Licença
Este projeto está licenciado sob a Licença MIT – veja o arquivo [LICENSE](LICENSE) para mais detalhes.

