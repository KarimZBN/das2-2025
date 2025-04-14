
# Resumo das Aulas - Design e Arquitetura de Software 2
**Professor:**  Walter Silvestre Coan 

**Aluno:**  Karim Galil Tamimi Alzeben

---

### Aula 24/02 - Well-Architected Framework (AWS)
Introdução ao AWS Well-Architected Framework, que define seis pilares essenciais para desenvolvimento de sistemas na nuvem:
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

Discutimos como escolher o banco mais adequado baseado em necessidade de consistência, escalabilidade, modelo de dados e performance.
