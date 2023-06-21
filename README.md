## Projeto de Rede de Computadores com Virtualização usando Vagrant e Ansible

Este projeto consiste na criação de uma rede de computadores com cinco máquinas virtuais provisionadas via Vagrant, utilizando o sistema operacional Ubuntu. A quinta máquina é configurada como um servidor Ansible, responsável por configurar as demais máquinas como servidores DNS, servidor web, servidor NFS e proxy Squid.

### Configurações e Requisitos

Para executar o projeto, certifique-se de ter os seguintes requisitos instalados:

- [Vagrant](https://www.vagrantup.com/) (veja o guia de instalação [aqui](https://learn.hashicorp.com/tutorials/vagrant/getting-started-install))
- [VirtualBox](https://www.virtualbox.org/) (veja o guia de instalação [aqui](https://www.virtualbox.org/wiki/Downloads))

### Instruções de Uso

1. Clone o repositório do projeto para sua máquina local.

2. Navegue até a pasta "/redes" dentro do repositório clonado.

3. Execute o seguinte comando no terminal:

``` vagrant up ```


- Durante o processo de inicialização, o terminal pode solicitar a seleção da interface de rede para montar as máquinas virtuais. Sempre escolha a opção 1.

4. Após a conclusão do processo, a rede de computadores com as cinco máquinas virtuais estará configurada e pronta para uso.

### Funcionalidades da Rede de Computadores

1. Servidor de DNS:
- Recebe solicitações de todas as outras máquinas virtuais.
- Caso o DNS local não encontre um registro, redireciona a solicitação para o DNS do Google (8.8.8.8).

2. Servidor Web:
- Instala o Docker e cria um contêiner com a imagem mais recente do Nginx.
- Realiza o encaminhamento de porta com o servidor host na porta 80.
- Para visualizar a página inicial do Nginx, acesse http://localhost:80 no navegador.

3. Servidor NFS:
- Instala o software do NFS (Network File System) e configura um diretório padrão para compartilhamento de arquivos.

4. Proxy Squid:
- Armazena em cache todas as requisições da rede local.

### Observações

Certifique-se de que todos os requisitos estão instalados corretamente antes de executar o projeto. O Vagrant e o VirtualBox são essenciais para a criação das máquinas virtuais e para a execução do ambiente de rede.

O projeto está estruturado para fornecer uma rede funcional com as configurações descritas acima. No entanto, caso deseje personalizar ou adicionar mais recursos, é possível ajustar o código-fonte do projeto de acordo com suas necessidades.
