<!DOCTYPE html>
<html lang="pt">
<head>
  <meta charset="UTF-8" />
  <title>Tinkave – Novos Acabamentos Têxteis</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <style>
    :root {
      --bg-dark: #111111;
      --bg-light: #f2f2f2;
      --text-main: #ffffff;
      --text-dark: #222222;
      --accent: #0f3d4c;
      --muted: #888888;
      --max-width: 1100px;
      --font-main: "Lato", system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
      --font-title: "Montserrat", system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
    }

    * { box-sizing: border-box; margin: 0; padding: 0; }

    body {
      font-family: var(--font-main);
      background-color: #ffffff;
      color: var(--text-dark);
      line-height: 1.6;
    }

    header {
      position: sticky;
      top: 0;
      z-index: 100;
      background-color: rgba(17, 17, 17, 0.96);
      color: var(--text-main);
      backdrop-filter: blur(10px);
    }

    .nav-inner {
      max-width: var(--max-width);
      margin: 0 auto;
      padding: 14px 20px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 24px;
    }

    .logo {
      font-family: var(--font-title);
      font-weight: 600;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      font-size: 14px;
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 18px;
      font-size: 14px;
    }

    nav a {
      color: var(--text-main);
      text-decoration: none;
      opacity: 0.85;
    }

    nav a:hover {
      opacity: 1;
    }

    .lang-switch {
      display: flex;
      gap: 8px;
      font-size: 13px;
    }

    .lang-switch button {
      background: transparent;
      border: 1px solid rgba(255, 255, 255, 0.25);
      color: var(--text-main);
      padding: 4px 8px;
      border-radius: 999px;
      cursor: pointer;
      font-size: 12px;
    }

    .lang-switch button.active {
      background-color: var(--accent);
      border-color: var(--accent);
    }

    main {
      max-width: var(--max-width);
      margin: 0 auto;
      padding: 40px 20px 60px;
    }

    section {
      margin-bottom: 60px;
    }

    .hero {
      display: grid;
      grid-template-columns: minmax(0, 1.4fr) minmax(0, 1fr);
      gap: 32px;
      align-items: center;
    }

    .hero-text h1 {
      font-family: var(--font-title);
      font-size: 32px;
      margin-bottom: 10px;
      letter-spacing: 0.04em;
      text-transform: uppercase;
    }

    .hero-text p {
      color: var(--muted);
      max-width: 520px;
      margin-bottom: 20px;
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
    }

    .btn {
      border-radius: 999px;
      padding: 9px 18px;
      font-size: 13px;
      border: 1px solid var(--accent);
      background-color: transparent;
      color: var(--accent);
      cursor: pointer;
    }

    .btn.primary {
      background-color: var(--accent);
      color: #ffffff;
    }

    .hero-image {
      width: 100%;
      aspect-ratio: 4 / 3;
      border-radius: 18px;
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      background-color: #222;
      /* Substituir URL pela imagem AI gerada */
      background-image: url("hero-textile-finish.jpg");
    }

    .section-title {
      font-family: var(--font-title);
      font-size: 22px;
      margin-bottom: 8px;
      text-transform: uppercase;
      letter-spacing: 0.08em;
    }

    .section-subtitle {
      color: var(--muted);
      font-size: 14px;
      margin-bottom: 20px;
    }

    .finish-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 1fr);
      gap: 28px;
      align-items: flex-start;
    }

    .finish-image {
      width: 100%;
      aspect-ratio: 4 / 3;
      border-radius: 16px;
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      background-color: #222;
    }

    .finish-image.crinkle {
      /* Substituir URL pela imagem AI gerada */
      background-image: url("permanent-crinkle-closeup.jpg");
    }

    .finish-image.esmeril {
      /* Substituir URL pela imagem AI gerada */
      background-image: url("carbon-emery-peach-skin-closeup.jpg");
    }

    .finish-text h3 {
      font-family: var(--font-title);
      font-size: 18px;
      margin-bottom: 10px;
    }

    .finish-text p {
      margin-bottom: 14px;
      font-size: 14px;
    }

    .finish-text ul {
      list-style: none;
      padding-left: 0;
      font-size: 14px;
    }

    .finish-text li::before {
      content: "• ";
      color: var(--accent);
    }

    .contact-box {
      background-color: var(--bg-light);
      border-radius: 14px;
      padding: 20px 18px;
      font-size: 14px;
    }

    .contact-box h3 {
      font-family: var(--font-title);
      font-size: 16px;
      margin-bottom: 8px;
    }

    .lang-block {
      display: none;
    }

    .lang-block.active {
      display: block;
    }

    footer {
      border-top: 1px solid #e0e0e0;
      padding: 18px 20px;
      font-size: 12px;
      color: #777;
      text-align: center;
    }

    @media (max-width: 800px) {
      .hero,
      .finish-grid {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>
<header>
  <div class="nav-inner">
    <div class="logo">TINKAVE</div>
    <nav>
      <ul>
        <li><a href="#hero">Home</a></li>
        <li><a href="#crinkle">Permanent Crinkle</a></li>
        <li><a href="#esmeril">Esmeril de Carbono</a></li>
        <li><a href="#contact">Contactos</a></li>
      </ul>
    </nav>
    <div class="lang-switch">
      <button data-lang="pt" class="active">PT</button>
      <button data-lang="en">EN</button>
      <button data-lang="es">ES</button>
      <button data-lang="fr">FR</button>
    </div>
  </div>
</header>

<main>
  <!-- PORTUGUÊS -->
  <div class="lang-block active" id="lang-pt">
    <section id="hero" class="hero">
      <div class="hero-text">
        <h1>Novos Acabamentos Têxteis Tinkave</h1>
        <p>Esmeril de Carbono e Permanent Crinkle: tecnologia, textura e diferenciação para marcas que procuram valor acrescentado.</p>
        <div class="hero-buttons">
          <a href="#crinkle"><button class="btn primary">Permanent Crinkle</button></a>
          <a href="#esmeril"><button class="btn">Esmeril de Carbono</button></a>
        </div>
      </div>
      <div class="hero-image"></div>
    </section>

    <section id="crinkle">
      <h2 class="section-title">Permanent Crinkle</h2>
      <p class="section-subtitle">Textura permanente com identidade própria.</p>
      <div class="finish-grid">
        <div class="finish-text">
          <h3>Textura permanente com identidade própria</h3>
          <p>O Permanent Crinkle é um acabamento têxtil avançado que cria uma textura tridimensional permanente, conferindo ao tecido um aspeto casual, moderno e naturalmente sofisticado. A combinação de tecnologia química e manipulação mecânica controlada garante um efeito duradouro, resistente ao uso e às lavagens.</p>
          <p>Ideal para vestuário e roupa de cama, este acabamento reduz a necessidade de engomar e oferece um visual descontraído e valorizado no mercado.</p>
          <ul>
            <li>Textura permanente e estável</li>
            <li>Aspeto casual premium</li>
            <li>Mantém o efeito após lavagens</li>
            <li>Adequado para bases leves e médias</li>
            <li>Diferenciação imediata do produto final</li>
          </ul>
        </div>
        <div class="finish-image crinkle"></div>
      </div>
    </section>

    <section id="esmeril">
      <h2 class="section-title">Esmeril de Carbono</h2>
      <p class="section-subtitle">Toque premium com aspeto pele de pêssego.</p>
      <div class="finish-grid">
        <div class="finish-text">
          <h3>Toque premium com aspeto pele de pêssego</h3>
          <p>O Esmeril de Carbono é um acabamento têxtil de alta qualidade que confere aos tecidos um toque extremamente suave, com um efeito pele de pêssego uniforme e elegante. A esmerilagem controlada com partículas de carbono cria uma superfície mais macia, fosca e sofisticada, ideal para marcas que procuram um acabamento premium com forte impacto sensorial.</p>
          <p>Com estabilidade e repetibilidade entre lotes, este acabamento eleva o valor percebido do produto final.</p>
          <ul>
            <li>Toque pele de pêssego suave e uniforme</li>
            <li>Aspeto fosco premium</li>
            <li>Ideal para moda e home textiles</li>
            <li>Processo estável e repetível</li>
            <li>Valor acrescentado imediato</li>
          </ul>
        </div>
        <div class="finish-image esmeril"></div>
      </div>
    </section>

    <section id="contact">
      <h2 class="section-title">Contactos</h2>
      <div class="contact-box">
        <h3>Tinkave – Acabamentos Ponte de Serves, Lda</h3>
        <p>Rua da Ponta do Campo, 193<br>
           4835-340 Selho São Jorge, Guimarães – Portugal</p>
        <p>Tel: +351 252 987 364 / 366<br>
           Email: geral@tinkave.pt</p>
      </div>
    </section>
  </div>

  <!-- ENGLISH -->
  <div class="lang-block" id="lang-en">
    <section class="hero">
      <div class="hero-text">
        <h1>New Textile Finishes by Tinkave</h1>
        <p>Carbon Emery Finish and Permanent Crinkle: technology, texture and differentiation for brands seeking added value.</p>
        <div class="hero-buttons">
          <a href="#crinkle"><button class="btn primary">Permanent Crinkle</button></a>
          <a href="#esmeril"><button class="btn">Carbon Emery Finish</button></a>
        </div>
      </div>
      <div class="hero-image"></div>
    </section>

    <section>
      <h2 class="section-title">Permanent Crinkle</h2>
      <p class="section-subtitle">Permanent texture with a unique identity.</p>
      <div class="finish-grid">
        <div class="finish-text">
          <h3>Permanent texture with a unique identity</h3>
          <p>Permanent Crinkle is an advanced textile finish that creates a permanent three-dimensional texture, giving fabrics a casual, modern and naturally sophisticated look. Through a combination of chemical fixation and controlled mechanical manipulation, the effect remains stable, durable and resistant to repeated washing.</p>
          <p>Ideal for apparel and home textiles, this finish reduces the need for ironing and delivers a relaxed, contemporary appearance highly valued in today’s market.</p>
          <ul>
            <li>Permanent and stable texture</li>
            <li>Premium casual appearance</li>
            <li>Maintains the effect after washing</li>
            <li>Suitable for light and medium-weight fabrics</li>
            <li>Immediate product differentiation</li>
          </ul>
        </div>
        <div class="finish-image crinkle"></div>
      </div>
    </section>

    <section>
      <h2 class="section-title">Carbon Emery Finish</h2>
      <p class="section-subtitle">Premium soft touch with a peach-skin effect.</p>
      <div class="finish-grid">
        <div class="finish-text">
          <h3>Premium soft touch with a peach-skin effect</h3>
          <p>The Carbon Emery Finish is a high-quality textile treatment that gives fabrics an exceptionally soft touch with a uniform, elegant peach-skin effect. Controlled carbon-particle sanding creates a smoother, matte and more sophisticated surface, ideal for brands seeking a premium finish with strong sensory appeal.</p>
          <p>With excellent stability and batch-to-batch consistency, this finish enhances the perceived value of the final product.</p>
          <ul>
            <li>Soft and uniform peach-skin touch</li>
            <li>Premium matte appearance</li>
            <li>Ideal for fashion and home textiles</li>
            <li>Stable and repeatable process</li>
            <li>Immediate added value</li>
          </ul>
        </div>
        <div class="finish-image esmeril"></div>
      </div>
    </section>

    <section>
      <h2 class="section-title">Contacts</h2>
      <div class="contact-box">
        <h3>Tinkave – Acabamentos Ponte de Serves, Lda</h3>
        <p>Rua da Ponta do Campo, 193<br>
           4835-340 Selho São Jorge, Guimarães – Portugal</p>
        <p>Tel: +351 252 987 364 / 366<br>
           Email: geral@tinkave.pt</p>
      </div>
    </section>
  </div>

  <!-- ESPAÑOL -->
  <div class="lang-block" id="lang-es">
    <section class="hero">
      <div class="hero-text">
        <h1>Novedades en Acabados Textiles</h1>
        <p>Esmeril de Carbono y Permanent Crinkle: tecnología, textura y valor añadido para marcas que buscan diferenciación.</p>
        <div class="hero-buttons">
          <a href="#crinkle"><button class="btn primary">Permanent Crinkle</button></a>
          <a href="#esmeril"><button class="btn">Esmeril de Carbono</button></a>
        </div>
      </div>
      <div class="hero-image"></div>
    </section>

    <section>
      <h2 class="section-title">Permanent Crinkle</h2>
      <p class="section-subtitle">Textura permanente con identidad propia.</p>
      <div class="finish-grid">
        <div class="finish-text">
          <h3>Textura permanente con identidad propia</h3>
          <p>Permanent Crinkle es un acabado textil avanzado que crea una textura tridimensional permanente, aportando al tejido un aspecto casual, moderno y naturalmente sofisticado. Gracias a la combinación de fijación química y manipulación mecánica controlada, el efecto se mantiene estable, duradero y resistente a los lavados.</p>
          <p>Ideal para moda y ropa de cama, este acabado reduce la necesidad de planchado y ofrece un aspecto relajado muy apreciado en el mercado actual.</p>
          <ul>
            <li>Textura permanente y estable</li>
            <li>Aspecto casual premium</li>
            <li>Mantiene el efecto tras los lavados</li>
            <li>Adecuado para bases ligeras y medias</li>
            <li>Diferenciación inmediata del producto</li>
          </ul>
        </div>
        <div class="finish-image crinkle"></div>
      </div>
    </section>

    <section>
      <h2 class="section-title">Esmeril de Carbono</h2>
      <p class="section-subtitle">Tacto premium con efecto piel de melocotón.</p>
      <div class="finish-grid">
        <div class="finish-text">
          <h3>Tacto premium con efecto piel de melocotón</h3>
          <p>El Esmeril de Carbono es un acabado textil de alta calidad que aporta a los tejidos un tacto extremadamente suave, con un efecto piel de melocotón uniforme y elegante. El proceso de esmerilado controlado con partículas de carbono crea una superficie más suave, mate y sofisticada, ideal para marcas que buscan un acabado premium con fuerte impacto sensorial.</p>
          <p>Con gran estabilidad y repetibilidad entre lotes, este acabado aumenta el valor percibido del producto final.</p>
          <ul>
            <li>Tacto piel de melocotón suave y uniforme</li>
            <li>Aspecto mate premium</li>
            <li>Ideal para moda y hogar</li>
            <li>Proceso estable y repetible</li>
            <li>Valor añadido inmediato</li>
          </ul>
        </div>
        <div class="finish-image esmeril"></div>
      </div>
    </section>

    <section>
      <h2 class="section-title">Contactos</h2>
      <div class="contact-box">
        <h3>Tinkave – Acabados Ponte de Serves, Lda</h3>
        <p>Rua da Ponta do Campo, 193<br>
           4835-340 Selho São Jorge, Guimarães – Portugal</p>
        <p>Tel: +351 252 987 364 / 366<br>
           Email: geral@tinkave.pt</p>
      </div>
    </section>
  </div>

  <!-- FRANÇAIS -->
  <div class="lang-block" id="lang-fr">
    <section class="hero">
      <div class="hero-text">
        <h1>Nouvelles Finitions Textiles Tinkave</h1>
        <p>Émeri de Carbone et Permanent Crinkle : technologie, texture et valeur ajoutée pour les marques exigeantes.</p>
        <div class="hero-buttons">
          <a href="#crinkle"><button class="btn primary">Permanent Crinkle</button></a>
          <a href="#esmeril"><button class="btn">Émeri de Carbone</button></a>
        </div>
      </div>
      <div class="hero-image"></div>
    </section>

    <section>
      <h2 class="section-title">Permanent Crinkle</h2>
      <p class="section-subtitle">Texture permanente avec identité propre.</p>
      <div class="finish-grid">
        <div class="finish-text">
          <h3>Texture permanente avec identité propre</h3>
          <p>Permanent Crinkle est une finition textile avancée qui crée une texture tridimensionnelle permanente, donnant au tissu un aspect casual, moderne et naturellement sophistiqué. Grâce à la combinaison de fixation chimique et de manipulation mécanique contrôlée, l’effet reste stable, durable et résistant aux lavages répétés.</p>
          <p>Idéale pour l’habillement et le linge de lit, cette finition réduit le besoin de repassage et offre un look décontracté très apprécié sur le marché.</p>
          <ul>
            <li>Texture permanente et stable</li>
            <li>Aspect casual premium</li>
            <li>Effet durable après lavage</li>
            <li>Adapté aux bases légères et moyennes</li>
            <li>Différenciation immédiate du produit</li>
          </ul>
        </div>
        <div class="finish-image crinkle"></div>
      </div>
    </section>

    <section>
      <h2 class="section-title">Émeri de Carbone</h2>
      <p class="section-subtitle">Toucher premium avec effet peau de pêche.</p>
      <div class="finish-grid">
        <div class="finish-text">
          <h3>Toucher premium avec effet peau de pêche</h3>
          <p>L’Émeri de Carbone est une finition textile de haute qualité qui offre aux tissus un toucher extrêmement doux, avec un effet peau de pêche uniforme et élégant. Le ponçage contrôlé avec particules de carbone crée une surface plus douce, mate et sophistiquée, idéale pour les marques recherchant une finition premium à fort impact sensoriel.</p>
          <p>Grâce à sa stabilité et à sa répétabilité entre lots, cette finition valorise immédiatement le produit final.</p>
          <ul>
            <li>Toucher peau de pêche doux et uniforme</li>
            <li>Aspect mat premium</li>
            <li>Idéal pour mode et linge de maison</li>
            <li>Processus stable et reproductible</li>
            <li>Valeur ajoutée immédiate</li>
          </ul>
        </div>
        <div class="finish-image esmeril"></div>
      </div>
    </section>

    <section>
      <h2 class="section-title">Contacts</h2>
      <div class="contact-box">
        <h3>Tinkave – Acabamentos Ponte de Serves, Lda</h3>
        <p>Rua da Ponta do Campo, 193<br>
           4835-340 Selho São Jorge, Guimarães – Portugal</p>
        <p>Tel: +351 252 987 364 / 366<br>
           Email: geral@tinkave.pt</p>
      </div>
    </section>
  </div>
</main>

<footer>
  © Tinkave – Acabamentos Têxteis. All rights reserved.
</footer>

<script>
  const buttons = document.querySelectorAll(".lang-switch button");
  const blocks = document.querySelectorAll(".lang-block");

  buttons.forEach(btn => {
    btn.addEventListener("click", () => {
      const lang = btn.dataset.lang;
      buttons.forEach(b => b.classList.remove("active"));
      btn.classList.add("active");
      blocks.forEach(block => {
        block.classList.toggle("active", block.id === "lang-" + lang);
      });
      document.documentElement.lang = lang;
    });
  });
</script>
</body>
</html>
