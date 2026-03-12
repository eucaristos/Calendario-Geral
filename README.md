# 📅 Calendário Eucaristós

Calendário oficial da Comunidade Católica Eucaristós, desenvolvido para organizar e visualizar os eventos comunitários e formativos ao longo do ano pastoral.

> **Este projeto foi desenvolvido com o auxílio de Inteligência Artificial (Perplexity AI), que colaborou na arquitetura, codificação e refinamento de todas as funcionalidades.**

---

## ✨ Funcionalidades

- 📆 **Visualização mensal e em lista** — alternância entre os modos Mês e Lista
- 🎨 **Dois tipos de eventos** — Calendário Geral e Calendário Formativo, cada um com sua cor
- 🔍 **Filtro por categoria** — botões para filtrar por tipo de evento
- 🖱️ **Clique no evento** — exibe popup central com nome e categoria do evento
- 📅 **Clique na data** — exibe popup com todos os eventos daquele dia
- 🌙☀️ **Modo escuro e claro** — alternância de tema com preferência salva no navegador
- 📱 **Totalmente responsivo** — layout adaptado para desktop e dispositivos móveis
- ⚠️ **Tela de erro** — mensagem amigável em caso de falha ao carregar os dados
- ⏳ **Tela de carregamento** — exibida enquanto os eventos são buscados
- 🔖 **Favicon** personalizado

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia                                  | Descrição                                    |
|---------------------------------------------|----------------------------------------------|
| HTML5 + CSS3                                | Estrutura e estilização                      |
| JavaScript (ES6+)                           | Lógica e interatividade                      |
| [FullCalendar v6](https://fullcalendar.io/) | Biblioteca de calendário                     |
| Google Sheets                               | Fonte de dados dos eventos (via CSV público) |
| Google Fonts                                | Fontes Cinzel, Lora e Inter                  |

---

## 📁 Estrutura de Arquivos

```
/
├── index.html          # Arquivo principal da aplicação
├── logo-header.webp    # Logo exibida no cabeçalho
├── favicon.png         # Ícone da aba do navegador
└── README.md           # Este arquivo
```


---

## 📊 Fonte de Dados

Os eventos são carregados automaticamente a partir de uma **planilha do Google Sheets** publicada como CSV.

### Formato esperado das colunas:

| Coluna | Campo          | Exemplo                                      |
|--------|----------------|----------------------------------------------|
| A      | Nome do evento | `Adoração Comunitária`                       |
| B      | Data de início | `15/06/2026`                                 |
| C      | Data de fim    | `15/06/2026`                                 |
| D      | Categoria      | `Calendário Geral` ou `Calendário Formativo` |
| E      | Setor          | `Núcleo Centro`                              |
| F      | Observações    | `Confirmar local`                            |

### Como atualizar a planilha:
1. Acesse a planilha no Google Sheets
2. Edite ou adicione eventos respeitando o formato acima
3. Certifique-se de que a planilha está publicada em **Arquivo → Compartilhar → Publicar na web → CSV**
4. O calendário atualiza automaticamente ao recarregar a página

---

## 🎨 Personalização

Todas as cores e variáveis visuais estão centralizadas no bloco `:root` do CSS, no início do `<style>`. Para alterar o visual, basta modificar os valores lá:

```css
:root {
  --color-accent:     #b45309;  /* Cor principal — dark mode */
  --color-comum:      #0891b2;  /* Cor dos eventos do Calendário Geral */
  --color-formativo:  #16a34a;  /* Cor dos eventos do Calendário Formativo */
  /* ... */
}

body.light {
  --color-accent: #0369a1;      /* Cor principal — light mode */
  /* ... */
}
```

