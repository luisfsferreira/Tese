# 🫀 Tese de Mestrado: Segmentação Automática de Fibrose Miocárdica

Este repositório contém o trabalho desenvolvido no âmbito da minha tese de mestrado, cujo objetivo foi adaptar e melhorar uma ferramenta de segmentação automática do miocárdio utilizando **Deep Learning**. A ferramenta permite distinguir entre **tecido saudável e tecido fibroso**, com a introdução de um **novo mecanismo de atenção** que visa melhorar a extração de características e a identificação precisa da fibrose miocárdica.

---

## 🗂️ Dataset

Foram utilizadas imagens provenientes do dataset da **competição MyoPS 2020**, realizada em colaraboração com a conferência **MICCAI 2020**. Este conjunto de dados é composto por:

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

#### 🧠 Arquitetura Utilizada na Segunda Etapa

Foi utilizada uma variante da arquitetura **UNeSt**, composta por:
- **Encoder** baseado em um **Hierarchical Transformer Encoder**
- **Decoder** baseado em **convoluções**

