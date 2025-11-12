#  PyCaret 

Este repositório demonstra o uso do **PyCaret** dentro de um ambiente **Docker**, utilizando a imagem oficial [`pycaret/full`](https://hub.docker.com/r/pycaret/full).  
O projeto exemplifica a execução de experimentos de *Machine Learning* aplicados ao conjunto de dados **NSL-KDD**, utilizado para detecção de intrusões em redes (IDS – *Intrusion Detection System*).

---


## Ambiente Docker

A execução foi feita usando a imagem oficial:

```
docker pull pycaret/full
```

Essa imagem já vem com:
- **Python 3.10** - compatível com PyCaret
- **PyCaret (Full)** com todas as dependências
- **Jupyter Notebook/Lab** configurado e pronto para uso

---

## Como executar o projeto

### 1️. Instalar o Docker
Baixe e instale o **[Docker Desktop](https://www.docker.com/products/docker-desktop)** (Windows/macOS/Linux).

Verifique se está funcionando:
```bash
docker --version
```

---

### 2. Baixar a imagem PyCaret
```bash
docker pull pycaret/full
```

---

### 3. Executar o container no Docker

1. Abra o **Docker Desktop** → guia **Images** → selecione `pycaret/full:latest` → clique em **Run**.  

2. Em **Container name**, opcionalmente defina algo como:
   ```
   pycaret_kdd
   ```
3. Em **Ports**, defina:
   ```
   Host port: 8888
   ```
   Isso faz o Jupyter abrir em **http://localhost:8888**.  
  

4. Em **Volumes**, clique nos três pontos, e em **Host path** selecione a pasta local onde estão seus arquivos, por exemplo:
  
   Em **Container path**, digite:
   ```
   /workspace
   ```
   Isso mapeia sua pasta local para a pasta de trabalho do container, permitindo salvar notebooks e resultados localmente.

5. Deixe as demais opções em branco.  
6. Clique em **Run**.

Após alguns segundos, o container iniciará e os logs exibirão um link como:
```
http://127.0.0.1:8888/?token=<token_aqui>
```

Copie e cole esse link no navegador para abrir o **Jupyter Notebook**.  
Acesse a pasta `/workspace` para encontrar seus arquivos:
- `KDDTrain.txt`
- `KDDTest.txt`
- `Pycaret Docker.ipynb`

Execute o notebook dentro do ambiente PyCaret.

---

## Referências

- [PyCaret Official Docker Hub](https://hub.docker.com/r/pycaret/full)
- [NSL-KDD Dataset](https://ieee-dataport.org/documents/nsl-kdd)

---

👩‍💻 **Autora:** Wiliane Carolina Silva  

