# Hackathon CNJ Inova 2020

## Descrição do Projeto

descrição aqui

## Tecnologia

O projeto foi construido com base em técnologias de conteinerização, banco de dados NoSql, banco de dados relacionais, estatística e visualizações interativas de business intelligence.

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

### Power BI

O Power BI é um serviço de análise de negócios da Microsoft, que tem o de fornecer visualizações interativas e recursos de business intelligence com uma interface simples para que os usuários finais criem os seus próprios relatórios e dashboards, conceito conhecido como self-service BI. Apesar de ser proprietário, possui versão gratuita que permite ter conjuntos de dados de até 1GB, armazenamento de até 10GB e compartilhamento público na nuvem.

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

6. Por fim os dados são consumidos pelo dashboard construido a partir do Power BI.
    
    (Escolhemos o Power BI pois ele atende os requisitos iniciais do projeto sem custo, além de ser amplamente difundido no mercado, facilitando o processo de repasse da sustentação da solução para uma outra equipe. No entanto, o modelo de dados construído na solução pode ser consumido facilmente por qualquer outra solução de BI do mercado, seja ela proprietária ou opensource.)

7. Por fim o usuário pode utilizar os gráficos e indicadores disponibilizados para tomar descisões estratégicas.
