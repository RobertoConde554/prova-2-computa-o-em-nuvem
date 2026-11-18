# prova-2-computa-o-em-nuvem

roberto conde sato
18/11/2026

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

R:  A principal diferença entre uma máquina virtual  e um contêiner está no nível de virtualização e na forma como eles utilizam o sistema operacional:

Máquina Virtual: virtualiza o hardware físico por meio de um hypervisor (VMM), rodando um Guest OS completo e independente em cada instância, com seus próprios binários/bibliotecas e aplicações.

Contêiner: virtualiza a camada do sistema operacional, compartilhando o kernel da máquina hospedeira (host machine) e isolando os processos, o que o torna mais leve e rápido para iniciar.
