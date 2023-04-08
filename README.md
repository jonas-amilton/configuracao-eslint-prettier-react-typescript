# **Como configurar Eslint e Prettier em um Projeto ReactJS TypeScript**

• Vamos criar o nosso projeto ReactJS

`npx create-react-app my-app --template typescript`

• Acesse a pasta do projeto e vamos instalar o Eslint

`npm init @eslint/config`

• Ao instalar o Eslint precisamos escolher as configurações desejadas, abaixo segue as escolhas para este tutorial

```
❯ To check syntax, find problems, and enforce code style

❯ JavaScript modules (import/export)

❯ React

? Does your project use TypeScript? › No / Yes (Yes)

✔ Browser

❯ Answer questions about your style

❯ JSON

❯ Spaces

❯ Single

❯ Unix

? Do you require semicolons? › No / Yes (Yes)

? Would you like to install them now? › No / Yes (Yes)

❯ npm
```

• Agora vamos instalar o Prettier

`npm install --save-dev --save-exact prettier`

• Precisamos criar um arquivo com nome ***.prettierrc*** na raiz do projeto e colocar a configuração abaixo

```
{
	"printWidth": 120,
	"singleQuote": true,
	"tabWidth": 2,
	"useTabs": false,
	"trailingComma": "none",
	"arrowParens": "avoid"
}
```

• Depois precisamos incluir a configuração do Prettier para Eslint

`npm install --save-dev eslint-config-prettier`

• Na configuração do Eslint que fica na pasta raiz do projeto com nome ***.eslintrc.json*** coloque a extensão do Prettier

```
{
  "extends": [
    "some-other-config-you-use",
    "prettier"
  ]
}
```

Tudo pronto agora seu projeto está configurado. 😎👍
