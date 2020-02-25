# DesafioWebServiceAutomation
Projeto com Postman realizando funções de teste na API disponibilizado pela **Inmetrics**.

# Índice

- Pré-requisito
- Instalação e Execução do Projeto
- Query
- Suporte
- License

# Pré Requisitos

- Postman install

# Execução do Projeto

1. Faça o download do zip ou clone do repositório Git
2. Descompacte o arquivo zip (se você tiver baixado um)
3. Abra o Postman
4. File ->> Import ->> Import File ->> Navegue até a pasta em que você descompactou o zip
5. Você ira executar o teste na aba "Tests" no Postman
6. Clicar no botão "Send"
7. Visualizar o resultado da query pelo "Test Results 2/2" ou pelo Console
8. View ->> Show Postman Console ou Alt + Ctrl + C

# Autorização

```
GET http://swapi.co/api/films
```

# Query

- Arquivo de exemplo para realizar a pesquisa no Json

```
// Método que retorna o código 200
pm.test ("O código de status é 200", function () {
    pm.response.to.have.status (200);
});

// Método que realiza a busca pelos títulos que tenham George Lucas e Rick McCallum.
pm.test("O resultado dos filmes está ok!", function () {
    var jsonData = pm.response.json();
    var list = [];
    jsonData.results.forEach(function(element) {
         if (element.director == "George Lucas" && element.producer.indexOf("Rick McCallum") != -1) {

             list.push(element.title);
         }
    });
    console.log(list);
});
```

## Status Código

Código de status da API:

| Status Código | Descrição |
| :--- | :--- |
| 200 | `OK` |
    
# Suporte
## E-mail: massayoshi.campos@gmail.com
## Linkedin: https://www.linkedin.com/in/massayoshi-campos/
> Se você tiver alguma dúvida sobre este repositório ou precisar de ajuda para contribuir, não hesite em entrar em contato comigo.

## Contribuições
> Se você tem algum exemplo de código que gostaria de contribuir para este repositório, sinta-se à vontade para abrir uma solicitação de recebimento.

## Comentário
> Os colaboradores deste repositório ficarão muito gratos por receber feedback! Se você deseja elogiar ou comentar algum exemplo de teste ou o repositório como um todo, faça-o pelo e-mail. Eu adoraria ouvir o que você pensa, então, reserve um momento para me informar.

# License
- Copyright 2020 ©Massayoshi Campos
