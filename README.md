# FinDash
Finance Control Pro - Dashboard de Análise Financeira

📜 Descrição

O Finance Control Pro é um dashboard de front-end completo, projetado para visualização e análise de dados financeiros. Construído inteiramente com HTML, CSS e JavaScript, este projeto simula um ambiente de Business Intelligence (BI) interativo, sem a necessidade de um back-end. A aplicação é totalmente autocontida em um único arquivo HTML, demonstrando o poder das tecnologias web modernas para criar aplicações ricas e funcionais.

Nota: A aplicação utiliza localStorage e sessionStorage para simular a autenticação e persistência de dados, sendo ideal para demonstrações e portfólio.

✨ Funcionalidades Principais

O dashboard é dividido em várias seções, cada uma com funcionalidades específicas:

1. Autenticação de Usuário

Tela de Login e Cadastro: Sistema simulado de criação de conta e login.

Persistência de Sessão: Utiliza sessionStorage para manter o usuário logado durante a sessão.

Armazenamento Local: As informações de usuário são salvas no localStorage do navegador.

2. Dashboard Principal

KPIs (Key Performance Indicators): Cards de resumo que exibem métricas importantes, como orçamento total, departamento com maior crescimento e média de orçamento, com indicadores de performance em relação ao ano anterior.

Gráfico Interativo: Um gráfico dinâmico (criado com Chart.js) que permite a visualização dos dados em múltiplos formatos:

Barras

Linhas

Radar

Pizza

Filtro Global por Ano: Um seletor global que atualiza todos os dados do dashboard (KPIs, gráfico e relatórios) para o ano selecionado.

3. Simulador de Investimentos

Cálculo de ROI: Uma aba dedicada onde o usuário pode inserir um valor e selecionar um departamento para simular o retorno de investimento (ROI) projetado com base em taxas pré-definidas.

4. Relatórios

Tabela Detalhada: Apresenta os dados brutos em um formato de tabela, mostrando o orçamento do ano atual, do ano anterior e a variação percentual para cada departamento, com destaques de cor para crescimento (verde) e queda (vermelho).

5. Perfil do Usuário

Gerenciamento de Conta: Uma seção para visualizar os dados do perfil, como nome, email, data de criação da conta e último login.

Troca de Tema: Funcionalidade para alternar entre tema claro (Light Mode) e escuro (Dark Mode), com a preferência salva no localStorage.

Alteração de Senha: Formulário para alteração da senha do usuário (simulado).

Zona de Perigo: Interface para ações destrutivas, como deletar a conta.

6. Exportação de Dados

Exportar para PDF: Utilizando as bibliotecas html2canvas e jsPDF, o usuário pode exportar a visualização da aba atual para um arquivo PDF.

Exportar para CSV: Funcionalidade para baixar os dados da tabela de relatórios em formato .csv.

🛠️ Tecnologias Utilizadas

HTML5: Estrutura semântica da aplicação.

CSS3: Estilização base com variáveis para o sistema de temas.

Tailwind CSS: Framework de CSS utilitário para a criação rápida de uma interface moderna e responsiva.

JavaScript (ES6+): Lógica principal da aplicação, incluindo manipulação do DOM, gerenciamento de estado simulado e interatividade.

Chart.js: Biblioteca para a criação dos gráficos dinâmicos.

html2canvas & jsPDF: Bibliotecas utilizadas para a funcionalidade de exportação para PDF.

🚀 Como Executar

Por ser um projeto autocontido em um único arquivo, a execução é extremamente simples:

Faça o download do arquivo index.html.

Abra o arquivo em qualquer navegador web moderno (Google Chrome, Firefox, Edge, etc.).

E pronto! A aplicação estará totalmente funcional.

🧬 Estrutura do Código

Todo o código está contido no arquivo index.html, organizado da seguinte forma:

<head>:

Importação dos CDNs para Tailwind CSS, Chart.js, jsPDF e html2canvas.

Bloco <style> com as variáveis CSS para os temas (Dark/Light) e estilos customizados.

<body>:

Tela de Autenticação (#auth-screen): HTML para os formulários de login e cadastro.

Aplicação Principal (#app):

Sidebar (<aside>): Barra de navegação lateral com os links para as abas.

Conteúdo Principal (<main>):

Cabeçalho (<header>): Título da página, mensagem de boas-vindas, seletor de ano e botões de exportação.

Área de Conteúdo (#content-area): Contêiner para as abas, onde cada div com a classe .tab-content representa uma seção (Dashboard, Simulador, etc.).

<script>:

Cache de Elementos: Todos os elementos do DOM são selecionados e armazenados em um objeto els para melhor performance.

Dados Mockados (mockDatabase): Um objeto JavaScript que simula um banco de dados com os dados financeiros por ano.

Módulos de Lógica: O código é organizado em "módulos" (objetos), como ThemeManager e Auth, para separar responsabilidades.

Funções Principais:

createOrUpdateChart(): Lida com a renderização e atualização dos gráficos.

updateDashboardData(): Função central que atualiza toda a UI com base no ano selecionado.

setupTabs(): Gerencia a navegação por abas.

Listeners de Evento: Lógica para todos os elementos interativos, como botões, formulários e seletores.
