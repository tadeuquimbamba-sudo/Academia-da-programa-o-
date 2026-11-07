# Academia da Programação

Site catálogo de cursos de programação, só com front-end (HTML, CSS e JavaScript), sem servidor nem base de dados.
Cada botão **Matricular** abre o WhatsApp com a mensagem do curso e do preço já escrita.

## O que tem

- Mais de 70 linguagens de programação, cada uma com "Para que serve" e "Onde usar"
- Pesquisa e filtros por área (Web, Mobile, Dados, Sistemas, Educação e outras)
- Faixa de promoção e secção "Como te matriculas"
- Logótipos das linguagens (biblioteca aberta Devicon); quando não existe logótipo aparece um monograma

## Estrutura

```
index.html   o site completo (estilos e scripts incluídos)
README.md    este ficheiro
netlify.toml configuração para publicar no Netlify
.gitignore
```

## Como publicar

**GitHub Pages**
1. Cria um repositório no GitHub e envia estes ficheiros.
2. Vai a *Settings > Pages*, escolhe *Deploy from a branch*, branch `main` e pasta `/ (root)`.
3. O site fica disponível no endereço que o GitHub indicar.

**Netlify**
1. Em *Add new site > Import an existing project*, liga o repositório.
2. Deixa o comando de build vazio e a pasta de publicação como `.`.

Também podes arrastar a pasta para o Netlify Drop.

## Como alterar

Tudo está no fim do `index.html`, na secção `<script>`:

- **Número do WhatsApp:** variável `N` (formato internacional, sem + nem espaços, por exemplo `244928379657`). Os links fixos do cabeçalho e do rodapé usam o mesmo número em `https://wa.me/...`.
- **Preço:** variável `P`. A faixa de promoção está no HTML, na secção com `id="precos"`.
- **Linguagens:** a lista `D` tem uma linha por linguagem, no formato
  `Nome|logo|Área|Para que serve|Onde usar`
  O campo `logo` é o nome da pasta em https://devicon.dev (deixa vazio para mostrar o monograma).

## Notas

- Os logótipos e as fontes precisam de ligação à internet.
- Os logótipos pertencem aos respectivos titulares.
