# 🚀 Red Hat OpenShift AI & MLOps (AI500) - Hands-on Labs

Este repositório contém as notas, códigos, manifestos e projetos práticos desenvolvidos durante o curso **AI500: Red Hat OpenShift AI & MLOps**. 

O objetivo principal desta jornada é estruturar o ciclo de vida completo de modelos de Machine Learning e Inteligência Artificial (MLOps) em plataformas nativas em nuvem, utilizando o ecossistema **Red Hat OpenShift AI (RHOAI)**, pipelines de automação e práticas de GitOps.

---

## 🛠️ Tecnologias & Ferramentas Utilizadas

- **Plataforma de Nuvem & Containers:** Red Hat OpenShift Container Platform (OCP)
- **AI/ML Platform:** Red Hat OpenShift AI (RHOAI) / JupyterLab Notebooks
- **Controle de Versão & GitOps:** Gitea, Git, Red Hat OpenShift GitOps (ArgoCD)
- **CI/CD & Pipelines de ML:** Red Hat OpenShift Pipelines (Tekton), Elyra Pipelines, Kubeflow Pipelines
- **RAG & GenAI Frameworks:** Python, LangChain, Vector Databases, Hugging Face, vLLM
- **Serving & Monitoramento:** KServe / ModelMesh, Prometheus, Grafana

---

## 🏗️ Módulos & Conteúdo Prático

### 1. **Ambientes de Ciência de Dados & RHOAI**
- Provisionamento de workbench customizado no OpenShift AI.
- Gerenciamento de aceleradores (GPUs) e volumes de armazenamento persistente (PVCs).
- Rastreamento de experimentos e gerenciamento de dependências no JupyterLab.

### 2. **Automação & Pipelines de MLOps**
- Criação e execução de pipelines de dados e treinamento usando **Elyra** e **Tekton**.
- Integração contínua de código de ML através de webhooks do **Gitea** e **OpenShift Pipelines**.
- Versionamento de artefatos de modelos e datasets.

### 3. **Implantação e Servir Modelos (Model Serving)**
- Deploy de modelos preditivos e LLMs utilizando **KServe** e **ModelMesh**.
- Configuração de endpoints seguros via HTTPS/Ingress no OpenShift.
- Testes de inferência REST/gRPC e validação de latência.

### 4. **Aplicações de IA Generativa & RAG (Retrieval-Augmented Generation)**
- Construção de pipelines RAG conectando fontes de dados corporativas a Large Language Models (LLMs).
- Integração de vetores e buscas por similaridade para enriquecimento de contexto.
- Deploy da aplicação de referência (**Jukebox App**) integrando backend de IA com interface gráfica.

---

## 🎯 Projeto de Destaque: Jukebox MLOps Pipeline

Durante os exercícios práticos, foi desenvolvida a automação ponta a ponta do projeto **Jukebox**:

1. **Ingestão & Treinamento:** Processamento de dados e treino do modelo em Jupyter Notebooks no RHOAI.
2. **Versionamento:** Armazenamento do código no servidor Git interno (**Gitea**) e artefatos no cluster.
3. **Pipeline CI/CD:** Trigger automático via Tekton Pipelines no OpenShift ao realizar `git push`.
4. **Deploy:** Servimento do modelo preditivo e integração com a aplicação final.

---

## 💻 Como Reproduzir / Estrutura do Repositório

```text
.
├── notebooks/          # Jupyter Notebooks de exploração, treino e RAG
├── pipelines/          # Definições de Tekton Pipelines e Elyra Workflows
├── manifests/          # Arquivos YAML de deployment no OpenShift (KServe, Routes, PVCs)
└── src/                # Código fonte das aplicações e scripts Python de inferência
