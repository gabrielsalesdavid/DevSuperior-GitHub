# 📚 Fundamentos de Programação Web

## Introdução

Este documento apresenta os fundamentos essenciais para desenvolvimento web, baseado nas atividades práticas do projeto DevSuperior. Aqui você encontrará os conceitos básicos necessários para começar sua jornada no desenvolvimento web.

---

## 1. Estrutura HTML

### O que é HTML?

HTML (HyperText Markup Language) é a linguagem de marcação utilizada para criar a estrutura e o conteúdo de páginas web. É a base de toda página web e funciona através de **tags** que indicam ao navegador como o conteúdo deve ser exibido.

### Elementos Fundamentais

#### 1.1 Declaração DOCTYPE
```html
<!DOCTYPE html>
```
- Define que o documento é uma página HTML5
- Deve estar sempre na primeira linha do arquivo

#### 1.2 Elemento Root `<html>`
```html
<html lang="en">
  <!-- conteúdo da página -->
</html>
```
- Elemento raiz que encapsula toda a página
- O atributo `lang` define o idioma da página

#### 1.3 Head `<head>`
O `<head>` contém informações sobre o documento que não são exibidas diretamente na página:

```html
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Título da Página</title>
</head>
```

**Elementos importantes do Head:**

| Elemento | Função |
|----------|--------|
| `<meta charset="UTF-8">` | Define a codificação de caracteres |
| `<meta name="viewport">` | Configura responsividade para dispositivos móveis |
| `<title>` | Título exibido na aba do navegador |

#### 1.4 Body `<body>`
```html
<body>
    <!-- Conteúdo visível da página -->
</body>
```
- Contém todo o conteúdo visível da página
- É aqui que você adiciona textos, imagens, links, etc.

### Estrutura Básica Completa

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Minha Primeira Página</title>
</head>
<body>
    <!-- Conteúdo aqui -->
</body>
</html>
```

---

## 2. Tags Básicas de Conteúdo

### Títulos e Parágrafos

#### Títulos (Headings)
```html
<h1>Título Principal</h1>      <!-- Maior, mais importante -->
<h2>Subtítulo</h2>
<h3>Sub-subtítulo</h3>
<h4>Título Nível 4</h4>
<h5>Título Nível 5</h5>
<h6>Título Nível 6</h6>         <!-- Menor -->
```

**Importância:** Use apenas um `<h1>` por página. Os títulos devem seguir uma hierarquia lógica.

#### Parágrafos
```html
<p>Este é um parágrafo de texto. O navegador adiciona espaço antes e depois automaticamente.</p>
```

### Exemplos do Projeto

No arquivo `index.html`:
```html
<h1>Pagina Inicial</h1>
<a href = "vendas.html">Ir para a pagina de vendas</a>
```

No arquivo `vendas.html`:
```html
<h1>Pagina de Vendas</h1>
<p>Vendas = R$ 5000,00</p>
<a href = "index.html">Voltar para a pagina Inicial</a>
```

---

## 3. Links e Navegação

### Tag de Âncora `<a>`

A tag `<a>` é usada para criar links que permitem a navegação entre páginas.

#### Sintaxe Básica
```html
<a href="destino.html">Texto do Link</a>
```

#### Atributos Importantes

| Atributo | Função | Exemplo |
|----------|--------|---------|
| `href` | Define o destino do link | `href="vendas.html"` |
| `target` | Define onde abrir o link | `target="_blank"` (nova aba) |
| `title` | Texto ao passar mouse | `title="Clique aqui"` |

#### Tipos de Links

**1. Links Relativos (Entre páginas do projeto)**
```html
<!-- Na mesma pasta -->
<a href="vendas.html">Ir para vendas</a>

<!-- Em subpasta -->
<a href="Atividades/vendas.html">Vendas</a>

<!-- Para pasta pai -->
<a href="../index.html">Voltar</a>
```

**2. Links Absolutos (Para sites externos)**
```html
<a href="https://www.example.com">Visite Example</a>
```

**3. Links para Email**
```html
<a href="mailto:email@example.com">Enviar Email</a>
```

**4. Links para Telefone**
```html
<a href="tel:+5511999999999">Ligar</a>
```

### Navegação no Projeto DevSuperior

O projeto usa links relativos para conectar as páginas:
- `index.html` → `vendas.html`
- `vendas.html` → `index.html`

Essa estrutura cria uma navegação bidirecional entre as duas páginas.

---

## 4. Atributos HTML

Os atributos fornecem informações adicionais sobre os elementos HTML.

### Atributos Globais

| Atributo | Função |
|----------|--------|
| `id` | Identificador único do elemento |
| `class` | Classe para agrupar elementos |
| `style` | Estilos CSS inline |
| `title` | Texto que aparece ao passar mouse |
| `lang` | Idioma do conteúdo |

### Exemplo de Uso
```html
<h1 id="principal" class="titulo" title="Título da página" lang="pt-BR">
    Bem-vindo!
</h1>
```

---

## 5. Charset e Encoding

### O que é Charset?

Charset define como os caracteres são codificados no arquivo HTML.

```html
<meta charset="UTF-8">
```

### Importância

- **UTF-8** é o padrão universal que suporta todos os idiomas
- Sem esta declaração, caracteres especiais (acentos, cedilha) podem aparecer incorretamente
- Deve ser a primeira tag no `<head>`

---

## 6. Viewport e Responsividade

### Meta Viewport

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Função

- **width=device-width**: A página se adapta à largura do dispositivo
- **initial-scale=1.0**: Define o zoom inicial em 100%
- Essencial para que o site funcione bem em celulares e tablets

### Sem Viewport
- Página aparece muito pequena em dispositivos móveis
- Usuários precisam fazer zoom para ler

### Com Viewport
- Página se adapta automaticamente
- Melhor experiência em qualquer dispositivo

---

## 7. Semântica HTML

### O que é Semântica?

Usar as tags HTML corretas para cada tipo de conteúdo, não apenas `<div>` e `<span>`.

### Tags Semânticas Importantes

```html
<header>...</header>    <!-- Cabeçalho da página -->
<nav>...</nav>          <!-- Menu de navegação -->
<main>...</main>        <!-- Conteúdo principal -->
<article>...</article>  <!-- Artigo independente -->
<section>...</section>  <!-- Seção de conteúdo -->
<aside>...</aside>      <!-- Conteúdo lateral -->
<footer>...</footer>    <!-- Rodapé da página -->
```

### Benefícios

✅ Melhor SEO (Search Engine Optimization)  
✅ Maior acessibilidade  
✅ Código mais legível e manutenível  
✅ Melhor suporte para leitores de tela  

### Exemplo Antes (Sem Semântica)
```html
<div>
    <div>
        <h1>Meu Site</h1>
    </div>
    <div>
        <a href="/">Home</a>
        <a href="/vendas">Vendas</a>
    </div>
    <div>
        <p>Conteúdo principal</p>
    </div>
    <div>© 2026</div>
</div>
```

### Exemplo Depois (Com Semântica)
```html
<body>
    <header>
        <h1>Meu Site</h1>
    </header>
    <nav>
        <a href="/">Home</a>
        <a href="/vendas">Vendas</a>
    </nav>
    <main>
        <p>Conteúdo principal</p>
    </main>
    <footer>© 2026</footer>
</body>
```

---

## 8. Boas Práticas Fundamentais

### 1. Indentação
```html
<html>
  <head>
    <title>Bem Indentado</title>
  </head>
  <body>
    <h1>Título</h1>
  </body>
</html>
```
- Melhora legibilidade
- Facilita debugging

### 2. Nomenclatura
```html
<!-- ✅ BOM -->
<a href="pagina-vendas.html">Vendas</a>

<!-- ❌ RUIM -->
<a href="paginaVendas.html">Vendas</a>
<a href="Pagina_Vendas.html">Vendas</a>
```

### 3. Comentários
```html
<!-- Este é um comentário -->
<!-- Comentários não aparecem na página -->

<!-- 
    Comentários podem ocupar
    várias linhas
-->
```

### 4. Fechar Todas as Tags
```html
<!-- ✅ BOM -->
<p>Parágrafo</p>
<br>

<!-- ❌ RUIM -->
<p>Parágrafo
<br
```

### 5. Usar Aspas em Atributos
```html
<!-- ✅ BOM -->
<a href="vendas.html" title="Página de Vendas">

<!-- ❌ RUIM -->
<a href=vendas.html title=Página de Vendas>
```

---

## 9. Estrutura de Projeto

### Organização Recomendada
```
projeto/
├── index.html           (página inicial)
├── vendas.html          (página de vendas)
├── css/
│   └── style.css        (estilos)
├── js/
│   └── script.js        (scripts)
├── images/
│   └── logo.png         (imagens)
└── docs/                (documentação)
```

### Benefícios
- Facilita manutenção
- Melhora organização
- Escalável para projetos maiores

---

## 10. Resumo dos Fundamentos

| Conceito | Descrição |
|----------|-----------|
| **HTML** | Linguagem de marcação para estrutura |
| **Tags** | Marcadores que definem elementos |
| **Atributos** | Informações adicionais dos elementos |
| **Head** | Contém metadados da página |
| **Body** | Contém conteúdo visível |
| **Links** | Permite navegação entre páginas |
| **Semântica** | Uso correto das tags para significado |
| **Responsividade** | Adaptação para diferentes dispositivos |

---

## Próximos Passos

Agora que você entende os fundamentos, o próximo passo é aprender:

1. **CSS** - Estilo e layout das páginas
2. **JavaScript** - Interatividade e lógica
3. **Web Design** - Princípios de design responsivo
4. **Acessibilidade** - WCAG guidelines
5. **SEO** - Otimização para buscadores

---

**Última atualização:** 17 de janeiro de 2026  
**Nível:** Iniciante  
**Tempo de leitura:** ~20-30 minutos
