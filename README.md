# Contador React Simples

Um aplicativo de contador React simples que utiliza o hook `useState` para gerenciar o estado do contador. Fornece botões para incrementar e decrementar o valor.

## Instruções de Instalação

1. Clone o repositório:

    ```bash
    git clone https://github.com/Raphael015/aumentar-o-valor-de-uma-propriedade
    ```

2. Navegue até o diretório do projeto:

    ```bash
    cd seu-projeto
    ```

3. Instale as dependências:

    ```bash
    npm install
    ```

4. Execute o aplicativo:

    ```bash
    npm start
    ```

O aplicativo será iniciado em `http://localhost:3000/`.

## Exemplos de Uso

Este aplicativo é bastante simples. Ao iniciar, você verá a contagem atual e dois botões para incrementar e decrementar o valor.

```jsx
import React, { useState } from 'react';
import './App.css';
import obterMensagem from './api/mensagem';
import MeuComponente from './MeuComponente';

function App() {
  const mensagem = obterMensagem();
  const [count, setCount] = useState(0);

  const increment = () => {
    setCount(count + 1);
  };

  return (
    <div className="App">
      <header className="App-header">
        <MeuComponente mensagem={`Olá, Raphael!`} />
        <p>{mensagem}</p>
        <h1>Contador</h1>
        <p>Contagem: {count}</p>
        <button onClick={increment}>Aumentar Contador</button>
      </header>
    </div>
  );
}

export default App;
