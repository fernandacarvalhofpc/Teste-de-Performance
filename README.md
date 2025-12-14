README — Execução dos Testes de Performance (API de CEP)
📌 Visão Geral

Este projeto tem como objetivo demonstrar a execução de testes de performance em uma API REST de consulta de CEP, utilizando a ferramenta Apache JMeter.

O vídeo anexado a este material apresenta a execução prática dos testes, enquanto este README descreve passo a passo como configurar e rodar os scripts.

🎯 Objetivo dos Testes

Avaliar o tempo de resposta da API de CEP

Verificar o comportamento da API sob carga concorrente

Identificar possíveis gargalos de performance

Analisar métricas como:

Tempo médio de resposta

P90 e P95

Taxa de erro 

🛠️ Pré-requisitos

Antes de executar os testes, certifique-se de que possui:

Java JDK 8 ou superior instalado

Apache JMeter instalado (versão 5.x ou superior)

Sistema operacional Windows, Linux ou macOS

Para verificar se o Java está instalado:

java -version

📂 Estrutura dos Arquivos

A estrutura do projeto segue o padrão abaixo:

/jmeter
 └── teste_api_cep.jmx
 └── ceps.csv

teste_api_cep.jmx → Contém o plano de teste do JMeter (.jmx)

ceps.csv → Arquivo CSV com os CEPs utilizados nas requisições

1️⃣ Abrir o JMeter
Navegue até a pasta onde o JMeter foi instalado

Execute o arquivo:

Windows: jmeter.bat

Linux/Mac: jmeter.sh

2️⃣ Abrir o Script de Teste

No menu superior, clique em File → Open

Selecione o arquivo:

scripts/teste_api_cep.jmx

3️⃣ Configuração do Plano de Teste

O script já contém:

Thread Group configurado para simular múltiplos usuários (com 4 e 5 usuários)

HTTP Request apontando para o endpoint da API de CEP

Listeners para análise dos resultados (Summary Report, View Results Tree, Aggregate Report)

4️⃣ Executar o Teste

Clique no botão Start (▶️) no topo da ferramenta

Aguarde a finalização da execução conforme o cenário configurado

5️⃣ Analisar os Resultados

Após a execução, consulte os listeners configurados para verificar:

Tempo médio de resposta

Percentis P90 e P95

Taxa de erro

Throughput

Esses dados são utilizados para avaliar a performance e escalabilidade da API de CEP.

🎥 Sobre o Vídeo de Demonstração

O vídeo anexado apresenta:

Execução do cenário com usuários simultâneos

Visualização dos resultados nos listeners

O objetivo do vídeo é comprovar a execução prática do artefato, complementando este README.

✅ Observações Importantes

Os testes foram executados em ambiente de QA, portanto os resultados não representam produção

A execução em ambiente produtivo requer cuidados adicionais

Os valores obtidos devem ser analisados considerando o contexto do ambiente

🏁 Conclusão

Este projeto demonstra como testes de performance em APIs REST, mesmo em serviços simples como uma API de consulta de CEP, são fundamentais para garantir estabilidade, previsibilidade e qualidade do sistema.

A utilização do JMeter permitiu simular cenários reais de carga e identificar limites de desempenho, reforçando a importância dos testes não funcionais no processo de desenvolvimento de software.
