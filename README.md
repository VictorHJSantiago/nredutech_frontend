<div align="center">
  <br />
  <img src="https://raw.githubusercontent.com/victorhjsantiago/nredutech/main/public/images/nredutech.png" alt="Logo NREduTech" width="150" style="border-radius: 50%;">
  
  <h1 style="border-bottom: none; font-size: 2.5em; margin-bottom: 0;">NREduTech (Frontend)</h1>
  
  <strong style="font-size: 1.2em; color: #555;">
    Protótipo Estático de Alta Fidelidade
  </strong>
  
  <br />
  <p style="font-size: 1.1em; max-width: 700px;">
    Este repositório contém o protótipo estático (HTML/CSS) para o Sistema de Gestão Acadêmica <strong>NREduTech</strong>. Ele serve como a "View" (Visão) da arquitetura MVC, estabelecendo o Design System, a responsividade e a experiência do utilizador antes da integração com o backend Laravel.
  </p>

  <p>
    <img src="https://img.shields.io/badge/status-Protótipo%20Estático-blue?style=for-the-badge" alt="Status do Projeto: Protótipo Estático">
    <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5">
    <img src="https://img.shields.io/badge/CSS3_(Vanilla)-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3 (Vanilla)">
    <img src="https://img.shields.io/badge/Design-Responsivo-green?style=for-the-badge&logo=MobileView" alt="Design Responsivo">
  </p>
</div>

---

## 📖 Sobre o Projeto

O **NREduTech Frontend** é a contraparte visual do sistema de gestão acadêmica. Este projeto foi concebido como um protótipo de alta fidelidade para validar os fluxos de utilizador, definir um Design System coeso e fornecer *templates* HTML/CSS prontos para serem integrados ao backend (ex: convertidos em *views* do Laravel Blade).

O foco principal foi criar uma interface limpa, profissional e responsiva (Mobile-First), utilizando CSS puro (Vanilla CSS) com uma arquitetura modularizada e baseada em variáveis.

## ✨ Telas Prototipadas (Funcionalidades)

Este protótipo cobre todos os principais fluxos de utilizador definidos nos requisitos do sistema:

* **🔐 Autenticação:**
    * Tela de Login
    * Tela de Cadastro de Usuário

* **🏠 Dashboard (Início):**
    * Página principal pós-login com cartões de navegação.

* **👥 Gestão de Usuários (Admin):**
    * Listagem, aprovação e filtros de usuários.
    * Formulário de Cadastro de Usuário.
    * Formulário de Edição de Usuário.

* **📂 Gestão de Disciplinas:**
    * Consulta e filtro de disciplinas.
    * Formulário de Cadastro de Disciplina.
    * Formulário de Edição de Disciplina.

* **👩‍🏫 Gestão de Professores:**
    * Listagem/Consulta de professores.
    * Formulário de Cadastro de Professor.
    * Formulário de Edição de Professor.

* **📖 Gestão de Recursos Didáticos:**
    * Listagem/Consulta de recursos.
    * Formulário de Cadastro de Recurso.
    * Formulário de Edição de Recurso.

* **🔬 Laboratórios e Componentes:**
    * Visualização de status de Laboratórios.
    * Visualização de Componentes Curriculares (vínculo Turma-Professor-Matéria).

* **📊 Relatórios e Configurações:**
    * Formulário de geração de Relatórios.
    * Página de Notificações.
    * Página de Configurações (com múltiplos formulários).

---

## 🛠️ Arquitetura de CSS e Design System

Diferente de um projeto backend, os requisitos técnicos aqui estão focados na manutenibilidade, escalabilidade e consistência do CSS. A arquitetura segue padrões modernos de frontend.

### Requisitos Não-Funcionais (RNF) Implementados

<div style="width: 100%; overflow-x: auto;">
  <table width="100%" style="border-collapse: collapse; border-radius: 8px; overflow: hidden; box-shadow: 0 2px 8px rgba(0,0,0,0.1); font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;">
    <thead style="background-color: #0169b4; color: white;">
      <tr>
        <th style="padding: 12px 15px; text-align: left;">Tópico</th>
        <th style="padding: 12px 15px; text-align: left;">Implementação</th>
        <th style="padding: 12px 15px; text-align: left;">Justificativa</th>
      </tr>
    </thead>
    <tbody style="background-color: #fff; color: #333;">
      <tr style="border-bottom: 1px solid #ddd; background-color: #f9f9f9;">
        <td style="padding: 12px 15px;"><strong>Design System Centralizado</strong></td>
        <td style="padding: 12px 15px;">Uso extensivo de <strong>Variáveis CSS (<code>:root</code>)</strong> para cores (<code>--azul-principal</code>, <code>--verde-principal</code>), fontes e sombras (<code>--sombra</code>).</td>
        <td style="padding: 12px 15px;">Permite que a identidade visual do sistema seja alterada globalmente num único arquivo, garantindo consistência e facilitando a manutenção ou a criação de temas (como um "modo escuro").</td>
      </tr>
      <tr style="border-bottom: 1px solid #ddd;">
        <td style="padding: 12px 15px;"><strong>CSS Modular (OOCSS)</strong></td>
        <td style="padding: 12px 15px;">Cada tela ou componente principal possui seu próprio arquivo CSS (ex: <code>disciplinas_consulta.css</code>, <code>login.css</code>, <code>index.css</code>).</td>
        <td style="padding: 12px 15px;">Evita a sobreposição de estilos e conflitos de especificidade. O <code>index.css</code> define o layout global (sidebar, main-content), enquanto os arquivos específicos cuidam apenas do conteúdo da sua própria página.</td>
      </tr>
      <tr style="border-bottom: 1px solid #ddd; background-color: #f9f9f9;">
        <td style="padding: 12px 15px;"><strong>Responsividade (Mobile-First)</strong></td>
        <td style="padding: 12px 15px;">Utilização de <strong>Flexbox</strong>, <strong>CSS Grid</strong> (<code>.form-grid</code>) e <code>@media</code> queries para adaptar a interface a tablets e telemóveis.</td>
        <td style="padding: 12px 15px;">Garante a usabilidade do sistema em qualquer dispositivo (RNF-001 do projeto backend). A barra lateral, por exemplo, é recolhida em ecrãs menores.</td>
      </tr>
      <tr style="border-bottom: 1px solid #ddd;">
        <td style="padding: 12px 15px;"><strong>Componentes Reutilizáveis</strong></td>
        <td style="padding: 12px 15px;">Classes genéricas como <code>.btn-primary</code>, <code>.form-group</code>, <code>.header-section</code>, e <code>.table-section</code> são usadas em múltiplas páginas.</td>
        <td style="padding: 12px 15px;">Cria uma Interface de Utilizador (UI) consistente e previsível, reduzindo a duplicação de código e acelerando o desenvolvimento de novas telas (ex: <code>professores.css</code> e <code>laboratorios.css</code> partilham estilos de tabela).</td>
      </tr>
    </tbody>
  </table>
</div>

---

## 🚀 Stack Tecnológica

A seleção de tecnologias foi intencionalmente minimalista para focar na pureza do HTML/CSS, garantindo que os *templates* sejam leves, rápidos e universalmente compatíveis para integração.

<div style="width: 100%; overflow-x: auto;">
  <table width="100%" style="border-collapse: collapse; border-radius: 8px; overflow: hidden; box-shadow: 0 2px 8px rgba(0,0,0,0.1); font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;">
    <thead style="background-color: #444; color: white;">
      <tr>
        <th style="padding: 12px 15px; text-align: left;">Tecnologia</th>
        <th style="padding: 12px 15px; text-align: left;">Justificativa (Por que foi escolhida?)</th>
      </tr>
    </thead>
    <tbody style="background-color: #fff; color: #333;">
      <tr style="border-bottom: 1px solid #ddd; background-color: #f9f9f9;">
        <td style="padding: 12px 15px;"><strong>HTML5 (Semântico)</strong></td>
        <td style="padding: 12px 15px;">Estruturação de todas as páginas (ex: <code>index.html</code>, <code>login.html</code>). O uso de tags como <code>&lt;nav&gt;</code>, <code>&lt;header&gt;</code>, e <code>&lt;section&gt;</code> melhora a acessibilidade (RNF-006) e a legibilidade do código.</td>
      </tr>
      <tr style="border-bottom: 1px solid #ddd;">
        <td style="padding: 12px 15px;"><strong>CSS3 (Puro / Vanilla)</strong></td>
        <td style="padding: 12px 15px;">Escolhido em detrimento de *frameworks* (como Bootstrap ou Tailwind) para criar um Design System 100% customizado e leve, sem "lutar" contra estilos pré-definidos. Permite controlo total sobre a responsividade e a arquitetura modular.</td>
      </tr>
      <tr style="background-color: #f9f9f9;">
        <td style="padding: 12px 15px;"><strong>Google Fonts</strong></td>
        <td style="padding: 12px 15px;">A fonte <em>Roboto</em> foi importada para garantir uma tipografia limpa, moderna e consistente em todos os sistemas operativos.</td>
      </tr>
    </tbody>
  </table>
</div>

---

## 💡 Próximos Passos (Integração Backend)

Este protótipo está pronto para a "próxima fase": a integração com um backend como o Laravel.

* **Formulários:** Todos os formulários (ex: `login.html`, `disciplinas_cadastro.html`) usam `method="GET"` e apontam para outros arquivos `.html` apenas para fins de prototipagem. Na integração, seriam alterados para `method="POST"` e incluiriam a diretiva `@csrf` do Blade.
* **Dados Estáticos:** As tabelas (ex: `professores.html`) contêm dados estáticos (hardcoded). Estes `<tbody>`s seriam substituídos por loops `@foreach` do Blade para popular os dados dinamicamente a partir do Controller.
* **Estado Ativo:** A classe `.active` na barra de navegação está definida manualmente em cada arquivo. O backend controlaria isso dinamicamente, usando `Request::is()` do Laravel para aplicar a classe ao link da rota atual.

---

## 👨‍💻 Autor

<div style="width: 100%; overflow-x: auto;">
  <table width="100%" style="border-collapse: collapse; border-radius: 8px; overflow: hidden; box-shadow: 0 2px 8px rgba(0,0,0,0.1); font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background-color: #f9f9f9;">
    <tr>
      <td style="padding: 20px; width: 100px; text-align: center;">
        <img src="https://avatars.githubusercontent.com/u/142981329?v=4" width="90" alt="Avatar do Victor" style="border-radius: 50%;">
      </td>
      <td style="padding: 20px; color: #333;">
        <strong style="font-size: 1.3em; color: #0169b4;">Victor Henrique Jesus Santiago</strong><br>
        Desenvolvedor Full Stack<br><br>
        📧 <a href="mailto:victorhenriquedejesussantiago@gmail.com" style="color: #0169b4; text-decoration: none;">victorhenriquedejesussantiago@gmail.com</a><br>
        👔 <a href="kedin.com/in/victor-henrique-de-jesus-santiago/" style="color: #0169b4; text-decoration: none;">LinkedIn/Victor Henrique de Jesus Santiago</a><br>  
        🐙 <a href="https://github.com/victorhjsantiago" style="color: #0169b4; text-decoration: none;">GitHub/victorhjsantiago</a>
      </td>
    </tr>
  </table>
</div>
