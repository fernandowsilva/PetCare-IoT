#PetCare IoT - Arquitetura do Sistema

## 1. Visao geral

O PetCare IoT e um projeto de automacao de alimentos e hidratacao de animais domesticos. 
O sistema pretende monitorar o consumo de agua e racao, automatizar o abastecimento e armazenar informacoes para consulta em uma dashboard web.

## 2. Arquitetura geral

O sistema sera dividido em tres partes principais:

### 2.1 ESP32

Responsavel pelo controle fisico do equipamento.

Funcoes planejadas:
- Leitura das celulas de carga.
- Controle do dosador de racao.
- Controle da bomba de agua.
- Armazenamento local de eventos.
- Comunicacao via WIi-Fi. 

### 2.2 Ubuntu Server

Responsavel pelo processamento e armazenamento dos dados.

Tecnologias planejadas:
- Pyton
- FastAPI
- SQLite

### 2.3 Dashboard Web

Interface para visualizacao e gerenciamento do sistema.

Tecnologias planejadas: 
- HTML
-CSS
-JavaScript

## 3. Comunicacao

O ESP32 enviara informacoes ao servidor por meio de comunicacao via Wi-Fi.

A comunicacao podera utilizar API REST ou MQTT

## 4. Funcionamento offline

O ESP32 devera continuar executando as automacoes mesmo quando o servidor estiver indisponivel.

Os eventos serao armazenados localmente e enviados ao servidor quando a comunicacao for restabelecida.

## 5. Monitoramento

O sistema devera acompanhar:

- Peso da racao disponivel
- Peso da racao no recipiente
- Quantidade estimada de agua
- Abastecimentos realizados
- Consumo estimado
- Falhas e eventos de automacao

##6 Estado do projeto

Fase atual: planejamento e desenvolvimento da estrutura inicial de software.

As funcionalidades descritas ainda serao implementadas e testadas. 
