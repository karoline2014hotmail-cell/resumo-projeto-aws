# resumo-projeto-aws
um resumo detalhado de tudo que eu aprendi no curso aws code girls santander pela dio 


  Amazon DynamoDB
- Tipo de banco: NoSQL, totalmente gerenciado e sem servidor.
- Características principais:
- Alta escalabilidade e desempenho com latência inferior a 10 milissegundos.
- Ideal para aplicações com grandes volumes de leitura e escrita, como carrinhos de compras e jogos online.
- Suporte a replicação global, TTL (Time to Live), backups automáticos e integrações com serviços de machine learning.
- Casos de uso: Aplicações em tempo real, IoT, mobile, e-commerce.

🧱 Amazon RDS (Relational Database Service)
- Tipo de banco: Relacional, gerenciado pela AWS.
- Engines suportadas: MySQL, PostgreSQL, Oracle, SQL Server, MariaDB e Amazon Aurora.
- Características principais:
- Automatiza tarefas como provisionamento, backups, patching e monitoramento.
- Suporte a alta disponibilidade com Multi-AZ e réplicas de leitura.
- Escalabilidade vertical e horizontal (dependendo da engine).
- Casos de uso: Aplicações empresariais, ERPs, CRMs, sistemas financeiros.

🔄 Recuperação de Dados na AWS
- Backups automáticos: Tanto o RDS quanto o DynamoDB oferecem backups contínuos e snapshots manuais.
- Recuperação pontual (Point-in-Time Recovery):
- RDS permite restaurar o banco para qualquer ponto dentro do período de retenção.
- DynamoDB oferece recuperação contínua com o recurso de backup contínuo (PITR).
- Alta disponibilidade: Implementações Multi-AZ e replicação global ajudam a garantir resiliência e recuperação rápida em caso de falhas.

-  Amazon S3 (Simple Storage Service)
• 	Tipo de serviço: Armazenamento de objetos escalável e altamente disponível.
• 	Características principais:
• 	Armazena qualquer tipo de dado (imagens, vídeos, documentos, backups).
• 	Classes de armazenamento para diferentes necessidades: Standard, Intelligent-Tiering, Glacier, Deep Archive.
• 	Suporte a versionamento, replicação entre regiões e controle de acesso granular.
• 	Casos de uso: Sites, aplicativos móveis, backups, big data, machine learning.

❄️ Amazon S3 Glacier
• 	Tipo de serviço: Armazenamento de longo prazo com baixo custo.
• 	Características principais:
• 	Ideal para arquivamento de dados que são acessados raramente.
• 	Três classes de recuperação: Instant Retrieval, Flexible Retrieval e Deep Archive.
• 	Integração com o Amazon S3 para gerenciamento unificado.
• 	Casos de uso: Arquivos históricos, registros legais, backups antigos.

🚀 Amazon CloudFront
• 	Tipo de serviço: CDN (Content Delivery Network) da AWS.
• 	Características principais:
• 	Distribui conteúdo (imagens, vídeos, arquivos, sites) com baixa latência e alta velocidade.
• 	Usa pontos de presença (edge locations) ao redor do mundo.
• 	Suporte a HTTPS, autenticação, cache e integração com outros serviços da AWS como S3 e Lambda@Edge.
• 	Casos de uso: Sites de alto tráfego, streaming de vídeo, APIs, aplicações globais.

🗂️ Conceitos de Armazenamento na AWS
• 	Armazenamento de objetos: Como o S3, ideal para arquivos e dados não estruturados.
• 	Armazenamento em bloco: Usado por serviços como EBS (Elastic Block Store), ideal para discos de máquinas virtuais.
• 	Armazenamento de arquivos: Como o Amazon EFS, para compartilhamento de arquivos entre instâncias.

🌐 Conceito de CDN (Content Delivery Network)
• 	Definição: Rede de servidores distribuídos que entrega conteúdo de forma rápida e eficiente.
• 	Benefícios:
• 	Redução de latência.
• 	Melhor desempenho e experiência do usuário.
• 	Proteção contra picos de tráfego e ataques DDoS.
• 	Exemplo na AWS: Amazon CloudFront é a CDN que acelera a entrega de conteúdo hospedado no S3, EC2 ou outros serviços.

Comparativo dos Serviços AWS


📦 Conceitos de Armazenamento na AWS
• 	Armazenamento de Objetos: Ideal para arquivos como imagens, vídeos e documentos. Exemplo: Amazon S3.
• 	Armazenamento em Bloco: Usado por sistemas operacionais e bancos de dados. Exemplo: Amazon EBS.
• 	Armazenamento de Arquivos: Compartilhamento de arquivos entre instâncias. Exemplo: Amazon EFS.
• 	Classes de Armazenamento: S3 oferece classes como Standard, Intelligent-Tiering, Glacier e Deep Archive para otimizar custo e desempenho.

🌐 Conceito de CDN (Content Delivery Network)
• 	Definição: Rede de servidores distribuídos globalmente que entrega conteúdo de forma rápida e eficiente.
• 	Benefícios:
• 	Redução de latência.
• 	Melhoria na experiência do usuário.
• 	Proteção contra picos de tráfego e ataques.
• 	Exemplo: Amazon CloudFront entrega arquivos estáticos e dinâmicos com alta performance, integrando-se com S3, EC2 e Lambda@Edge.

 AWS Lambda
• 	Tipo de serviço: Computação sem servidor (serverless).
• 	Funcionamento:
• 	Executa funções em resposta a eventos (como uploads no S3 ou chamadas de API).
• 	Não exige gerenciamento de servidores ou infraestrutura.
• 	Cada função Lambda roda em um container isolado, com suporte a várias linguagens como Python, Node.js, Java, Go, entre outras.
• 	Containers personalizados: É possível empacotar funções Lambda como imagens Docker, permitindo mais controle sobre dependências e ambiente.
• 	Ideal para: Tarefas curtas, automações, microsserviços simples e integrações com outros serviços AWS.

📦 Amazon ECS (Elastic Container Service)
• 	Tipo de serviço: Orquestração de containers gerenciada pela AWS.
• 	Funcionamento:
• 	Gerencia e escala containers Docker em clusters de instâncias EC2 ou com Fargate (sem servidor).
• 	Simples de configurar e operar, com integração nativa com outros serviços AWS.
• 	Ideal para: Aplicações pequenas e médias, com foco em simplicidade e integração rápida.

🧬 Amazon EKS (Elastic Kubernetes Service)
• 	Tipo de serviço: Orquestração de containers baseada em Kubernetes.
• 	Funcionamento:
• 	Gerencia clusters Kubernetes com alta disponibilidade e escalabilidade.
• 	Suporta workloads complexos, com portabilidade entre nuvens e ambientes locais.
• 	Requer mais configuração e conhecimento técnico do que o ECS.
• 	Ideal para: Aplicações empresariais, arquiteturas de microsserviços complexas e equipes que já usam Kubernetes.

 Amazon SNS (Simple Notification Service)
• 	Modelo: Publicação/Assinatura (Pub/Sub).
• 	Funcionamento:
• 	Um produtor publica mensagens em um tópico.
• 	Vários consumidores (assinantes) recebem essas mensagens simultaneamente.
• 	Suporta entrega por e-mail, SMS, HTTP, Lambda e SQS.
• 	Ideal para: Notificações em tempo real, fanout de mensagens para múltiplos destinos.


📩 Amazon SQS (Simple Queue Service)
• 	Modelo: Fila de mensagens.
• 	Funcionamento:
• 	Um produtor envia mensagens para uma fila.
• 	Um ou mais consumidores processam essas mensagens de forma independente e assíncrona.
• 	Suporta filas padrão (alta taxa de transferência) e FIFO (ordem garantida).
• 	Ideal para: Processamento desacoplado, escalável e confiável de tarefas.


🔄 AWS Step Functions
• 	Tipo: Orquestrador de fluxos de trabalho serverless.
• 	Funcionamento:
• 	Permite criar fluxos visuais com estados, decisões, paralelismo e esperas.
• 	Integra-se com mais de 220 serviços AWS, incluindo Lambda, SQS, SNS, DynamoDB, etc.
• 	Usa máquinas de estado para controlar a lógica de execução.
• 	Ideal para: Automatizar processos complexos, como pipelines de dados, processamento de imagens, ou sistemas de aprovação.


