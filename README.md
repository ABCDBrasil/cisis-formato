A linguagem de formato CISIS é constituida de uma série de comandos e funcões que permitem a formatação do conteúdo dos campos de dados de bases de dados ISIS.

Esta linguagem serve para definir como os dados inseridos em uma base de dados serão exibidos na tela.

O ABCD utiliza a Linguagem de Formato mesclada com HTML, portanto é necessário um conhecimento básico prévio em HTML para criar formatos de dados.

## Uso básico

O uso mais comum da linguagem de formatação acontece quando um campo precisa ser exibido na tela, exemplo:

* Campo autor na base MARC

O campo autor é representado pela tag 100, no MARC. No ABCD a tag precisa vir acompanhada da letra **v** para ser identificada, ou seja:

    v100

Neste caso, todas as informações, preenchidas no campo 100 no MARC seriam exibidas. Isto inclui subcampos. Portanto para exibir apenas o subcampo do autor no campo 100, é preciso filtrar pelo subcampo **a**.
No ABCD isto acontece pelo identificador **^a**.

Para exibir o subcampo de autor do campo 100 do MARC utilizamos o formato:

    v100^a


## Uso com HTML

Para que a Linguagem de Formato CISIS funcione em um sistema WEB como o ABCD, é preciso mesclar com uma linguagem que possa ser interpretada por um navegador. 
O mais comum é o HTML, que é uma linguagem de marcação de texto.

Para usar a Linguagem de Formato com HTML é necessário colocar o HTML entre aspas simples **'<html></html>'** e a cada intervalo de inserção de campos cuidar para que o HTML esteja devidamente fechado entre suas aspas.

Exemplo:

```language
'<p><b>Autor:</b>' v100^a '</p>'
```

Isto vai exibir na tela:

> **Autor:**  Assis, Machado


## Uso no ABCD

A linguagem de formato é utilizada no ABCD para praticamente tudo, portanto é muito importante aprender o básico para dar mais liberdade na hora de gerenciar os recursos do sistema.

Você verá linguagem de formato em:

* Indexação de dados;
* Dicionário de termos;
* Relatórios;
* Estatísticas;
* Recibos;
* Conexão entre bases de dados;
* Conversão de dados.

Utilize a barra lateral a esquerda para navegar ou utilize a busca no campo superior para localizar os comandos.
