# 📌 Aprendizagem de Regras para Classificação de Patologias da Coluna

## 📖 Sobre o Projeto

Este projeto implementa um sistema lógico capaz de aprender regras em Forma Normal Disjuntiva (DNF) para classificar pacientes com ou sem patologias da coluna vertebral, utilizando dados biomecânicos binarizados obtidos de radiografias.

A proposta combina lógica proposicional, modelagem com Z3 SMT Solver e avaliação experimental para determinar se um conjunto limitado de regras é capaz de classificar corretamente todos os pacientes do conjunto de treinamento — e medir sua capacidade preditiva no conjunto de teste.

## 🧠 Objetivo

Dado um arquivo CSV contendo atributos binários derivados de medições anatômicas, além de dois parâmetros:

- M → número máximo de regras (termos da DNF)
- L → número máximo de atributos por regra

o sistema deve:

- Modelar o problema em lógica proposicional
- Verificar satisfatibilidade no Z3
- Extrair as regras aprendidas, caso existam
- Avaliar a taxa de acerto em um conjunto de teste

## 🧩 Modelagem Lógica

As regras aprendidas devem satisfazer:

✔ Verdadeiras para todos os pacientes com classe P

✔ Falsas para todos os pacientes com classe NO

✔ No máximo M regras

✔ No máximo L atributos por regra

✔ Atributos podem ser afirmados ou negados

Caso o Z3 determine que a fórmula é insatisfatível, significa que não existe conjunto de regras dentro das restrições impostas.

## 🛠️ Tecnologias Utilizadas

- Python
- Z3 SMT Solver

## Autores

- Erivando de Castro
- Enderson Linhares
