## 🙋‍♂️ Autor

<div align="center">
  <img src="https://avatars.githubusercontent.com/ninomiquelino" width="100" height="100" style="border-radius: 50%">
  <br>
  <strong>Onivaldo Miquelino</strong>
  <br>
  <a href="https://github.com/ninomiquelino">@ninomiquelino</a>
</div>

---

# 🔍 Vanilla Search Select

![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E.svg?style=for-the-badge&logo=javascript&logoColor=black)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-CSS-38B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Responsive](https://img.shields.io/badge/Design-Responsive-FF6B6B.svg?style=for-the-badge)
![Zero Dependencies](https://img.shields.io/badge/Dependencies-Zero-27AE60.svg?style=for-the-badge)
![License MIT](https://img.shields.io/badge/License-MIT-green)
![Status Stable](https://img.shields.io/badge/Status-Stable-success)
![Version 1.0.0](https://img.shields.io/badge/Version-1.0.0-blue)
![GitHub stars](https://img.shields.io/github/stars/NinoMiquelino/vanilla-search-select?style=social)
![GitHub forks](https://img.shields.io/github/forks/NinoMiquelino/vanilla-search-select?style=social)
![GitHub issues](https://img.shields.io/github/issues/NinoMiquelino/vanilla-search-select)

Um componente de busca e seleção moderno e totalmente funcional, construído com JavaScript vanilla e estilizado com Tailwind CSS. Perfeito para projetos que precisam de uma solução leve e customizável sem dependências externas.

## ✨ Funcionalidades Comprovadas

### 🎯 **Funcionalidades Principais**
- **✅ Busca em Tempo Real** - Filtragem instantânea de opções
- **✅ Seleção Múltipla e Única** - Dois modos de operação
- **✅ Interface Responsiva** - Funciona em mobile e desktop
- **✅ Design Moderno** - Estilizado com Tailwind CSS
- **✅ Fácil Integração** - Simples de implementar

### 🎨 **Recursos de UI/UX**
- **Dropdown Animado** - Transições suaves de abertura/fechamento
- **Placeholders Dinâmicos** - Texto contextual
- **Estados Visuais** - Hover, focus e estados selecionados
- **Ícones Integrados** - Ícones de busca e dropdown
- **Feedback Visual** - Display claro dos itens selecionados

### ⚡ **Performance**
- **Zero Dependencies** - Apenas JavaScript vanilla
- **CSS Leve** - Tailwind CSS via CDN
- **Carregamento Rápido** - Sem build necessário
- **Fácil Manutenção** - Código limpo e organizado

## 🚀 Demonstração Imediata

### Como testar:
1. **Salve o código** como `index.html`
2. **Abra no navegador** - funciona instantaneamente
3. **Interaja com os componentes**:
   - Clique para abrir os dropdowns
   - Digite para buscar
   - Selecione múltiplos itens
   - Use os botões "Exemplo" e "Limpar"

### Exemplos Incluídos:
- **Países** - Seleção única com busca e emojis
- **Cidades** - Seleção única sem busca
- **Tecnologias** - Seleção múltipla ilimitada  
- **Categorias** - Seleção múltipla com limite (max 3)

## 🛠️ Implementação Rápida

### Método 1: Copiar e Colar (Recomendado)
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meu Projeto</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-50 p-4">
    <div id="meuSelect"></div>

    <script>
        // Cole a classe SearchSelect aqui
        class SearchSelect {
            // ... código da classe completo
        }

        // Inicialize o componente
        const meuSelect = new SearchSelect({
            container: '#meuSelect',
            options: [
                { value: '1', label: 'Opção 1' },
                { value: '2', label: 'Opção 2' },
                { value: '3', label: 'Opção 3' }
            ],
            placeholder: 'Selecione uma opção...',
            searchable: true,
            multiple: false,
            onSelect: (selected) => {
                console.log('Selecionado:', selected);
            }
        });
    </script>
</body>
</html>
```

Método 2: Arquivo Separado

```javascript
// search-select.js
class SearchSelect {
    // ... código da classe
}

// Inicialização
const select = new SearchSelect({
    container: '#container',
    options: [/* suas opções */],
    // ... configurações
});
```

⚙️ Configuração Simplificada

Opções Básicas:

```javascript
const config = {
    container: '#elemento',      // Onde renderizar (obrigatório)
    options: [                   // Lista de opções (obrigatório)
        { value: 'br', label: 'Brasil', emoji: '🇧🇷' },
        { value: 'us', label: 'EUA', emoji: '🇺🇸' }
    ],
    placeholder: 'Selecione...', // Texto padrão
    searchable: true,           // Habilitar busca
    multiple: false,            // Seleção múltipla
    maxSelections: null,        // Limite para múltipla seleção
    onSelect: (selected) => {   // Callback quando seleciona
        console.log(selected);
    }
};
```

Métodos Disponíveis:

```javascript
const select = new SearchSelect(config);

// Obter itens selecionados
const selecionados = select.getSelected();

// Definir seleção programaticamente  
select.setSelected(['valor1', 'valor2']);

// Limpar seleção
select.clear();
```

🎨 Personalização

Cores e Estilos:

O componente usa classes Tailwind CSS que podem ser facilmente customizadas:

```html
<!-- No trigger -->
<div class="search-select-trigger 
    border-2 border-blue-500    <!-- Cor da borda -->
    bg-white                    <!-- Cor de fundo -->
    rounded-xl                  <!-- Bordas arredondadas -->
    ...">

<!-- Nas opções -->
<div class="option-item 
    hover:bg-blue-50           <!-- Cor no hover -->
    ...">
```

Modo Escuro:

Funciona automaticamente com as classes dark do Tailwind:

```html
<body class="dark:bg-gray-900">
    <!-- O componente se adapta automaticamente -->
</body>
```

📱 Responsividade

Comportamento por Dispositivo:

· Mobile: Dropdown em tela cheia, toque otimizado
· Tablet: Layout adaptativo
· Desktop: Experiência completa com animações

Touch-Friendly:

· Áreas de toque grandes (mínimo 44px)
· Scroll suave em dispositivos móveis
· Feedback visual para interações touch

🔧 Uso em Produção

Pronto para Produção:

· ✅ Testado e Funcional
· ✅ Código Limpo
· ✅ Sem Dependências
· ✅ Performance Otimizada
· ✅ Fácil Manutenção

Exemplo de Implementação Real:

```javascript
// Em um formulário de cadastro
const countrySelect = new SearchSelect({
    container: '#countryField',
    options: countriesList,
    placeholder: 'Selecione seu país...',
    searchable: true,
    multiple: false,
    onSelect: (selected) => {
        document.getElementById('country').value = selected[0]?.value || '';
    }
});
```

🐛 Solução de Problemas

Problemas Comuns:

O componente não aparece:

· Verifique se o container existe no DOM
· Confirme se o JavaScript está carregado
· Verifique o console por erros

A busca não funciona:

· Certifique-se que searchable: true
· Verifique se há opções para filtrar

Seleção múltipla não funciona:

· Configure multiple: true

Debug:

```javascript
// Adicione para debug
const select = new SearchSelect(config);
console.log('Select inicializado:', select);
```

📦 Estrutura do Projeto

```
vanilla-search-select/
│
├── index.html          # Arquivo principal com demonstração
├── README.md           # Este arquivo
└── examples/           # (Opcional) Exemplos adicionais
    ├── basic.html      # Uso básico
    ├── advanced.html   # Recursos avançados
    └── custom.html     # Customização
```

---

<div align="center">
Desenvolvido com ❤️ usando JavaScript vanilla e Tailwind CSS.
</div>

---

## 🤝 Contribuições
Contribuições são sempre bem-vindas!  
Sinta-se à vontade para abrir uma [*issue*](https://github.com/NinoMiquelino/vanilla-search-select/issues) com sugestões ou enviar um [*pull request*](https://github.com/NinoMiquelino/vanilla-search-select/pulls) com melhorias.

---

## 💬 Contato
📧 [Entre em contato pelo LinkedIn](https://www.linkedin.com/in/onivaldomiquelino/)  
💻 Desenvolvido por **Onivaldo Miquelino**

---
