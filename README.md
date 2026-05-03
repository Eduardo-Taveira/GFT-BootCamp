## Gerenciamento de Instâncias EC2: AMIs e Snapshots

## Descrição do Projeto
Este repositório contém a documentação e os passos práticos realizados durante o laboratório de Gerenciamento de Instâncias EC2 na AWS. O foco principal deste desafio foi compreender e aplicar conceitos de resiliência e backup na nuvem, utilizando Amazon Machine Images (AMIs) e Snapshots do Amazon EBS.

O objetivo é demonstrar a capacidade de criar, fazer backup e restaurar servidores virtuais, habilidades essenciais para manter a alta disponibilidade de aplicações e proteger dados críticos contra falhas.

## Tecnologias Utilizadas
*   Amazon EC2 (Elastic Compute Cloud): Provisionamento da máquina virtual.
*   Amazon EBS (Elastic Block Store): Armazenamento em bloco de alta performance.
*   AWS Management Console: Interface para gerenciamento da infraestrutura.
*   Git & GitHub: Versionamento e documentação do projeto.

## Passos Realizados

Ao longo do laboratório, as seguintes etapas foram executadas:

1.  Lançamento da Instância EC2 Base: 
    - Criação de uma instância EC2 (ex: t2.micro) selecionando a imagem do sistema operacional e configurando as chaves de acesso (Key Pair) e o Grupo de Segurança (Security Group).
2.  Criação do Snapshot EBS:
    -   Navegação até a seção do Elastic Block Store.
    -   Geração de um Snapshot manual do volume anexado à instância EC2, criando um backup pontual do disco.
3.  Criação de uma AMI Personalizada:
    -   A partir da instância em execução (ou do Snapshot), foi gerada uma nova Amazon Machine Image. 
    -   Essa AMI serve como um "molde" contendo o sistema operacional e todas as configurações atuais do servidor.
4.  Restauração e Novo Lançamento (Testando o Backup):
    -   Lançamento de uma nova instância EC2 utilizando a AMI personalizada criada no passo anterior.
    -   Resultado: Validação de que o novo servidor é uma réplica exata do servidor original, comprovando o sucesso da estratégia de backup.

## Evidências Visuais

As capturas de tela comprovando a execução de cada etapa estão organizadas na pasta `/images` deste repositório.

   [`/images/01-ec2-running.png`](./images/01-ec2-running.png) - Instância original em execução.
   [`/images/02-snapshot-created.png`](./images/02-snapshot-created.png) - Snapshot do volume EBS concluído.
   [`/images/03-ami-available.png`](./images/03-ami-available.png) - AMI personalizada listada no painel.
   [`/images/04-ec2-restored.png`](./images/04-ec2-restored.png) - Nova instância criada a partir da AMI.

---
**Autor:** Fabrício
*Estudante de Desenvolvimento Web e entusiasta em Cloud Computing e Automação de Infraestrutura.*
