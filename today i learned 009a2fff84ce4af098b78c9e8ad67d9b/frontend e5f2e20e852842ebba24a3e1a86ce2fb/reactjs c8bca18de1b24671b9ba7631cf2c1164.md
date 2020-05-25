# reactjs

- biblioteca javascript para criação de interfaces de usuário
- muito utilizado na construção de aplicações SPA ( single-page-applications )
- dentro de um componente react nós não devemos setar nossas próprias variáveis. Em vez disso, utilizamos o conceito de estado.

    ```jsx
    state = {
    		products: []
    }
    ```

- e para alterarmos o valor de um estado, utilizamos a função `setState( )`

    ```jsx
    this.setState({products: response.data.docs}); // setando a 'variável' (estado) com esse resultado
    ```

# react-router-dom

- nos permite trabalhar com as rotas da nossa aplicação