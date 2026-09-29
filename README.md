# Grupo-terap-utico-
Site grupo terapêutico 
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Entre Nós — Grupo Terapêutico para Mulheres | Kesia Figueiredo</title>
<meta name="description" content="Grupo terapêutico online para mulheres que querem parar de se sabotar, confiar mais em si e se relacionar com mais leveza. Com Kesia Figueiredo, psicóloga CRP 06/206769.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;1,500&family=Jost:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  /* ============ TOKENS ============ */
  :root{
    --bg:#F5EFE8;
    --surface:#FBF6EF;
    --text:#3A1F2B;
    --text-soft:#7A5C63;
    --heading:#55213A;
    --brand:#7B2D42;
    --brand-deep:#55213A;
    --accent:#C9A96E;
    --accent-soft:#D9CCC4;
    --border:rgba(123,45,66,0.16);
    --on-dark:#FBF3EA;
    --on-dark-soft:rgba(251,243,234,0.78);
    --focus:#C9A96E;
    --neon:#FF2E9E;
    --font-display:'Cormorant Garamond', Georgia, 'Times New Roman', serif;
    --font-body:'Jost', 'Helvetica Neue', Arial, sans-serif;
    color-scheme: light;
  }
  @media (prefers-color-scheme: dark){
    :root:not([data-theme="light"]){
      --bg:#22121A;
      --surface:#2B1720;
      --text:#F2E3DF;
      --text-soft:#D2ACB3;
      --heading:#E4C193;
      --brand:#E2A7BB;
      --brand-deep:#3A1621;
      --accent:#DCC08D;
      --accent-soft:#CDBCB5;
      --border:rgba(228,193,147,0.22);
    }
  }
  :root[data-theme="dark"]{
    --bg:#22121A;
    --surface:#2B1720;
    --text:#F2E3DF;
    --text-soft:#D2ACB3;
    --heading:#E4C193;
    --brand:#E2A7BB;
    --brand-deep:#3A1621;
    --accent:#DCC08D;
    --accent-soft:#CDBCB5;
    --border:rgba(228,193,147,0.22);
  }

  /* ============ BASE ============ */
  *,*::before,*::after{ box-sizing:border-box; }
  html{ scroll-behavior:smooth; }
  @media (prefers-reduced-motion: reduce){
    html{ scroll-behavior:auto; }
    *,*::before,*::after{ animation-duration:0.01ms !important; animation-iteration-count:1 !important; transition-duration:0.01ms !important; }
  }
  body{
    margin:0;
    background:var(--bg);
    color:var(--text);
    font-family:var(--font-body);
    font-weight:400;
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }
  img,svg{ max-width:100%; display:block; }
  a{ color:inherit; }
  :focus-visible{ outline:3px solid var(--focus); outline-offset:3px; }

  h1,h2,h3{
    font-family:var(--font-display);
    font-weight:500;
    color:var(--heading);
    margin:0 0 0.5em;
  }
  p{ margin:0 0 1.1em; color:var(--text); }
  .lede{ color:var(--text-soft); }

  .container{
    width:100%;
    max-width:720px;
    margin:0 auto;
    padding:0 24px;
  }
  .container--wide{ max-width:920px; }

  .section{ padding:88px 0; overflow-x:hidden; }
  @media (max-width:640px){ .section{ padding:64px 0; } }

  /* ============ BUTTONS ============ */
  .btn{
    display:inline-flex;
    align-items:center;
    gap:10px;
    font-family:var(--font-body);
    font-weight:500;
    font-size:1.02rem;
    padding:16px 30px;
    border-radius:6px;
    text-decoration:none;
    border:1px solid transparent;
    cursor:pointer;
    transition:transform 0.18s ease, box-shadow 0.18s ease;
  }
  .btn:hover{ transform:translateY(-2px); }
  .btn-primary{
    background:var(--accent);
    color:var(--brand-deep);
    box-shadow:0 10px 24px -12px rgba(0,0,0,0.35);
  }
  .btn-primary:hover{ box-shadow:0 14px 28px -12px rgba(0,0,0,0.4); }
  .btn-outline{
    background:transparent;
    border-color:var(--on-dark-soft);
    color:var(--on-dark);
  }
  .btn-outline:hover{ background:rgba(251,243,234,0.08); }
  .btn svg{ width:18px; height:18px; flex-shrink:0; }

  /* ============ HEADER ============ */
  .site-header{
    position:fixed;
    top:0; left:0; right:0;
    z-index:40;
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:16px 24px;
    background:transparent;
    transform:translateY(-100%);
    transition:transform 0.35s ease, background 0.35s ease, box-shadow 0.35s ease;
  }
  .site-header.is-visible{
    transform:translateY(0);
    background:var(--surface);
    box-shadow:0 4px 18px -12px rgba(0,0,0,0.25);
    border-bottom:1px solid var(--border);
  }
  .site-header__name{
    font-family:var(--font-display);
    font-size:1.15rem;
    color:var(--heading);
    font-weight:500;
  }
  .site-header .btn{ padding:10px 18px; font-size:0.92rem; }

  /* ============ HERO ============ */
  .hero{
    min-height:100svh;
    display:flex;
    align-items:center;
    padding:140px 24px 100px;
    background:linear-gradient(150deg, var(--brand-deep) 0%, var(--brand) 48%, var(--accent) 100%);
    position:relative;
  }
  .hero__inner{
    max-width:680px;
    margin:0 auto;
    text-align:center;
    animation:heroReveal 0.9s ease both;
  }
  @keyframes heroReveal{
    from{ opacity:0; transform:translateY(14px); }
    to{ opacity:1; transform:translateY(0); }
  }
  .hero__photo{
    width:150px; height:150px;
    margin:0 auto 26px;
    border-radius:50%;
    object-fit:cover;
    border:3px solid var(--accent);
    box-shadow:0 14px 32px -14px rgba(0,0,0,0.55);
  }
  .hero__eyebrow{
    display:inline-flex;
    align-items:center;
    gap:10px;
    color:var(--on-dark-soft);
    font-size:0.92rem;
    letter-spacing:0.01em;
    margin-bottom:22px;
  }
  .hero__eyebrow::before,
  .hero__eyebrow::after{
    content:"";
    width:28px;
    height:1px;
    background:var(--on-dark-soft);
  }
  .hero__title{
    color:var(--on-dark);
    font-family:var(--font-display);
    font-weight:600;
    font-size:clamp(2.9rem, 9vw, 5.4rem);
    line-height:1;
    margin-bottom:30px;
  }
  .hero__promise{
    color:var(--on-dark);
    font-family:var(--font-display);
    font-weight:500;
    font-size:clamp(1.35rem, 3vw, 1.85rem);
    line-height:1.32;
    margin-bottom:16px;
  }
  .hero p.lede{
    color:var(--on-dark-soft);
    font-size:1.08rem;
    line-height:1.7;
    max-width:540px;
    margin:0 auto 36px;
  }

  /* ============ DOR (checklist interativo) ============ */
  .section--dor{ background:var(--bg); }
  .dor-hint{ color:var(--text-soft); font-size:0.95rem; margin:-8px 0 24px; }
  .dor-list{
    list-style:none;
    margin:0;
    padding:0;
    display:grid;
    gap:12px;
  }
  .dor-item{
    width:100%;
    display:flex;
    align-items:center;
    gap:16px;
    text-align:left;
    background:var(--surface);
    border:1px solid var(--border);
    border-radius:6px;
    padding:16px 20px;
    font-family:var(--font-body);
    font-size:1.02rem;
    color:var(--text);
    cursor:pointer;
    transition:background 0.2s ease, border-color 0.2s ease;
  }
  .dor-item__mark{
    width:22px; height:22px;
    border-radius:50%;
    border:2px solid var(--accent);
    flex-shrink:0;
    position:relative;
  }
  .dor-item__mark::after{
    content:"";
    position:absolute;
    inset:4px;
    border-radius:50%;
    background:var(--accent);
    transform:scale(0);
    transition:transform 0.2s ease;
  }
  .dor-item:hover,
  .dor-item[aria-pressed="true"]{
    background:var(--neon);
    border-color:var(--neon);
  }
  .dor-item:hover .dor-item__mark,
  .dor-item[aria-pressed="true"] .dor-item__mark{ border-color:#fff; }
  .dor-item:hover .dor-item__mark::after,
  .dor-item[aria-pressed="true"] .dor-item__mark::after{ transform:scale(1); background:#fff; }
  .dor-item:hover .dor-item__text,
  .dor-item[aria-pressed="true"] .dor-item__text{ color:#fff; }
  .dor-response{
    margin-top:30px;
    min-height:1.6em;
    font-family:var(--font-display);
    font-style:italic;
    font-size:1.3rem;
    color:var(--heading);
    line-height:1.5;
  }

  /* ============ PARA QUEM ============ */
  .section--publico{ background:color-mix(in srgb, var(--accent-soft) 26%, var(--bg)); }
  .publico-lede{ color:var(--text-soft); margin-bottom:28px; }
  .publico-list{
    list-style:none;
    margin:0 0 28px;
    padding:0;
    display:grid;
    gap:14px;
  }
  .publico-list li{
    display:flex;
    gap:12px;
    align-items:flex-start;
    font-size:1.04rem;
    color:var(--text);
  }
  .publico-list svg{ width:18px; height:18px; margin-top:4px; flex-shrink:0; color:var(--brand); }
  .publico-closing{
    font-family:var(--font-display);
    font-style:italic;
    font-size:1.25rem;
    color:var(--heading);
    margin-bottom:0;
  }
  .kw{ color:var(--brand); font-weight:600; }

  /* ============ COMO FUNCIONA ============ */
  .section--como{ background:var(--surface); border-top:1px solid var(--border); border-bottom:1px solid var(--border); }
  .como-grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:36px 40px;
    margin-top:44px;
  }
  @media (max-width:640px){ .como-grid{ grid-template-columns:1fr; } }
  .como-item{ padding-top:18px; border-top:2px solid var(--accent); }
  .como-item h3{
    font-family:var(--font-body);
    font-weight:600;
    font-size:1.05rem;
    color:var(--heading);
    margin-bottom:8px;
  }
  .como-item p{ color:var(--text-soft); font-size:0.98rem; margin-bottom:0; }

  /* ============ PROVA SOCIAL ============ */
  .section--prova{ background:var(--bg); }
  .quote-card{
    background:var(--surface);
    border:1px solid var(--border);
    padding:48px clamp(24px,5vw,56px);
    position:relative;
  }
  .quote-card + .quote-card{ margin-top:28px; }
  .quote-mark{
    font-family:var(--font-display);
    font-size:4.5rem;
    color:var(--accent-soft);
    line-height:1;
    margin-bottom:8px;
    display:block;
  }
  .quote-card blockquote{
    margin:0;
    font-family:var(--font-display);
    font-size:clamp(1.15rem,2.4vw,1.45rem);
    line-height:1.6;
    color:var(--text);
  }
  .quote-card blockquote p{ color:inherit; }
  .quote-card cite{
    display:block;
    margin-top:22px;
    font-style:normal;
    font-family:var(--font-body);
    font-weight:500;
    color:var(--brand);
    font-size:0.98rem;
  }
  .prova-intro{ color:var(--text-soft); margin-bottom:28px; }
  .prova-note{
    margin-top:24px;
    color:var(--text-soft);
    font-size:0.96rem;
  }

  /* ============ SOBRE MIM ============ */
  .section--sobre{
    background:var(--brand-deep);
    color:var(--on-dark);
  }
  .section--sobre .container{ text-align:center; }
  .sobre-foto{
    width:140px; height:140px;
    margin:0 auto 28px;
    border-radius:50%;
    object-fit:cover;
    border:3px solid var(--accent);
    box-shadow:0 12px 30px -14px rgba(0,0,0,0.5);
  }
  .section--sobre h2{ color:var(--on-dark); }
  .section--sobre p{ color:var(--on-dark-soft); font-size:1.06rem; line-height:1.75; }
  .sobre-credencial{
    margin-top:26px;
    font-size:0.92rem;
    color:var(--accent);
  }
  .sobre-credencial a{ text-decoration:none; border-bottom:1px solid rgba(201,169,110,0.5); }
  .section--sobre .kw{ color:var(--accent); }

  /* ============ FAQ ============ */
  .section--faq{ background:var(--bg); }
  .faq-item{ border-bottom:1px solid var(--border); }
  .faq-item:first-of-type{ border-top:1px solid var(--border); }
  .faq-question{
    width:100%;
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:20px;
    background:none;
    border:none;
    text-align:left;
    padding:22px 0;
    font-family:var(--font-body);
    font-weight:500;
    font-size:1.06rem;
    color:var(--heading);
    cursor:pointer;
  }
  .faq-icon{
    position:relative;
    width:18px; height:18px;
    flex-shrink:0;
  }
  .faq-icon::before,
  .faq-icon::after{
    content:"";
    position:absolute;
    background:var(--brand);
    top:50%; left:50%;
    transform:translate(-50%,-50%);
  }
  .faq-icon::before{ width:16px; height:2px; }
  .faq-icon::after{ width:2px; height:16px; transition:transform 0.25s ease; }
  .faq-question[aria-expanded="true"] .faq-icon::after{ transform:translate(-50%,-50%) rotate(90deg); opacity:0; }
  .faq-answer{
    max-height:0;
    overflow:hidden;
    transition:max-height 0.32s ease;
  }
  .faq-answer p{
    padding:0 0 22px;
    color:var(--text-soft);
    font-size:0.99rem;
    max-width:60ch;
  }

  /* ============ OFERTA ============ */
  .section--oferta{
    background:linear-gradient(150deg, var(--brand-deep) 0%, var(--brand) 55%, var(--accent) 100%);
    text-align:center;
  }
  .section--oferta h2{ color:var(--on-dark); }
  .section--oferta .lede{ color:var(--on-dark-soft); max-width:560px; margin:0 auto 30px; }
  .oferta-list{
    list-style:none;
    padding:0;
    margin:0 0 36px;
    display:inline-flex;
    flex-direction:column;
    gap:12px;
    text-align:left;
  }
  .oferta-list li{
    color:var(--on-dark);
    font-size:1rem;
    display:flex;
    gap:12px;
    align-items:flex-start;
  }
  .oferta-list svg{ width:18px; height:18px; margin-top:3px; flex-shrink:0; color:var(--accent); }
  .oferta-cta{ margin-top:6px; }

  /* ============ FOOTER ============ */
  .site-footer{
    background:var(--surface);
    border-top:1px solid var(--border);
    padding:36px 24px;
    text-align:center;
    color:var(--text-soft);
    font-size:0.9rem;
  }
  .site-footer a{ color:var(--brand); text-decoration:none; border-bottom:1px solid var(--border); }

  /* ============ FLOATING WHATSAPP ============ */
  .floating-whatsapp{
    position:fixed;
    right:20px; bottom:20px;
    width:56px; height:56px;
    border-radius:50%;
    background:var(--accent);
    color:var(--brand-deep);
    display:flex; align-items:center; justify-content:center;
    box-shadow:0 10px 24px -10px rgba(0,0,0,0.45);
    z-index:50;
    text-decoration:none;
    opacity:0;
    transform:translateY(12px);
    pointer-events:none;
    transition:opacity 0.3s ease, transform 0.3s ease;
  }
  .floating-whatsapp.is-visible{ opacity:1; transform:translateY(0); pointer-events:auto; }
  .floating-whatsapp svg{ width:26px; height:26px; }
</style>
</head>
<body>

<header class="site-header" id="siteHeader">
  <span class="site-header__name">Kesia Figueiredo</span>
  <a class="btn btn-primary whatsapp-cta" data-message="Olá, Kesia! Vi a página do Entre Nós e quero saber mais." href="#" target="_blank" rel="noopener">Falar no WhatsApp</a>
</header>

<main>

  <section class="hero" id="hero">
    <div class="hero__inner">
      <img class="hero__photo" src="data:image/jpeg;base64,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
