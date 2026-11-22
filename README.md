<!doctype html>

<html lang="pt-BR">  
<head>  
  <meta charset="utf-8">  
  <meta name="viewport" content="width=device-width, initial-scale=1">  
  <title>Quartel General da Nova Era — EBNE</title>  
  <style>  
    :root {  
      --bg: #090909;  
      --panel: #151515;  
      --line: #343434;  
      --text: #f5f5f5;  
      --muted: #b5b5b5;  
    }  * { box-sizing: border-box; }  

body {  
  margin: 0;  
  min-height: 100vh;  
  background: var(--bg);  
  color: var(--text);  
  font-family: Arial, Helvetica, sans-serif;  
}  

.sidebar {  
  position: fixed;  
  inset: 0 auto 0 0;  
  width: 250px;  
  padding: 26px 16px;  
  background: #101010;  
  border-right: 1px solid var(--line);  
  display: flex;  
  flex-direction: column;  
}  

.brand {  
  margin: 0 8px 30px;  
  letter-spacing: 2px;  
}  

.brand strong {  
  display: block;  
  font-size: 16px;  
}  

.brand span {  
  color: var(--muted);  
  font-size: 12px;  
}  

.nav {  
  display: grid;  
  gap: 7px;  
}  

.nav button,  
.primary,  
.secondary {  
  border: 1px solid var(--line);  
  border-radius: 8px;  
  color: var(--text);  
  background: transparent;  
  cursor: pointer;  
}  

.nav button {  
  padding: 12px;  
  text-align: left;  
}  

.nav button:hover,  
.nav button.active {  
  background: #262626;  
}  

.discord {  
  margin-top: auto;  
  padding: 13px;  
  border: 1px solid #555;  
  border-radius: 8px;  
  color: white;  
  background: #202020;  
  text-align: center;  
  text-decoration: none;  
  font-weight: bold;  
}  

main {  
  margin-left: 250px;  
  padding: 40px;  
  max-width: 1200px;  
}  

.view { display: none; }  
.view.active { display: block; }  

.hero,  
.panel,  
.card {  
  border: 1px solid var(--line);  
  border-radius: 12px;  
  background: var(--panel);  
}  

.hero {  
  padding: 42px;  
  background: linear-gradient(135deg, #191919, #0e0e0e);  
}  

h1 {  
  margin: 8px 0 14px;  
  font-size: clamp(38px, 6vw, 62px);  
  letter-spacing: -2px;  
}  

h2 { margin-top: 0; }  
p, li { color: var(--muted); line-height: 1.6; }  

.actions {  
  display: flex;  
  flex-wrap: wrap;  
  gap: 10px;  
  margin-top: 24px;  
}  

.primary,  
.secondary {  
  display: inline-flex;  
  align-items: center;  
  justify-content: center;  
  min-height: 42px;  
  padding: 10px 15px;  
  text-decoration: none;  
}  

.primary {  
  background: #f5f5f5;  
  color: #101010;  
  border-color: #f5f5f5;  
  font-weight: bold;  
}  

.secondary:hover { background: #242424; }  

.grid {  
  display: grid;  
  grid-template-columns: repeat(3, 1fr);  
  gap: 14px;  
  margin-top: 20px;  
}  

.card,  
.panel {  
  padding: 22px;  
}  

.rank {  
  display: flex;  
  justify-content: space-between;  
  gap: 16px;  
  margin-top: 8px;  
  padding: 13px;  
  border: 1px solid #2d2d2d;  
  border-radius: 8px;  
}  

.rank span {  
  color: var(--muted);  
  text-align: right;  
}  

form {  
  display: grid;  
  grid-template-columns: repeat(2, 1fr);  
  gap: 14px;  
  margin-top: 18px;  
}  

label {  
  display: grid;  
  gap: 7px;  
}  

label.full {  
  grid-column: 1 / -1;  
}  

input,  
select,  
textarea {  
  width: 100%;  
  padding: 11px;  
  border: 1px solid #3b3b3b;  
  border-radius: 7px;  
  background: #0e0e0e;  
  color: white;  
}  

textarea {  
  min-height: 100px;  
  resize: vertical;  
}  

.form-actions {  
  grid-column: 1 / -1;  
}  

.result {  
  display: none;  
  margin-top: 18px;  
  padding: 16px;  
  border: 1px solid #555;  
  border-radius: 8px;  
  background: #1d1d1d;  
}  

.result.show { display: block; }  

.result pre {  
  white-space: pre-wrap;  
  color: #ededed;  
  font-family: monospace;  
}  

footer {  
  margin-top: 35px;  
  color: #777;  
  font-size: 12px;  
}  

@media (max-width: 760px) {  
  .sidebar {  
    position: sticky;  
    width: 100%;  
    height: auto;  
    padding: 12px;  
  }  

  .brand { margin-bottom: 10px; }  

  .nav {  
    display: flex;  
    overflow-x: auto;  
  }  

  .nav button {  
    white-space: nowrap;  
  }  

  .discord { display: none; }  

  main {  
    margin: 0;  
    padding: 20px 14px;  
  }  

  .hero { padding: 25px 18px; }  

  .grid,  
  form {  
    grid-template-columns: 1fr;  
  }  

  label.full,  
  .form-actions {  
    grid-column: auto;  
  }  

  .rank {  
    flex-direction: column;  
  }  

  .rank span {  
    text-align: left;  
  }  
}

  </style>  
</head>  
<body>  
  <aside class="sidebar">  
    <div class="brand">  
      <strong>EBNE</strong>  
      <span>Quartel General da Nova Era</span>  
    </div>  <nav class="nav">  
  <button class="active" data-view="inicio">Início</button>  
  <button data-view="hierarquia">Hierarquia</button>  
  <button data-view="solicitacoes">Solicitações</button>  
  <button data-view="divisoes">Divisões</button>  
  <button data-view="codigos">Códigos de up</button>  
</nav>  

<a class="discord" href="https://discord.gg/EhHrcCbBu" target="_blank" rel="noopener">  
  Acessar servidor do Discord  
</a>

  </aside>    <main>  
    <section class="view active" id="inicio">  
      <div class="hero">  
        <h1>Disciplina.<br>Honra. EBNE.</h1>  
        <p>Portal oficial do Quartel General da Nova Era.</p>  
        <div class="actions">  
          <button class="primary" data-go="solicitacoes">Fazer solicitação</button>  
          <button class="secondary" data-go="hierarquia">Consultar hierarquia</button>  
        </div>  
      </div>  <div class="grid">  
    <article class="card">  
      <h2>Hierarquia</h2>  
      <p>Consulte os cargos e a cadeia de comando.</p>  
      <button class="secondary" data-go="hierarquia">Acessar</button>  
    </article>  

    <article class="card">  
      <h2>Solicitações</h2>  
      <p>Promoções e rebaixamentos gerais ou divisionais.</p>  
      <button class="secondary" data-go="solicitacoes">Acessar</button>  
    </article>  

    <article class="card">  
      <h2>Códigos de up</h2>  
      <p>Encontre os códigos oficiais no Discord.</p>  
      <button class="secondary" data-go="codigos">Acessar</button>  
    </article>  
  </div>  
</section>  

<section class="view" id="hierarquia">  
  <h1>Hierarquia Geral</h1>  
  <div class="panel">  
    <div class="rank"><strong>Recruta</strong><span>Patente inicial</span></div>  
    <div class="rank"><strong>Soldado</strong><span>Efetivo operacional</span></div>  
    <div class="rank"><strong>Cabo</strong><span>Apoio operacional</span></div>  
    <div class="rank"><strong>Sargento</strong><span>Liderança de equipe</span></div>  
    <div class="rank"><strong>Oficial</strong><span>Comando e administração</span></div>  
    <div class="rank"><strong>Alto Comando</strong><span>Direção do quartel</span></div>  
  </div>  
</section>  

<section class="view" id="solicitacoes">  
  <h1>Solicitações</h1>  

  <div class="panel">  
    <h2>Promoção ou rebaixamento</h2>  
    <form class="request-form">  
      <label>  
        Tipo  
        <select name="Tipo" required>  
          <option value="">Selecione</option>  
          <option>Promoção</option>  
          <option>Rebaixamento</option>  
        </select>  
      </label>  

      <label>  
        Nome do militar  
        <input name="Militar" required>  
      </label>  

      <label>  
        Cargo atual  
        <input name="Cargo atual" required>  
      </label>  

      <label>  
        Cargo solicitado  
        <input name="Cargo solicitado" required>  
      </label>  

      <label class="full">  
        Justificativa  
        <textarea name="Justificativa" required></textarea>  
      </label>  

      <div class="form-actions">  
        <button class="primary" type="submit">Gerar solicitação</button>  
      </div>  
    </form>  

    <div class="result">  
      <strong>Solicitação pronta</strong>  
      <pre></pre>  
      <button class="secondary copy-button" type="button">Copiar texto</button>  
    </div>  
  </div>  

  <br>  

  <div class="panel">  
    <h2>Promoção ou rebaixamento em divisão</h2>  
    <form class="request-form">  
      <label>  
        Tipo  
        <select name="Tipo" required>  
          <option value="">Selecione</option>  
          <option>Promoção em divisão</option>  
          <option>Rebaixamento em divisão</option>  
        </select>  
      </label>  

      <label>  
        Nome do militar  
        <input name="Militar" required>  
      </label>  

      <label>  
        Divisão  
        <input name="Divisão" required>  
      </label>  

      <label>  
        Cargo divisional solicitado  
        <input name="Cargo divisional solicitado" required>  
      </label>  

      <label class="full">  
        Justificativa  
        <textarea name="Justificativa" required></textarea>  
      </label>  

      <div class="form-actions">  
        <button class="primary" type="submit">Gerar solicitação</button>  
      </div>  
    </form>  

    <div class="result">  
      <strong>Solicitação pronta</strong>  
      <pre></pre>  
      <button class="secondary copy-button" type="button">Copiar texto</button>  
    </div>  
  </div>  
</section>  

<section class="view" id="divisoes">  
  <h1>Divisões</h1>  
  <div class="grid">  
    <article class="card">  
      <h2>Treinamento</h2>  
      <p>Formação e instrução dos militares.</p>  
    </article>  

    <article class="card">  
      <h2>Segurança</h2>  
      <p>Proteção e cumprimento das regras.</p>  
    </article>  

    <article class="card">  
      <h2>Administrativa</h2>  
      <p>Gestão de membros e registros.</p>  
    </article>  
  </div>  

  <br>  

  <div class="panel">  
    <h2>Hierarquia Divisional</h2>  
    <div class="rank"><strong>Membro</strong><span>Integrante</span></div>  
    <div class="rank"><strong>Auxiliar</strong><span>Apoio à divisão</span></div>  
    <div class="rank"><strong>Supervisor</strong><span>Liderança operacional</span></div>  
    <div class="rank"><strong>Comandante</strong><span>Comando da divisão</span></div>  
  </div>  
</section>  

<section class="view" id="codigos">  
  <h1>Códigos de UP</h1>  
  <div class="panel">  
    <h2>Acesso oficial</h2>  
    <p>Os códigos devem ser consultados apenas nos canais oficiais do servidor do EBNE.</p>  
    <p>Não utilize códigos divulgados por fontes não autorizadas.</p>  
    <a class="primary" href="https://discord.gg/EhHrcCbBu" target="_blank" rel="noopener">  
      Abrir servidor do Discord  
    </a>  
  </div>  
</section>  

<footer>  
  Quartel General da Nova Era · EBNE  
</footer>

  </main>    <script>  
    const botoes = document.querySelectorAll(".nav button");  
    const telas = document.querySelectorAll(".view");  
  
    function abrirTela(id) {  
      telas.forEach(tela =>  
        tela.classList.toggle("active", tela.id === id)  
      );  
  
      botoes.forEach(botao =>  
        botao.classList.toggle("active", botao.dataset.view === id)  
      );  
  
      window.scrollTo({ top: 0, behavior: "smooth" });  
    }  
  
    botoes.forEach(botao =>  
      botao.addEventListener("click", () =>  
        abrirTela(botao.dataset.view)  
      )  
    );  
  
    document.querySelectorAll("[data-go]").forEach(botao =>  
      botao.addEventListener("click", () =>  
        abrirTela(botao.dataset.go)  
      )  
    );  
  
    document.querySelectorAll(".request-form").forEach(form => {  
      form.addEventListener("submit", evento => {  
        evento.preventDefault();  
  
        const linhas = ["**Solicitação — EBNE**"];  
        new FormData(form).forEach((valor, campo) => {  
          if (String(valor).trim()) {  
            linhas.push(`**${campo}:** ${valor}`);  
          }  
        });  
  
        const resultado = form.nextElementSibling;  
        resultado.querySelector("pre").textContent = linhas.join("\n");  
        resultado.classList.add("show");  
      });  
    });  
  
    document.querySelectorAll(".copy-button").forEach(botao => {  
      botao.addEventListener("click", async () => {  
        const texto = botao.parentElement.querySelector("pre").textContent;  
        await navigator.clipboard.writeText(texto);  
        botao.textContent = "Copiado";  
      });  
    });  
  </script>  </body>  
</html>
