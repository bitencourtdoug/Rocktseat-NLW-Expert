# React  Expert

<aside>
💡 Feito com 💜 pela Rocketseat

</aside>

Diferente de outros aplicativos de notas, na trilha React do NLW Expert estamos criando uma aplicação em que você pode gravar uma nota usando áudio que será convertido em texto automaticamente. 

Isso é feito usando a interface da própria web, sem necessidade de contas externas, utilizando a [Speech Recognition API](https://developer.mozilla.org/en-US/docs/Web/API/SpeechRecognition), disponível nos navegadores modernos.

![Home.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/08f749ff-d06d-49a8-a488-9846e081b224/b41f2ad6-01c2-4dae-b6cd-92b6f1db1b25/Home.png)

Além disso, vamos criar um aplicativo responsivo, aprendendo sobre estilização e responsividade. Vamos abordar também a acessibilidade da aplicação e a criação de modais usando uma biblioteca específica.

No FIGMA do projeto, você encontrará todos os recursos necessários já organizados, entre eles: estados da aplicação, layouts para diferentes modo de gravação e visualização de notas, informações sobre tipografia, cores,, pacote de ícones e layouts detalhados da aplicação.

<aside>
📌 Para começar a desenvolver, é importante criar um projeto em um local adequado no seu computador. Evite pastas sincronizadas com sistemas de nuvem, pois isso pode causar problemas.

</aside>

### Node.js

É necessário ter o Node.js instalado, preferencialmente na versão LTS. Versões acima de 18 funcionam, mas a LTS é mais estável. Para verificar sua versão do Node.js, use o comando `node -v` no terminal. Nas aulas do NLW Expert, estamos usando a versão 20.1, que é a LTS atual.

Para instalar o Node.js, siga as instruções específicas para seu sistema operacional disponíveis no site oficial: https://nodejs.org/en.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/08f749ff-d06d-49a8-a488-9846e081b224/483d134c-9e5a-46dc-b557-4f65477a622c/Untitled.png)

Uma vez com o Node.js instalado, podemos começar a criar nossa aplicação.

### Vite

Para iniciar o desenvolvimento do projeto, utilizamos o comando **`npm create vite@latest`**, uma instrução específica para criar um novo projeto com o Vite, uma ferramenta de construção moderna que oferece uma experiência de desenvolvimento mais rápida e eficiente em comparação com configurações tradicionais baseadas em webpack. 

```css
npm create vite@latest
```

Após executar o comando **`npm create vite@latest`**, o assistente de criação do Vite pergunta qual framework você deseja utilizar (React, Vue, Svelte, etc.) e configurações adicionais, como o nome do projeto. 

Vamos escolher React e mão na massa 🚀

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/08f749ff-d06d-49a8-a488-9846e081b224/f5144ceb-effb-4dfe-9ca2-05f81dfc40f8/Untitled.png)

### Tailwind

No coração da nossa aplicação React, temos alguns elementos-chave para examinar. Primeiro, o arquivo `index.html`, que serve como ponto de entrada da nossa aplicação, contém apenas uma div com um ID específico e um script para importar o React.

O arquivo `index.js` é crucial pois ele localiza essa div e injeta nossa aplicação React nela através do método de renderização. 

Este método é fundamental em aplicações React, pois é responsável por exibir os componentes na tela. Utilizamos o React DOM para este propósito, que, apesar de não ser um elemento visual, ajuda a prevenir erros comuns.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/08f749ff-d06d-49a8-a488-9846e081b224/e933625c-c38a-4dff-8172-bb40e1b917bf/Untitled.png)

### Componentes

Componentes são, basicamente, funções com a primeira letra maiúscula que retornam JSX, uma sintaxe que permite escrever HTML dentro do JavaScript. Porém, é importante notar que o JSX não é HTML puro; é uma representação que, eventualmente, é convertida em JavaScript. Este processo facilita a criação de interfaces de usuário de forma declarativa e compreensível.

Dentro da nossa aplicação, vamos introduzir o Tailwind CSS, que nos traz vantagens significativas. Tailwind introduz o conceito de **utility-first**, permitindo a criação de interfaces com uma consistência estilística sem precedentes. 

Isso é alcançado através de um sistema de classes que aplicam estilos diretamente no HTML, embora possam ser extraídas para arquivos separados para manter a organização.

O uso do Tailwind promove a adesão a um sistema de design consistente, limitando a escolha de valores arbitrários para propriedades de estilo. Isso significa que, em vez de usar tamanhos de fonte, cores, ou espaçamentos aleatórios, você é incentivado a utilizar os valores definidos pelo sistema de design do Tailwind. Essa abordagem reduz a inconsistência no design e facilita a manutenção da aplicação a longo prazo.

Para integrar o Tailwind na nossa aplicação React, vamos seguir alguns passos específicos, incluindo a instalação via NPM e a configuração inicial. 

Este processo envolve a criação de arquivos de configuração do Tailwind e a especificação de quais arquivos do projeto utilizarão as classes do Tailwind. Isso é feito modificando o arquivo `tailwind.config.js` para incluir os caminhos dos arquivos relevantes.

Vamos instalar o tailwind:

```jsx
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

Após rodar o código acima, você vai perceber que foram criados 2 arquivos o `tailwind.config.js` e o `postcss.config.js`

Modificando o arquivo `tailwind.config.js`:

Originalmente seu arquivo estará assim: 

```jsx
/** @type {import('tailwindcss').Config} */
export default {
  content: [
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

Você precisa deixar como o código abaixo para incluir os caminhos de arquivos relevantes:

```jsx
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

E no arquivo `index.css`, dentro da pasta `src`, você vai precisar colocar essas três linhas:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Agora você vai perceber como essa biblioteca pode transformar a experiência de desenvolvimento de interfaces, oferecendo um controle preciso sobre o design ao mesmo tempo em que mantém o código limpo e organizado. 

Depois da leitura desse material você está ainda mais preparado(a) para continuar sua jornada no NLW Expert.

A aula prática #03 será liberada dia 07 de fevereiro, às 18h. 

Nós te vemos lá! 

#NeverStopLearning 🚀