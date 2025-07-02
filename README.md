
# Resumo das Aulas - Design e Arquitetura de Software 2
**Professor:**  Walter Silvestre Coan 

**Aluno:**  Karim Galil Tamimi Alzeben

---

### Aula 24/02 - Well-Architected Framework (AWS)
- **Excelência Operacional:** executar, monitorar e melhorar continuamente.
- **Segurança:** proteção contra ameaças internas e externas.
- **Confiabilidade:** resiliência e capacidade de recuperação.
- **Eficiência de Performance:** alocação eficiente de recursos.
- **Otimização de Custos:** balancear qualidade com custo.
- **Sustentabilidade:** reduzir impactos ambientais.

---

### Aula 27/02 - Trade-Offs e Boas Práticas de Design
- **Trade-Offs:** decisões que equilibram consistência, durabilidade, espaço e performance.
- **Escalabilidade e Elasticidade:** crescer e reduzir com base na demanda.
- **Auto Scaling:** automatização para escalar recursos automaticamente.
- **Infraestrutura como Código:** automatizar provisionamento.
- **Recursos descartáveis:** instâncias que podem ser recriadas rapidamente.
- **Baixo acoplamento:** facilitar substituição de componentes.
- **Design de serviços, não de servidores:** foco em funcionalidades.
- **Escolha do banco de dados:** baseado em requisitos de acesso, modelo e volume.

---

### Aula 06/03 - Resiliência, Cache e Infraestrutura AWS
- **Evitar ponto único de falha:** usar múltiplas instâncias e replicação.
- **Cache:** melhora performance e reduz carga em banco.
- **Trade-Offs entre custo e disponibilidade.**
- **Infraestrutura global:**
  - Regiões
  - Zonas de Disponibilidade
  - Local Zones
  - Data Centers

---

### Aula 10/03 - Segurança e Acesso na AWS
- **POPs / Edge Locations:** pontos de entrega de conteúdo.
- **Segurança:** responsabilidade compartilhada.
- **Autenticação e Autorização.**
- **Privilégio mínimo.**
- **Criptografia de dados.**

---

### Aula 13/03 - IAM e Gerenciamento de Acesso
- **Modelo de responsabilidade compartilhada.**
- **IAM:** gerenciamento de usuários, grupos e permissões.
- **Autenticação vs Autorização.**
- **Acesso via console ou programático.**

---

### Aula 17/03 - Policies e S3
- **Policy de Identidade vs Policy de Recurso.**
- **Amazon S3:** armazenamento em objeto, escalável, até 5TB por objeto.

---

### Aula 20/03 - S3: Casos de Uso e Classes
- **Casos de uso:** sites estáticos, análise financeira, recuperação de desastres.
- **Criptografia padrão.**
- **Uploads:** via web, CLI, API e Multipart.
- **AWS Transfer Family.**
- **Classes de armazenamento:**
  - S3 Standard
  - S3 Intelligent-Tiering
  - S3 IA e One-Zone IA
  - Glacier / Deep Archive

---

### Aula 24/03 - Lifecycle, Versionamento e CORS
- **Lifecycle:** transição automática entre classes.
- **Versionamento de objetos.**
- **CORS:** configurações de acesso entre origens diferentes.

---

### Aula 27/03 e 31/03 - Prática com S3
- Implementação de buckets, políticas, uploads, versionamento e CORS.

---

### Aula 03/04 - EC2, EBS e AMI
- **EC2:** instâncias sob demanda para computação escalável.
- **EBS:** volumes persistentes de armazenamento.
- **AMI:** imagens de máquinas para replicação de ambiente.
- **Modelos de execução:** ECS, EKS, Lambda, Beanstalk, Lightsail.

---

### Aula 07/04 - Placement e Compra de Instâncias
- **Placement Groups:**
  - Cluster (baixa latência)
  - Spread (tolerância a falhas)
  - Partition (isolamento por partições)
- **Modelos de Compra EC2:**
  - On-Demand
  - Reserved
  - Savings Plans
  - Spot (instâncias ociosas com até 90% de desconto)

---

### Aula 10/04 - RDS e Bancos Relacionais vs Não-Relacionais
- **Amazon RDS:** banco relacional gerenciado com backup, failover e escalabilidade.
- **Bancos Relacionais:** consistência e ACID (MySQL, PostgreSQL etc).
- **Bancos Não-Relacionais:** escaláveis, flexíveis (DynamoDB, MongoDB etc).
- **Critérios de escolha:** tipo de dado, padrão de acesso, consistência e volume.


RDS: serviço de banco relacional gerenciado (MySQL, PostgreSQL, Oracle, etc.).

Não-Relacionais: bancos como DynamoDB, MongoDB, voltados para dados flexíveis e escaláveis.

---

# Segundo Bimestre

---

## Aula 05/05 – Redes Básicas na Nuvem

### VPC (Virtual Private Cloud)
Cria uma rede isolada dentro da AWS, onde você pode lançar recursos de forma segura. Permite total controle sobre IPs, sub-redes, rotas e segurança.

### CIDR (Classless Inter-Domain Routing)
Define o bloco de endereços IP da VPC (ex: 10.0.0.0/16). Um número menor após a barra representa mais IPs disponíveis.

### Subnet Pública
Sub-rede com acesso direto à internet através de um Internet Gateway. Utilizada para recursos que precisam estar acessíveis externamente, como servidores web.

---

## Aula 12/05 – Laboratórios Práticos

### Laboratórios Canvas
- Guided Lab: Creating a Virtual Private Cloud ✔️ Nota: 50.4/56
- Challenge Lab (Café): Creating a VPC Networking Environment for the Café ✔️ Nota: 45/56

---

## Aula 15/05 – Reforço de VPC

### Laboratórios Canvas (Revisão e prática)
- Guided Lab: Creating a Virtual Private Cloud ✔️ Nota: 50.4/56
- Challenge Lab (Café): Creating a VPC Networking Environment for the Café ✔️ Nota: 45/56

---

## Aula 19/05 – Conectividade entre Redes

### VPC Peering
Permite a comunicação entre duas VPCs, mesmo em contas ou regiões diferentes. Ideal para integrar diferentes ambientes de forma segura e privada.

### AWS VPN Site-to-Site
Conexão criptografada entre a AWS e um data center local (on-premises) via internet pública.

### AWS Direct Connect
Conexão física dedicada entre a AWS e o seu ambiente local. Garante menor latência e maior estabilidade em comparação com VPN.

---

## Aula 26/05 – Identidade e Acesso

### IAM Groups
Conjunto de usuários IAM com políticas de permissão aplicadas em grupo, facilitando o gerenciamento de acesso.

### IAM Roles + AWS STS
- Roles: Concedem permissões temporárias a usuários, serviços ou contas.
- STS (Security Token Service): Gera credenciais temporárias seguras com validade limitada.

### AWS Cognito
Serviço de gerenciamento de identidade para autenticação de usuários em aplicações web e mobile. Suporta login com redes sociais e provedores externos.

---

## Aula 29/05 – Criptografia

### Criptografia Simétrica
Usa a mesma chave para criptografar e descriptografar. Rápida, ideal para dados armazenados. Exemplo: AES.

### Criptografia Assimétrica
Utiliza um par de chaves (pública e privada). Mais segura para troca de dados entre partes. Exemplo: RSA.

---

## Aula 09/06 – Alta Disponibilidade

### Laboratórios Canvas
- Guided Lab: Creating a Highly Available Environment ✔️ Nota: 41.07/56
- Challenge Lab (Café): Creating a Scalable and Highly Available Environment for the Café ✔️ Nota: 56/56

---

## Aula 12/06 – Continuação da Alta Disponibilidade

### Laboratórios Canvas
- Guided Lab: Creating a Highly Available Environment ✔️ Nota: 41.07/56
- Challenge Lab (Café): Creating a Scalable and Highly Available Environment for the Café ✔️ Nota: 56/56

---

## Aula 16/06 – Balanceamento e Resolução de Nomes

### Load Balancer
Distribui automaticamente o tráfego entre várias instâncias para garantir desempenho e tolerância a falhas. Tipos: ALB, NLB, GLB.

### DNS (Domain Name System)
Resolve nomes de domínio em endereços IP. O serviço Amazon Route 53 fornece DNS escalável, seguro e com integração à AWS.

---

## Aula 23/06 – Infraestrutura como Código (IaC)

### IaC (Infrastructure as Code)
Permite definir e provisionar a infraestrutura via código, garantindo consistência, automação e versionamento.  
Ferramentas populares:
- AWS CloudFormation (nativo da AWS)
- Terraform (multi-cloud)

---

