# Default eslint, prettier and editorConfig to use in a RaeactJS project

# VScode extensions
  -> bracket pair colorizer
  -> color highlight
  -> docs-preview
  -> DotENV
  -> Dracula Offial
  -> EditorConfig for VS Code
  -> Eslint
  -> Material Icon Theme
  -> Prettier - Cide formatter
  -> Rocketseat React Native
  -> Rocketseat ReactJS
  -> SQLite
  -> vscode-styled-components

# VSCode settings
  -> ctrl+shift+p 
  ## settings.json

    {
      "breadcrumbs.enabled": true,

      "editor.fontFamily": "Fira Code",
      "editor.fontSize": 19,
      "editor.fontLigatures": true,
      "editor.lineHeight": 26,
      "editor.rulers": [80, 120],
      "editor.tabSize": 2,
      "editor.renderLineHighlight": "gutter",
      "editor.parameterHints.enabled": false,
      
      "explorer.confirmDelete": false,
      "explorer.confirmDragAndDrop": false,
      "explorer.compactFolders": false,
      
      "extensions.ignoreRecommendations": true,

      "emmet.syntaxProfiles": {
        "javascript": "jsx"
      },
      "emmet.includeLanguages": {
        "javascript": "javascriptreact"
      },

      "javascript.updateImportsOnFileMove.enabled": "never",
      "javascript.suggest.autoImports": false,
      
      "terminal.integrated.fontSize": 15,
      "terminal.integrated.fontFamily": "Fira Code",
      "typescript.updateImportsOnFileMove.enabled": "never",

      "workbench.iconTheme": "material-icon-theme",
      "workbench.colorTheme": "Dracula",
      "window.zoomLevel": 0,
      "workbench.startupEditor": "newUntitledFile",
      "workbench.editor.labelFormat": "short",

      "[javascript]": {
        "editor.codeActionsOnSave": {
          "source.fixAll.eslint": true,
        }
      },
      "[javascriptreact]": {
        "editor.codeActionsOnSave": {
          "source.fixAll.eslint": true,
        }
      },
      "[typescript]": {
        "editor.codeActionsOnSave": {
          "source.fixAll.eslint": true,
        }
      },
      "[typescriptreact]": {
        "editor.codeActionsOnSave": {
          "source.fixAll.eslint": true,
        },
        "editor.defaultFormatter": "esbenp.prettier-vscode"
      },
      "[jsonc]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
      },
      "workbench.sideBar.location": "left",

      "material-icon-theme.folders.associations": {
        "infra": "app",
        "entities": "class",
        "schemas": "class",
        "typeorm": "database",
        "repositories": "mappings",
        "http": "container",
        "migrations": "tools",
        "modules": "components",
        "implementations": "core",
        "dtos": "typescript",
        "fakes": "mock",
        "measures": ""
      },
      
      "material-icon-theme.files.associations": {
        "tsconfig.json": "tune",
        "ormconfig.json": "database"
      },
    }

# EditorConfig
  ## .editorconfig

    root = true
    [*]
    end_of_line = lf
    indent_style = space
    indent_size = 2
    charset = utf-8
    trim_trailing_whitespace = true
    insert_final_newline = true

# Eslint
  -> yarn add eslint -D
  -> yarn eslint --init
  -> yarn add eslint-plugin-react@^7.19.0 @typescript-eslint/eslint-plugin@latest eslint-config-airbnb@latest eslint@ eslint-plugin-import@^2.20.1 eslint-plugin-jsx-a11y@^6.2.3 eslint-plugin-react-hooks@^2.5.0 @typescript-eslint/parser@latesteslint -D
  -> yarn add prettier eslint-config-prettier eslint-plugin-prettier -D
  -> yarn add eslint-import-resolver-typescript -D  

  ## .eslintignore

    **/*.js
    node_modules
    build

  ## .eslintrc.json

    {
    "env": {
      "browser": true,
      "es6": true
    },
    "extends": [
      "plugin:react/recommended",
      "airbnb",
      "plugin:@typescript-eslint/recommended",
      "prettier/@typescript-eslint",
      "plugin:prettier/recommended"
    ],
    "globals": {
      "Atomics": "readonly",
      "SharedArrayBuffer": "readonly"
    },
    "parser": "@typescript-eslint/parser",
    "parserOptions": {
      "ecmaFeatures": {
        "jsx": true
      },
      "ecmaVersion": 2018,
      "sourceType": "module"
    },
    "plugins": ["react", "react-hooks", "@typescript-eslint", "prettier"],
    "rules": {
      "import/no-extraneous-dependencies": "off",
      "camelcase": "off",
      "prettier/prettier": "error",
      "@typescript-eslint/explicit-function-return-type": "off",
      "@typescript-eslint/explicit-module-boundary-types": "off",
      "react/jsx-props-no-spreading": "off",
      "react/prop-types": "off",
      "jsx-a11y/label-has-associated-control": "off",
      "@typescript-eslint/ban-types": "off",
      "no-unused-expressions": "off",
      "react-hooks/rules-of-hooks": "error",
      "react-hooks/exhaustive-deps": "warn",
      "react/jsx-filename-extension": [1, { "extensions": [".tsx"] }],
      "import/prefer-default-export": "off",
      "@typescript-eslint/naming-convention": [
        "error",
        {
          "selector": "interface",
          "format": ["PascalCase"],
          "custom": {
            "regex": "^I[A-Z]",
            "match": true
          }
        }
      ],
      "import/extensions": [
        "error",
        "ignorePackages",
        {
          "ts": "never",
          "tsx": "never"
        }
      ]
    },
    "settings": {
      "import/resolver": {
        "typescript": {}
      }
    }
  }

# Prettier
  ## prettier.config.js

    module.exports = {
      singleQuote: true,
      trailingComma: 'all',
      allowParens: 'avoid',
    };