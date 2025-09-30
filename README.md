# Documentação do Blog IA - BIA
> Usando GitHub Pages e Jekyll

### Ferramentas Jekyll localmente (Testes do Projeto)
> Requer instalação do Ruby e do Jekyll na máquina

```bash
    # Instalar dependências
    bundle install
    
    # Executar servidor local
    bundle exec jekyll serve
    
    # Limpar registro do servidor local
    bundle exec jekyll clean
```

### Configuração do servidor

> Arquivo _config.yml 

```yaml

# Define título principal do site
title:  IA BLOG - UFRPE

# Endereço de contato
email:  sarahpereiradal@gmail.com

# Descrição do site
description:  >- (define que nao deve ter quebra de linha no texto abaixo)
Esse é um blog de IA, onde serão postados artigos e tutoriais sobre Inteligência Artificial,
Aprendizado de Máquina e Ciência de Dados.

# Define o diretório no qual o site será servido
baseurl:  ""  # the subpath of your site, e.g. /blog

# Domínio padrão do GitHub Pages
url:  "iablog.github.io" 

# Informação adicional para ser anexada ao site caso necessário
github_username:  iablog

# Processador de .md para HTML
markdown:  kramdown

# Syntax Higlight nos blocos de código

highlighter: rouge
kramdown:
  input: GFM 

# Listas de plugins do Jekyll
plugins:
- jekyll-sass-converter
```

### Estrutura do diretório

#### Pasta Principal (root)

- _includes (Armazena elementos portáteis para as páginas)
	- footer.html
	- header.html

- _ layouts (Estrutura das páginas)
	- default.html
	- post.html
	- 404.html
  - category_page.html

- assets (Estilização das páginas e Imagens dos posts)
  - css
	  - style.css
    - syntax.css
  - img 
    - api-gemini.png

> Precisam seguir uma convenção de nomenclatura:  ANO-MÊS-DIA-titulo-do-post
- _posts (Pasta especial que armazena as postagens)
	- 2025-06-16-post.md 
	
- pages (Armazena as páginas principais do site)
	- index.md
	- about.md
	- posts.md
	- 404.md

- category (Armazena as páginas com os posts de cada categoria)
  - deep-learning.md
  - inteligencia-artifical.md

### Estrutura dos Posts

> Front Matter: Define os metadados da página e as variáveis personalizadas
```yaml
---
layout:  post
image: assets/img/api-gemini.png
image_caption: Uma imagem descritiva do Gemini AI
title:  Utilizando a API do Google Gemini
subtitle:  Use o Modelo de IA do Google em Python
date:  2024-09-10 14:30:00 -0300
author:  Vinicius B. Pessoa
categories: [Inteligência Artificial, Deep Learning]
tags: [IA Generativa, Chatbots, Criação de Conteúdo, DALL-E]
---
```
---
[Exemplo: conteúdo do post](/_posts/2025-06-16-post.md)