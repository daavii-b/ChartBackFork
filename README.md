# ChartProjectB
Repositório dedicado para o projeto QuickChart | BackEnd


# copie essas linhas no seu settings.json
    "editor.codeActionsOnSave": {
        "source.fixAll.eslint": true
    }

# Configurações do ESLint
## Este projeto utiliza o ESLint para garantir a qualidade do código. As seguintes configurações foram aplicadas no arquivo .eslintrc.js:

module.exports = {
  env: {
    browser: true,
    es2021: true,
  },
  extends: 'airbnb-base',
  overrides: [
  ],
  parserOptions: {
    ecmaVersion: 'latest',
    sourceType: 'module',
  },
  rules: {
    'no-console': 'off',
    'class-methods-use-this': 'off',
    'import/first': 'off',
    'import/no-extraneous-dependencies': 'off',
    'import/prefer-default-export': 'off',
    'import/no-default-export': 'error',
    'import/order': [
      'error',
      {
        'newlines-between': 'always',
        pathGroups: [
          {
            pattern: 'react',
            group: 'builtin',
            position: 'before',
          },
          {
            pattern: 'components/**',
            group: 'external',
            position: 'after',
          },
          {
            pattern: 'templates/**',
            group: 'external',
            position: 'after',
          },
          {
            pattern: 'types/**',
            group: 'external',
            position: 'after',
          },
          {
            pattern: 'utils/**',
            group: 'external',
            position: 'after',
          },
        ],
        pathGroupsExcludedImportTypes: ['builtin'],
        groups: [
          'builtin',
          'external',
          'internal',
          'parent',
          'sibling',
          'index',
          'object',
        ],
        alphabetize: {
          order: 'asc',
        },
      },
    ],
  },
};

As configurações acima definem o ambiente de execução do código (browser: true e es2021: true), a extensão do ESLint (airbnb-base), as opções de parser (ecmaVersion: 'latest' e sourceType: 'module') e as regras de qualidade do código que serão verificadas. Algumas regras foram desabilitadas (no-console, class-methods-use-this, import/first, import/no-extraneous-dependencies, import/prefer-default-export) e outras foram habilitadas (import/no-default-export, import/order) com suas respectivas configurações específicas.
