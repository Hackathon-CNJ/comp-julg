# Hackathon CNJ Inova 2020

## Descrição do Projeto

descrição aqui

## Técnologia

O projeto foi construido com base em técnologias de conteinerização, banco de dados NoSql, banco de dados relacionais, estatística e visualização dashboard.

![diagrama](assets/img/diagram.jpeg)

Durante todo o projeto tomamos cuidado para que todas e/ou praticamente todas técnologias utilizadas fossem open-source, para que não acarretassem custos extras para o CNJ.

### Docker

O Docker é uma plataforma open source que facilita a criação e administração de ambientes isolados. Ele possibilita o empacotamento de uma aplicação ou ambiente dentro de um container, se tornando portátil para qualquer outro host que contenha o Docker instalado.

### MongoDB

O MongoDB é um banco de dados noSQL, ou seja, não utiliza a linguagem SQL. Ele é um banco orientado a objetos, que no caso, são chamados de documentos. Basicamente, ele serve para dados sem uma estrutura definida, sua linguagem facilita a performance das consultas realizadas.

### MySQL

MySQL, o mais popular sistema de gerenciamento de banco de dados SQL de código aberto, é desenvolvido, distribuído e apoiado pela Oracle Corporation.

### Python

Python é uma linguagem de programação de alto nível, interpretada, de script, imperativa, orientada a objetos, funcional, de tipagem dinâmica e forte. Atualmente possui um modelo de desenvolvimento comunitário, aberto e gerenciado pela organização sem fins lucrativos Python Software Foundation.

------------

## Pipeline (Segmentação de Instruções)

1. **Download**

    O primeiro passo da pipeline (acompanhar imagem acima) é o download dos dados através deste [link](). Você pode ou não ter uma estrutura Docker,  caso já ter as instâncias de MySQL e MongoDB a disposição só é preciso configurar seus acessos no arquivo `/notebooks/processo.ipynb`.
    
    Caso não tiver uma instância dos banco de dados se faz necessário executar o arquivo `Dockerfile`, ele será responsável por instâncias os mesmos.

    A partir daqui todas as instruções serão executadas dentro do arquivo `/notebooks/processo.ipynb`

2. O segundo passo consiste na importação da base do CNJ para a estrutura Mongo.

3. Em seguida os dados serão preparados para a extração de indicadores e também as transformações necessárias para que os dados sejão consumidos pelo PowerBI.

4. Neste passo são calculados diversos indicadores. (As descrições podem ser encontradas na tabela `aq` dentro do MySQL)

5. A rotina agora faz a inserção de todas as informações no MySQL.

6. Por fim os dados são consumidos pelo dashboard construido a partir do PowerBI.
    
    Escolhemos o PowerBI por uma questão de maior afinidade com a ferramenta, os dados podem ser consumidos a partir de qualquer ferramenta de B.I ou dashboard desenvolvido.

7. Por fim o usuário pode utilziar os gráficos e indicadores disponibilizados para tomar descisões estratégicas.
