# Tese

Esta tese de mestrado teve como objetivo adaptar uma ferramenta de segmentação automática do miocárdio, que é baseado em técnicas de deep learning e permite a destinção entre o tecido saudável e o tecido fibroso. Para isso foi introduzido um novo mecanismo de atenção na arquitetura base do algoritmo com o intuito de tornar o modelo mais eficiente na extração de características da imagem e na identificação da fibrose miocárdica.

Para isso, foram utilizadas imagens provenientes do dataset da competição MyoPS 2020, que foi realizada em colaboração com a conferência MICCAI 2020 e disponibilizada publicamente. O MyoPS é uma base de dados específica para segmentação de patologias miocárdicas, composta por imagens de ressonância magnética cardíaca (RMC) adquiridas de forma anómina de pacientes diagnosticados com condições agudas, fornecendo três sequências distintas: bSSFP, LGE e T2, além do Ground Truth.

Este trabalho é estruturado em duas etapas, sendo que o principal foco do trabalho foi na segunda fase e a primeira fase apenas serviu de base.  Na primeira fase, o objetivo é prever a área do miocárdio, o que requer a segmentação de três constituintes cardíacos: ventrículo esquerdo (VE), ventrículo direito (VD) e miocárdio do VE. Já na segunda fase, o objetivo principal consiste na previsão da área das patologias miocárdicas, incluindo cicatriz (tecido fibroso) e edema. 

A rede que foi utilizada na segunda etapa, que consistiu numa variante da Unest, em que temos o encoder baseado em transformer à esquerda e um decoder baseado em convoluções à direita. 

# 🫀 Tese de Mestrado: Segmentação Automática de Fibrose Miocárdica

Este repositório contém o trabalho desenvolvido no âmbito da minha tese de mestrado, cujo objetivo foi adaptar e melhorar uma ferramenta de segmentação automática do miocárdio utilizando **Deep Learning**. A ferramenta permite distinguir entre **tecido saudável e tecido fibroso**, com a introdução de um **novo mecanismo de atenção** que visa melhorar a extração de características e a identificação precisa da fibrose miocárdica.

---

## 🗂️ Dataset

Foram utilizadas imagens do dataset da **competição MyoPS 2020**, realizada em parceria com a conferência **MICCAI 2020**. Este conjunto de dados é composto por:

- Imagens de **Ressonância Magnética Cardíaca (RMC)** de pacientes com condições agudas
- Três sequências distintas por paciente:
  - `bSSFP`
  - `LGE`
  - `T2`
- Máscaras de **Ground Truth** com anotações de especialistas

---

## 🧪 Estrutura do Projeto

O projeto está dividido em duas fases principais:

### 📌 Fase 1: Segmentação Anatómica

Objetivo: **Segmentar estruturas cardíacas principais**:
- Ventrículo Esquerdo (VE)
- Ventrículo Direito (VD)
- Miocárdio do VE

> Esta fase serviu como base preparatória para a segunda fase.

### 📌 Fase 2: Segmentação de Patologias

Objetivo principal: **Segmentar regiões afetadas por patologias miocárdicas**, incluindo:
- **Fibrose (cicatriz miocárdica)**
- **Edema**

#### 🧠 Arquitetura Utilizada

Foi utilizada uma variante da arquitetura **UNeSt**, composta por:
- **Encoder** baseado em um **Transformer hierárquico aninhado**
- **Decoder** baseado em **convoluções**
