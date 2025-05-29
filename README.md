# Clone iFood React Native

## Descrição Breve
Um aplicativo em React Native que replica funcionalidades chave do iFood, desenvolvido para fins de estudo e portfólio.

## Tecnologias Utilizadas
*   React Native
*   React Navigation (para navegação)
*   JavaScript
*   Context API (para gerenciamento de estado global)
*   Styled-components
*   ESLint (para linting de código)
*   Prettier (para formatação de código)
*   React Native CLI

## Funcionalidades Implementadas/Esperadas
*   [x] Listagem de Restaurantes (tela principal)
*   [x] Funcionalidade de Busca (básica)
*   [x/o] Detalhes do Produto/Restaurante (estrutura da tela existe)
*   [ ] Autenticação de Usuário
*   [ ] Carrinho de Compras
*   [ ] Perfil do Usuário
*   [ ] Finalização de Pedido

## Como Instalar e Rodar o Projeto Localmente

```bash
# 1. Clone este repositório
git clone https://github.com/SFTBit/ # Substitua pela URL real do seu repositório
cd clone-ifood-react-native # Ou o nome da pasta do seu projeto

# 2. Instale as dependências
yarn install
# ou
npm install

# 3. Execute o projeto

# Para React Native CLI:
# Certifique-se de ter o ambiente de desenvolvimento React Native configurado
# Veja: https://reactnative.dev/docs/environment-setup

# Link de assets (fontes customizadas, etc.) - pode não ser necessário para todos os projetos
# react-native link 

# Iniciar o Metro Bundler (geralmente inicia automaticamente com os comandos abaixo)
# yarn start --reset-cache
# ou
# npm start -- --reset-cache

# Em outro terminal, execute para Android:
yarn android
# ou
npm run android

# Em outro terminal, execute para iOS (somente macOS):
yarn ios
# ou
npm run ios


# Para Expo:
# Certifique-se de ter o Expo CLI instalado: npm install -g expo-cli

# Iniciar o projeto
# yarn start
# ou
# npm start
# Em seguida, escaneie o QR code com o app Expo Go no seu dispositivo
# ou rode em um emulador/simulador (pressione 'a' para Android, 'i' para iOS no terminal).
```
**Observação:** Substitua `<URL_DO_SEU_REPOSITORIO_AQUI>` pela URL real do seu repositório quando ele estiver no GitHub.
Se você estiver usando React Native CLI, pode ser necessário configurar seu ambiente de desenvolvimento (Android Studio, Xcode) corretamente.

## Estrutura de Pastas Principal
```
clone-ifood-react-native/
├── src/
│   ├── assets/         # Imagens, fontes, etc.
│   ├── components/     # Componentes reutilizáveis
│   ├── contexts/       # Context API para gerenciamento de estado
│   ├── hooks/          # Hooks customizados
│   ├── navigation/     # Configuração de navegação (React Navigation)
│   ├── screens/        # Telas da aplicação
│   ├── services/       # Lógica de API, serviços externos
│   ├── utils/          # Funções utilitárias
│   └── config/         # Configurações (ex: Reactotron)
├── android/            # Arquivos específicos para Android
├── ios/                # Arquivos específicos para iOS
├── .github/            # Templates para Issues e PRs (opcional)
├── .gitignore
├── package.json
└── README.md
```

## Como Contribuir
Contribuições são bem-vindas! Sinta-se à vontade para abrir uma *issue* para discutir uma nova funcionalidade ou relatar um bug. Se desejar contribuir com código, por favor, crie um *fork* do projeto e envie um *pull request*.

## Licença
Distribuído sob a licença MIT. Veja `LICENSE` para mais informações.

## Capturas de Tela / GIFs
*(Adicione aqui capturas de tela ou GIFs do seu aplicativo em funcionamento)*
*(Exemplo:)*
*![Tela Principal](caminho/para/sua/imagem_tela_principal.png)*
