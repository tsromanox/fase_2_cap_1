# FIAP - Faculdade de Informática e Administração Paulista

<p align="center">
<a href= "https://www.fiap.com.br/"><img src="assets/logo-fiap.png" alt="FIAP - Faculdade de Informática e Admnistração Paulista" border="0" width=40% height=40%></a>
</p>

<br>

# Otimização de Recursos Hídricos e Nutricionais na Agricultura Através de Sensoriamento e Análise de Dados.

## FarmTech Solutions

## 👨‍🎓 Integrantes: 
- <a href="https://www.linkedin.com/company/inova-fusca">Anna Cecilia Moreira Cabral</a>
- <a href="https://www.linkedin.com/company/inova-fusca">Heitor Exposito de Sousa</a>
- <a href="https://www.linkedin.com/company/inova-fusca">Letícia Gomez Pinheiro</a> 
- <a href="https://www.linkedin.com/company/inova-fusca">Thiago Sabato Romano</a> 
- <a href="https://www.linkedin.com/company/inova-fusca">Vicenzo de Simone Montefusco</a>

## 👩‍🏫 Professores:
### Tutor(a) 
- <a href="https://www.linkedin.com/company/inova-fusca">Leonardo Ruiz Orabona</a>
### Coordenador(a)
- <a href="https://www.linkedin.com/company/inova-fusca">Andre Godoi Chiovato</a>


## 📜 Descrição

### Otimizando Recursos Agrícolas Através de Dados
<p>
A agricultura moderna enfrenta o desafio crescente de produzir mais alimentos com menos recursos, impulsionada por pressões econômicas e preocupações ambientais.1 No Brasil, onde a agricultura é um pilar econômico, a otimização do uso de água e nutrientes é fundamental para a sustentabilidade e rentabilidade das lavouras. Tradicionalmente, muitas práticas agrícolas baseiam-se na experiência e intuição do produtor. No entanto, a agricultura de precisão (AP) oferece uma abordagem transformadora, utilizando dados coletados em tempo real para tomar decisões mais informadas e eficientes.</p>
<p>Este relatório apresenta um guia técnico detalhado para o produtor rural interessado em implementar um sistema de monitoramento e análise de dados baseado em sensores de umidade do solo (S1), pH do solo (S2) e nutrientes NPK (Nitrogênio, Fósforo e Potássio - S3). O objetivo central é aplicar a quantidade certa de água e vitaminas (nutrientes) no momento certo e no local certo, visando aumentar a produção e otimizar o uso de insumos [User Query].</p>

O sistema proposto abrange diversos componentes interconectados:
- <b>Sensores</b>: Coletam dados cruciais sobre as condições do solo (umidade, pH, NPK) em tempo real.
- <b>Transmissão de Dados</b>: Protocolos e redes que enviam os dados dos sensores para um sistema central.
- <b>Armazenamento de Dados</b>: Bancos de dados adequados para guardar grandes volumes de dados de séries temporais gerados pelos sensores.
- <b>Análise de Dados</b>: Processamento dos dados coletados para identificar tendências, correlações e, potencialmente, prever necessidades futuras usando técnicas estatísticas e de aprendizado de máquina (Machine Learning - ML).
- <b>Suporte à Decisão e Automação</b>: Utilização das análises para gerar recomendações de manejo ou integrar-se a sistemas de controle para ajustar automaticamente a irrigação e a fertirrigação.
- <b>Visualização</b>: Apresentação clara das informações e recomendações ao produtor através de painéis de controle (dashboards).

<p>Ao adotar essa abordagem data-driven, o produtor pode transcender as limitações das práticas tradicionais, transformando dados brutos em inteligência acionável para uma gestão agrícola mais eficiente, sustentável e lucrativa.2 Este documento servirá como um roteiro prático, abordando desde a escolha da tecnologia de banco de dados até a interpretação de estudos de caso relevantes.</p>

## 📁 Estrutura de pastas

Dentre os arquivos e pastas presentes na raiz do projeto, definem-se:

- <b>assets</b>: Diagrama do Projeto em formato PDF

- <b>document</b>: aqui estão todos os documentos do projeto que as atividades poderão pedir. Na subpasta "other", adicione documentos complementares e menos importantes.

- <b>mapa_do_tesouro.dmd</b>: Projeto do modelo MER que deve ser aberto com o <a href="https://www.oracle.com/br/database/sqldeveloper/technologies/sql-data-modeler/download/">SQL Developer Data Modeler</a>

- <b>README.md</b>: arquivo que serve como guia e explicação geral sobre o projeto (o mesmo que você está lendo agora).

## 🔧 Como executar o código

*Acrescentar as informações necessárias sobre pré-requisitos (IDEs, serviços, bibliotecas etc.) e instalação básica do projeto, descrevendo eventuais versões utilizadas. Colocar um passo a passo de como o leitor pode baixar o seu código e executá-lo a partir de sua máquina ou seu repositório. Considere a explicação organizada em fase.*

## 📊 Entidades
### - <b>Fazenda</b>: Fazenda a ser monitorda

ENTIDADE: T_FTS_FAZENDA
| ATRIBUTO            | TIPO ATRIBUTO           | CARD MIN           |       CARD MAX         |
|------------------|------------------|---------------------|----------------------|
| cd_fazenda | simples, determinante | 1 = mandatório | 1 = monovalorado |
| nm_fazenda | simples | 1 = mandatório | 1 = monovalorado |

### - <b>Campo</b>: Divisoes da Fazenda ,por exemplo: Campo Sul, Norte, Leste, etc

ENTIDADE: T_FTS_CAMPO
| ATRIBUTO            | TIPO ATRIBUTO           | CARD MIN           |       CARD MAX         |
|------------------|------------------|---------------------|----------------------|
| cd_campo | simples, determinante | 1 = mandatório | 1 = monovalorado |
| nm_campo | simples | 1 = mandatório | 1 = monovalorado |

### - <b>Zona de Manejo</b>: Cada Campo, sera dividido em porçoes menores onde teremos o cultivo de um unica cultura e onde serão instalados um sensor de cada tipo(S1, S2 e s3).
ENTIDADE: T_FTS_ZONA

| ATRIBUTO            | TIPO ATRIBUTO           | CARD MIN           |       CARD MAX         |
|------------------|------------------|---------------------|----------------------|
| cd_zona | simples, determinante | 1 = mandatório | 1 = monovalorado |
| nm_zona | simples | 1 = mandatório | 1 = monovalorado |

### - <b>Cultura</b>: Tipos de Cultura, esta podera ser cultivada em mais de uma Zona, porem cada Zora somente podera receber uma Cultura
ENTIDADE: T_FTS_CULTURA

| ATRIBUTO            | TIPO ATRIBUTO           | CARD MIN           |       CARD MAX         |
|------------------|------------------|---------------------|----------------------|
| cd_cultura | simples, determinante | 1 = mandatório | 1 = monovalorado |
| nm_cultura | simples | 1 = mandatório | 1 = monovalorado |

### - <b>Sensor</b>: Cadastro dos sensores utilizados
ENTIDADE: T_FTS_SENSOR

| ATRIBUTO            | TIPO ATRIBUTO           | CARD MIN           |       CARD MAX         |
|------------------|------------------|---------------------|----------------------|
| cd_sensor | simples, determinante | 1 = mandatório | 1 = monovalorado |
| nm_sensor | simples | 1 = mandatório | 1 = monovalorado |

### - <b>Sensor Tipo</b>: Cadastro dos sensores utilizados
ENTIDADE: T_FTS_SENSOR_TIPO

| ATRIBUTO            | TIPO ATRIBUTO           | CARD MIN           |       CARD MAX         |
|------------------|------------------|---------------------|----------------------|
| cd_sensor_tipo | simples, determinante | 1 = mandatório | 1 = monovalorado |
| nm_sensor_tipo | simples | 1 = mandatório | 1 = monovalorado |

<p>Tipos de Sensores:</p>
<p>O sistema proposto utiliza três tipos principais de sensores:</p>
<p>S1: Sensores de Umidade do Solo:</p>
<p>Tecnologias: Existem várias tecnologias para medir a umidade do solo, incluindo TDR (Reflectometria no Domínio do Tempo), FDR (Reflectometria no Domínio da Frequência), sensores capacitivos, tensiômetros e blocos de gesso. Sensores TDR/FDR e capacitivos medem a constante dielétrica do solo, que varia com o teor de água. Tensiômetros medem diretamente a tensão ou potencial matricial da água no solo (SMP).

Saída: Sensores dielétricos (TDR, FDR, capacitivos) geralmente fornecem a Umidade Volumétrica do Solo (Volumetric Water Content - VWC), expressa como porcentagem (%) ou fração.Tensiômetros fornecem o Potencial Matricial do Solo (Soil Matric Potential - SMP), geralmente em quilopascals (kPa) ou centibares (cb). É importante notar que 1 kPa é aproximadamente igual a 1 cb, e o SMP é tecnicamente uma pressão negativa (sucção).

Considerações: Sensores baseados em VWC muitas vezes requerem calibração específica para o tipo de solo para maior precisão. Tensiômetros são frequentemente preferidos para culturas sensíveis ao estresse hídrico (como hortaliças e frutas vermelhas) e funcionam bem em diferentes texturas de solo sem calibração específica do solo, mas são mais precisos em condições mais úmidas (próximo à capacidade de campo). Os dados podem ser lidos localmente ou transmitidos remotamente.</p>
<p>S2: Sensores de pH do Solo:</p>
<p>Função: Medem a acidez ou alcalinidade do solo, um fator crítico que afeta a disponibilidade de nutrientes para as plantas.

Princípio: Geralmente baseados em reações eletroquímicas, onde um eletrodo reage com a concentração de íons hidrogênio na solução do solo para gerar um sinal elétrico que é convertido em valor de pH.

Considerações: A precisão depende de calibração regular. O intervalo de medição típico é de 0 a 14 unidades de pH.</p>
<p>S3: Sensores de Nutrientes do Solo (NPK):</p>
Função: Monitoram os níveis dos macronutrientes primários: Nitrogênio (N), Fósforo (P) e Potássio (K).

Princípio: Podem utilizar tecnologias espectroscópicas (medindo a absorção de luz em diferentes comprimentos de onda) ou eletroquímicas (medindo respostas de corrente a íons específicos), combinadas com algoritmos de análise de dados.

Considerações: Fornecem dados em tempo real para orientar a fertilização de precisão. A tecnologia de sensores NPK diretos no solo ainda está em evolução, e sua precisão e confiabilidade podem variar em comparação com análises laboratoriais tradicionais, embora ofereçam a vantagem da medição instantânea no campo.

### - <b>Metrica</b>: Cadastro dos sensores utilizados
ENTIDADE: T_FTS_Metrica

| ATRIBUTO            | TIPO ATRIBUTO           | CARD MIN           |       CARD MAX         |
|------------------|------------------|---------------------|----------------------|
| cd_metrica | simples, determinante | 1 = mandatório | 1 = monovalorado |
| vl_metrica | simples | 1 = mandatório | 1 = monovalorado |
| vl_longitude | simples | 1 = mandatório | 1 = monovalorado |
| vl_latitude | simples | 1 = mandatório | 1 = monovalorado |

## 🗃 Histórico de lançamentos

* 0.1.0 - 22/04/2025
    *

## 📋 Licença

<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1"><p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/agodoi/template">MODELO GIT FIAP</a> por <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://fiap.com.br">Fiap</a> está licenciado sobre <a href="http://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">Attribution 4.0 International</a>.</p>

