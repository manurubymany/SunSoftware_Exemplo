# SunSoftware_Exemplo
Site de comunicação informações internas TI
# ☀️ Portal Interno TI — SUN SOFTWARES

Este projeto é um protótipo de **Front-end Single Page Application (SPA)** desenvolvido em um único arquivo HTML. Ele simula um portal corporativo de TI para gerenciamento de ERP, relatórios, chamados e usuários, demonstrando interfaces modernas e interativas sem a necessidade de um backend real.

## 🚀 Visão Geral

O sistema simula um ambiente intranet onde colaboradores podem:
- Acompanhar notícias do sistema (estilo jornal).
- Gerenciar versões e logs de atualização do ERP.
- Monitorar o status do banco de dados (gráficos de carga e CPU).
- Abrir e consultar chamados de suporte (Helpdesk).
- Gerenciar usuários (CRUD simulado).

## ✨ Funcionalidades Principais

*   **Autenticação Simulada:** Tela de login com validação de credenciais e modal de boas-vindas.
*   **Tema Dinâmico:** Alternância entre **Modo Escuro** (padrão) e **Modo Claro**, com persistência via `localStorage`.
*   **Dashboard "Jornal":** Layout estilo *newspaper* para exibir as últimas notícias e atualizações do sistema.
*   **Visualização de Dados:**
    *   Gráficos de Barras (Carga do Servidor, Chamados por Categoria) feitos puramente com CSS/HTML.
    *   Gráfico de Pizza (Donut Chart) interativo feito com SVG dinâmico.
*   **Gestão de Chamados:** Tabela com filtros em tempo real (pesquisa, tipo, status) e paginação visual.
*   **Relatórios de Versão:** Funcionalidade de gerar um relatório de impressão (PDF) nativo do navegador para builds de versão.
*   **Gestão de Usuários:** Interface para cadastrar, editar e ativar/desativar usuários.

## 🛠️ Tecnologias Utilizadas

O projeto foi construído sem frameworks ou bibliotecas externas (Vanilla), garantindo alta performance e portabilidade.

*   **HTML5:** Estrutura semântica.
*   **CSS3:**
    *   Variáveis CSS (Custom Properties) para temas.
    *   Flexbox e CSS Grid para layouts responsivos.
    *   Animações (`keyframes`) para transições suaves.
*   **JavaScript (ES6+):**
    *   Manipulação do DOM.
    *   Lógica de "Roteamento" simples (troca de abas/telas).
    *   Banco de dados simulado em memória (`const DB`).

## 🔑 Credenciais de Acesso

Como o sistema não possui backend, utilize os usuários fictícios abaixo para testar:

| Nível | Login | Senha | Permissões |
| :--- | :--- | :--- | :--- |
| **Administrador** | `admin` | `admin123` | Acesso total (inclui gestão de usuários). |
| **Visitante** | `visitante` | `1234` | Acesso visualização (sem permissão para editar usuários). |

## 📦 Como Executar

1.  Baixe o arquivo `Portal de noticias TI.html`.
2.  Abra o arquivo diretamente em qualquer navegador moderno (Chrome, Edge, Firefox, Safari).
    *   *Não é necessário instalar Node.js ou servidores web.*
3.  Utilize as credenciais acima para entrar.

## 📂 Estrutura do Código

Todo o código reside em um único arquivo para facilidade de transporte e teste:

*   **CSS (`<style>`):** Contém todo o design system, reset, componentes (cards, tabelas, botões) e temas de cores.
*   **HTML (`<body>`):** Estrutura dos modais, tela de login e o container principal da aplicação (`#app`).
*   **JavaScript (`<script>`):**
    *   `DB`: Objeto JSON que simula o banco de dados.
    *   `r[NomeDaFuncao]`: Funções de renderização (ex: `rChamados`, `rHomeProd`).
    *   Lógica de Login, Filtros e Interatividade.

## 🎨 Personalização

Para alterar as cores do tema, procure no início do bloco `<style>` as variáveis `:root` e `[data-theme="dark"]`:

```css
:root {
  --bug: #F04040; /* Cor para erros/bugs */
  --mel: #2ECC71; /* Cor para melhorias */
  --p: #6A0DAD;   /* Cor primária (Roxo) */
  /* ... */
}
