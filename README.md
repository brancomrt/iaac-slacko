# Instrucoes para execucao da playbook de instalacao da aplicacao slacko

- Caso deseja executar em sua maquina local, copiar os arquivos da pasta ansible (inventory,playbook.yml) para o diretorio home de seu usuario.

- Editar a variável "home_user" na playbook.yml com o seu usuario home.

- Executar a playbook.

# Instrucoes de instalacao da aplicacao slacko em maquina virtual qemu/kvm no Vagrant

- Criar o diretorio iaac-slacko em seu diretorio home do usuário:

  mkdir -p ~/iaac-slacko/ansible

- Copiar os arquivos (inventory,playbook.yml) para pasta ~/iaac-slacko/ansible

- Iniciar a criacao da maquina virtual no Vagrant denominada "server"

  cd ~/iaac-slacko/
  
  vagrant up
  
  - Logar na maquina virtual "server"
  
  cd ~/iaac-slacko/
  
  vagrant ssh
  
