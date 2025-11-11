<!--
SCARO - Single-file website (index.html)
Instructions:
1) Place this file as `index.html` in the root of a GitHub Pages repository named `scaro.info` (or any repo and enable Pages).
2) Add assets to the repo root or change paths below:
   - LOGO_SCARO_WHITE.png  (used in header)
   - LOGO_SCARO_BLACK.png  (optional alternative)
   - hero.jpg (poster image for hero)
   - gallery images (gallery1.jpg, gallery2.jpg...)
3) Video: we included an embedded Google Drive preview. If you want autoplay background, use a hosted MP4 and update the <video> source.
4) Edit contact details, dates, social links in the `data` object inside the <script> section.

This single-file site is responsive, uses Google Fonts, and follows the graphic charter provided (colors, fonts, accents).
-->

<!doctype html>
<html lang="fr">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Scaro — Duo père/fils | Chanson urbaine & Variété française</title>
  <meta name="description" content="Scaro — duo père/fils qui mêle chanson urbaine et variété française. Engagement climatique, justice sociale et énergie scénique." />
  <link rel="icon" href="LOGO_SCARO_WHITE.png" />

  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@600;800&family=Open+Sans:wght@300;400;600&family=Playfair+Display:ital,wght@0,400;1,400&family=Raleway:wght@500&display=swap" rel="stylesheet">

  <style>
    :root{
      --black:#0B0B0B;
      --white:#F4F4F4;
      --accent:#F4C542; /* safran */
      --green:#3E7C6E;
      --red:#C4452F;
      --maxwidth:1100px;
    }
    *{box-sizing:border-box}
    body{margin:0;font-family:'Open Sans',system-ui,Arial;background:var(--white);color:var(--black);-webkit-font-smoothing:antialiased}
    a{color:inherit;text-decoration:none}

    header{background:linear-gradient(180deg, rgba(11,11,11,0.95), rgba(11,11,11,0.85));position:sticky;top:0;z-index:40}
    .nav-inner{max-width:var(--maxwidth);margin:0 auto;display:flex;align-items:center;justify-content:space-between;padding:12px}
    .logo{display:flex;align-items:center;gap:12px}
    .logo img{height:46px}
    nav ul{display:flex;gap:18px;list-style:none;margin:0;padding:0}
    nav a{color:var(--white);font-weight:600}
    .cta{background:var(--accent);color:var(--black);padding:8px 14px;border-radius:12px;font-weight:700}

    .hero{position:relative;min-height:72vh;display:flex;align-items:center;}
    .hero-inner{max-width:var(--maxwidth);margin:0 auto;padding:48px;display:grid;grid-template-columns:1fr 420px;gap:32px;align-items:center}
    .hero h1{font-family:'Montserrat',sans-serif;font-size:40px;color:var(--white);margin:0 0 12px}
    .hero p{color:var(--white);margin:0 0 18px;font-size:16px}
    .hero .buttons{display:flex;gap:12px}
    .btn{display:inline-block;padding:10px 16px;border-radius:10px;font-weight:700}
    .btn-outline{background:transparent;border:2px solid var(--white);color:var(--white)}
    .btn-primary{background:var(--accent);color:var(--black)}

    .hero-media{background:rgba(255,255,255,0.02);border-radius:12px;overflow:hidden;box-shadow:0 8px 30px rgba(0,0,0,0.5)}
    .hero-media iframe{width:100%;height:100%;min-height:320px;border:0}

    main{max-width:var(--maxwidth);margin:36px auto;padding:0 18px}

    .section{padding:36px 0;border-top:1px solid rgba(0,0,0,0.06)}
    .section h2{font-family:'Montserrat';font-size:22px;margin:0 0 10px}
    .about-grid{display:grid;grid-template-columns:1fr 320px;gap:20px;align-items:start}
    .card{background:linear-gradient(180deg, #fff, #fbfbfb);padding:18px;border-radius:10px;box-shadow:0 8px 20px rgba(0,0,0,0.04)}

    .tags{display:flex;gap:8px;flex-wrap:wrap}
    .tag{background:var(--black);color:var(--accent);padding:6px 10px;border-radius:20px;font-weight:700;font-size:13px}

    .gallery{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:12px}
    .gallery img{width:100%;height:200px;object-fit:cover;border-radius:8px}

    .dates{display:flex;flex-direction:column;gap:14px}
    .date-item{display:flex;justify-content:space-between;align-items:center;padding:12px;border-radius:8px;background:linear-gradient(180deg,#fff,#f7f7f7)}

    footer{background:var(--black);color:var(--white);padding:28px 18px;margin-top:48px}
    .footer-inner{max-width:var(--maxwidth);margin:0 auto;display:flex;justify-content:space-between;gap:20px;align-items:center}
    .social a{margin-right:12px;color:var(--white);font-weight:700}

    /* Responsive */
    @media (max-width:900px){
      .hero-inner{grid-template-columns:1fr;}
      nav ul{display:none}
    }

    /* Small helpers */
    .muted{color:#6b6b6b}
    blockquote{font-family:'Playfair Display',serif;font-style:italic;font-size:18px;margin:12px 0;padding-left:10px;border-left:4px solid var(--accent)}
  </style>
</head>
<body>

<header>
  <div class="nav-inner">
    <div class="logo">
      <img src="LOGO_SCARO_WHITE.png" alt="Scaro logo" />
      <div style="color:var(--white)"><strong>Scaro</strong><div style="font-size:12px;color:rgba(255,255,255,0.7)">Duo père / fils</div></div>
    </div>
    <nav>
      <ul>
        <li><a href="#about">À propos</a></li>
        <li><a href="#music">Musique</a></li>
        <li><a href="#live">Live</a></li>
        <li><a href="#gallery">Galerie</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
    <a class="cta" href="#contact">Book & Press</a>
  </div>
</header>

<section class="hero" style="background:linear-gradient(180deg, rgba(3,3,3,0.8), rgba(3,3,3,0.45)), url('hero.jpg') center/cover no-repeat">
  <div class="hero-inner">
    <div>
      <h1>Scaro — Duo père / fils</h1>
      <p>Entre <strong>chanson urbaine</strong> et <strong>variété française</strong>, des textes qui questionnent notre rapport au monde, à soi et aux autres. Urgence climatique, justice sociale — mais toujours l’envie de partager et de danser.</p>
      <div class="buttons">
        <a class="btn btn-primary" href="#live">Voir la tournée</a>
        <a class="btn btn-outline" href="#music">Écouter</a>
      </div>

      <div style="margin-top:18px">
        <blockquote>“Une complicité père/fils qui fait vibrer toute la salle.”</blockquote>
      </div>
    </div>

    <div class="hero-media card">
      <!-- Google Drive preview (replace ID with your file ID). File ID used below from provided link: 1wANZgkITxju4rkMNBx6l8TEOo344P0jC -->
      <iframe src="https://drive.google.com/file/d/1wANZgkITxju4rkMNBx6l8TEOo344P0jC/preview" allow="autoplay; encrypted-media"></iframe>
    </div>
  </div>
</section>

<main>
  <section id="about" class="section">
    <div style="display:flex;justify-content:space-between;align-items:flex-start;gap:20px;max-width:var(--maxwidth);margin:0 auto;padding:0 18px;">
      <div style="flex:1">
        <h2>À propos</h2>
        <p><strong>Scaro</strong> est un duo père/fils qui fait se rencontrer la <strong>chanson urbaine</strong> et la <strong>variété française</strong>. Leur écriture interroge notre rapport au monde, à soi et à l'autre, et met en lumière des thèmes tels que l'<strong>urgence climatique</strong> et la <strong>justice sociale</strong>.</p>
        <p>Sur scène, Scaro propose un live festif, chaleureux et engagé — une expérience où le public est invité à chanter, danser, réfléchir et partager.</p>

        <div style="margin-top:12px" class="tags">
          <div class="tag">Chanson Urbaine</div>
          <div class="tag">Variété Française</div>
          <div class="tag">Écologie</div>
          <div class="tag">Justice Sociale</div>
          <div class="tag">Live Énergétique</div>
        </div>
      </div>

      <aside style="width:320px">
        <div class="card">
          <h3 style="margin-top:0">Fiche rapide</h3>
          <p><strong>Formation :</strong> Duo père / fils</p>
          <p><strong>Style :</strong> Chanson urbaine / Variété</p>
          <p><strong>Live :</strong> Festif, engagé, énergique</p>
          <p><strong>Contacts :</strong><br><a href="mailto:booking@scaro.info">booking@scaro.info</a></p>
        </div>
      </aside>
    </div>
  </section>

  <section id="music" class="section">
    <h2>Musique & Vidéos</h2>
    <div style="display:flex;gap:18px;flex-wrap:wrap;align-items:flex-start">
      <div style="flex:1;min-width:320px" class="card">
        <h3 style="margin-top:0">Derniers morceaux</h3>
        <p>Des titres qui mêlent sens et rythmes — focalisés aujourd'hui sur l'urgence climatique et la justice. (Ajoute ici les liens SoundCloud / YouTube / Bandcamp quand prêts.)</p>
        <div style="margin-top:12px">
          <a class="btn btn-primary" href="#" onclick="alert('Ajoute les liens de streaming dans le fichier index.html')">Écouter / Streaming</a>
        </div>
      </div>

      <div style="width:420px;min-width:300px" class="card">
        <h4 style="margin-top:0">Clip live</h4>
        <!-- If you prefer a modal player, we open the drive link in a new tab -->
        <a href="https://drive.google.com/file/d/1wANZgkITxju4rkMNBx6l8TEOo344P0jC/view?usp=drive_link" target="_blank" class="btn btn-outline">Voir la vidéo</a>
      </div>
    </div>
  </section>

  <section id="live" class="section">
    <h2>Live & Tournée</h2>
    <div class="dates card">
      <!-- Dates data injected by script -->
      <div id="dates-list"></div>
    </div>
  </section>

  <section id="gallery" class="section">
    <h2>Galerie</h2>
    <div class="gallery" id="gallery-grid">
      <!-- drop images named gallery1.jpg, gallery2.jpg... into repo -->
      <img src="gallery1.jpg" alt="live 1" onerror="this.src='hero.jpg'" />
      <img src="gallery2.jpg" alt="live 2" onerror="this.src='hero.jpg'" />
      <img src="gallery3.jpg" alt="coulisses" onerror="this.src='hero.jpg'" />
      <img src="gallery4.jpg" alt="public" onerror="this.src='hero.jpg'" />
    </div>
  </section>

  <section id="press" class="section">
    <h2>Presse & Témoignages</h2>
    <div class="card">
      <p>Extraits de retours du public :</p>
      <ul>
        <li>"Une vraie claque d'énergie et d'émotion !"</li>
        <li>"Une complicité père/fils qui fait vibrer toute la salle."</li>
        <li>"Impossible de rester assis, l'énergie est contagieuse !"</li>
      </ul>
      <p style="margin-top:12px">Pour recevoir le dossier presse (PDF) : <a href="mailto:press@scaro.info?subject=Demande%20dossier%20presse">press@scaro.info</a></p>
    </div>
  </section>

  <section id="contact" class="section">
    <h2>Contact & Booking</h2>
    <div style="display:grid;grid-template-columns:1fr 320px;gap:20px;align-items:start">
      <div class="card">
        <h3 style="margin-top:0">Booking & Press</h3>
        <p>Pour toute demande de booking, interview ou presse, écris-nous :</p>
        <p><strong>booking@scaro.info</strong></p>
        <p>Tu peux aussi utiliser le formulaire ci-dessous pour envoyer un message rapidement.</p>

        <form id="contact-form">
          <div style="display:flex;gap:8px;margin-bottom:8px">
            <input name="name" placeholder="Ton nom" style="flex:1;padding:10px;border-radius:6px;border:1px solid #ddd" required />
          </div>
          <div style="display:flex;gap:8px;margin-bottom:8px">
            <input name="email" placeholder="Ton email" style="flex:1;padding:10px;border-radius:6px;border:1px solid #ddd" required />
          </div>
          <textarea name="message" placeholder="Ton message" style="width:100%;padding:10px;border-radius:6px;border:1px solid #ddd;height:120px" required></textarea>
          <div style="margin-top:10px"><button class="btn btn-primary" type="submit">Envoyer</button></div>
        </form>
        <p id="form-status" class="muted" style="margin-top:10px"></p>
      </div>

      <aside class="card">
        <h4 style="margin-top:0">Infos utiles</h4>
        <p><strong>Line-up :</strong> Duo père / fils</p>
        <p><strong>Durée live :</strong> 45 - 90 mins (configurable)</p>
        <p><strong>Rider :</strong> Disponible sur demande</p>
        <p><strong>Contact :</strong><br><a href="mailto:booking@scaro.info">booking@scaro.info</a></p>
      </aside>
    </div>
  </section>
</main>

<footer>
  <div class="footer-inner">
    <div>
      <img src="LOGO_SCARO_WHITE.png" alt="Scaro" style="height:40px;margin-bottom:6px" />
      <div class="muted" style="font-size:13px">© Scaro — Duo père/fils</div>
    </div>
    <div style="text-align:right">
      <div class="social">
        <a href="#">Instagram</a>
        <a href="#">Facebook</a>
        <a href="#">YouTube</a>
      </div>
      <div style="margin-top:6px;font-size:13px">Made with ❤ — Scaro</div>
    </div>
  </div>
</footer>

<script>
// Editable data: update shows/dates and contact info here
const data = {
  dates: [
    {date:'2026-06-15', city:'Nantes', venue:'Voyage à Nantes - Scène Principale', info:'Festival'},
    {date:'2026-07-02', city:'Rennes', venue:'La Carrière', info:'Concert'}
  ],
  contactEmail:'booking@scaro.info'
}

function renderDates(){
  const list = document.getElementById('dates-list');
  list.innerHTML = '';
  data.dates.forEach(d=>{
    const el = document.createElement('div');
    el.className = 'date-item';
    el.innerHTML = `<div><strong>${d.date}</strong><div class="muted">${d.city} — ${d.venue}</div></div><div class="muted">${d.info}</div>`;
    list.appendChild(el);
  })
}
renderDates();

// Contact form: simple mailto fallback
const form = document.getElementById('contact-form');
form.addEventListener('submit', (e)=>{
  e.preventDefault();
  const f = new FormData(form);
  const name = f.get('name');
  const email = f.get('email');
  const message = f.get('message');
  const subject = encodeURIComponent('Contact depuis site Scaro — ' + name);
  const body = encodeURIComponent(`Nom: ${name}\nEmail: ${email}\n\n${message}`);
  const mailto = `mailto:${data.contactEmail}?subject=${subject}&body=${body}`;
  window.location.href = mailto;
  document.getElementById('form-status').textContent = 'Votre client mail devrait s'ouvrir pour envoyer le message.';
})

</script>

</body>
</html>
