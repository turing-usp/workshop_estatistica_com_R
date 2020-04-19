# Instalação

Neste tutorial vamos ensinar a utilizar a linguagem de programação R no Jupyter Notebook.

O Jupyter Notebook é um ambiente de desenvolvimento de programação para as linguagens: Julia, Python e R.

- [Windows ou Mac](#a-windows-ou-mac)
- [Linux](#b-linux)

## A. Windows ou Mac

### A.1 - Instale o Anaconda

Anaconda é uma distribuição de Python e R, que inclui jupyter notebook.

A instalação pode ser feita acessando esse [link](https://www.anaconda.com/distribution/).

### A.2 - Navegador Anaconda (Anaconda Navigator)

#### A.2.1 - Abra o Navegador Anaconda

![alt text](https://docs.anaconda.com/_images/rJupyterStep1.png)

#### A.2.2 - Crie um novo Ambiente

Clique em ambientes (environments) na lateral esquerda, em seguida clique em criar (create).

![alt text](https://docs.anaconda.com/_images/rJupyterStep2.png)

Adicione um nome "r-tutorial", e selecione Python 3.x e R. Clique em create.

![alt text](https://docs.anaconda.com/_images/rJupyterStep2-1.png)

#### A.2.3 - Abra o ambiente criado

O ambiente criado aparecera na listagem dos seus ambientes, por default você terá um ambiente "base (root)" e após executar os passos acima terá um ambiente "r-tutorial". 

![alt text](https://docs.anaconda.com/_images/rJupyterStep3.png)

Como indicado na figura, abra o Jupyter Notebook.

**Obs**: caso deseje acessar um diretório específico, clique em abra terminal. Acesse o diretório pelo comando:

```bash
> cd caminho_pro_diretorio
```

Em seguida execute:

```bash
> jupyter notebook
```

### A.3 - Crie um novo Notebook

![alt text](https://docs.anaconda.com/_images/rJupyterStep4.png)

Clique em "new" no canto superior direito depois em "R", conforme a imagem acima e divirta-se!

## B. Linux

### B.1 - Instale R

**Obs:** a instalação de R abordada nesse tutorial é somente para o Ubuntu.
Os passos seguintes são válidos para sistemas Linux em geral.

Para instalar R, execute o seguinte comando no terminal:

```bash
sudo apt install r-base
```

### B.2 - Instale o Anaconda

Anaconda é uma distribuição de Python e R, que inclui o jupyter notebook.

A instalação pode ser feita com os seguintes comandos:

```bash
cd /tmp
curl -O https://repo.anaconda.com/archive/Anaconda3-2020.02-Windows-x86_64.exe
bash Anaconda3-2020.02-Windows-x86_64.exe
```

Esse último comando vai abrir o instalador do Anaconda:

1. segure <kbd>enter</kbd> até passar por todos os termos e condições;

2. digite `"yes"` para aceitar os termos e condições;

3. digite enter para aceitar a localização de instalação padrão;

4. espere a instalação terminar;

5. digite `"yes"` para configurar o anaconda no seu sistema.

   ```bash
   source ~/.bashrc
   ```

Em seguida, feche e abra o seu terminal para completar a instalação do anaconda.

#### B.2.2 - Crie e ative um novo ambiente do anaconda

O comando abaixo cria um ambiente chamado "r-tutorial" com o jupyter notebook
instalado.

```bash
conda create -n r-tutorial notebook
```

Para ativar esse ambiente, basta executar:

```bash
conda activate
```

### B.3 - Instale as bibliotecas de R

Ainda no terminal, execute:

```bash
R
install.packages("tidyverse")
# Selecione um dos mirrors
install.packages('IRkernel')
IRkernel::installspec()
q() # escolha a opção n
```

### B.4 - Abra o Jupyter Notebook

Para abrir o Jupyter notebook, execute no terminal:

```bash
conda activate r-tutorial  # ativa o anaconda
jupyter notebook           # abre o jupyter
```

Só é necessário executar o primeiro comando se você ainda não tiver
ativado o anaconda desde que abriu o terminal.

### B.5 - Crie um novo Notebook

Da mesma forma que [no Windows](#a3-crie-um-novo-notebook)
