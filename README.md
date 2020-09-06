# LUMEN. Gestão da Matriz Energética.  

Sistema para gerenciamento de energias.

Histórico: 
Mesmo existindo sistemas similares no mercado, os clientes precisavam de acesso ao banco de dados para integra os dados de energia com os da produção, além disso, também solicitavam relatórios da qualidade da energia.
Estes pontos motivaram este projeto:
1. Disponibilizando os dados via REST/JSON para os diversos clientes.
2. Datalog para exportar os dados:  Conrrente (A, B, C e neutro), Fator de Potência (A, B, C e Total), Frequência, Potência Aparente (A, B, C e Total), Potência Reativa (A, B, C e Total), Potência Ativa (A, B, C e Total), Tensão (AB, BC, CA, AN, BN, CN), Distroções Harmônicas de Corrente (A, B, C), Distroções Harmônicas de Tensão (AB, BC, CA, AN, BN, CN).

Os multimedodores e relés de proteção que possuem drive de comunicação já utilizados são: PM9C, PM500, PM750, PM3255, PM5110, SEPAM S80, S40, S20, PAC3200, KRON MULTI K, NSX.
Os multimedidores com comunicação possuem um mapa de memória disponível, então caso não estejam na lista podem ser implementados.

Nota: No fluxigrama básico, figura abaixo, o equipamento abaixo do servidor é um gateway, contudo pode ser um controlador de demanda afim de controlar fator de potência e que não haja ultrapassagens de demanda.


*******

<div id='tela1'/>  

## Fluxograma Básico da troca de mensagens entre os ativos e passisvos da rede.  

![](https://github.com/iberematias/LUMEN-Gegenriamento_Energias/blob/master/src/img/0-fluxobasico.png)

*******

Este software contém os seguintes requisitos:
 1. Painel para visualizar, graficamente sete medições simultaneas;
 2. Ultimas medições; 
 3. Relatórios gráficos e tabela de resumo: Demanda, consumo e fator de potência;
 4. Tela com o Diagrama Unifilar do cliente; 
 5. Relatório de produção, para consumo específico, Normal metro cúbico por Tonelada Produzida;
 6. Relatório gráfico de variável de processos: Temperatura, pressão, umidade etc;
 7. Monitoração online de relés de proteção;
 8. Relatório de eventos;
 9. Envio de email alarmes (demanda, consumo, fp) e dos ativos de rede;
 10. Relatórios de tensão (V), corrente (A) e distorções harmônicas (THD).

*******
Tecnologias    
 1. Grails: Fronteend, páginas web e serviços REST.
 2. Groovy: Drive de Comunicação com protocolos industriais: Modbus e Ethenet/IP. 
 3. Postgresql: Base de dados.
 
*******

<div id='tela1'/>  

## Telas do Projeto: Login.  

![](https://github.com/iberematias/LUMEN-Gegenriamento_Energias/blob/master/src/img/1-login.png)

*******

<div id='tela2'/>  

## Telas do Projeto: Lista de Medidores com as últimas medições.   

![](https://github.com/iberematias/LUMEN-Gegenriamento_Energias/blob/master/src/img/2-listaM.png)

*******

<div id='tela3'/>  

## Telas do Projeto: Painel.    

![](https://github.com/iberematias/LUMEN-Gegenriamento_Energias/blob/master/src/img/3-painel.png)

*******

<div id='tela4'/>  

## Telas do Projeto: Relatório de Demanda (KW).   

![](https://github.com/iberematias/CLUMEN-Gegenriamento_Energias/blob/master/src/img/4-Demanda.png)

*******

<div id='tela5'/>  

## Telas do Projeto: Relatório de Consumo (kWh).   

![](https://github.com/iberematias/LUMEN-Gegenriamento_Energias/blob/master/src/img/5-Consumo.png)

*******

<div id='tela6'/>  

## Telas do Projeto: Diagrama Unifilar   

![](https://github.com/iberematias/LUMEN-Gegenriamento_Energias/blob/master/src/img/6-alarms.png)

*******

<div id='tela7'/>  

## Telas do Projeto: Relatório de variável de processos (Temperatura, pressão, umidade etc)   

![](https://github.com/iberematias/LUMEN-Gegenriamento_Energias/blob/master/src/img/7-vp.png)

*******

<div id='tela8'/>  

## Telas do Projeto: Relatório de Consumo (Nm³) e Consumo Específico (Nm³/Ton)   

![](https://github.com/iberematias/LUMEN-Gegenriamento_Energias/blob/master/src/img/8-consumoespecifico.png)

*******