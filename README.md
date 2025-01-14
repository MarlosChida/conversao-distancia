# Desafio Devops & Cloud

Este repositório contém os arquivos utilizados para realizar o Desafio 01 do treinamento DevOps & Cloud

Treinamento realizado por Fabricio Veronez em 13/01/2025

## 🚀 Começando

Essas instruções permitirão que você gere a imagem Docker da aplicação, realize o upload da imagem para o Docker Hub e instancie um container utilizando a imagem gerada.


### 📋 Pré-requisitos

Os seguintes requisitos são necessários para gerar a Imagem:
* [Docker](https://docker.com) - Docker engine instalado.
* [Docker Hub](https://hub.docker.com/) - Conta criada no Docker Hub para upload da imagem gerada.

### 🔧Geração da Imagem 

Para a geração da imagem Docker à partir do código-fonte e Dockerfile, os seguintes comandos devem ser executados.

Geração da Imagem (ajustar tag da versão se necessário, neste e nos demais comandos):

```
docker build -t conversao-distancia:v1 .
```

A imagem gerada estará disponível localmente.

## ⚙️ Criando tag "latest" e realizando upload das imagens para Docker Hub

Criar tags para o Docker Hub (seu repositório), criando também a tag  "latest" para a imagem gerada acima:

Executar os comandos abaixo, ajustando o nome do repositório conforme desejado:

```
docker tag conversao-distancia:v1 marloschida/conversao-distancia:v1
docker tag marloschida/conversao-distancia:v1 marloschida/conversao-distancia:latest
docker push marloschida/conversao-distancia:v1
docker push marloschida/conversao-distancia:latest
```

## 📦 Executando o container

Executar os comandos abaixo para criar um container à partir da imagem disponível no Docker hub.

Realizar os ajustes conforme desejado.
```
docker run -d --name conversao-distancia -p 8083:5000 marloschida/conversao-distancia:v1
```


## 🛠️ Construído com

Projeto desenvolvido com:

* [Visual Studio Code](https://code.visualstudio.com/) - Framework de Desenvolvimento


## 📌 Versão

1.0

## ✒️ Autores

Projeto original desenvolvido por Fabricio Veronez.

Colaborador:

* **Marlos Chida** - *Dockerfile, ajustes, testes e documentação* 


## 📄 Licença

Este projeto é um fork do repositório [conversao-distancia](https://github.com/KubeDev/conversao-distancia)  e não possui licença atrelada oficialmente. Consulte o repositório de origem para detalhes.

---
⌨️ por [Marlos Chida](mailto:marlos.chida@qriar.com?subject=DevOps)
