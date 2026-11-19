# prova-2-computa-o-em-nuvem

roberto conde sato
18/11/2026

Atividade Prática: Computação em Nuvem, Docker e Kubernetes

Nesta atividade prática, foram estudados conceitos fundamentais de computação em nuvem, como os modelos IaaS e SaaS, os tipos de implantação em nuvem e as diferenças entre máquinas virtuais e contêineres. Também foram realizadas atividades utilizando o Docker para criar e executar contêineres, além do Kubernetes para gerenciar aplicações, controlar Pods e utilizar Deployments, permitindo compreender na prática como funciona a administração e a escalabilidade de aplicações em ambientes de nuvem.



Durante esta atividade prática, aprendi como funcionam os principais conceitos de computação em nuvem e a importância dessas tecnologias. Com o Docker, aprendi a criar e executar contêineres de forma prática e organizada. Com o Kubernetes, entendi como gerenciar Pods, utilizar Deployments e manter aplicações funcionando automaticamente. Foi uma experiência importante para ampliar meus conhecimentos sobre infraestrutura, virtualização e gerenciamento de aplicações.






1 qual e a diferença entre laas e saas ? cite um exemplo de utilização de cada modelo

R: 1. IaaS (Infraestrutura como Serviço)
O que é: O provedor fornece a infraestrutura básica de TI virtualizada pela internet — como servidores virtuais (máquinas virtuais), armazenamento, redes e firewalls.

Responsabilidade: O provedor gerencia apenas o hardware físico e a virtualização. Você é responsável por instalar, configurar e manter o sistema operacional, os bancos de dados, as bibliotecas e as aplicações que rodam nesse servidor.

Exemplo de utilização: Criar uma máquina virtual no Amazon EC2 (AWS) ou no Microsoft Azure Virtual Machines para instalar um servidor Linux, configurar um banco de dados e hospedar o backend de um sistema próprio.

2. SaaS (Software como Serviço)

O que é: O provedor entrega uma aplicação completa e pronta para uso, acessada diretamente pelo navegador web ou aplicativo, sem exigir instalação local ou manutenção de infraestrutura.

Responsabilidade: O provedor gerencia absolutamente tudo: o hardware físico, a rede, o sistema operacional, o armazenamento, a segurança e as atualizações do software. O usuário apenas utiliza a ferramenta.

Exemplo de utilização: Usar o Google Workspace (Gmail, Google Docs) ou o Microsoft 365 no dia a dia para escrever documentos e enviar e-mails, sem precisar configurar servidores ou atualizar o programa manualmente.


2 uma empresa utiliza servidores próprios e também recursos de um provedor de nuvem publica. qual  modelo de implantação em nuvem essa empresa ultiliza

R: A empresa utiliza o modelo de Nuvem Híbrida (ou Hybrid Cloud).

Esse modelo combina a infraestrutura local (on-premises, composta pelos servidores próprios/nuvem privada da empresa) com serviços de nuvem pública (como AWS, Microsoft Azure ou Google Cloud), permitindo que dados e aplicações sejam compartilhados entre ambos os ambientes conforme a necessidade de segurança, custo ou escalabilidade.



3 qual e a principal diferença entre uma maquina virtual e um contêiner

R: Máquina Virtual: virtualiza o hardware físico por meio de um hypervisor (VMM), rodando um Guest OS completo e independente em cada instância, com seus próprios binários/bibliotecas e aplicações.

Contêiner: virtualiza a camada do sistema operacional, compartilhando o kernel da máquina hospedeira (host machine) e isolando os processos, o que o torna mais leve e rápido para iniciar.





qual e a diferença entre uma imagem docker e um conteiner em execuçao
R: Imagem Docker (Docker Image)
O que contém: O código da aplicação, ambiente de execução, bibliotecas, dependências, variáveis de ambiente e configurações necessárias para rodar.

Comportamento: Funciona como um molde ou template construído (geralmente a partir de um Dockerfile) e armazenado em registros como o Docker Hub.

Imutabilidade: Suas camadas são somente leitura — ela não é alterada quando um contêiner roda.

 Contêiner em Execução (Running Container)
O que é: É o processo isolado e ativo criado quando você executa uma imagem (por exemplo, com docker run).

Camada gravável: Adiciona uma camada de leitura e escrita (writable layer) sobre a imagem base, permitindo criar arquivos temporários, salvar logs ou modificar dados durante a execução.

Ciclo de vida: Pode ser iniciado, parado, reiniciado ou removido sem afetar a imagem original. Você pode iniciar vários contêineres independentes a partir da mesma imagem.


qual e a funcao de um deployment no kubernnets
R:Principais Funções
Auto-recuperação (self-healing): Se um Pod for excluído ou falhar, o Deployment detecta que a quantidade ativa ficou abaixo do desejado e sobe outro automaticamente.

Escalonamento (scaling): Permite aumentar ou diminuir o número de réplicas facilmente (por exemplo, com kubectl scale deployment <nome> --replicas=3) para suportar mais ou menos carga.

Atualizações graduais (rolling updates): Ao trocar a imagem do contêiner, o Deployment substitui os Pods antigos pelos novos aos poucos, evitando indisponibilidade.

Reversão (rollback): Se uma nova versão apresentar problema, dá para voltar rapidamente para uma revisão anterior estável com kubectl rollout undo.

o que aconteceu quando voce excluiu um pod por que isso acontece 
R: Ao excluir o Pod, o Kubernetes o removeu e criou outro automaticamente logo em seguida.

Isso acontece por causa do mecanismo de auto-recuperação (self-healing) do Deployment: como você configurou o estado desejado para 3 réplicas, o Kubernetes monitora o cluster constantemente e, ao detectar que o número caiu para 2, sobe uma nova instância para manter a aplicação disponível com as 3 réplicas exigidas.
