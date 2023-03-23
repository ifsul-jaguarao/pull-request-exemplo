people.tchelinux.org.br
====================

Este repositório contém páginas com informações para contato dos membros do Tchelinux, similares a pagina https://people.tchelinux.org/tchelinux/.

## 10 passos para criar a sua página

1. Crie um fork deste este repositorio
    > Você pode fazer isso diretamente no github. Vá ao repositório do projeto e no lado direito vai aparecer um botão "Fork". Clique no botão e uma cópia do seu repositório será criada na sua conta.

2. Clone o repositório que você acabou de fazer para trabalhar localmente:

```
  $ git clone https://github.com/<username>/people.git
``` 

3. Crie um diretório com nome do seu usuário (usando apenas letras minúsculas), este será o nome que aparecerá na URL da sua página (ex. https://people.tchelinux.org/leonardovaz)

``` 
  $ mkdir people/<username>
``` 

4. Copie o arquivo `template.json` para o diretório criado no passo anterior

```
  $ cp template.json people/<username>/
```

5. Edite o arquivo `people/<username>/template.json`, insira seu nome e demais informações que quiser compartilhar. Uma lista contendo todos campos suportados pelo template [podem ser encontrados aqui](TEMPLATE.md).
    > Importante: os campos `User` e `Nome` são mandatórios para que a página possa ser propriamente criada. Sugerimos que pelo menos um meio de contato seja adicionado (website, email ou rede social). O campo `User` deve ter o mesmo valor de `<username> 

6. Instale o pacote `jq` (ou outra ferramenta para fazer a validação do arquivo JSON) e verifique se o mesmo não contém nenhum erro

```
  $ cat <username>/template.json |jq [.]
  [
    {
      "User": "tchelinux",
      "Nome": "Tchelinux",
      "Info": "Grupo de usuários de Software Livre do Sul do Brasil",
      "Cidade": "Porto Alegre",
      "Estado": "RS",
      "Foto": "https://avatars1.githubusercontent.com/u/8228496",
      "Email": "tchelinux-eventos@gmail.com",
      "Website": "https://tchelinux.org",
      "Github": "https://github.com/tchelinux",
      "Linkedin": "https://www.linkedin.com/groups/771307",
      "Twitter": "https://twitter.com/tchelinux",
      "Mastodon": "https://mastodon.social/@tchelinux",
      "Youtube": "https://youtube.com/tchelinux",
      "Instagram": "https://instagram.com/tchelinux",
      "Facebook": "https://facebook.com/tchelinux",
      "Messenger": "https://m.me/tchelinux",
      "Telegram": "https://t.me/tchelinux",
      "Whatsapp": "https://api.whatsapp.com/send?phone=5551912345678"
   }
 ]

```

7. Ao concluir as edições (e certificar que o arquivo `template.json` não contem erros!), adicione o novo diretório <username> ao seu repositório local

```
  $ git add people/<username>
```

8. Faça o commit localmente

``` 
  $ git commit -m "Adicionado página do <seu_nome_aqui> no people.tchelinux.org"
``` 

9. Envie as mudanças para seu repositório

``` 
  $ git push
``` 

10. Por fim, crie um pull-request para o repositório original para que possamos criar sua página.
