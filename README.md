<!DOCTYPE html>
<html lang="sk">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>StavV2 – Stavebná firma Trenčín</title>
  <meta name="description" content="StavV2 – stavebná firma v Trenčíne. Stavba domov, zateplenie fasád, obklady a dlažby. Kontakt: stavv2@hotmail.com" />

  <style>
    :root{
      --bg:#070b16;
      --card:#0f1730;
      --card2:#0c1226;
      --text:#eef4ff;
      --muted:#b9c7e6;
      --accent:#3b82f6;
      --accent2:#22c55e;
      --border:rgba(255,255,255,.10);
      --shadow:0 18px 60px rgba(0,0,0,.35);
      --radius:22px;
    }
    *{box-sizing:border-box;margin:0;padding:0;font-family:system-ui,-apple-system,Segoe UI,Roboto,Arial,sans-serif}
    body{
      background:radial-gradient(900px 400px at 20% 0%, rgba(59,130,246,.20), transparent 55%),
                 radial-gradient(900px 400px at 80% 10%, rgba(34,197,94,.18), transparent 60%),
                 linear-gradient(120deg,#070b16,#0b1430);
      color:var(--text);
    }
    a{color:inherit;text-decoration:none}
    .container{max-width:1150px;margin:0 auto;padding:22px}
    header{
      display:flex;align-items:center;justify-content:space-between;gap:14px;
      padding:14px 0; position:sticky; top:0; z-index:50;
      backdrop-filter: blur(10px);
      background:rgba(7,11,22,.75);
      border-bottom:1px solid var(--border);
    }
    .logo{display:flex;gap:12px;align-items:center}
    .logo-badge{
      width:46px;height:46px;border-radius:14px;
      background:linear-gradient(135deg,var(--accent),#8b5cf6);
      display:grid;place-items:center;font-weight:900;
      box-shadow:0 14px 40px rgba(59,130,246,.25);
      letter-spacing:.5px;
    }
    .logo-title{font-weight:900;font-size:16px}
    .logo-sub{font-size:12.5px;color:var(--muted);margin-top:2px}
    nav{display:flex;gap:16px;flex-wrap:wrap;align-items:center}
    nav a{color:var(--muted);font-weight:700;font-size:14px}
    nav a:hover{color:var(--text)}
    .right-tools{display:flex;gap:10px;align-items:center;flex-wrap:wrap}
    .btn{
      display:inline-flex;align-items:center;justify-content:center;gap:8px;
      padding:12px 14px;border-radius:16px;border:1px solid var(--border);
      background:rgba(255,255,255,.04); color:var(--text); font-weight:800;
      transition:.2s;
      cursor:pointer;
    }
    .btn:hover{transform:translateY(-1px);border-color:rgba(255,255,255,.22)}
    .btn.primary{background:linear-gradient(135deg,var(--accent),#2563eb);border:none}
    .btn.green{background:linear-gradient(135deg,var(--accent2),#16a34a);border:none}
    .btn.small{padding:10px 12px;border-radius:14px;font-size:13px}
    .lang{
      display:inline-flex;gap:6px;align-items:center;
      padding:8px;border-radius:16px;border:1px solid var(--border);
      background:rgba(255,255,255,.03);
    }
    .lang button{
      border:none;background:transparent;color:var(--muted);
      padding:8px 10px;border-radius:12px;font-weight:900;cursor:pointer;
    }
    .lang button.active{background:rgba(59,130,246,.20);color:var(--text)}
    .hero{padding:44px 0 18px}
    .hero-grid{display:grid;grid-template-columns:1.15fr .85fr;gap:16px;align-items:stretch}
    .card{
      background:rgba(15,23,48,.86);
      border:1px solid var(--border);
      border-radius:var(--radius);
      padding:22px;
      box-shadow:var(--shadow);
    }
    .card.soft{background:rgba(12,18,38,.78)}
    h1{font-size:44px;line-height:1.08;margin-bottom:12px}
    .lead{color:var(--muted);font-size:16.5px;line-height:1.65;margin-bottom:16px}
    .pill-row{display:flex;gap:10px;flex-wrap:wrap;margin:16px 0}
    .pill{
      padding:10px 12px;border-radius:999px;border:1px solid var(--border);
      color:var(--muted);font-weight:800;font-size:13px;background:rgba(255,255,255,.03)
    }
    .cta-row{display:flex;gap:10px;flex-wrap:wrap;margin-top:14px}
    .mini{display:grid;gap:10px;grid-template-columns:1fr 1fr;margin-top:12px}
    .stat{
      padding:14px;border-radius:18px;border:1px solid var(--border);
      background:rgba(255,255,255,.03)
    }
    .stat b{font-size:15px}
    .stat span{display:block;color:var(--muted);margin-top:6px;font-size:12.5px;line-height:1.4}
    .section{padding:26px 0}
    .section h2{font-size:28px;margin-bottom:10px}
    .section p{color:var(--muted);line-height:1.75}
    .grid3{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;margin-top:14px}
    .service h3{font-size:18px;margin-bottom:8px}
    .service p{font-size:14px}
    .badge{
      display:inline-block;margin-bottom:10px;
      padding:8px 10px;border-radius:12px;
      background:rgba(34,197,94,.12);
      border:1px solid rgba(34,197,94,.25);
      color:#b7f7cf;font-weight:900;font-size:12px
    }

    .gallery{
      display:grid;
      grid-template-columns:repeat(3, 1fr);
      gap:12px;
      margin-top:14px;
    }
    .photo{
      position:relative;
      border-radius:18px;
      overflow:hidden;
      border:1px solid var(--border);
      background:rgba(255,255,255,.03);
      min-height:160px;
      cursor:pointer;
      transition:.2s;
    }
    .photo:hover{transform:translateY(-2px);border-color:rgba(255,255,255,.22)}
    .photo img{
      width:100%;
      height:100%;
      object-fit:cover;
      display:block;
      filter:saturate(1.05);
    }
    .photo .label{
      position:absolute;left:12px;bottom:12px;
      padding:8px 10px;border-radius:14px;
      background:rgba(0,0,0,.45);
      border:1px solid rgba(255,255,255,.18);
      font-weight:900;font-size:12px;
      backdrop-filter: blur(8px);
    }

    .contact-grid{display:grid;grid-template-columns:1fr 1fr;gap:14px;margin-top:14px}
    .contact-item{padding:16px;border-radius:18px;border:1px solid var(--border);background:rgba(255,255,255,.03)}
    .input{
      width:100%;
      padding:12px 14px;
      border-radius:16px;
      border:1px solid var(--border);
      background:rgba(255,255,255,.03);
      color:var(--text);
      outline:none;
      font-weight:700;
    }
    textarea.input{min-height:110px;resize:vertical}
    .hint{font-size:12.5px;color:var(--muted);margin-top:8px;line-height:1.45}
    .kpi{
      display:grid;grid-template-columns:repeat(4,1fr);
      gap:12px;margin-top:14px;
    }
    .kpi .box{
      padding:16px;border-radius:18px;border:1px solid var(--border);
      background:rgba(255,255,255,.03)
    }
    .kpi .box b{font-size:18px}
    .kpi .box span{display:block;margin-top:6px;color:var(--muted);font-size:12.5px;line-height:1.35}

    footer{padding:22px 0;color:var(--muted);border-top:1px solid var(--border);margin-top:28px}
    .small{font-size:13px;color:var(--muted)}
    .modal{
      position:fixed;inset:0;display:none;align-items:center;justify-content:center;
      background:rgba(0,0,0,.62);z-index:100;
      padding:18px;
    }
    .modal.open{display:flex}
    .modal-content{
      width:min(920px, 100%);
      border-radius:22px;
      border:1px solid rgba(255,255,255,.16);
      overflow:hidden;
      background:rgba(10,15,28,.95);
      box-shadow:0 30px 90px rgba(0,0,0,.55);
    }
    .modal-top{
      display:flex;align-items:center;justify-content:space-between;
      padding:12px 14px;border-bottom:1px solid rgba(255,255,255,.10)
    }
    .modal-top b{font-size:14px}
    .modal-close{
      border:none;background:rgba(255,255,255,.06);
      color:var(--text);font-weight:900;border-radius:14px;
      padding:10px 12px;cursor:pointer
    }
    .modal-img{width:100%;height:auto;display:block;max-height:70vh;object-fit:contain;background:#000}

    .floating{
      position:fixed;right:16px;bottom:16px;display:flex;flex-direction:column;gap:10px;
      z-index:80;
    }
    .fab{
      display:flex;align-items:center;justify-content:center;
      width:54px;height:54px;border-radius:18px;
      border:1px solid rgba(255,255,255,.16);
      background:rgba(255,255,255,.06);
      box-shadow:0 18px 50px rgba(0,0,0,.45);
      transition:.2s;
      font-weight:900;
    }
    .fab:hover{transform:translateY(-2px);border-color:rgba(255,255,255,.25)}
    .fab.whatsapp{background:linear-gradient(135deg, rgba(34,197,94,.95), rgba(22,163,74,.95));border:none}
    .fab.viber{background:linear-gradient(135deg, rgba(139,92,246,.95), rgba(99,102,241,.95));border:none}

    @media (max-width: 980px){
      .hero-grid{grid-template-columns:1fr}
      .grid3{grid-template-columns:1fr}
      .gallery{grid-template-columns:1fr}
      .contact-grid{grid-template-columns:1fr}
      .kpi{grid-template-columns:1fr 1fr}
      h1{font-size:36px}
      nav{display:none}
    }
  </style>
</head>

<body>
  <div class="container">
    <header>
      <div class="logo">
        <div class="logo-badge">V2</div>
        <div>
          <div class="logo-title">StavV2</div>
          <div class="logo-sub" data-i18n="subtitle">Stavebná firma • Trenčín, Slovensko</div>
        </div>
      </div>

      <div class="right-tools">
        <div class="lang" title="Jazyk / Мова">
          <button id="lang-sk" class="active">SK</button>
          <button id="lang-ua">UA</button>
        </div>
        <a class="btn primary" href="#kontakt" data-i18n="get_offer">Cenová ponuka</a>
      </div>
    </header>

    <section class="hero" id="top">
      <div class="hero-grid">
        <div class="card">
          <div class="badge" data-i18n="badge">Spoľahlivo • Kvalitne • Na čas</div>
          <h1 data-i18n="h1">Stavby, fasády a obklady v Trenčíne</h1>
          <p class="lead" data-i18n="lead">
            Sme stavebná firma pôsobiaca v meste Trenčín a okolí.
            Zabezpečujeme výstavbu rodinných domov, zateplenie fasád a pokládku dlažby a obkladov.
            Pracujeme čisto, precízne a férovo.
          </p>

          <div class="pill-row">
            <div class="pill" data-i18n="pill1">Rodinné domy</div>
            <div class="pill" data-i18n="pill2">Zateplenie fasád</div>
            <div class="pill" data-i18n="pill3">Obklady a dlažby</div>
            <div class="pill" data-i18n="pill4">Trenčín a okolie</div>
          </div>

          <div class="cta-row">
            <a class="btn primary" href="#kontakt" data-i18n="cta1">Získať cenovú ponuku</a>
            <a class="btn" href="#realizacie" data-i18n="cta2">Pozrieť realizácie</a>
            <a class="btn green" href="mailto:stavv2@hotmail.com?subject=Dopyt%20-%20StavV2" data-i18n="cta3">Napísať e-mail</a>
          </div>

          <div class="mini">
            <div class="stat">
              <b data-i18n="stat1t">✔ Individuálny prístup</b>
              <span data-i18n="stat1d">Poradíme a navrhneme riešenie</span>
            </div>
            <div class="stat">
              <b data-i18n="stat2t">✔ Kvalitné prevedenie</b>
              <span data-i18n="stat2d">Dôraz na detail a čistú prácu</span>
            </div>
          </div>
        </div>

        <div class="card soft">
          <h2 style="font-size:22px;margin-bottom:10px" data-i18n="what_title">Čo robíme</h2>
          <p class="lead" style="font-size:15px" data-i18n="what_desc">
            Kompletné stavebné práce od základov až po finálne dokončenie.
          </p>

          <div style="display:grid;gap:12px;margin-top:14px">
            <div class="contact-item">
              <b data-i18n="w1t">🏠 Výstavba domov</b>
              <div class="small" data-i18n="w1d">Hrubá stavba, murovanie, dokončovacie práce</div>
            </div>
            <div class="contact-item">
              <b data-i18n="w2t">🧱 Zateplenie fasád</b>
              <div class="small" data-i18n="w2d">Izolácia, fasádne omietky, finálne úpravy</div>
            </div>
            <div class="contact-item">
              <b data-i18n="w3t">🧩 Obklady a dlažby</b>
              <div class="small" data-i18n="w3d">Kúpeľne, kuchyne, terasy, chodby</div>
            </div>
            <div class="contact-item">
              <b>📞 Telefón</b>
              <div class="small"><a href="tel:+421940825374">+421 940 825 374</a></div>
            </div>
          </div>

          <div class="kpi">
            <div class="box">
              <b data-i18n="kpi1t">Rýchla komunikácia</b>
              <span data-i18n="kpi1d">E-mail odpoveď čo najskôr</span>
            </div>
            <div class="box">
              <b data-i18n="kpi2t">Kvalita</b>
              <span data-i18n="kpi2d">Precízna práca a detail</span>
            </div>
            <div class="box">
              <b data-i18n="kpi3t">Férové ceny</b>
              <span data-i18n="kpi3d">Transparentná ponuka</span>
            </div>
            <div class="box">
              <b data-i18n="kpi4t">Trenčín</b>
              <span data-i18n="kpi4d">Pracujeme v TN a okolí</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="sluzby" class="section">
      <h2 data-i18n="services_title">Služby</h2>
      <p data-i18n="services_desc">
        Ponúkame profesionálne stavebné práce pre rodinné domy, byty aj menšie projekty.
        Každú zákazku riešime individuálne podľa vašich požiadaviek.
      </p>

      <div class="grid3">
        <div class="card service">
          <h3 data-i18n="s1t">🏗️ Stavba rodinných domov</h3>
          <p data-i18n="s1d">Realizácia novostavieb, hrubé stavby aj dokončovacie práce. Pomôžeme vám od plánovania až po finálne odovzdanie.</p>
        </div>

        <div class="card service">
          <h3 data-i18n="s2t">🧊 Zateplenie fasád</h3>
          <p data-i18n="s2d">Zateplenie a finálna fasáda pre lepšiu úsporu energie a moderný vzhľad. Pracujeme kvalitne a precízne.</p>
        </div>

        <div class="card service">
          <h3 data-i18n="s3t">🧱 Pokládka obkladov a dlažby</h3>
          <p data-i18n="s3d">Obklady a dlažby v interiéri aj exteriéri – kúpeľne, kuchyne, chodby, terasy a ďalšie priestory.</p>
        </div>
      </div>
    </section>

    <section id="realizacie" class="section">
      <h2 data-i18n="gallery_title">Realizácie</h2>
      <p data-i18n="gallery_desc">
        Ukážky našich prác. Fotky sú ilustračné – neskôr ich môžete jednoducho nahradiť vlastnými.
      </p>

      <div class="gallery">
        <div class="photo" data-title="Zateplenie fasády">
          <img alt="Zateplenie fasády" src="https://images.unsplash.com/photo-1590725121839-892b458a74fe?auto=format&fit=crop&w=1200&q=80">
          <div class="label" data-i18n="g1">Zateplenie fasády</div>
        </div>
        <div class="photo" data-title="Obklady a dlažby">
          <img alt="Obklady a dlažby" src="https://images.unsplash.com/photo-1582582429416-969c8b3a5a4a?auto=format&fit=crop&w=1200&q=80">
          <div class="label" data-i18n="g2">Obklady a dlažby</div>
        </div>
        <div class="photo" data-title="Stavba domu">
          <img alt="Stavba domu" src="https://images.unsplash.com/photo-1501183638710-841dd1904471?auto=format&fit=crop&w=1200&q=80">
          <div class="label" data-i18n="g3">Stavba domu</div>
        </div>
      </div>

      <p class="hint" data-i18n="gallery_hint">
        Tip: Pošlite мені 6–10 ваших фото і я вставлю їх на сайт красиво.
      </p>
    </section>

    <section id="o-nas" class="section">
      <h2 data-i18n="about_title">O nás</h2>
      <div class="card" style="margin-top:14px">
        <p data-i18n="about_desc">
          StavV2 je stavebná firma pôsobiaca v Trenčíne.
          Našou prioritou je spokojnosť zákazníka, kvalitné materiály a precízne prevedenie.
          Ak hľadáte spoľahlivého partnera pre stavbu domu, zateplenie fasády alebo obklady a dlažby,
          radi vám pripravíme ponuku.
        </p>
      </div>
    </section>

    <section id="kontakt" class="section">
      <h2 data-i18n="contact_title">Kontakt</h2>
      <p data-i18n="contact_desc">
        Pošlite nám správu cez formulár alebo e-mail. Odpovieme čo najskôr.
      </p>

      <div class="contact-grid">
        <div class="card">
          <h3 style="font-size:18px;margin-bottom:10px" data-i18n="email_title">📩 E-mail</h3>
          <p style="font-size:16px">
            <a class="btn primary" href="mailto:stavv2@hotmail.com?subject=Dopyt%20-%20StavV2">stavv2@hotmail.com</a>
          </p>

          <div class="contact-item" style="margin-top:12px">
            <b>📞 Telefón</b>
            <div class="small">
              <a class="btn small" href="tel:+421940825374">+421 940 825 374</a>
            </div>
          </div>

          <div class="contact-item" style="margin-top:12px">
            <b>💬 WhatsApp</b>
            <div class="small">
              <a class="btn small green" target="_blank"
                 href="https://wa.me/421940825374?text=Dobr%C3%BD%20de%C5%88%2C%20m%C3%A1m%20z%C3%A1ujem%20o%20cenov%C3%BA%20ponuku%20(StavV2).">
                Otvoriť WhatsApp
              </a>
            </div>
          </div>

          <div class="contact-item" style="margin-top:12px">
            <b>💜 Viber</b>
            <div class="small">
              <a class="btn small" href="viber://chat?number=%2B421940825374">Otvoriť Viber</a>
            </div>
          </div>

          <div class="contact-item" style="margin-top:12px">
            <b data-i18n="location_title">📍 Lokalita</b>
            <div class="small" data-i18n="location_desc">Trenčín, Slovensko</div>
          </div>

          <div style="margin-top:12px;border-radius:18px;overflow:hidden;border:1px solid var(--border)">
            <iframe
              title="Trenčín mapa"
              src="https://www.google.com/maps?q=Tren%C4%8D%C3%ADn%2C%20Slovakia&output=embed"
              width="100%"
              height="260"
              style="border:0"
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"></iframe>
          </div>
        </div>

        <div class="card">
          <h3 style="font-size:18px;margin-bottom:10px" data-i18n="form_title">📝 Formulár (dopyt)</h3>

          <form action="https://formsubmit.co/stavv2@hotmail.com" method="POST">
            <input type="hidden" name="_subject" value="Nový dopyt zo stránky StavV2">
            <input type="hidden" name="_captcha" value="false">
            <input type="hidden" name="_template" value="table">

            <div style="display:grid;gap:10px">
              <input class="input" name="Meno" required placeholder="Meno / Firma" data-i18n-placeholder="ph_name">
              <input class="input" name="Email" required type="email" placeholder="Váš e-mail" data-i18n-placeholder="ph_email">
              <input class="input" name="Mesto" placeholder="Mesto (napr. Trenčín)" data-i18n-placeholder="ph_city">
              <select class="input" name="Služba" required>
                <option value="" selected disabled data-i18n="ph_service">Vyberte službu</option>
                <option data-i18n="opt1">Stavba domu</option>
                <option data-i18n="opt2">Zateplenie fasády</option>
                <option data-i18n="opt3">Obklady a dlažby</option>
                <option data-i18n="opt4">Iné</option>
              </select>
              <textarea class="input" name="Správa" required placeholder="Popíšte, čo potrebujete..." data-i18n-placeholder="ph_msg"></textarea>

              <button class="btn primary" type="submit" data-i18n="send">Odoslať dopyt</button>
            </div>

            <p class="hint" data-i18n="form_hint">
              Formulár je zdarma. Pri prvom odoslaní FormSubmit môže vyžadovať potvrdenie na e-mail.
            </p>
          </form>
        </div>
      </div>
    </section>

    <footer>
      <div>© <span id="year"></span> StavV2 • Trenčín, Slovensko</div>
      <div class="small" style="margin-top:6px" data-i18n="footer">
        Stavba domov • Zateplenie fasád • Obklady a dlažby
      </div>
    </footer>
  </div>

  <div class="floating">
    <a class="fab whatsapp"
       href="https://wa.me/421940825374?text=Dobr%C3%BD%20de%C5%88%2C%20m%C3%A1m%20z%C3%A1ujem%20o%20cenov%C3%BA%20ponuku%20(StavV2)."
       target="_blank" title="WhatsApp">
      WA
    </a>
    <a class="fab viber" href="viber://chat?number=%2B421940825374" title="Viber">
      VB
    </a>
    <a class="fab" href="#top" title="Hore">↑</a>
  </div>

  <div class="modal" id="modal">
    <div class="modal-content">
      <div class="modal-top">
        <b id="modalTitle">Foto</b>
        <button class="modal-close" id="modalClose">Zavrieť</button>
      </div>
      <img class="modal-img" id="modalImg" alt="Preview">
    </div>
  </div>

  <script>
    document.getElementById("year").textContent = new Date().getFullYear();

    const modal = document.getElementById("modal");
    const modalImg = document.getElementById("modalImg");
    const modalTitle = document.getElementById("modalTitle");
    const modalClose = document.getElementById("modalClose");

    document.querySelectorAll(".photo").forEach(p => {
      p.addEventListener("click", () => {
        const img = p.querySelector("img");
        modalImg.src = img.src;
        modalTitle.textContent = p.getAttribute("data-title") || "Foto";
        modal.classList.add("open");
      });
    });

    modalClose.addEventListener("click", () => modal.classList.remove("open"));
    modal.addEventListener("click", (e) => {
      if(e.target === modal) modal.classList.remove("open");
    });

    const dict = {
      sk: {
        subtitle: "Stavebná firma • Trenčín, Slovensko",
        get_offer: "Cenová ponuka",
        badge: "Spoľahlivo • Kvalitne • Na čas",
        h1: "Stavby, fasády a obklady v Trenčíne",
        lead: "Sme stavebná firma pôsobiaca v meste Trenčín a okolí. Zabezpečujeme výstavbu rodinných domov, zateplenie fasád a pokládku dlažby a obkladov. Pracujeme čisto, precízne a férovo.",
        pill1: "Rodinné domy",
        pill2: "Zateplenie fasád",
        pill3: "Obklady a dlažby",
        pill4: "Trenčín a okolie",
        cta1: "Získať cenovú ponuku",
        cta2: "Pozrieť realizácie",
        cta3: "Napísať e-mail",
        stat1t: "✔ Individuálny prístup",
        stat1d: "Poradíme a navrhneme riešenie",
        stat2t: "✔ Kvalitné prevedenie",
        stat2d: "Dôraz na detail a čistú prácu",
        what_title: "Čo robíme",
        what_desc: "Kompletné stavebné práce od základov až po finálne dokončenie.",
        w1t: "🏠 Výstavba domov",
        w1d: "Hrubá stavba, murovanie, dokončovacie práce",
        w2t: "🧱 Zateplenie fasád",
        w2d: "Izolácia, fasádne omietky, finálne úpravy",
        w3t: "🧩 Obklady a dlažby",
        w3d: "Kúpeľne, kuchyne, terasy, chodby",
        w4t: "📍 Lokalita",
        w4d: "Trenčín, Slovensko + okolie",
        kpi1t: "Rýchla komunikácia",
        kpi1d: "E-mail odpoveď čo najskôr",
        kpi2t: "Kvalita",
        kpi2d: "Precízna práca a detail",
        kpi3t: "Férové ceny",
        kpi3d: "Transparentná ponuka",
        kpi4t: "Trenčín",
        kpi4d: "Pracujeme v TN a okolí",
        services_title: "Služby",
        services_desc: "Ponúkame profesionálne stavebné práce pre rodinné domy, byty aj menšie projekty. Každú zákazku riešime individuálne podľa vašich požiadaviek.",
        s1t: "🏗️ Stavba rodinných domov",
        s1d: "Realizácia novostavieb, hrubé stavby aj dokončovacie práce. Pomôžeme vám od plánovania až po finálne odovzdanie.",
        s2t: "🧊 Zateplenie fasád",
        s2d: "Zateplenie a finálna fasáda pre lepšiu úsporu energie a moderný vzhľad. Pracujeme kvalitne a precízne.",
        s3t: "🧱 Pokládka obkladov a dlažby",
        s3d: "Obklady a dlažby v interiéri aj exteriéri – kúpeľne, kuchyne, chodby, terasy a ďalšie priestory.",
        gallery_title: "Realizácie",
        gallery_desc: "Ukážky našich prác. Fotky sú ilustračné – neskôr ich môžete jednoducho nahradiť vlastnými.",
        g1: "Zateplenie fasády",
        g2: "Obklady a dlažby",
        g3: "Stavba domu",
        gallery_hint: "Tip: Pošlite mi 6–10 vašich foto a ja ich vložím do galérie pekne.",
        about_title: "O nás",
        about_desc: "StavV2 je stavebná firma pôsobiaca v Trenčíne. Našou prioritou je spokojnosť zákazníka, kvalitné materiály a precízne prevedenie. Ak hľadáte spoľahlivého partnera pre stavbu domu, zateplenie fasády alebo obklady a dlažby, radi vám pripravíme ponuku.",
        contact_title: "Kontakt",
        contact_desc: "Pošlite nám správu cez formulár alebo e-mail. Odpovieme čo najskôr.",
        email_title: "📩 E-mail",
        location_title: "📍 Lokalita",
        location_desc: "Trenčín, Slovensko",
        form_title: "📝 Formulár (dopyt)",
        ph_name: "Meno / Firma",
        ph_email: "Váš e-mail",
        ph_city: "Mesto (napr. Trenčín)",
        ph_service: "Vyberte službu",
        opt1: "Stavba domu",
        opt2: "Zateplenie fasády",
        opt3: "Obklady a dlažby",
        opt4: "Iné",
        ph_msg: "Popíšte, čo potrebujete...",
        send: "Odoslať dopyt",
        form_hint: "Formulár je zdarma. Pri prvom odoslaní FormSubmit môže vyžadovať potvrdenie na e-mail.",
        footer: "Stavba domov • Zateplenie fasád • Obklady a dlažby"
      },
      ua: {
        subtitle: "Будівельна фірма • Тренчин, Словаччина",
        get_offer: "Отримати пропозицію",
        badge: "Надійно • Якісно • Вчасно",
        h1: "Будівництво, фасади та плитка у Тренчині",
        lead: "Ми будівельна фірма в місті Тренчин та околицях. Виконуємо будівництво будинків, утеплення фасадів та укладання плитки. Працюємо чисто, акуратно та чесно.",
        pill1: "Будинки",
        pill2: "Утеплення фасадів",
        pill3: "Плитка та облицювання",
        pill4: "Тренчин та околиці",
        cta1: "Отримати ціну",
        cta2: "Переглянути роботи",
        cta3: "Написати e-mail",
        stat1t: "✔ Індивідуальний підхід",
        stat1d: "Порадимо та запропонуємо рішення",
        stat2t: "✔ Якісне виконання",
        stat2d: "Увага до деталей і чиста робота",
        what_title: "Що ми робимо",
        what_desc: "Повний комплекс будівельних робіт від фундаменту до завершення.",
        w1t: "🏠 Будівництво будинків",
        w1d: "Мурування, чорнові та чистові роботи",
        w2t: "🧱 Утеплення фасадів",
        w2d: "Ізоляція, фасадні роботи, фініш",
        w3t: "🧩 Плитка та облицювання",
        w3d: "Ванна, кухня, тераси, коридори",
        w4t: "📍 Локація",
        w4d: "Тренчин, Словаччина + околиці",
        kpi1t: "Швидкий зв’язок",
        kpi1d: "Відповідаємо на e-mail якнайшвидше",
        kpi2t: "Якість",
        kpi2d: "Акуратність і деталі",
        kpi3t: "Чесні ціни",
        kpi3d: "Прозора пропозиція",
        kpi4t: "Тренчин",
        kpi4d: "Працюємо в TN та околицях",
        services_title: "Послуги",
        services_desc: "Професійні будівельні роботи для будинків та квартир. Кожне замовлення робимо індивідуально.",
        s1t: "🏗️ Будівництво будинків",
        s1d: "Новобудови, чорнові та завершальні роботи. Допоможемо від плану до здачі.",
        s2t: "🧊 Утеплення фасадів",
        s2d: "Утеплення та фінішний фасад для економії енергії та гарного вигляду.",
        s3t: "🧱 Укладання плитки",
        s3d: "Плитка всередині та зовні: ванна, кухня, тераса, коридор та інше.",
        gallery_title: "Реалізації",
        gallery_desc: "Приклади робіт. Фото тимчасові — легко замінити на ваші.",
        g1: "Утеплення фасаду",
        g2: "Плитка та облицювання",
        g3: "Будівництво дому",
        gallery_hint: "Порада: надішліть 6–10 ваших фото — я красиво вставлю їх на сайт.",
        about_title: "Про нас",
        about_desc: "StavV2 — будівельна фірма в Тренчині. Наш пріоритет — якість, чесність та задоволений клієнт. Якщо вам потрібно побудувати будинок, утеплити фасад або покласти плитку — напишіть нам і ми підготуємо пропозицію.",
        contact_title: "Контакти",
        contact_desc: "Напишіть через форму або e-mail. Відповімо якнайшвидше.",
        email_title: "📩 E-mail",
        location_title: "📍 Локація",
        location_desc: "Тренчин, Словаччина",
        form_title: "📝 Форма заявки",
        ph_name: "Ім’я / Компанія",
        ph_email: "Ваш e-mail",
        ph_city: "Місто (наприклад Trenčín)",
        ph_service: "Оберіть послугу",
        opt1: "Будівництво дому",
        opt2: "Утеплення фасаду",
        opt3: "Плитка та облицювання",
        opt4: "Інше",
        ph_msg: "Опишіть, що потрібно зробити...",
        send: "Надіслати заявку",
        form_hint: "Форма безкоштовна. При першій відправці FormSubmit може попросити підтвердження на e-mail.",
        footer: "Будівництво • Утеплення фасадів • Плитка та облицювання"
      }
    };

    function setLang(lang){
      document.querySelectorAll("[data-i18n]").forEach(el=>{
        const key = el.getAttribute("data-i18n");
        if(dict[lang][key]) el.textContent = dict[lang][key];
      });
      document.querySelectorAll("[data-i18n-placeholder]").forEach(el=>{
        const key = el.getAttribute("data-i18n-placeholder");
        if(dict[lang][key]) el.setAttribute("placeholder", dict[lang][key]);
      });

      document.getElementById("lang-sk").classList.toggle("active", lang==="sk");
      document.getElementById("lang-ua").classList.toggle("active", lang==="ua");
      localStorage.setItem("stavv2_lang", lang);
    }

    document.getElementById("lang-sk").addEventListener("click", ()=>setLang("sk"));
    document.getElementById("lang-ua").addEventListener("click", ()=>setLang("ua"));

    const saved = localStorage.getItem("stavv2_lang") || "sk";
    setLang(saved);
  </script>
</body>
</html>
