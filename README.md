# desafio-nodejs

<img src="https://d2eip9sf3oo6c2.cloudfront.net/tags/images/000/000/256/full/nodejslogo.png" title="NodeJS" alt="NodeJS" width="100" align="center">


# Desafio: Conceitos do Node.js

> Começando no Bootcamp do excelente Gostack 11 disponibilizado pela Instituição de Ensino Rocketseat

- O objetivo do desafio era criar um servidor que fosse capaz de listar os repositorios, receber novos repositorios, deletar ou atualizar e receber likes de acordo com a chamada url. Utilizei a ferramenta <a href="https://insomnia.rest/"> Imsomnia</a> para poder testar cada chamada HTTP e seus métodos


## Exemplo de um dos métodos que aprendemos e praticamos

```javascript
// code away!

app.put("/repositories/:id", (request, response) => {
  const { id } = request.params;
  const { title, url, techs } = request.body;


  const repositoryIndex = repositories.findIndex(repository => repository.id === id)

  if(repositoryIndex < 0) {
    return response.status(400).json({error: "Repository not found"})
  }

  const repository = {
    id,
    title,
    url,
    techs,
    likes: 0
  }

  repositories[repositoryIndex] = repository;

  return response.json(repository);
});
```

---

## Instalação

- Possua o Node mais atual é o ideal para o servidor funcionar de forma eficaz

### Clone

- Clone esse repositório na sua maquina utilizando `https://github.com/luizcdribeiro/desafio-nodejs.git`

### Configuração

> Verifique se possui o `yarn` e o `node` instalados e atualizados na sua máquina

```shell
$ yarn -v
$ node -v
```

> Execute o comando abaixo e inicie o node para a aplicação iniciar

```shell
$ yarn
$ yarn dev //inicia o nodemon
```
> Execute o comando abaixo para realizar os testes da aplicação

```shell
$ yarn test
```

## Contato

<a href="https://twitter.com/luizjuniordant1">
  <img align="left" alt="Ajay's Twitter" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/twitter.svg" />
</a>
<a href="https://www.linkedin.com/in/luiz-carlos-dantas-ribeiro-junior-7422b9124/">
  <img align="left" alt="Ajay's Linkdein" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/linkedin.svg" />
</a>
<a href="https://github.com/luizcdribeiro">
  <img align="left" alt="Ajay's Github" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/github.svg" />
</a>
