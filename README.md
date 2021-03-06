## Antes de qualquer execução, existem alguns requisitos que devem ser obedecidos:

### INSTRUÇÕES PARA CONFIGURAÇÃO

1.  As informações no arquivo de configuração **(/system/config/settings.yml)** devem estar preenchidas.

```
url: caminho inicial do sistema
log_file_path: nome da pasta onde serão criadas as pastas com evidências
project_code: código do projeto
project_name: nome do projeto
save_evidences: define se as evidências serão salvas ou não (on/off)
```

2. Você deve editar a variável de sistema **Path** e adicionar o diretório onde estão os drivers do Chrome e Firefox. Esses drivers se encontram na pasta **drivers** na raiz desse projeto.


### INSTRUÇÕES PARA EXECUÇÃO

1. Primeiramente devemos instalar as **gems** necessárias para executar o projeto. Primeiramente instalamos a gem **bundler** com o comando abaixo:

```
gem install bundler
```

Em seguida, vamos instalar todas as gems necessárias para rodar o projeto, ou seja, todas as gems existentes no arquivo Gemfile. Para isso, basta rodar o comando abaixo na pasta raiz do projeto.

```
bundle install
```

2. Após a instalação das gems, ainda na pasta raiz do projeto, podemos executar a feature com o comando abaixo:

```
cucumber features\store.feature
```

O comando acima usa como padrão o driver do Google Chrome. Caso deseje rodar com o driver do Firefox, execute o comando abaixo:

```
cucumber features\store.feature browser=firefox
```


Versões utilizadas no desenvolvimento do projeto:

* cucumber 3.1.2
* ruby 2.6.5
* driver firefox 0.27.0
* driver Chrome 85.0.4183.87
* selenium-webdriver 3.142.6
