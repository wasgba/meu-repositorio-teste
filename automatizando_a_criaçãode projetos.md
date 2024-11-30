#!/bin/bash

# Solicita o nome do novo projeto
echo "Digite o nome do projeto:"
read nome_projeto

# Cria a pasta e entra nela
mkdir ~/meu_projetos/$nome_projeto
cd ~/meu_projetos/$nome_projeto

# Inicializa o repositório git
git init

# Cria o repositório no GitHub (manual) e obtém o link SSH do repositório

# Adiciona o repositório remoto
git remote add origin git@github.com:wasgba/$nome_projeto.git

# Adiciona os arquivos e faz o primeiro commit
git add .
git commit -m "Primeiro commit"

# Envia para o GitHub
git push -u origin main

echo "Projeto '$nome_projeto' configurado com sucesso no GitHub!"

