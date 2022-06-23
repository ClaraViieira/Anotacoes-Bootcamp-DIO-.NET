# Anotações sobre Git e GitHub

### Conceitos e definições do Git/GitHub

O Git é sistema de controle de versão de código aberto e distribuído. Através do Git Bash, um terminal extensivo do Git, é possível que haja a colaboração de projetos de arquivos distribuídos que residem no desenvolvedor local do autor, para um repositório público que reside dentro da plataforma de nuvem do GitHub. 

Ou seja, Git e GitHub não são a mesma coisa. Enquanto o GIT é o sistema que versa o código de forma aberta e distribuída para que seja possível que ele seja commitado na nuvem e não que fique somente preso no desenvolvedor local, o GitHub é a própria nuvem. 

Mas qual o conceito de nuvem? A nuvem é um servidor de espaço físico. Sim, isso mesmo, ela ocupa um lugar físico no mundo, não sendo uma coisa abstrata. A nuvem é o servidor de diversas empresas e serve para armazenar projetos, códigos, arquivos, sistemas e programas, dentro outros. O GitHub especificamente é um lugar de armazenamento de códigos abertos feitos através do Git Bash. 

Ambos as plataformas são complementares entre si, apesar de agirem de forma independente. 

### Comandos do Git Bash 

Para a criação de um reposítório, são necessárias alguns comandos, que estão descritos abaixo: 

Comando | Descrição
------- | ---------
git init | Inicializar um novo repositório
git status | Mostrar o status atual do repositório
git add "Nome do arquivo" | Adicionar somente um arquivo da pasta ao commit
git add . | Adicionar todos o arquivos da pasta de uma vez ao commit 
git commit -m "Mensagem do commit" | Criar um novo commit com uma mensagem
git config --global user.email "you@exemplo.com" | Configurar um e-mail para o uso do Git como autor dos códigos
git config --global user.name "Your Name" | Configurar um nome para o uso do Git como autor dos códigos 
git push | Enviar os novos arquivos ou as atualizações para a nuvem do GitHub
git remote add origin -url- | Enviar os arquivos para o repositório criado na nuvem
git branch | Permite ver qual branch está ativa atuamente para modificações
git branch "nome da branch" | Criar uma nova branch "secundária", a branch oficial sempre é a master 
git checkout "nome da branch" | Permite mudar de branch 
git merge "nome da branch secundária" | Permite atualizar a branch oficial com as atualizações feitas na outra branch
git pull | Permite trazer as novas atualizções da branch atual 