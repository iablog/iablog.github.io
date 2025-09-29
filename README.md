# Documentação do Blog IA - BIA
> Usando Github pages e Jkelly

### Ferramentas jkelly localmente (Testes do Projeto)
> Requer instalação do Ruby e do Jkelly na máquina

```bash
    # Instalar dependencias
    bundle install
    
    # Executar servidor local
    bundle exec jekyll serve
    
    # Limpar registro do servidor local
    bundle exec jekyll clean
```

### Configuração do servidor

> Arquivo _config.yml 

```yaml

# Define titulo principal do site
title:  IA BLOG - UFRPE

# Endereco de contato
email:  gabrielbelo.dev@gmail.com

# Descricao do site
description:  >- (define que nao deve ter quebra de linha no texto abaixo)
Esse e um blog de IA, onde serão postados artigos e tutoriais sobre Inteligência Artificial,
Aprendizado de Máquina e Ciência de Dados.

# Define o diretorio no qual o site sera servido
baseurl:  "/blog-IA"  # the subpath of your site, e.g. /blog

# Dominio padrao do Github Pages
url:  "gabrielbelo2007.github.io" 

# Informacao adicional para ser anexada ao site caso necessario
github_username:  gabrielbelo2007

# Processador de .md para HTML
markdown:  kramdown

# Syntax Higlight nos blocos de código

highlighter: rouge
kramdown:
  input: GFM 

# Listas de plugins do Jkelly
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

