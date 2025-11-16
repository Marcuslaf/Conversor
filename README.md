# 💱 Conversor de Moedas

Um conversor de moedas desktop desenvolvido em Java com interface gráfica moderna, que utiliza taxas de câmbio em tempo real através da API ExchangeRate-API.

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![Swing](https://img.shields.io/badge/Swing-GUI-blue?style=for-the-badge)
![Gson](https://img.shields.io/badge/Gson-JSON-green?style=for-the-badge)

## 📋 Índice

- [Características](#-características)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [Pré-requisitos](#-pré-requisitos)
- [Instalação](#-instalação)
- [Como Usar](#-como-usar)
- [Estrutura do Projeto](#-estrutura-do-projeto)
- [Desenvolvimento com IA](#-desenvolvimento-com-ia)
- [API Utilizada](#-api-utilizada)
- [Capturas de Tela](#-capturas-de-tela)
- [Licença](#-licença)

## ✨ Características

- ✅ Conversão entre 10 moedas diferentes
- 🌐 Taxas de câmbio em tempo real
- 🎨 Interface gráfica moderna e intuitiva
- 🔄 Botão para trocar moedas rapidamente
- ⚡ Operação assíncrona (não trava a interface)
- ✔️ Validação de entrada de dados
- 🎯 Fácil de usar e responsivo

## 🛠️ Tecnologias Utilizadas

### Linguagem e Framework
- **Java 8+** - Linguagem de programação principal
- **Swing** - Framework para interface gráfica (GUI)
- **SwingWorker** - Para operações assíncronas e melhor experiência do usuário

### Bibliotecas
- **Gson 2.10.1** - Biblioteca do Google para parsing de JSON
  - Utilizada para deserializar a resposta da API
  - Mais leve e eficiente que alternativas
  
### IDE
- **IntelliJ IDEA** - Ambiente de desenvolvimento integrado
  - Autocomplete inteligente
  - Refatoração de código
  - Debugging avançado

### API Externa
- **ExchangeRate-API v6** - API REST para taxas de câmbio
  - Endpoint: `https://v6.exchangerate-api.com/v6/{API_KEY}/latest/{BASE_CURRENCY}`
  - Fornece taxas atualizadas diariamente
  - Suporta mais de 160 moedas

## 📦 Pré-requisitos

Antes de começar, você precisará ter instalado:

- [Java JDK 8 ou superior](https://www.oracle.com/java/technologies/downloads/)
- [IntelliJ IDEA](https://www.jetbrains.com/idea/download/) (Community ou Ultimate)
- Conexão com a internet (para consumir a API)

## 🚀 Instalação

### 1. Clone ou baixe o projeto

```bash
git clone https://github.com/Marcuslaf/Conversor
cd Conversor
```

### 2. Abra no IntelliJ IDEA

- Abra o IntelliJ IDEA
- Selecione **File → Open**
- Navegue até a pasta do projeto
- Clique em **OK**

### 3. Adicione a dependência Gson

#### Opção A: Maven (Recomendado)

Adicione ao arquivo `pom.xml`:

```xml
<dependencies>
    <dependency>
        <groupId>com.google.code.gson</groupId>
        <artifactId>gson</artifactId>
        <version>2.10.1</version>
    </dependency>
</dependencies>
```

#### Opção B: Gradle

Adicione ao arquivo `build.gradle`:

```gradle
dependencies {
    implementation 'com.google.code.gson:gson:2.10.1'
}
```

#### Opção C: JAR Manual

1. Baixe o [gson-2.10.1.jar](https://repo1.maven.org/maven2/com/google/code/gson/gson/2.10.1/gson-2.10.1.jar)
2. No IntelliJ: **File → Project Structure → Libraries → + → Java**
3. Selecione o arquivo JAR baixado

### 4. Execute o projeto

- Localize a classe `CurrencyConverter.java`
- Clique com botão direito → **Run 'CurrencyConverter.main()'**
- Ou pressione `Shift + F10`

## 💡 Como Usar

1. **Digite o valor** que deseja converter no campo "Valor"
2. **Selecione a moeda de origem** no dropdown "De:"
3. **Selecione a moeda de destino** no dropdown "Para:"
4. **Clique em "Converter"** para ver o resultado
5. Use o botão **"⇅ Trocar Moedas"** para inverter rapidamente as moedas selecionadas

### Moedas Disponíveis

| Código | Moeda |
|--------|-------|
| USD | Dólar Americano |
| BRL | Real Brasileiro |
| EUR | Euro |
| GBP | Libra Esterlina |
| JPY | Iene Japonês |
| CAD | Dólar Canadense |
| AUD | Dólar Australiano |
| CHF | Franco Suíço |
| CNY | Yuan Chinês |
| INR | Rúpia Indiana |

## 📁 Estrutura do Projeto

```
conversor-moedas/
│
├── src/
│   └── CurrencyConverter.java    # Classe principal com GUI e lógica
│
├── lib/                           # Bibliotecas externas (se usar JAR manual)
│   └── gson-2.10.1.jar
│
├── pom.xml                        # Configuração Maven (opcional)
├── build.gradle                   # Configuração Gradle (opcional)
└── README.md                      # Este arquivo
```

## 🤖 Desenvolvimento com IA

Este projeto foi desenvolvido com o auxílio de **Inteligência Artificial (Claude - Anthropic)**, que contribuiu significativamente em várias etapas:

### Áreas de Contribuição da IA

#### 1. **Arquitetura do Código**
- Sugestão da estrutura MVC simplificada
- Organização dos componentes Swing
- Implementação de padrões de design (SwingWorker para operações assíncronas)

#### 2. **Interface Gráfica**
- Design e layout dos componentes visuais
- Escolha de cores e paleta harmônica
- Posicionamento com GridBagLayout
- Melhorias na legibilidade e contraste dos botões

#### 3. **Integração com API**
- Implementação da requisição HTTP
- Tratamento de resposta JSON com Gson
- Gerenciamento de erros e exceções
- Configuração de timeouts

#### 4. **Boas Práticas**
- Validação de entrada do usuário
- Tratamento de erros com mensagens amigáveis
- Uso de threads separadas para não bloquear a UI
- Nomenclatura clara de variáveis e métodos

#### 5. **Documentação**
- Comentários no código
- Este README completo
- Instruções de instalação e uso

### Metodologia de Desenvolvimento

O desenvolvimento seguiu uma abordagem iterativa:

1. **Requisitos iniciais** - Definição das funcionalidades principais
2. **Prototipagem rápida** - Criação da estrutura básica com IA
3. **Refinamento** - Ajustes de UI/UX baseados em feedback
4. **Testes** - Validação de funcionalidades
5. **Documentação** - Criação do README e comentários

### Benefícios do Uso de IA

- ⚡ **Velocidade**: Desenvolvimento acelerado
- 🎯 **Qualidade**: Código seguindo boas práticas
- 📚 **Aprendizado**: Explicações sobre tecnologias utilizadas
- 🐛 **Debugging**: Identificação rápida de problemas
- 🎨 **Design**: Sugestões de melhorias visuais

## 🌐 API Utilizada

### ExchangeRate-API

**Endpoint Base:**
```
https://v6.exchangerate-api.com/v6/{API_KEY}/latest/{BASE_CURRENCY}
```

**Exemplo de Requisição:**
```
GET https://v6.exchangerate-api.com/v6/86387097a157d1b3a20362d4/latest/USD
```

**Exemplo de Resposta:**
```json
{
  "result": "success",
  "documentation": "https://www.exchangerate-api.com/docs",
  "terms_of_use": "https://www.exchangerate-api.com/terms",
  "time_last_update_unix": 1699920001,
  "time_last_update_utc": "Tue, 14 Nov 2023 00:00:01 +0000",
  "time_next_update_unix": 1700006401,
  "time_next_update_utc": "Wed, 15 Nov 2023 00:00:01 +0000",
  "base_code": "USD",
  "conversion_rates": {
    "USD": 1,
    "BRL": 4.9234,
    "EUR": 0.9234,
    "GBP": 0.7987,
    ...
  }
}
```

### Limitações da API (Plano Gratuito)
- 1.500 requisições por mês
- Taxas atualizadas diariamente
- Sem necessidade de autenticação complexa

## 📸 Capturas de Tela

### Tela Principal
```
┌─────────────────────────────────────┐
│     💱 Conversor de Moedas          │
├─────────────────────────────────────┤
│                                     │
│  Valor: [1.00____________]          │
│                                     │
│  De:    [USD - Dólar Americano ▼]  │
│                                     │
│        [⇅ Trocar Moedas]            │
│                                     │
│  Para:  [BRL - Real Brasileiro ▼]  │
│                                     │
│         [   Converter   ]           │
│                                     │
├─────────────────────────────────────┤
│  1.00 USD = 4.92 BRL                │
└─────────────────────────────────────┘
```

## 🔧 Possíveis Melhorias Futuras

- [ ] Adicionar histórico de conversões
- [ ] Implementar gráfico de variação cambial
- [ ] Salvar moedas favoritas
- [ ] Modo offline com cache de taxas
- [ ] Tema escuro/claro
- [ ] Internacionalização (i18n)
- [ ] Exportar resultados para PDF/Excel

---

## 👨‍💻 Autor

Desenvolvido por Marcus Lafaiete e auxílio de IA (Claude - Anthropic)

🙏 Agradecimentos

Alura e Oracle One - Pelo excelnte curso e conhecimento compartilhado
Alunos - Ao queridos alunos (colegas de jornada) que compartilham suas experiências na comunicade e nos canais do Discord

⭐ Se este projeto foi útil para você, considere dar uma estrela no repositório!
---

⭐ Se este projeto foi útil para você, considere dar uma estrela no repositório!
