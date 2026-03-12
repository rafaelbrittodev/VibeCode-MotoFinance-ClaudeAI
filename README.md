# VibeCode-MotoFinance-ClaudeAI
# 🏍️ Simulador de Compra — Royal Enfield Meteor 350

> Projeto desenvolvido via **vibe coding** no [Claude](https://claude.ai) (Anthropic) — uma experiência de construção de software através de conversa natural, sem escrever uma linha de código manualmente.

---

## 📖 Sobre o Projeto

Este é um simulador financeiro completo para a compra da **Royal Enfield Meteor 350 Stellar Black 2026**.

O objetivo foi criar uma ferramenta prática que qualquer pessoa — mesmo sem conhecimento financeiro — consiga usar para tomar uma decisão de compra mais consciente, entendendo o real custo de financiar uma moto: juros, documentação, manutenção e estratégias de amortização.

---

## ✨ Funcionalidades

### 💰 Financiamento
- Simulação completa pelo **Sistema Price** com taxa configurável (padrão: 2,07% a.m.)
- Comparação de 4 cenários de entrada: **20%, 30%, 40% e 50%**
- Prazos de **12x, 24x e 36x**
- Exibe mensalidade, total pago, juros totais e percentual de juros por cenário
- Gráfico visual comparativo de juros entre os cenários

### 📉 Amortização
- Simulação de estratégia de **pagamento duplo mensal** (2x o valor da parcela todo mês)
- Cálculo mês a mês via Tabela Price real — sem simplificações
- Mostra o **prazo real** resultante (ex: 36x → ~18x)
- Calcula economia total de juros, meses eliminados e redução do desembolso total

### 🔧 Manutenção
- Revisões obrigatórias Royal Enfield 350cc para manter a garantia
- Dois cenários de uso: **500 km/mês** e **1.000 km/mês**
- Calendário visual mês a mês indicando quando cada revisão será necessária
- Custo médio mensal de manutenção e total no 1º ano

### 📋 Documentação & Frete
- Detalhamento de todos os custos iniciais: registro, licenciamento, placa Mercosul, IPVA
- IPVA calculado com alíquota real de 2% para motos acima de 180cc em SP
- Frete **R$ 0** — com localização da concessionária oficial em Mogi das Cruzes
- Linha do tempo de desembolsos nos primeiros dias após a compra

### 🧮 Resumo Total
- Painel consolidado combinando todos os custos
- Seleção dinâmica de entrada, prazo e quilometragem
- Exibe **custo total no 1º ano** e **custo total do contrato**
- Destaca o custo real do primeiro mês (entrada + docs + 1ª revisão)

---

## 🛠️ Tecnologias

| Tecnologia | Uso |
|------------|-----|
| HTML5 | Estrutura do documento |
| CSS3 | Estilização, layout responsivo, animações |
| JavaScript (Vanilla) | Lógica financeira, simulações, interatividade |
| Google Fonts | Tipografia (Playfair Display + DM Sans) |

Nenhuma dependência externa. **Zero frameworks. Zero bibliotecas JS.** Funciona offline, basta abrir o arquivo `.html` em qualquer navegador moderno.

---

## 🧮 Lógica Financeira

### Sistema Price
As parcelas são calculadas pela fórmula clássica do Sistema Francês de Amortização (Price):

```
PMT = PV × [ i × (1+i)^n ] / [ (1+i)^n - 1 ]

Onde:
  PV = saldo devedor (valor financiado)
  i  = taxa de juros mensal
  n  = número de parcelas
```

### Amortização Dupla (simulação mês a mês)
A cada mês, o simulador executa o seguinte loop:

```
1. Juros do mês  = saldo_devedor × taxa
2. Amort. normal = parcela - juros_do_mês
3. Amort. extra  = parcela (valor total extra aplicado no principal)
4. Novo saldo    = saldo - amort_normal - amort_extra
5. Repete até saldo ≤ 0
```

Isso garante que o prazo resultante e a economia de juros sejam calculados com precisão real, sem aproximações.

---

## 🚀 Como Usar

1. Faça o download do arquivo `simulador-meteor350.html` ou abra via GitHub Pages.
2. Abra em qualquer navegador (Chrome, Firefox, Edge, Safari)
3. Navegue pelas abas no menu superior
4. Ajuste a **taxa de juros** diretamente no cabeçalho
5. Use os botões de seleção para personalizar entrada, prazo e quilometragem

Não requer instalação, servidor ou internet após o carregamento inicial das fontes.

---

## 💬 Como foi construído — Vibe Coding com Claude

Todo este projeto foi criado através de **conversa natural** com o Claude (Anthropic), sem escrever código manualmente. O processo foi:

1. **Ideação conversacional** — descrevi o problema: queria entender o custo real de comprar uma moto financiada
2. **Iterações progressivas** — cada funcionalidade foi pedida em linguagem natural ("adiciona a simulação de amortização", "quero ver o custo de manutenção por km rodado")
3. **Correção colaborativa** — erros de lógica financeira foram identificados e corrigidos em conversa ("tem certeza que está certo? Se pago 2x a parcela todo mês, o prazo não deveria cair pela metade?")
4. **Refinamento de UX** — ajustes visuais e de usabilidade também via descrição ("deixa a taxa de juros editável direto no cabeçalho")

### O que o vibe coding demonstra aqui:
- É possível construir ferramentas financeiras funcionais e matematicamente corretas sem saber programar
- A qualidade do resultado depende da **clareza das perguntas e da capacidade de revisar criticamente** as respostas
- O processo é iterativo — bugs e imprecisões são encontrados e corrigidos em conversa
- Conhecimento do domínio (neste caso, finanças pessoais) é mais importante do que conhecimento técnico

---

## ⚠️ Aviso

Este simulador tem **fins exclusivamente informativos**. Os valores de taxa de juros, IPVA, documentação e revisões são estimativas baseadas em dados de mercado de 2026. Confirme todas as condições com a concessionária e instituição financeira antes de fechar qualquer negócio.

---

## 📄 Licença

MIT License — sinta-se livre para usar, modificar e distribuir.

---

*Feito com ❤️ e muita conversa com IA.*
