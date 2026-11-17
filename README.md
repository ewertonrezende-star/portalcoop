# Portal COOPSINTRA

Portal interno da **Cooperativa Agrícola de Sintra**, desenvolvido para centralizar o acesso às ferramentas de gestão e às áreas de trabalho das lojas.

O projeto é publicado como site estático através do **GitHub Pages**.

## Funcionalidades

- Autenticação de utilizadores através do Supabase.
- Área de gestão para utilizadores com permissões administrativas.
- Acesso à área de trabalho das lojas.
- Entrada nos módulos **Mapa Geral** e **Mapa Cereais e Rações**.
- Acesso à funcionalidade de geração de encomendas, conforme as permissões configuradas.
- Atalho **E-mail COOPSINTRA**, que abre o Roundcube numa nova aba.

> O atalho de e-mail encaminha para o webmail em [mail.coopsintra.pt](https://mail.coopsintra.pt). A autenticação automática (SSO) depende de suporte e configuração por parte do fornecedor do serviço de e-mail; o simples atalho não substitui o início de sessão do Roundcube.

## Tecnologias

| Tecnologia | Utilização |
| --- | --- |
| HTML5 | Estrutura da aplicação |
| CSS3 | Estilos e apresentação visual |
| JavaScript | Navegação e lógica do portal |
| Supabase JS v2 | Autenticação e integração com os serviços Supabase |
| GitHub Pages | Alojamento e publicação do portal |

A aplicação está atualmente concentrada no ficheiro `index.html`, incluindo os estilos e os scripts necessários. Esta organização evita introduzir um processo de compilação ou dependências locais que o projeto ainda não utiliza.

## Estrutura do repositório

```text
portalcoop/
├── index.html       # Aplicação principal do Portal COOPSINTRA
├── README.md        # Documentação do projeto
└── .gitignore       # Exclusões para ficheiros locais e temporários
```

## Aceder ao portal

- **Portal publicado:** https://ewertonrezende-star.github.io/portalcoop/
- **Repositório:** https://github.com/ewertonrezende-star/portalcoop
- **Webmail:** https://mail.coopsintra.pt/

## Publicação

O portal é servido pelo GitHub Pages a partir da branch `main`, na raiz do repositório.

Para publicar uma atualização:

1. Fazer as alterações necessárias no projeto.
2. Rever e testar o ficheiro `index.html`.
3. Guardar as alterações na branch `main`.
4. Aguardar a atualização do GitHub Pages.
5. Abrir o portal publicado e validar o acesso e as funcionalidades alteradas.

Não é necessário executar `npm install`, compilar ou gerar uma pasta `dist` para a estrutura atual.

## Configuração e segurança

- A autenticação é integrada com o projeto Supabase utilizado pelo portal.
- As permissões de acesso devem ser geridas no ambiente administrativo do Supabase e nas políticas de segurança correspondentes.
- Nunca colocar palavras-passe, chaves `service_role`, tokens privados ou outros segredos no HTML, JavaScript do navegador ou no repositório.
- Se for necessária uma chave pública `anon`/publishable no frontend, confirmar que as tabelas e operações estão protegidas por políticas **Row Level Security (RLS)**.
- Não transmitir credenciais de e-mail através de parâmetros de URL nem as expor no código do navegador.
- Alterações de autenticação, permissões ou integração com serviços externos devem ser testadas antes da publicação.

## Manutenção

Para preservar a estabilidade do portal:

- Fazer alterações pontuais e documentadas.
- Evitar reformulações visuais ou refatorações não solicitadas.
- Não alterar os fluxos de autenticação e os módulos de mapas ao adicionar novas funcionalidades.
- Validar os acessos de gestão e de loja após alterações relevantes.
- Manter cópias de segurança do código antes de mudanças estruturais.

## Estado do projeto

O repositório contém a aplicação atualmente publicada e a documentação de apoio. A documentação descreve a estrutura observada no código; não substitui a configuração efetiva dos serviços externos, do Supabase ou do alojamento.
