# Proposta Técnica: Totem Inteligente FlexMedia
  https://docs.google.com/document/d/1DhDPqPwXxP_s5cN4GDjyzxuer0-A6LmppBoKmOaHSs8/edit?tab=t.0#heading=h.7adthb9gk6zu

### Integrantes
- Filipe Marques Previato - RM567720
- Victor Araujo Ferreira - RM567619
- Pedro Zanon Castro - RM567350
- Jonathan Gomes Ribeiro Franco - RM567109

## Visão Geral
Este documento apresenta a proposta técnica do **Totem Inteligente "Smart-Guide" FlexMedia**, uma solução para transformar a experiência do visitante em museus e exposições culturais, com foco em:

- Engajamento inteligente: personalização de rotas e conteúdos em tempo real.  
- Privacidade por design: processamento de dados anônimos localmente, em conformidade com LGPD.  
- Geração de insights acionáveis: métricas de engajamento e heatmaps para curadoria.

## Arquitetura da Solução
A solução é modular e escalável, dividida entre **Edge Computing** (processamento local) e **Cloud** (processamento e armazenamento centralizado).  
O fluxo de dados funciona assim:

1. Sensor de presença (PIR) ativa o microcontrolador ESP32-CAM.  
2. O dispositivo analisa a atenção do usuário anonimamente e descarta imagens, enviando apenas metadados para a nuvem.  
3. A Google Cloud Platform processa os dados via API Gateway, Cloud Functions e Firestore.

## Tecnologias Principais
- **Hardware / Edge**: ESP32-CAM, TensorFlow Lite Micro.  
- **Nuvem**: API Gateway, Cloud Functions (Python), Firestore (NoSQL).  
- **Interação / IA**: Dialogflow, Speech-to-Text e Text-to-Speech do Google.

## Segurança e Privacidade
- Anonimização de dados de imagem.  
- Criptografia TLS/HTTPS nas comunicações.  
- Autenticação via API Keys (totens) e Tokens JWT (dashboard).

## Responsabilidades da Equipe
- **Filipe Marques Previato**: Gerenciamento de Projeto e Documentação  
- **Jonathan Gomes Ribeiro Franco**: IA, Segurança e Tecnologias  
- **Victor Araujo Ferreira**: Arquitetura de Nuvem e Backend  
- **Pedro Zanon Castro**: Hardware, Edge e Coleta de Dados

---

> Este README serve como **porta de entrada** para o documento completo, fornecendo visão geral, arquitetura, tecnologias e responsabilidades. Para detalhes completos, consulte o documento técnico principal.

