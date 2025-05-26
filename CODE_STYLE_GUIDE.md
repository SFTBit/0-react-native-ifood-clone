# Guia de Estilo e Boas Práticas de Código

Este documento fornece um conjunto de diretrizes e boas práticas para manter o código do projeto limpo, consistente e fácil de entender.

## 1. Convenções de Nomenclatura

*   **Componentes React (Arquivos e Nomes):** Use PascalCase.
    *   Exemplo de arquivo: `src/components/MeuComponente/index.js` (ou `MeuComponente.js`)
    *   Exemplo de nome de componente: `function MeuComponente() { ... }`
*   **Arquivos e Pastas (não componentes):** Use kebab-case para nomes de arquivos e pastas, especialmente para utilitários, serviços, etc. Para componentes, a pasta pode ser PascalCase se contiver um `index.js` que exporta o componente com o mesmo nome.
    *   Exemplo: `src/utils/calculate-price.js`
    *   Exemplo: `src/components/UserProfile/`
*   **Variáveis e Funções:** Use camelCase.
    *   Exemplo: `const itemCount = 10;`
    *   Exemplo: `function getUserProfile() { ... }`
*   **Constantes Globais ou de Módulo:** Use SCREAMING_SNAKE_CASE.
    *   Exemplo: `const API_URL = 'https://api.example.com';`
*   **Estilos (Styled Components):** Use PascalCase para componentes estilizados.
    *   Exemplo: `const Container = styled.View\`...\`;`

## 2. Organização de Imports

Mantenha os imports organizados e consistentes. Uma boa prática é agrupá-los e ordená-los da seguinte forma:

1.  Imports de bibliotecas padrão do React / React Native.
2.  Imports de bibliotecas de terceiros (ex: `react-navigation`, `axios`).
3.  Imports de componentes da aplicação (usando aliases como `~/components/`).
4.  Imports de utilitários, serviços, hooks, contextos da aplicação.
5.  Imports relativos (`./` ou `../`) para arquivos no mesmo módulo ou vizinhos.
6.  Imports de arquivos de estilo (se separados).

**Exemplo:**

```javascript
import React, { useState, useEffect } from 'react';
import { View, Text, StyleSheet, TouchableOpacity } from 'react-native';

import { useNavigation } from '@react-navigation/native';
import PropTypes from 'prop-types';
import Icon from 'react-native-vector-icons/MaterialIcons';

import Button from '~/components/Common/Button';
import Section from '~/components/Common/Section';
import { useCart } from '~/contexts/CartContext';
import api from '~/services/api';
import { formatPrice } from '~/utils/formatters';

import styles from './styles'; // Se você tiver um arquivo de estilos separado
```

Tente manter os imports de cada grupo ordenados alfabeticamente.

## 3. Linting e Formatação

*   **ESLint:** Este projeto já está configurado com ESLint (`.eslintrc.json`). Ele ajuda a identificar e corrigir problemas de estilo de código e potenciais erros automaticamente.
    *   Execute `yarn lint` ou `npm run lint` para verificar o código.
    *   Integre o ESLint ao seu editor de código para feedback em tempo real.
*   **Prettier:** Este projeto também possui configuração para o Prettier (`.prettierrc.js`). Prettier formata automaticamente o código para garantir um estilo consistente.
    *   Configure seu editor para formatar ao salvar usando Prettier.
    *   Você pode adicionar um script no `package.json` para formatar todos os arquivos, por exemplo: `"format": "prettier --write "src/**/*.js""`

## 4. Componentes

*   **Pequenos e Reutilizáveis:** Crie componentes pequenos e focados em uma única responsabilidade. Isso os torna mais fáceis de entender, testar e reutilizar.
*   **PropTypes (ou TypeScript):** Use `PropTypes` (como já está parcialmente no projeto) ou TypeScript para definir os tipos das props dos seus componentes. Isso ajuda a prevenir bugs e melhora a documentação.
*   **Estado e Lógica:** Separe a lógica de apresentação da lógica de negócio sempre que possível. Hooks customizados e Context API (ou Redux) podem ajudar nisso.

## 5. JavaScript Moderno (ES6+)

Utilize os recursos modernos do JavaScript para um código mais limpo e eficiente:

*   `const` e `let` em vez de `var`.
*   Arrow functions.
*   Destructuring.
*   Spread e Rest operators.
*   Template literals.
*   Async/await para operações assíncronas.

## 6. Comentários

*   Comente partes complexas do código ou lógica de negócio que não seja óbvia.
*   Evite comentários desnecessários que apenas repetem o que o código já diz.
*   Use `// TODO:` para marcar lugares onde trabalho futuro é necessário.

## 7. Gerenciamento de Estado

*   Para estados simples e locais, use o hook `useState`.
*   Para estados mais complexos ou compartilhados entre muitos componentes, considere a Context API (já existe a pasta `src/contexts`) ou uma biblioteca de gerenciamento de estado como Redux ou Zustand.

Ao seguir estas diretrizes, você contribuirá para um código base mais saudável e colaborativo!
