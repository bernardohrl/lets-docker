# Instalando Docker



### 1. Desinstalar versões antigas

```sudo apt-get remove docker docker-engine docker.io```


### 2. Atualizaí

```sudo apt-get update```

### 3. Pacotitos

```sudo apt-get install \apt-transport-https \ca-certificates \curl \software-properties-common```

### 4. Adicionar a GPG key

```curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -```

 Verifique se você tem o fingerprint

```sudo apt-key fingerprint 0EBFCD88```

### 5. Crie um repositório estável
```sudo add-apt-repository \"deb [arch=amd64] https://download.docker.com/linux/ubuntu \$(lsb_release -cs) \table"```

**OBS:** Note: The lsb_release -cs sub-command below returns the name of your Ubuntu distribution, such as xenial. Sometimes, in a distribution like Linux Mint, you might need to change $(lsb_release -cs) to your parent Ubuntu distribution. For example, if you are using Linux Mint Rafaela, you could use trusty.

### 6. Atualiza again e instala!

```sudo apt-get update```

e então

```sudo apt-get install docker-ce```


### 7. Agora é só dar um Hello World' :)

```sudo docker run hello-world```



# Instalando Docker-Compose

### 1. Gente muito simples, usa o docker pra baixar o compose

```sudo curl -L "https://github.com/docker/compose/releases/download/1.22.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose```

### 2. Da permissões de leitura

```sudo chmod +x /usr/local/bin/docker-compose```

### 3. Agora só ver se deu

```docker-compose --version```