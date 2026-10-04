# Simulador de Investimentos em Fundos Imobiliários (FIIs)

Ferramenta de modelagem financeira desenvolvida em Excel para simulação de carteiras de Fundos Imobiliários, projeção de dividendos e análise de cenários a longo prazo, considerando impactos reais de mercado como Imposto de Renda e Inflação.

## Objetivo do Projeto
Esta ferramenta foi desenvolvida para responder às cinco principais perguntas de negócio antes de um investimento:
1. Quanto investir por mês;
2. Por quantos anos;
3. Qual a taxa de rendimento mensal esperada;
4. Quanto de patrimônio será acumulado no período;
5. Qual será a renda passiva (dividendos) gerada.

## Evoluções Implementadas
Além do escopo inicial, apliquei regras de negócio avançadas para aproximar a ferramenta da realidade do mercado financeiro:
* Criei um gráfico de pizza, que atualiza a projeção percentualmente do portfólio de FIIs, e é atualizado conforme o perfil do usuário
* Também acrescentei uma tabela com o nome "Análise de Retorno Real", onde eu calculei o Lucro Bruto conforme o valor e quantidade de anos indicado pelo usuário, o cálculo básico do Imposto de Renda (20% em cima do lucro), o patrimônio líquido (lucro bruto - imposto de renda) e o poder de compra real (patrimônio líquido agindo de acordo com a inflação que o usuário decide).

## Meu Raciocínio Lógico e Estrutura Técnica
Abaixo, detalho como utilizei as funções do Excel e a matemática financeira para construir o motor do simulador:

### 1. Função VF (Valor Futuro) e Projeção de Cenários
  * Utilizei a função VF (Valor Futuro) para calcular os juros compostos de 2 a 30 anos, fixando referências absolutas para garantir a integridade dos cálculos em massa.

### 2. PROCV e Chave Composta na Matriz de Alocação
  * Apliquei na matriz de alocação para cruzar o perfil do investidor com os tipos de fundos, alimentando o gráfico de forma automatizada através de tabelas criadas em outra planilha.

### 3. Intervalos Nomeados
  * Substitui as células (como C4 ou D5) por variáveis semânticas (ex: `taxa_mensal`, `Aporte`, `inflacao`), deixando as fórmulas limpas, profissionais e dinâmicas.


## 📸 Demonstração da Ferramenta

### Simulação 1: Perfil Agressivo
<img width="797" height="942" alt="Captura de tela 2026-10-04 201723" src="https://github.com/user-attachments/assets/390c95b2-f6ca-42a4-ba9e-9403c62c82c8" />
<img width="795" height="815" alt="Captura de tela 2026-10-04 201729" src="https://github.com/user-attachments/assets/06235f6c-7d94-4d13-8d90-156d13f1e997" />

### Simulação 2: Perfil Conservador
<img width="812" height="940" alt="Captura de tela 2026-10-04 201749" src="https://github.com/user-attachments/assets/830c7a63-7e29-4baa-9581-7ef3c37ef91e" />
<img width="815" height="842" alt="Captura de tela 2026-10-04 201753" src="https://github.com/user-attachments/assets/3776fdbc-86d6-4f83-8012-d59ed0d8b6e5" />
