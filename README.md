# Vigilante — Detecção de Posição Humana com YOLO

Prova de conceito desenvolvida para a disciplina de Inteligência Computacional com o objetivo de explorar a aplicação de visão computacional na detecção da posição de pessoas.

## Sobre o projeto

O projeto consiste no desenvolvimento de uma prova de conceito utilizando um modelo YOLO para detectar pessoas em três diferentes posições:

* Em pé
* Sentada
* Deitada

A ideia surgiu da possibilidade de utilizar a detecção da posição corporal como parte de um sistema de auxílio e alerta para pessoas muito idosas, permitindo identificar situações que poderiam exigir a comunicação com uma pessoa responsável ou alguém próximo.

O projeto foi desenvolvido academicamente como uma primeira experiência prática com modelos de Inteligência Artificial e visão computacional.

## Objetivo

Explorar, de forma prática, o processo de construção e aplicação de um modelo de detecção de objetos, passando pela criação de um dataset próprio, anotação das imagens, treinamento do modelo e utilização do modelo treinado em uma aplicação de inferência.

## Dataset

Foi construído um dataset próprio a partir de fotografias produzidas pela equipe durante o desenvolvimento do projeto.

O conjunto de dados possui mais de 200 imagens, que foram anotadas manualmente utilizando bounding boxes para identificar as posições das pessoas presentes nas imagens.

As três classes utilizadas foram:

| Classe    | Descrição      |
| --------- | -------------- |
| `em_pe`   | Pessoa em pé   |
| `sentada` | Pessoa sentada |
| `deitada` | Pessoa deitada |

O dataset original não está incluído neste repositório.

## Funcionamento

O modelo treinado foi integrado a uma aplicação Python utilizando as bibliotecas necessárias para realizar inferência sobre imagens e vídeos.

A aplicação também foi preparada para utilizar uma webcam como fonte de entrada.

Durante a inferência, as detecções são apresentadas visualmente por meio de bounding boxes e informações de confiança.

De forma simplificada, o fluxo do projeto pode ser representado como:

```text
Fotografias próprias
        │
        ▼
Anotação manual
        │
        ▼
Dataset
        │
        ▼
Treinamento do modelo YOLO
        │
        ▼
Modelo treinado
        │
        ▼
Aplicação de inferência
```

## Tecnologias

* Python
* YOLO
* Ultralytics
* OpenCV
* NumPy
* Jupyter Notebook

## Estrutura do projeto

```text
.
├── README.md
├── LICENSE
├── notebooks/
│   └── vigilante_yolo_inference.ipynb
```

## Execução

O principal material de execução do projeto está disponível no notebook localizado em:

```text
notebooks/vigilante_yolo_inference.ipynb
```

As dependências utilizadas pelo notebook incluem a biblioteca Ultralytics, OpenCV e NumPy.

O modelo treinado originalmente e os vídeos utilizados durante o desenvolvimento não estão disponíveis neste repositório público devido a restrições de redistribuição.

## Limitações

Este projeto deve ser entendido como uma prova de conceito acadêmica e não como um sistema de monitoramento ou dispositivo médico validado.

O projeto não possui, nesta versão, métricas de avaliação preservadas que permitam quantificar formalmente o desempenho do modelo.

Além disso, o dataset original, o modelo treinado e os vídeos utilizados durante os testes não podem ser redistribuídos.

## Possíveis melhorias

Entre as possibilidades de evolução do projeto estão:

* reconstrução e ampliação do dataset;
* utilização de métricas formais para avaliação do modelo;
* comparação entre diferentes versões e configurações de modelos YOLO;
* melhoria do processo de treinamento;
* realização de testes em diferentes condições de iluminação e ambientes;
* criação de uma aplicação independente do notebook;
* implementação de mecanismos de alerta;
* registro e análise histórica das detecções;
* avaliação mais sistemática de falsos positivos e falsos negativos.

## Contexto acadêmico

Projeto desenvolvido para a disciplina de Inteligência Computacional como uma prova de conceito de aplicação de modelos de visão computacional.
