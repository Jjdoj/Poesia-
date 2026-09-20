<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Versos e Letras</title>
  <meta name="description" content="Site de poesia com poemas, reflexões e contato" />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet" />
  <style>
    :root {
      --bg: #f9f5f1;
      --bg-strong: #efe2d5;
      --paper: #fffdfb;
      --paper-2: #f7efe8;
      --text: #231f1d;
      --muted: #655d5a;
      --accent: #8d6851;
      --accent-strong: #6b4d39;
      --line: #e7d9cd;
      --shadow: 0 18px 40px rgba(60, 42, 31, 0.08);
      --shadow-soft: 0 10px 28px rgba(60, 42, 31, 0.05);
      --radius: 22px;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: "Inter", sans-serif;
      background:
        radial-gradient(circle at top, rgba(255,255,255,0.85), transparent 38%),
        var(--bg);
      color: var(--text);
      line-height: 1.7;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    img {
      max-width: 100%;
      display: block;
    }

    button, input, textarea {
      font: inherit;
    }

    .container {
      width: min(1180px, calc(100% - 32px));
      margin: 0 auto;
    }

    .section {
      padding: 110px 0;
    }

    .eyebrow {
      display: inline-block;
      text-transform: uppercase;
      letter-spacing: 2.2px;
      font-size: 0.76rem;
      font-weight: 700;
      color: var(--accent);
      margin-bottom: 16px;
    }

    .site-header {
      padding-top: 26px;
      position: sticky;
      top: 0;
      background: rgba(249, 245, 241, 0.78);
      backdrop-filter: blur(10px);
      -webkit-backdrop-filter: blur(10px);
      z-index: 20;
      border-bottom: 1px solid rgba(141, 104, 81, 0.1);
    }

    .navbar {
      display: flex;
      align-items: center;
      justify-content: space-between;
      min-height: 76px;
      gap: 20px;
    }

    .logo {
      font-family: "Cormorant Garamond", serif;
      font-size: clamp(2rem, 2.5vw, 2.7rem);
      color: var(--accent);
      font-weight: 700;
      letter-spacing: 0.06em;
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 26px;
      flex-wrap: wrap;
    }

    .nav-links a {
      font-size: 0.75rem;
      text-transform: uppercase;
      letter-spacing: 1.8px;
      color: var(--text);
      position: relative;
      padding-bottom: 6px;
      transition: color 0.25s ease;
    }

    .nav-links a::after {
      content: "";
      position: absolute;
      left: 0;
      bottom: 0;
      width: 100%;
      height: 2px;
      background: var(--accent);
      transform: scaleX(0);
      transform-origin: center;
      transition: transform 0.25s ease;
    }

    .nav-links a:hover {
      color: var(--accent);
    }

    .nav-links a:hover::after {
      transform: scaleX(1);
    }

    .hero {
      display: grid;
      grid-template-columns: 1.25fr 0.75fr;
      align-items: center;
      gap: 40px;
      padding: 80px 0 60px;
    }

    .hero-copy h1 {
      font-family: "Cormorant Garamond", serif;
      font-size: clamp(4rem, 8vw, 7rem);
      line-height: 0.9;
      letter-spacing: -0.04em;
      margin-bottom: 18px;
      color: var(--text);
    }

    .hero-copy p {
      max-width: 620px;
      color: var(--muted);
      font-size: 1.08rem;
    }

    .hero-actions {
      display: flex;
      align-items: center;
      gap: 16px;
      flex-wrap: wrap;
      margin-top: 28px;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      border-radius: 999px;
      padding: 15px 24px;
      font-weight: 600;
      transition: transform 0.2s ease, box-shadow 0.2s ease;
      cursor: pointer;
      border: none;
    }

    .btn:hover {
      transform: translateY(-2px);
    }

    .btn-primary {
      background: var(--accent);
      color: #fff;
      box-shadow: var(--shadow-soft);
    }

    .btn-secondary {
      background: transparent;
      border: 1px solid var(--line);
      color: var(--text);
    }

    .hero-card {
      background: linear-gradient(135deg, #fffdfb 0%, #f3e7df 100%);
      border: 1px solid var(--line);
      border-radius: var(--radius);
      padding: 30px 24px 26px;
      box-shadow: var(--shadow);
      position: relative;
      overflow: hidden;
      min-height: 300px;
      display: flex;
      align-items: center;
      justify-content: center;
      text-align: center;
    }

    .hero-card::before {
      content: "";
      position: absolute;
      inset: 14px;
      border: 1px solid rgba(141, 104, 81, 0.2);
      border-radius: 18px;
    }

    .hero-card-inner {
      position: relative;
      z-index: 1;
      max-width: 280px;
    }

    .hero-card-label {
      text-transform: uppercase;
      letter-spacing: 2px;
      font-size: 0.7rem;
      color: var(--accent);
      font-weight: 700;
      margin-bottom: 12px;
    }

    .hero-card blockquote {
      font-family: "Cormorant Garamond", serif;
      font-size: clamp(2.1rem, 3vw, 3rem);
      line-height: 1.15;
      color: var(--text);
    }

    .stats {
      display: flex;
      gap: 16px;
      flex-wrap: wrap;
      margin-top: 38px;
    }

    .stat {
      min-width: 120px;
      background: rgba(255,255,255,0.3);
      border: 1px solid var(--line);
      border-radius: 16px;
      padding: 14px 16px;
    }

    .stat strong {
      display: block;
      font-size: 1.3rem;
      color: var(--accent);
      font-weight: 700;
    }

    .stat span {
      color: var(--muted);
      font-size: 0.8rem;
      text-transform: uppercase;
      letter-spacing: 1.1px;
    }

    .section-head {
      margin-bottom: 40px;
      text-align: center;
    }

    .section-head h2 {
      font-family: "Cormorant Garamond", serif;
      font-size: clamp(2.8rem, 4vw, 4rem);
      line-height: 1;
      font-weight: 600;
      letter-spacing: -0.04em;
      color: var(--text);
    }

    .section-head p {
      margin-top: 12px;
      color: var(--muted);
      font-size: 1rem;
    }

    .poem-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 26px;
    }

    .poem-card {
      background: var(--paper);
      border: 1px solid var(--line);
      border-radius: var(--radius);
      padding: 30px 24px 24px;
      box-shadow: var(--shadow-soft);
      transition: transform 0.25s ease, box-shadow 0.25s ease;
      position: relative;
      overflow: hidden;
    }

    .poem-card::before {
      content: "";
      position: absolute;
      inset: 0 auto auto 0;
      width: 100%;
      height: 4px;
      background: linear-gradient(90deg, var(--accent), transparent);
    }

    .poem-card:hover {
      transform: translateY(-8px);
      box-shadow: var(--shadow);
    }

    .poem-card h3 {
      font-family: "Cormorant Garamond", serif;
      font-size: 2.2rem;
      margin-bottom: 18px;
      color: var(--text);
    }

    .poem-card p {
      font-family: "Cormorant Garamond", serif;
      font-size: 1.48rem;
      line-height: 1.3;
      color: #382f2b;
      white-space: pre-line;
      margin-bottom: 20px;
    }

    .poem-card .author {
      font-size: 0.75rem;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      color: var(--accent);
      font-weight: 700;
    }

    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 30px;
      align-items: center;
    }

    .about-card,
    .quote-card {
      background: var(--paper);
      border: 1px solid var(--line);
      border-radius: var(--radius);
      box-shadow: var(--shadow-soft);
    }

    .about-card {
      padding: 32px 30px;
    }

    .about-card h3 {
      font-family: "Cormorant Garamond", serif;
      font-size: clamp(2.3rem, 5vw, 3.2rem);
      margin-bottom: 16px;
    }

    .about-card p {
      color: var(--muted);
      margin-bottom: 16px;
    }

    .quote-card {
      min-height: 300px;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 28px;
      background: linear-gradient(135deg, var(--paper-2) 0%, #fff 100%);
    }

    .quote-card blockquote {
      font-family: "Cormorant Garamond", serif;
      font-size: clamp(2.1rem, 4vw, 3.2rem);
      line-height: 1.08;
      text-align: center;
      color: var(--text);
      max-width: 420px;
    }

    .features {
      display: grid;
      grid-template-columns: repeat(3, minmax(0,1fr));
      gap: 22px;
      margin-top: 28px;
    }

    .feature-box {
      background: rgba(255,255,255,0.4);
      border: 1px solid var(--line);
      border-radius: 18px;
      padding: 22px 18px;
      box-shadow: var(--shadow-soft);
    }

    .feature-box h4 {
      font-size: 1.05rem;
      margin-bottom: 10px;
      color: var(--text);
    }

    .feature-box p {
      color: var(--muted);
      font-size: 0.96rem;
    }

    .contact-grid {
      display: grid;
      grid-template-columns: 0.9fr 1.1fr;
      gap: 28px;
      align-items: start;
    }

    .contact-card,
    .form-card {
      background: var(--paper);
      border: 1px solid var(--line);
      border-radius: var(--radius);
      box-shadow: var(--shadow-soft);
    }

    .contact-card {
      padding: 32px 26px;
    }

    .contact-card h3,
    .form-card h3 {
      font-family: "Cormorant Garamond", serif;
      font-size: clamp(2.3rem, 5vw, 3rem);
      margin-bottom: 18px;
    }

    .contact-card p {
      color: var(--muted);
      margin-bottom: 20px;
    }

    .contact-list {
      list-style: none;
      display: grid;
      gap: 14px;
    }

    .contact-list li {
      display: flex;
      flex-direction: column;
      gap: 4px;
      color: var(--text);
    }

    .contact-list strong {
      font-size: 0.72rem;
      letter-spacing: 1.7px;
      text-transform: uppercase;
      color: var(--accent);
    }

    .form-card {
      padding: 28px 24px;
    }

    form {
      display: grid;
      gap: 18px;
    }

    .field {
      display: grid;
      gap: 8px;
    }

    label {
      font-size: 0.72rem;
      letter-spacing: 1.5px;
      text-transform: uppercase;
      font-weight: 700;
      color: var(--text);
    }

    input, textarea {
      width: 100%;
      border: 1px solid var(--line);
      border-radius: 14px;
      padding: 14px 15px;
      background: #fff;
      color: var(--text);
      transition: border-color 0.2s ease, box-shadow 0.2s ease;
    }

    input:focus, textarea:focus {
      border-color: var(--accent);
      box-shadow: 0 0 0 4px rgba(141,104,81,0.1);
      outline: none;
    }

    textarea {
      min-height: 150px;
      resize: vertical;
    }

    .site-footer {
      padding: 26px 0 42px;
      border-top: 1px solid rgba(141,104,81,0.12);
      text-align: center;
      color: var(--muted);
    }

    .hidden {
      opacity: 0;
      transform: translateY(20px);
      transition: opacity 0.6s ease, transform 0.6s ease;
    }

    .visible {
      opacity: 1;
      transform: translateY(0);
    }

    @media (max-width: 980px) {
      .hero,
      .about-grid,
      .contact-grid,
      .poem-grid,
      .features {
        grid-template-columns: 1fr;
      }

      .hero {
        padding-top: 42px;
      }
    }

    @media (max-width: 640px) {
      .navbar {
        flex-direction: column;
        justify-content: center;
        padding: 10px 0 18px;
      }

      .nav-links {
        justify-content: center;
      }

      .hero-copy h1 {
        font-size: 3.2rem;
      }

      .poem-card p {
        font-size: 1.3rem;
      }

      .btn {
        width: 100%;
      }

      .hero-actions {
        flex-direction: column;
        align-items: stretch;
      }
    }
  </style>
</head>
<body>
  <header class="site-header">
    <div class="container">
      <nav class="navbar">
        <a href="#inicio" class="logo">Versos e Letras</a>
        <div class="nav-links">
          <a href="#inicio">Início</a>
          <a href="#poemas">Poemas</a>
          <a href="#sobre">Sobre</a>
          <a href="#contato">Contato</a>
        </div>
      </nav>
    </div>
  </header>

  <main id="inicio">
    <section class="container hero">
      <div class="hero-copy hidden">
        <span class="eyebrow">Poesia em cada linha</span>
        <h1>Palavras que tocam a alma.</h1>
        <p>
          Um portal para reflexões, sentimentos e versos delicados. Aqui, o mundo desacelera
          e cada palavra encontra um lugar para respirar.
        </p>

        <div class="hero-actions">
          <a class="btn btn-primary" href="#poemas">Ver poemas</a>
          <a class="btn btn-secondary" href="#sobre">Conhecer mais</a>
        </div>

        <div class="stats">
          <div class="stat">
            <strong>120+</strong>
            <span>versos</span>
          </div>
          <div class="stat">
            <strong>08</strong>
            <span>poemas</span>
          </div>
          <div class="stat">
            <strong>24/7</strong>
            <span>inspiração</span>
          </div>
        </div>
      </div>

      <div class="hero-card hidden">
        <div class="hero-card-inner">
          <div class="hero-card-label">Citação do dia</div>
          <blockquote>
            “A poesia é o lugar onde o coração aprende a falar em silêncio.”
          </blockquote>
        </div>
      </div>
    </section>

    <section class="section" id="poemas">
      <div class="container">
        <div class="section-head hidden">
          <span class="eyebrow">Seleção</span>
          <h2>Poemas</h2>
          <p>Momentos que nascem em letras e florescem no coração.</p>
        </div>

        <div class="poem-grid">
          <article class="poem-card hidden">
            <h3>Mar Interior</h3>
            <p>Há mares que vêm para dentro,
onde os barcos não navegam,
mas a alma aprende a flutuar
em silêncio.

Basta fechar os olhos
para ouvir o som das ondas
batendo na margem do peito.</p>
            <div class="author">— Autor Desconhecido</div>
          </article>

          <article class="poem-card hidden">
            <h3>Tempo</h3>
            <p>O tempo não corre,
ele tece.
Fio a fio,
silenciosamente,
veste o mundo
de eternidade.</p>
            <div class="author">— Autor Desconhecido</div>
          </article>

          <article class="poem-card hidden">
            <h3>Luz de Madrugada</h3>
            <p>A madrugada abre as janelas
do coração.
Não há pressa,
apenas o perfume da lua
entre os lençóis do céu.

E o mundo acorda
como quem lembra
o nome do sonho.</p>
            <div class="author">— Autor Desconhecido</div>
          </article>
        </div>
      </div>
    </section>

    <section class="section" id="sobre">
      <div class="container">
        <div class="section-head hidden">
          <span class="eyebrow">Sobre</span>
          <h2>Uma casa para a poesia</h2>
        </div>

        <div class="about-grid">
          <div class="about-card hidden">
            <h3>O que somos</h3>
            <p>
              O Versos e Letras nasceu da vontade de reunir sentimentos em frases delicadas,
              histórias em versos e beleza em cada leitura.
            </p>
            <p>
              Acreditamos que poesia não é só literatura: é um modo de habitar o mundo com
              gentileza, atenção e profundidade.
            </p>
            <p>
              Aqui, cada verso convida a refletir, a sentir e a respirar mais devagar.
            </p>
          </div>

          <div class="quote-card hidden">
            <blockquote>
              “As palavras são as lembranças do coração quando ele não sabe como sorrir.”
            </blockquote>
          </div>
        </div>

        <div class="features">
          <div class="feature-box hidden">
            <h4>Reflexão</h4>
            <p>Versos que provocam pausa, presença e uma leitura mais íntima.</p>
          </div>

          <div class="feature-box hidden">
            <h4>Inspiração</h4>
            <p>Textos que ecoam sentimentos, memórias e sonhos do cotidiano.</p>
          </div>

          <div class="feature-box hidden">
            <h4>Beleza</h4>
            <p>Uma estética elegante para transformar letras em experiência sensível.</p>
          </div>
        </div>
      </div>
    </section>

    <section class="section" id="contato">
      <div class="container">
        <div class="section-head hidden">
          <span class="eyebrow">Contato</span>
          <h2>Fale conosco</h2>
          <p>Se você ama poesia, quer publicar um poema ou trocar ideias, essa é a sua casa.</p>
        </div>

        <div class="contact-grid">
          <div class="contact-card hidden">
            <h3>Vamos conversar</h3>
            <p>
              Estamos abertos a parcerias, poemas enviados, ideias e conversas sobre literatura,
              arte e sentimentos.
            </p>

            <ul class="contact-list">
              <li>
                <strong>E-mail</strong>
                <span>contato@versoseletras.com</span>
              </li>
              <li>
                <strong>Instagram</strong>
                <span>@versoseletras</span>
              </li>
              <li>
                <strong>Local</strong>
                <span>Entre as páginas e os sonhos</span>
              </li>
            </ul>
          </div>

          <div class="form-card hidden">
            <h3>Enviar mensagem</h3>
            <form id="formContato">
              <div class="field">
                <label for="nome">Nome</label>
                <input type="text" id="nome" placeholder="Seu nome" required />
              </div>

              <div class="field">
                <label for="email">E-mail</label>
                <input type="email" id="email" placeholder="seu@email.com" required />
              </div>

              <div class="field">
                <label for="mensagem">Mensagem</label>
                <textarea id="mensagem" placeholder="Escreva sua mensagem..." required></textarea>
              </div>

              <button type="submit" class="btn btn-primary">Enviar</button>
            </form>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer class="site-footer">
    <div class="container">
      <p>© 2026 Versos e Letras. Compartilhando poesia.</p>
    </div>
  </footer>

  <script>
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add("visible");
        }
      });
    }, { threshold: 0.2 });

    document.querySelectorAll(".hidden").forEach(el => observer.observe(el));

    document.getElementById("formContato").addEventListener("submit", function (event) {
      event.preventDefault();

      const nome = document.getElementById("nome").value.trim();
      const email = document.getElementById("email").value.trim();
      const mensagem = document.getElementById("mensagem").value.trim();

      if (!nome || !email || !mensagem) {
        alert("Preencha todos os campos antes de enviar.");
        return;
      }

      alert(`Obrigado, ${nome}! Sua mensagem foi enviada com sucesso.`);
      this.reset();
    });
  </script>
</body>
</html>
