# WASH-ME
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>WASH-ME · Autolavado a domicilio en Zapopan y Guadalajara</title>
<meta name="description" content="WASH-ME lava tu coche o camioneta en la puerta de tu casa. Servicio a domicilio exclusivo para Zapopan y Guadalajara. Planes Básico, Pro y Premium.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Anton&family=Work+Sans:wght@400;500;600;700;800&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#081B33;
    --ink-soft:#123259;
    --paper:#F3F6FB;
    --paper-dim:#E3EBF7;
    --accent:#2E6BFF;
    --accent-2:#154FDB;
    --accent-ink:#FFFFFF;
    --aqua:#39C6E6;
    --coral:#FF6A4D;
    --star:#FFB800;
    --muted:#57698A;
    --line:rgba(8,27,51,0.12);
    --radius:18px;
    --shadow:0 18px 40px rgba(8,27,51,0.14);
    --display:'Anton', sans-serif;
    --body:'Work Sans', sans-serif;
  }

  *{box-sizing:border-box; margin:0; padding:0;}
  html{scroll-behavior:smooth;}
  body{
    font-family:var(--body);
    background:var(--paper);
    color:var(--ink);
    line-height:1.5;
    -webkit-font-smoothing:antialiased;
  }
  img,svg{display:block; max-width:100%;}
  a{color:inherit; text-decoration:none;}
  ul{list-style:none;}
  button{font:inherit; cursor:pointer; border:none; background:none;}
  .container{
    width:100%;
    max-width:1180px;
    margin:0 auto;
    padding:0 24px;
  }
  section{padding:96px 0;}
  h1,h2,h3{font-family:var(--display); font-weight:400; letter-spacing:0.01em; line-height:1.05;}
  .eyebrow{
    display:inline-flex;
    align-items:center;
    gap:8px;
    font-size:13px;
    font-weight:700;
    letter-spacing:0.14em;
    text-transform:uppercase;
    color:var(--ink-soft);
    background:var(--paper-dim);
    border:1px solid var(--line);
    padding:8px 16px;
    border-radius:999px;
  }
  .eyebrow .dot{width:7px; height:7px; border-radius:50%; background:var(--accent); box-shadow:0 0 0 4px rgba(46,107,255,0.22);}

  /* Buttons */
  .btn{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    gap:10px;
    padding:16px 28px;
    border-radius:999px;
    font-weight:700;
    font-size:15px;
    white-space:nowrap;
    transition:transform 0.18s ease, box-shadow 0.18s ease, background 0.18s ease;
  }
  .btn-primary{
    background:linear-gradient(135deg, var(--accent), var(--accent-2));
    color:var(--accent-ink);
    box-shadow:0 10px 24px rgba(46,107,255,0.35);
  }
  .btn-primary:hover{transform:translateY(-2px); box-shadow:0 14px 30px rgba(46,107,255,0.45);}
  .btn-ghost{
    background:transparent;
    color:var(--paper);
    border:1.5px solid rgba(243,246,251,0.4);
  }
  .btn-ghost:hover{border-color:var(--paper); transform:translateY(-2px);}
  .btn-ghost-dark{
    background:transparent;
    color:var(--ink);
    border:1.5px solid var(--line);
  }
  .btn-ghost-dark:hover{border-color:var(--ink); transform:translateY(-2px);}
  .btn-dark{
    background:var(--ink);
    color:var(--paper);
  }
  .btn-dark:hover{transform:translateY(-2px); box-shadow:0 14px 30px rgba(8,27,51,0.35);}
  .btn-small{padding:11px 20px; font-size:13px;}
  .btn:disabled{opacity:0.5; cursor:not-allowed; transform:none !important;}

  /* ===== Header ===== */
  header{
    position:sticky;
    top:0;
    z-index:100;
    background:rgba(243,246,251,0.86);
    backdrop-filter:blur(10px);
    border-bottom:1px solid var(--line);
  }
  .nav{
    display:flex;
    align-items:center;
    justify-content:space-between;
    height:78px;
  }
  .logo{
    font-family:var(--display);
    font-size:26px;
    letter-spacing:0.03em;
    display:flex;
    align-items:center;
    gap:8px;
  }
  .logo .drop{
    width:14px; height:14px;
    background:linear-gradient(135deg, var(--accent), var(--aqua));
    border-radius:0 50% 50% 50%;
    transform:rotate(45deg);
    box-shadow:inset -2px -2px 0 rgba(0,0,0,0.08);
  }
  .nav-links{
    display:flex;
    align-items:center;
    gap:32px;
    font-size:14.5px;
    font-weight:600;
  }
  .nav-links a{
    position:relative;
    padding:6px 0;
    color:var(--ink-soft);
  }
  .nav-links a::after{
    content:"";
    position:absolute;
    left:0; bottom:0;
    width:0%; height:2px;
    background:var(--accent);
    transition:width 0.2s ease;
  }
  .nav-links a:hover::after{width:100%;}
  .nav-cta{display:flex; align-items:center; gap:16px;}
  .burger{
    display:none;
    flex-direction:column;
    gap:5px;
    padding:8px;
  }
  .burger span{width:24px; height:2px; background:var(--ink); display:block; border-radius:2px;}
  .mobile-menu{
    display:none;
    flex-direction:column;
    gap:4px;
    padding:8px 24px 24px;
    border-top:1px solid var(--line);
  }
  .mobile-menu.open{display:flex;}
  .mobile-menu a{
    padding:14px 4px;
    font-weight:600;
    border-bottom:1px solid var(--line);
  }

  /* ===== Hero ===== */
  .hero{
    background:radial-gradient(120% 100% at 50% 0%, #0E2A4C 0%, var(--ink) 55%, #04101F 100%);
    color:var(--paper);
    padding:72px 0 0;
    overflow:hidden;
    position:relative;
  }
  .hero::before{
    content:"";
    position:absolute;
    inset:0;
    background:
      radial-gradient(60% 50% at 85% 8%, rgba(46,107,255,0.28), transparent 60%),
      radial-gradient(50% 40% at 8% 92%, rgba(57,198,230,0.22), transparent 60%);
    pointer-events:none;
  }
  .hero-grid{
    position:relative;
    display:grid;
    grid-template-columns:1.05fr 0.95fr;
    gap:56px;
    align-items:center;
  }
  .hero h1{
    font-size:clamp(40px, 5.6vw, 68px);
    margin:22px 0 22px;
    max-width:12ch;
  }
  .hero h1 em{
    font-style:normal;
    background:linear-gradient(100deg, var(--aqua), var(--accent) 65%);
    -webkit-background-clip:text;
    background-clip:text;
    color:transparent;
  }
  .hero p.lead{
    font-size:18px;
    color:rgba(243,246,251,0.78);
    max-width:46ch;
    margin-bottom:34px;
  }
  .hero-ctas{display:flex; gap:14px; flex-wrap:wrap; margin-bottom:38px;}
  .hero-coverage{
    display:flex;
    align-items:center;
    gap:14px;
    font-size:13.5px;
    color:rgba(243,246,251,0.65);
    flex-wrap:wrap;
  }
  .hero-coverage .chip{
    display:inline-flex;
    align-items:center;
    gap:6px;
    background:rgba(243,246,251,0.08);
    border:1px solid rgba(243,246,251,0.18);
    padding:6px 12px;
    border-radius:999px;
    font-weight:600;
  }
  .hero-coverage .chip svg{width:12px; height:12px;}

  /* Before/after signature element */
  .reveal-card{
    position:relative;
    background:linear-gradient(160deg, #0F2C50, #0A2040);
    border-radius:24px;
    padding:16px;
    box-shadow:0 30px 70px rgba(2,10,22,0.55);
    border:1px solid rgba(243,246,251,0.1);
  }
  .reveal-wrap{
    position:relative;
    border-radius:18px;
    overflow:hidden;
    background:#081A30;
    touch-action:none;
    cursor:ew-resize;
    user-select:none;
  }
  .reveal-wrap svg{width:100%; height:auto; display:block;}
  .reveal-tag{
    position:absolute;
    top:16px;
    z-index:5;
    font-size:11px;
    font-weight:800;
    letter-spacing:0.1em;
    text-transform:uppercase;
    padding:7px 14px;
    border-radius:999px;
    backdrop-filter:blur(6px);
  }
  .reveal-tag.before{
    left:16px;
    background:rgba(8,27,51,0.55);
    color:rgba(243,246,251,0.85);
    border:1px solid rgba(243,246,251,0.25);
  }
  .reveal-tag.after{
    right:16px;
    background:linear-gradient(120deg, var(--accent), var(--aqua));
    color:#fff;
  }
  .reveal-hint{
    text-align:center;
    font-size:12.5px;
    color:rgba(243,246,251,0.45);
    margin-top:14px;
  }

  @keyframes twinkle{
    0%, 100%{ opacity:0.15; transform:scale(0.7); }
    50%{ opacity:0.95; transform:scale(1.05); }
  }
  @keyframes shineDrift{
    0%, 100%{ opacity:0.35; }
    50%{ opacity:0.75; }
  }
  @keyframes bubbleFloat{
    0%{ transform:translateY(0); }
    50%{ transform:translateY(-6px); }
    100%{ transform:translateY(0); }
  }
  .sparkle{ animation:twinkle 2.4s ease-in-out infinite; transform-origin:center; }
  .sparkle:nth-child(2){ animation-delay:0.5s; }
  .sparkle:nth-child(3){ animation-delay:1.1s; }
  .sparkle:nth-child(4){ animation-delay:1.6s; }
  .shine-el{ animation:shineDrift 3.2s ease-in-out infinite; }
  .bubble{ animation:bubbleFloat 4s ease-in-out infinite; }
  .bubble:nth-child(2){ animation-delay:0.8s; }
  .bubble:nth-child(3){ animation-delay:1.6s; }

  /* ===== How it works ===== */
  .how{background:var(--paper);}
  .section-head{
    max-width:640px;
    margin-bottom:56px;
  }
  .section-head h2{
    font-size:clamp(32px, 4vw, 46px);
    margin-top:16px;
  }
  .section-head p{
    color:var(--muted);
    font-size:16.5px;
    margin-top:14px;
    max-width:52ch;
  }
  .steps{
    display:grid;
    grid-template-columns:repeat(3, 1fr);
    gap:28px;
  }
  .step{
    background:#fff;
    border:1px solid var(--line);
    border-radius:var(--radius);
    padding:32px 26px;
    position:relative;
  }
  .step .num{
    font-family:var(--display);
    font-size:44px;
    color:var(--accent);
    -webkit-text-stroke:1.5px var(--ink);
    line-height:1;
    margin-bottom:18px;
  }
  .step h3{font-family:var(--body); font-weight:800; font-size:19px; margin-bottom:10px;}
  .step p{color:var(--muted); font-size:15px;}

  /* ===== Casos de éxito ===== */
  .cases{background:var(--paper);}
  .section-head-row{
    display:flex;
    align-items:flex-end;
    justify-content:space-between;
    gap:24px;
    flex-wrap:wrap;
    margin-bottom:44px;
  }
  .section-head-row .section-head{margin-bottom:0;}
  .admin-controls{
    display:flex;
    align-items:center;
    gap:12px;
    flex-wrap:wrap;
  }
  .admin-status{
    display:inline-flex;
    align-items:center;
    gap:6px;
    font-size:12.5px;
    font-weight:700;
    color:var(--ink-soft);
    background:var(--paper-dim);
    border:1px solid var(--line);
    padding:6px 12px;
    border-radius:999px;
  }
  .admin-status .dot{width:7px; height:7px; border-radius:50%; background:var(--aqua);}

  .cases-grid{
    display:grid;
    grid-template-columns:repeat(auto-fill, minmax(280px, 1fr));
    gap:26px;
  }
  .cases-empty{
    text-align:center;
    color:var(--muted);
    font-size:15px;
    padding:50px 20px;
    border:1.5px dashed var(--line);
    border-radius:var(--radius);
  }
  .case-card{
    position:relative;
    background:#fff;
    border:1px solid var(--line);
    border-radius:var(--radius);
    overflow:hidden;
    box-shadow:var(--shadow);
    display:flex;
    flex-direction:column;
  }
  .case-img-wrap{
    position:relative;
    width:100%;
    aspect-ratio:4/3;
    background:var(--paper-dim);
    overflow:hidden;
  }
  .case-img-wrap img{
    width:100%; height:100%;
    object-fit:cover;
  }
  .case-admin-actions{
    position:absolute;
    top:10px; right:10px;
    display:flex;
    gap:8px;
    z-index:2;
  }
  .icon-btn{
    width:34px; height:34px;
    border-radius:50%;
    background:rgba(8,27,51,0.72);
    color:#fff;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:15px;
    backdrop-filter:blur(4px);
    transition:transform 0.15s ease, background 0.15s ease;
  }
  .icon-btn:hover{transform:scale(1.08);}
  .icon-btn.danger:hover{background:var(--coral);}
  .case-body{
    padding:20px 22px 22px;
    display:flex;
    flex-direction:column;
    gap:10px;
    flex:1;
  }
  .case-body h3{font-family:var(--body); font-weight:800; font-size:17.5px;}
  .case-body p{color:var(--muted); font-size:14px; flex:1;}
  .case-date{font-size:11.5px; color:var(--muted); font-weight:600; text-transform:uppercase; letter-spacing:0.05em;}
  .case-reactions{
    display:flex;
    align-items:center;
    justify-content:space-between;
    flex-wrap:wrap;
    gap:10px;
    padding-top:14px;
    border-top:1px solid var(--line);
    margin-top:6px;
  }
  .react-buttons{display:flex; gap:8px;}
  .react-btn{
    display:inline-flex;
    align-items:center;
    gap:6px;
    background:var(--paper-dim);
    border:1px solid var(--line);
    padding:8px 13px;
    border-radius:999px;
    font-size:13px;
    font-weight:700;
    color:var(--ink-soft);
    transition:all 0.15s ease;
  }
  .react-btn:hover{transform:translateY(-1px);}
  .react-btn.active{background:var(--accent); border-color:var(--accent); color:#fff;}
  .react-btn.heart.active{background:var(--coral); border-color:var(--coral); color:#fff;}
  .stars{display:inline-flex; align-items:center; gap:2px;}
  .stars button{
    font-size:18px;
    line-height:1;
    color:#d7dfec;
    transition:transform 0.1s ease;
  }
  .stars button:hover{transform:scale(1.15);}
  .stars button.filled{color:var(--star);}
  .stars-avg{font-size:11.5px; color:var(--muted); font-weight:600; margin-left:4px; white-space:nowrap;}

  /* ===== Pricing ===== */
  .pricing{background:var(--ink); color:var(--paper);}
  .pricing .section-head p{color:rgba(243,246,251,0.65);}
  .pricing .section-head h2{color:var(--paper);}

  .switcher{
    display:inline-flex;
    background:rgba(243,246,251,0.08);
    border:1px solid rgba(243,246,251,0.18);
    padding:5px;
    border-radius:999px;
    margin-bottom:48px;
  }
  .switcher button{
    padding:12px 26px;
    border-radius:999px;
    font-weight:700;
    font-size:14.5px;
    color:rgba(243,246,251,0.65);
    display:flex;
    align-items:center;
    gap:8px;
    transition:all 0.2s ease;
  }
  .switcher button.active{
    background:linear-gradient(135deg, var(--accent), var(--accent-2));
    color:#fff;
  }

  .plans{
    display:grid;
    grid-template-columns:repeat(3, 1fr);
    gap:24px;
  }
  .plan{
    background:var(--ink-soft);
    border:1px solid rgba(243,246,251,0.12);
    border-radius:22px;
    padding:34px 28px;
    display:flex;
    flex-direction:column;
    position:relative;
  }
  .plan.featured{
    border-color:var(--accent);
    box-shadow:0 0 0 1px var(--accent), 0 24px 50px rgba(46,107,255,0.22);
  }
  .plan .badge{
    position:absolute;
    top:-13px;
    right:28px;
    background:linear-gradient(135deg, var(--accent), var(--aqua));
    color:#fff;
    font-size:11.5px;
    font-weight:800;
    letter-spacing:0.06em;
    text-transform:uppercase;
    padding:6px 14px;
    border-radius:999px;
  }
  .plan h3{
    font-family:var(--body);
    font-weight:700;
    font-size:15px;
    letter-spacing:0.1em;
    text-transform:uppercase;
    color:rgba(243,246,251,0.6);
    margin-bottom:14px;
  }
  .plan .price{
    font-family:var(--display);
    font-size:52px;
    line-height:1;
    margin-bottom:4px;
  }
  .plan .price sup{font-size:20px; top:-1.2em;}
  .plan .price small{
    font-family:var(--body);
    font-size:14px;
    font-weight:500;
    color:rgba(243,246,251,0.5);
  }
  .plan .desc{
    font-size:14px;
    color:rgba(243,246,251,0.6);
    margin:10px 0 24px;
  }
  .plan ul{
    display:flex;
    flex-direction:column;
    gap:12px;
    margin-bottom:30px;
    flex:1;
  }
  .plan ul li{
    display:flex;
    align-items:flex-start;
    gap:10px;
    font-size:14.5px;
    color:rgba(243,246,251,0.85);
  }
  .plan ul li svg{flex-shrink:0; margin-top:3px; width:16px; height:16px; color:var(--aqua);}
  .vehicle-group{display:none;}
  .vehicle-group.active{display:grid;}

  /* ===== Coverage ===== */
  .coverage{background:var(--paper);}
  .coverage-inner{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:56px;
    align-items:center;
  }
  .coverage-cities{
    display:flex;
    gap:16px;
    flex-wrap:wrap;
    margin:26px 0 30px;
  }
  .city-card{
    background:#fff;
    border:1px solid var(--line);
    border-radius:16px;
    padding:20px 22px;
    flex:1;
    min-width:150px;
  }
  .city-card .city-name{font-family:var(--display); font-size:24px; margin-bottom:4px;}
  .city-card .city-tag{font-size:12.5px; color:var(--muted); font-weight:600;}
  .notice{
    display:flex;
    gap:12px;
    align-items:flex-start;
    background:rgba(255,106,77,0.09);
    border:1px solid rgba(255,106,77,0.3);
    padding:16px 18px;
    border-radius:14px;
    font-size:14px;
    color:var(--ink-soft);
  }
  .notice svg{flex-shrink:0; width:20px; height:20px; color:var(--coral); margin-top:2px;}
  .map-art{
    background:var(--paper-dim);
    border:1px solid var(--line);
    border-radius:24px;
    padding:36px;
    position:relative;
    overflow:hidden;
    min-height:340px;
    display:flex;
    align-items:center;
    justify-content:center;
  }

  /* ===== Final CTA ===== */
  .cta-band{
    background:linear-gradient(120deg, var(--accent), var(--accent-2) 60%, #0B2A55);
    color:#fff;
  }
  .cta-inner{
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:40px;
    flex-wrap:wrap;
  }
  .cta-inner h2{font-size:clamp(28px,3.6vw,42px); max-width:14ch;}
  .cta-inner p{margin-top:10px; font-weight:600; opacity:0.85;}

  /* ===== Footer ===== */
  footer{
    background:var(--ink);
    color:rgba(243,246,251,0.7);
    padding:64px 0 32px;
  }
  .footer-grid{
    display:grid;
    grid-template-columns:1.4fr 1fr 1fr;
    gap:40px;
    padding-bottom:40px;
    border-bottom:1px solid rgba(243,246,251,0.12);
  }
  .footer-grid .logo{color:var(--paper);}
  .footer-grid p{font-size:14px; margin-top:14px; max-width:34ch; color:rgba(243,246,251,0.55);}
  .footer-col h4{
    font-size:13px;
    text-transform:uppercase;
    letter-spacing:0.1em;
    color:rgba(243,246,251,0.45);
    margin-bottom:16px;
  }
  .footer-col a, .footer-col span{
    display:block;
    font-size:14.5px;
    margin-bottom:12px;
    color:rgba(243,246,251,0.8);
  }
  .footer-col a:hover{color:var(--aqua);}
  .footer-bottom{
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding-top:26px;
    font-size:13px;
    color:rgba(243,246,251,0.4);
    flex-wrap:wrap;
    gap:10px;
  }

  /* WhatsApp floating button */
  .wa-float{
    position:fixed;
    bottom:22px;
    right:22px;
    z-index:200;
    background:linear-gradient(135deg, var(--accent), var(--aqua));
    color:#fff;
    width:58px;
    height:58px;
    border-radius:50%;
    display:flex;
    align-items:center;
    justify-content:center;
    box-shadow:0 12px 26px rgba(46,107,255,0.45);
    transition:transform 0.2s ease;
  }
  .wa-float:hover{transform:scale(1.08);}
  .wa-float svg{width:26px; height:26px;}

  /* ===== Modals ===== */
  .modal-overlay{
    display:none;
    position:fixed;
    inset:0;
    background:rgba(8,27,51,0.55);
    backdrop-filter:blur(4px);
    align-items:center;
    justify-content:center;
    z-index:400;
    padding:20px;
  }
  .modal-overlay.open{display:flex;}
  .modal{
    background:#fff;
    border-radius:22px;
    padding:32px;
    max-width:460px;
    width:100%;
    max-height:88vh;
    overflow-y:auto;
    box-shadow:0 30px 80px rgba(0,0,0,0.35);
    position:relative;
  }
  .modal h3{font-size:24px; margin-bottom:6px;}
  .modal .modal-sub{font-size:13.5px; color:var(--muted); margin-bottom:10px;}
  .modal label{
    display:block;
    font-size:12.5px;
    font-weight:700;
    text-transform:uppercase;
    letter-spacing:0.04em;
    margin:16px 0 6px;
    color:var(--ink-soft);
  }
  .modal input[type="text"],
  .modal input[type="password"],
  .modal textarea{
    width:100%;
    padding:12px 14px;
    border:1px solid var(--line);
    border-radius:10px;
    font:inherit;
    font-size:14.5px;
    background:var(--paper);
    color:var(--ink);
  }
  .modal input[type="text"]:focus,
  .modal input[type="password"]:focus,
  .modal textarea:focus{outline:2px solid var(--accent); outline-offset:1px;}
  .modal input[type="file"]{
    width:100%;
    font-size:13.5px;
  }
  .modal textarea{resize:vertical; min-height:90px;}
  #caseImagePreview{
    width:100%;
    max-height:220px;
    object-fit:cover;
    border-radius:12px;
    margin-top:10px;
    display:none;
  }
  .modal-actions{
    display:flex;
    justify-content:flex-end;
    gap:10px;
    margin-top:24px;
  }
  .modal-error{
    color:var(--coral);
    font-size:13px;
    font-weight:600;
    margin-top:12px;
    display:none;
  }
  .modal-error.show{display:block;}
  .modal-close-x{
    position:absolute;
    top:18px; right:18px;
    width:32px; height:32px;
    border-radius:50%;
    background:var(--paper-dim);
    display:flex; align-items:center; justify-content:center;
    font-size:16px;
    color:var(--ink);
  }

  @media (max-width:900px){
    section{padding:72px 0;}
    .hero-grid{grid-template-columns:1fr; gap:44px;}
    .hero{padding-top:24px;}
    .steps{grid-template-columns:1fr;}
    .plans{grid-template-columns:1fr;}
    .coverage-inner{grid-template-columns:1fr;}
    .footer-grid{grid-template-columns:1fr; gap:28px;}
    .nav-links{display:none;}
    .nav-cta .btn-small-desktop{display:none;}
    .burger{display:flex;}
    .section-head-row{flex-direction:column; align-items:flex-start;}
  }
</style>
</head>
<body>

<header>
  <div class="container nav">
    <a href="#top" class="logo"><span class="drop"></span>WASH-ME</a>
    <nav class="nav-links">
      <a href="#como-funciona">Cómo funciona</a>
      <a href="#casos-exito">Casos de éxito</a>
      <a href="#precios">Precios</a>
      <a href="#cobertura">Cobertura</a>
      <a href="#contacto">Contacto</a>
    </nav>
    <div class="nav-cta">
      <a class="btn btn-dark btn-small" href="https://wa.me/5213329630386?text=Hola%2C%20quiero%20agendar%20un%20lavado%20a%20domicilio%20con%20WASH-ME" target="_blank" rel="noopener">Agendar por WhatsApp</a>
      <button class="burger" id="burgerBtn" aria-label="Abrir menú">
        <span></span><span></span><span></span>
      </button>
    </div>
  </div>
  <div class="mobile-menu" id="mobileMenu">
    <a href="#como-funciona">Cómo funciona</a>
    <a href="#casos-exito">Casos de éxito</a>
    <a href="#precios">Precios</a>
    <a href="#cobertura">Cobertura</a>
    <a href="#contacto">Contacto</a>
  </div>
</header>

<main id="top">

  <!-- HERO -->
  <section class="hero">
    <div class="container hero-grid">
      <div>
        <span class="eyebrow"><span class="dot"></span> Autolavado a domicilio</span>
        <h1>Tu auto queda <em>impecable</em> sin salir de casa</h1>
        <p class="lead">Llevamos el equipo y los productos hasta tu puerta. Tú solo eliges el plan y la hora — nosotros hacemos que brille.</p>
        <div class="hero-ctas">
          <a class="btn btn-primary" href="#precios">Ver planes y precios</a>
          <a class="btn btn-ghost" href="https://wa.me/5213329630386?text=Hola%2C%20quiero%20agendar%20un%20lavado%20a%20domicilio%20con%20WASH-ME" target="_blank" rel="noopener">Escríbenos por WhatsApp</a>
        </div>
        <div class="hero-coverage">
          <span>Servicio disponible únicamente en:</span>
          <span class="chip">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 21s-7-6.2-7-11a7 7 0 0 1 14 0c0 4.8-7 11-7 11z"/><circle cx="12" cy="10" r="2.5"/></svg>
            Zapopan
          </span>
          <span class="chip">
            <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 21s-7-6.2-7-11a7 7 0 0 1 14 0c0 4.8-7 11-7 11z"/><circle cx="12" cy="10" r="2.5"/></svg>
            Guadalajara
          </span>
        </div>
      </div>

      <div>
        <div class="reveal-card">
          <div class="reveal-wrap" id="revealWrap">
            <span class="reveal-tag before">Antes</span>
            <span class="reveal-tag after">WASH-ME</span>
            <svg viewBox="0 0 600 320" xmlns="http://www.w3.org/2000/svg" id="revealSvg">
              <defs>
                <linearGradient id="dirtyBg" x1="0" y1="0" x2="0" y2="1">
                  <stop offset="0" stop-color="#1B2430"/>
                  <stop offset="1" stop-color="#10161F"/>
                </linearGradient>
                <linearGradient id="cleanBg" x1="0" y1="0" x2="1" y2="1">
                  <stop offset="0" stop-color="#0E2A4C"/>
                  <stop offset="1" stop-color="#081B33"/>
                </linearGradient>
                <linearGradient id="carDirty" x1="0" y1="0" x2="0" y2="1">
                  <stop offset="0" stop-color="#8f8879"/>
                  <stop offset="1" stop-color="#5c5648"/>
                </linearGradient>
                <linearGradient id="windowDirty" x1="0" y1="0" x2="0" y2="1">
                  <stop offset="0" stop-color="#4a4d43"/>
                  <stop offset="1" stop-color="#33362d"/>
                </linearGradient>
                <linearGradient id="carClean" x1="0" y1="0" x2="0" y2="1">
                  <stop offset="0" stop-color="#EAF4FF"/>
                  <stop offset="0.45" stop-color="#8FB9FF"/>
                  <stop offset="1" stop-color="#2E6BFF"/>
                </linearGradient>
                <linearGradient id="windowClean" x1="0" y1="0" x2="1" y2="1">
                  <stop offset="0" stop-color="#8FE0F2"/>
                  <stop offset="1" stop-color="#123259"/>
                </linearGradient>
                <linearGradient id="shine" x1="0" y1="0" x2="1" y2="1">
                  <stop offset="0" stop-color="#ffffff" stop-opacity="0"/>
                  <stop offset="0.5" stop-color="#ffffff" stop-opacity="0.85"/>
                  <stop offset="1" stop-color="#ffffff" stop-opacity="0"/>
                </linearGradient>
                <clipPath id="revealClip">
                  <rect id="revealRect" x="0" y="0" width="55%" height="320"/>
                </clipPath>
                <filter id="knobShadow" x="-60%" y="-60%" width="220%" height="220%">
                  <feDropShadow dx="0" dy="3" stdDeviation="4" flood-color="#020a17" flood-opacity="0.45"/>
                </filter>
              </defs>

              <!-- BEFORE: sucio -->
              <rect x="0" y="0" width="600" height="320" fill="url(#dirtyBg)"/>
              <g id="dirtyCar">
                <ellipse cx="300" cy="270" rx="255" ry="14" fill="#000" opacity="0.4"/>
                <ellipse cx="165" cy="250" rx="46" ry="10" fill="#000" opacity="0.35"/>
                <ellipse cx="435" cy="250" rx="46" ry="10" fill="#000" opacity="0.35"/>

                <path d="M60,248 L60,215 C60,195 72,182 92,178 L155,168 C170,130 205,100 255,96 L345,96 C395,100 428,128 442,166 L505,178 C528,182 540,196 540,216 L540,248 Z" fill="url(#carDirty)"/>
                <path d="M185,166 C198,132 225,108 258,104 L342,104 C378,108 402,128 418,164 Z" fill="url(#windowDirty)"/>
                <rect x="297" y="104" width="5" height="62" fill="#242017" opacity="0.7"/>
                <rect x="86" y="240" width="428" height="6" fill="#3a3427" opacity="0.6"/>
                <rect x="58" y="196" width="24" height="10" rx="4" fill="#a89f86"/>
                <rect x="516" y="198" width="22" height="9" rx="4" fill="#87735f"/>
                <path d="M178,158 L192,150 L196,160 L182,166 Z" fill="#736b58"/>

                <circle cx="165" cy="248" r="38" fill="#15130f"/>
                <circle cx="165" cy="248" r="17" fill="#3a352a"/>
                <circle cx="435" cy="248" r="38" fill="#15130f"/>
                <circle cx="435" cy="248" r="17" fill="#3a352a"/>

                <g stroke="#2b2818" stroke-width="2" opacity="0.35">
                  <line x1="120" y1="180" x2="112" y2="240"/>
                  <line x1="200" y1="172" x2="196" y2="238"/>
                  <line x1="270" y1="170" x2="268" y2="242"/>
                  <line x1="360" y1="170" x2="364" y2="242"/>
                  <line x1="430" y1="172" x2="438" y2="238"/>
                  <line x1="490" y1="182" x2="500" y2="240"/>
                </g>
                <g fill="#332f22" opacity="0.55">
                  <circle cx="150" cy="185" r="4"/><circle cx="230" cy="178" r="3"/><circle cx="300" cy="180" r="4"/>
                  <circle cx="370" cy="182" r="3"/><circle cx="460" cy="188" r="4"/><circle cx="500" cy="200" r="3"/>
                  <circle cx="170" cy="210" r="2.5"/><circle cx="410" cy="205" r="3"/>
                </g>
              </g>

              <!-- AFTER: limpio -->
              <g clip-path="url(#revealClip)">
                <rect x="0" y="0" width="600" height="320" fill="url(#cleanBg)"/>
                <g id="cleanCar">
                  <ellipse cx="300" cy="270" rx="255" ry="14" fill="#000" opacity="0.3"/>
                  <ellipse cx="165" cy="250" rx="46" ry="10" fill="#04162e" opacity="0.4"/>
                  <ellipse cx="435" cy="250" rx="46" ry="10" fill="#04162e" opacity="0.4"/>

                  <path d="M60,248 L60,215 C60,195 72,182 92,178 L155,168 C170,130 205,100 255,96 L345,96 C395,100 428,128 442,166 L505,178 C528,182 540,196 540,216 L540,248 Z" fill="url(#carClean)"/>
                  <path d="M185,166 C198,132 225,108 258,104 L342,104 C378,108 402,128 418,164 Z" fill="url(#windowClean)"/>
                  <rect x="297" y="104" width="4" height="62" fill="#eaf4ff" opacity="0.5"/>
                  <rect x="86" y="240" width="428" height="4" fill="#eaf4ff" opacity="0.55"/>
                  <rect x="58" y="196" width="24" height="10" rx="4" fill="#f5fbff"/>
                  <rect x="516" y="198" width="22" height="9" rx="4" fill="#ff5c4d"/>
                  <path d="M178,158 L192,150 L196,160 L182,166 Z" fill="#c9e6ff"/>

                  <circle cx="165" cy="248" r="38" fill="#0a2036"/>
                  <circle cx="165" cy="248" r="17" fill="#c7d8ec"/>
                  <circle cx="435" cy="248" r="38" fill="#0a2036"/>
                  <circle cx="435" cy="248" r="17" fill="#c7d8ec"/>

                  <rect class="shine-el" x="120" y="90" width="60" height="240" fill="url(#shine)" opacity="0.55" transform="rotate(22 300 165)"/>

                  <g class="sparkle" fill="#ffffff">
                    <path d="M240,120 l3,8 l8,3 l-8,3 l-3,8 l-3,-8 l-8,-3 l8,-3 Z"/>
                  </g>
                  <g class="sparkle" fill="#ffffff">
                    <path d="M400,140 l2.4,6.4 l6.4,2.4 l-6.4,2.4 l-2.4,6.4 l-2.4,-6.4 l-6.4,-2.4 l6.4,-2.4 Z"/>
                  </g>
                  <g class="sparkle" fill="#ffffff">
                    <path d="M330,108 l2,5.4 l5.4,2 l-5.4,2 l-2,5.4 l-2,-5.4 l-5.4,-2 l5.4,-2 Z"/>
                  </g>

                  <circle class="bubble" cx="480" cy="130" r="6" fill="#ffffff" opacity="0.55"/>
                  <circle class="bubble" cx="500" cy="155" r="4" fill="#ffffff" opacity="0.45"/>
                  <circle class="bubble" cx="520" cy="120" r="5" fill="#ffffff" opacity="0.5"/>
                </g>
              </g>

              <!-- Manija del slider -->
              <line id="handleLine" x1="330" y1="0" x2="330" y2="320" stroke="#F3F6FB" stroke-width="2.5" opacity="0.85"/>
              <circle id="handleKnob" cx="330" cy="160" r="22" fill="#F3F6FB" filter="url(#knobShadow)"/>
              <circle cx="330" cy="160" r="22" fill="none" stroke="var(--accent)" stroke-width="2" opacity="0.9"/>
              <path id="handleArrows" d="M321,160 l-6,-7 m6,7 l-6,7 M339,160 l6,-7 m-6,7 l6,7" stroke="#2E6BFF" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round" fill="none"/>
            </svg>
          </div>
          <p class="reveal-hint">Desliza para comparar el antes y el después ✨</p>
        </div>
      </div>
    </div>
  </section>

  <!-- COMO FUNCIONA -->
  <section class="how" id="como-funciona">
    <div class="container">
      <div class="section-head">
        <span class="eyebrow"><span class="dot"></span> El proceso</span>
        <h2>Tres pasos y listo</h2>
        <p>Sin filas, sin llevar el coche a ningún lado. Nosotros llegamos con todo lo necesario para dejarlo limpio en tu cochera o cajón de estacionamiento.</p>
      </div>
      <div class="steps">
        <div class="step">
          <div class="num">BÁSICO</div>
          <h3></h3>
          <p>*Ideal para mantener tu vehículo limpio y con una excelente presentación. 
             *Realizamos un lavado exterior con jabón neutro pH, diseñado para cuidar la pintura mientras elimina suciedad, polvo y residuos del camino. 
             *Un servicio rápido, seguro y perfecto para el mantenimiento diario. 
             *Tiempo estimado del servicio de 30 min. a 45 min.</p>
        </div>
        <div class="step">
          <div class="num">PRO</div>
          <h3></h3>
          <p>Incluye todo lo del Plan Básico, además de un aspirado completo del interior para eliminar polvo, tierra y residuos de alfombras, tapetes y asientos. La combinación perfecta para quienes buscan un vehículo limpio tanto por fuera como por dentro, sin invertir horas en hacerlo por su cuenta.
          Tiempo estimado del servicio de 45 min. a 1 hr.</p>
        </div>
        <div class="step">
          <div class="num">PREMIUM</div>
          <h3></h3>
          <p>Nuestro servicio más completo. Incluye todo lo del Plan Pro, además de una limpieza profunda del interior, restauración de plásticos para devolverles su apariencia original y un encerado exterior que aporta brillo y una capa extra de protección para la pintura. Es la mejor opción para quienes quieren mantener su vehículo impecable, protegido y con un acabado de nivel profesional.
Tiempo estimado del servicio de 1 hr y 15 min. a 1 hr y 30 min.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- CASOS DE ÉXITO -->
  <section class="cases" id="casos-exito">
    <div class="container">
      <div class="section-head-row">
        <div class="section-head">
          <span class="eyebrow"><span class="dot"></span> Galería</span>
          <h2>Casos de éxito</h2>
          <p>Coches y camionetas que dejamos brillando. Califica los que más te gusten.</p>
        </div>
        <div class="admin-controls">
          <span class="admin-status" id="adminStatus" style="display:none;"><span class="dot"></span> Modo administrador</span>
          <button class="btn btn-primary btn-small" id="addCaseBtn" style="display:none;">+ Agregar caso</button>
          <button class="btn btn-ghost-dark btn-small" id="adminToggleBtn">Acceder como administrador</button>
        </div>
      </div>

      <div class="cases-grid" id="casesGrid"></div>
      <p class="cases-empty" id="casesEmpty">Aún no hay casos publicados. Muy pronto verás aquí nuestros mejores trabajos.</p>
    </div>
  </section>

  <!-- PRECIOS -->
  <section class="pricing" id="precios">
    <div class="container">
      <div class="section-head">
        <span class="eyebrow" style="background:rgba(243,246,251,0.08); border-color:rgba(243,246,251,0.18); color:rgba(243,246,251,0.75);"><span class="dot"></span> Planes</span>
        <h2>Un plan para cada nivel de brillo</h2>
        <p>Elige el tipo de vehículo y el plan que necesitas. Los tres incluyen desplazamiento a domicilio dentro de Zapopan y Guadalajara.</p>
      </div>

      <div class="switcher" role="tablist">
        <button type="button" class="active" data-vehicle="coches" role="tab" aria-selected="true">🚗 Coches</button>
        <button type="button" data-vehicle="camionetas" role="tab" aria-selected="false">🚙 Camionetas</button>
      </div>

      <div class="plans vehicle-group active" data-group="coches">
        <div class="plan">
          <h3>Básico</h3>
          <div class="price">$150<small>&nbsp;MXN</small></div>
          <p class="desc">El refresh esencial para el día a día.</p>
          <ul>
            <li>✔️ Lavado exterior a mano</li>
            <li>✔️ Enjuague a presión</li>
            <li>✔️ Secado con microfibra</li>
            <li>✔️ Limpieza de llantas y rines</li>
          </ul>
          <a class="btn btn-primary" href="https://wa.me/5213329630386?text=Hola%2C%20quiero%20agendar%20el%20plan%20B%C3%A1sico%20para%20mi%20coche%20a%20domicilio" target="_blank" rel="noopener">Agendar Básico</a>
        </div>

        <div class="plan featured">
          <span class="badge">Más pedido</span>
          <h3>Pro</h3>
          <div class="price">$200<small>&nbsp;MXN</small></div>
          <p class="desc">Exterior e interior en un solo servicio.</p>
          <ul>
            <li>✔️ Todo lo del plan Básico</li>
            <li>✔️ Aspirado interior completo</li>
            <li>✔️ Limpieza de tablero y vidrios</li>
            <li>✔️ Aromatizante a elegir</li>
          </ul>
          <a class="btn btn-primary" href="https://wa.me/5213329630386?text=Hola%2C%20quiero%20agendar%20el%20plan%20Pro%20para%20mi%20coche%20a%20domicilio" target="_blank" rel="noopener">Agendar Pro</a>
        </div>

        <div class="plan">
          <h3>Premium</h3>
          <div class="price">$250<small>&nbsp;MXN</small></div>
          <p class="desc">Detallado completo, como recién salido de agencia.</p>
          <ul>
            <li>✔️ Todo lo del plan Pro</li>
            <li>✔️ Encerado protector</li>
            <li>✔️ Abrillantado de llantas</li>
            <li>✔️ Limpieza profunda de vestiduras</li>
          </ul>
          <a class="btn btn-primary" href="https://wa.me/5213329630386?text=Hola%2C%20quiero%20agendar%20el%20plan%20Premium%20para%20mi%20coche%20a%20domicilio" target="_blank" rel="noopener">Agendar Premium</a>
        </div>
      </div>

      <div class="plans vehicle-group" data-group="camionetas">
        <div class="plan">
          <h3>Básico</h3>
          <div class="price">$200<small>&nbsp;MXN</small></div>
          <p class="desc">El refresh esencial para el día a día.</p>
          <ul>
            <li>✔️ Lavado exterior a mano</li>
            <li>✔️ Enjuague a presión</li>
            <li>✔️ Secado con microfibra</li>
            <li>✔️ Limpieza de llantas y rines</li>
          </ul>
          <a class="btn btn-primary" href="https://wa.me/5213329630386?text=Hola%2C%20quiero%20agendar%20el%20plan%20B%C3%A1sico%20para%20mi%20camioneta%20a%20domicilio" target="_blank" rel="noopener">Agendar Básico</a>
        </div>

        <div class="plan featured">
          <span class="badge">Más pedido</span>
          <h3>Pro</h3>
          <div class="price">$250<small>&nbsp;MXN</small></div>
          <p class="desc">Exterior e interior en un solo servicio.</p>
          <ul>
            <li>✔️ Todo lo del plan Básico</li>
            <li>✔️ Aspirado interior completo</li>
            <li>✔️ Limpieza de tablero y vidrios</li>
            <li>✔️ Aromatizante a elegir</li>
          </ul>
          <a class="btn btn-primary" href="https://wa.me/5213329630386?text=Hola%2C%20quiero%20agendar%20el%20plan%20Pro%20para%20mi%20camioneta%20a%20domicilio" target="_blank" rel="noopener">Agendar Pro</a>
        </div>

        <div class="plan">
          <h3>Premium</h3>
          <div class="price">$300<small>&nbsp;MXN</small></div>
          <p class="desc">Detallado completo, como recién salido de agencia.</p>
          <ul>
            <li>✔️ Todo lo del plan Pro</li>
            <li>✔️ Encerado protector</li>
            <li>✔️ Abrillantado de llantas</li>
            <li>✔️ Limpieza profunda de vestiduras</li>
          </ul>
          <a class="btn btn-primary" href="https://wa.me/5213329630386?text=Hola%2C%20quiero%20agendar%20el%20plan%20Premium%20para%20mi%20camioneta%20a%20domicilio" target="_blank" rel="noopener">Agendar Premium</a>
        </div>
      </div>
    </div>
  </section>

  <!-- COBERTURA -->
  <section class="coverage" id="cobertura">
    <div class="container coverage-inner">
      <div>
        <span class="eyebrow"><span class="dot"></span> Zona de servicio</span>
        <h2 style="font-size:clamp(30px,3.6vw,42px); margin-top:16px;">Por ahora, solo aquí</h2>
        <div class="coverage-cities">
          <div class="city-card">
            <div class="city-name">Zapopan</div>
            <div class="city-tag">Cobertura activa</div>
          </div>
          <div class="city-card">
            <div class="city-name">Guadalajara</div>
            <div class="city-tag">Cobertura activa</div>
          </div>
        </div>
        <div class="notice">
          <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M12 9v4M12 17h.01M10.29 3.86l-8.18 14.18A2 2 0 0 0 3.82 21h16.36a2 2 0 0 0 1.71-2.96L13.71 3.86a2 2 0 0 0-3.42 0z"/></svg>
          <span>El servicio de WASH-ME se brinda <strong>únicamente a domicilio dentro de Zapopan y Guadalajara</strong>. Por el momento no cubrimos otros municipios ni zonas foráneas.</span>
        </div>
      </div>
      <div class="map-art">
        <svg viewBox="0 0 320 260" width="100%">
          <circle cx="160" cy="130" r="120" fill="var(--paper)" stroke="var(--line)" stroke-width="1.5"/>
          <circle cx="115" cy="105" r="7" fill="var(--accent)"/>
          <text x="115" y="90" text-anchor="middle" font-family="Work Sans, sans-serif" font-weight="700" font-size="12" fill="var(--ink)">Zapopan</text>
          <circle cx="185" cy="150" r="7" fill="var(--aqua)"/>
          <text x="185" y="175" text-anchor="middle" font-family="Work Sans, sans-serif" font-weight="700" font-size="12" fill="var(--ink)">Guadalajara</text>
          <path d="M115,105 Q150,120 185,150" stroke="var(--ink)" stroke-width="1.5" stroke-dasharray="4 5" fill="none" opacity="0.4"/>
        </svg>
      </div>
    </div>
  </section>

  <!-- CTA FINAL -->
  <section class="cta-band">
    <div class="container cta-inner">
      <div>
        <h2>¿Listo para que tu auto brille?</h2>
        <p>Agenda hoy y elige el horario que mejor te acomode.</p>
      </div>
      <a class="btn btn-dark" href="https://wa.me/5213329630386?text=Hola%2C%20quiero%20agendar%20un%20lavado%20a%20domicilio%20con%20WASH-ME" target="_blank" rel="noopener">Agendar por WhatsApp</a>
    </div>
  </section>

</main>

<footer id="contacto">
  <div class="container">
    <div class="footer-grid">
      <div>
        <a href="#top" class="logo"><span class="drop"></span>WASH-ME</a>
        <p>Autolavado a domicilio para coches y camionetas. Llevamos el equipo hasta tu puerta en Zapopan y Guadalajara.</p>
      </div>
      <div class="footer-col">
        <h4>Contacto</h4>
        <a href="https://wa.me/5213329630386" target="_blank" rel="noopener">+52 1 33 2963 0386</a>
        <a href="#precios">Ver planes y precios</a>
      </div>
      <div class="footer-col">
        <h4>Cobertura</h4>
        <span>Zapopan</span>
        <span>Guadalajara</span>
      </div>
    </div>
    <div class="footer-bottom">
      <span>© 2026 WASH-ME. Todos los derechos reservados.</span>
      <span>Servicio a domicilio · Zapopan y Guadalajara</span>
    </div>
  </div>
</footer>

<a class="wa-float" href="https://wa.me/5213329630386?text=Hola%2C%20quiero%20agendar%20un%20lavado%20a%20domicilio%20con%20WASH-ME" target="_blank" rel="noopener" aria-label="Escríbenos por WhatsApp">
  <svg viewBox="0 0 24 24" fill="currentColor"><path d="M12.04 2C6.58 2 2.13 6.45 2.13 11.91c0 1.75.46 3.46 1.32 4.96L2.05 22l5.25-1.38a9.9 9.9 0 0 0 4.74 1.21h.01c5.46 0 9.91-4.45 9.91-9.91 0-2.65-1.03-5.14-2.9-7.01A9.86 9.86 0 0 0 12.04 2m0 1.8a8.1 8.1 0 0 1 5.75 2.38 8.06 8.06 0 0 1 2.38 5.73c0 4.48-3.65 8.13-8.14 8.13a8.1 8.1 0 0 1-4.13-1.13l-.3-.17-3.11.82.83-3.04-.19-.31a8.06 8.06 0 0 1-1.24-4.31c0-4.49 3.65-8.14 8.15-8.14M8.53 6.98c-.17 0-.44.06-.67.31-.23.25-.88.86-.88 2.1 0 1.24.9 2.44 1.02 2.6.13.17 1.76 2.83 4.38 3.85 2.17.85 2.61.68 3.08.64.47-.04 1.52-.62 1.74-1.22.21-.6.21-1.11.15-1.22-.06-.11-.23-.17-.48-.3-.25-.13-1.52-.75-1.76-.83-.23-.09-.4-.13-.58.13-.17.25-.66.83-.81 1-.15.17-.29.19-.54.06-.25-.13-1.05-.39-2-1.23-.74-.66-1.24-1.47-1.39-1.72-.14-.25-.02-.38.11-.51.11-.11.25-.29.38-.44.13-.15.17-.25.25-.42.08-.17.04-.31-.02-.44-.06-.13-.58-1.4-.8-1.92-.21-.5-.42-.44-.58-.45z"/></svg>
</a>

<!-- MODAL: LOGIN ADMIN -->
<div class="modal-overlay" id="loginModal">
  <div class="modal">
    <button class="modal-close-x" id="closeLoginX">✕</button>
    <h3>Acceso administrador</h3>
    <p class="modal-sub">Solo el equipo de WASH-ME puede publicar casos de éxito.</p>
    <label for="adminEmailInput">Correo</label>
    <input type="text" id="adminEmailInput" placeholder="admin@washme.com" autocomplete="username">
    <label for="adminPasswordInput">Contraseña</label>
    <input type="password" id="adminPasswordInput" placeholder="••••••••" autocomplete="current-password">
    <p class="modal-error" id="loginError">Correo o contraseña incorrectos. Inténtalo de nuevo.</p>
    <div class="modal-actions">
      <button class="btn btn-ghost-dark btn-small" id="cancelLoginBtn">Cancelar</button>
      <button class="btn btn-primary btn-small" id="confirmLoginBtn">Entrar</button>
    </div>
  </div>
</div>

<!-- MODAL: AGREGAR / EDITAR CASO -->
<div class="modal-overlay" id="caseModal">
  <div class="modal">
    <button class="modal-close-x" id="closeCaseX">✕</button>
    <h3 id="caseModalTitle">Agregar caso de éxito</h3>
    <p class="modal-sub">Sube una foto y describe brevemente el trabajo realizado.</p>

    <label for="caseImageInput">Foto</label>
    <input type="file" id="caseImageInput" accept="image/*">
    <img id="caseImagePreview" alt="Vista previa">

    <label for="caseTitleInput">Título</label>
    <input type="text" id="caseTitleInput" placeholder="Ej. Suburban recién detallada">

    <label for="caseTextInput">Breve descripción del caso</label>
    <textarea id="caseTextInput" placeholder="Cuenta brevemente qué se hizo, el plan aplicado, el resultado..."></textarea>

    <p class="modal-error" id="caseError">Falta la foto o el título del caso.</p>

    <div class="modal-actions">
      <button class="btn btn-ghost-dark btn-small" id="cancelCaseBtn">Cancelar</button>
      <button class="btn btn-primary btn-small" id="saveCaseBtn">Guardar caso</button>
    </div>
  </div>
</div>

<script>
  /* ============ Menú móvil ============ */
  const burgerBtn = document.getElementById('burgerBtn');
  const mobileMenu = document.getElementById('mobileMenu');
  burgerBtn.addEventListener('click', () => mobileMenu.classList.toggle('open'));
  mobileMenu.querySelectorAll('a').forEach(link => {
    link.addEventListener('click', () => mobileMenu.classList.remove('open'));
  });

  /* ============ Selector Coches / Camionetas ============ */
  const switcherBtns = document.querySelectorAll('.switcher button');
  const groups = document.querySelectorAll('.vehicle-group');
  switcherBtns.forEach(btn => {
    btn.addEventListener('click', () => {
      switcherBtns.forEach(b => { b.classList.remove('active'); b.setAttribute('aria-selected','false'); });
      btn.classList.add('active');
      btn.setAttribute('aria-selected','true');
      const target = btn.dataset.vehicle;
      groups.forEach(g => g.classList.toggle('active', g.dataset.group === target));
    });
  });

  /* ============ Antes / después ============ */
  const wrap = document.getElementById('revealWrap');
  const rect = document.getElementById('revealRect');
  const line = document.getElementById('handleLine');
  const knob = document.getElementById('handleKnob');
  const arrows = document.getElementById('handleArrows');
  let dragging = false;

  function setReveal(pct){
    pct = Math.max(4, Math.min(96, pct));
    rect.setAttribute('width', pct + '%');
    const x = (pct / 100) * 600;
    line.setAttribute('x1', x); line.setAttribute('x2', x);
    knob.setAttribute('cx', x);
    arrows.setAttribute('transform', 'translate(' + (x - 330) + ',0)');
  }
  function pointerToPct(clientX){
    const box = wrap.getBoundingClientRect();
    return ((clientX - box.left) / box.width) * 100;
  }
  function startDrag(e){ dragging = true; move(e); }
  function move(e){
    if(!dragging) return;
    const clientX = e.touches ? e.touches[0].clientX : e.clientX;
    setReveal(pointerToPct(clientX));
  }
  function endDrag(){ dragging = false; }
  wrap.addEventListener('mousedown', startDrag);
  window.addEventListener('mousemove', move);
  window.addEventListener('mouseup', endDrag);
  wrap.addEventListener('touchstart', startDrag, {passive:true});
  window.addEventListener('touchmove', move, {passive:true});
  window.addEventListener('touchend', endDrag);

  let demo = 55, dir = 1, demoCount = 0;
  const demoInterval = setInterval(() => {
    if(dragging){ clearInterval(demoInterval); return; }
    demo += dir * 0.6;
    if(demo > 70 || demo < 40) dir *= -1;
    setReveal(demo);
    demoCount++;
    if(demoCount > 160) clearInterval(demoInterval);
  }, 30);
  setReveal(55);

  /* ============================================================
     CASOS DE ÉXITO — conectado a Firebase (Firestore + Auth)
     -------------------------------------------------------------
     1) Crea un proyecto en https://console.firebase.google.com
     2) Agrega una "Web app" y copia su firebaseConfig aquí abajo,
        reemplazando el objeto de ejemplo.
     3) Activa Firestore Database (modo producción) y pega las
        reglas de seguridad sugeridas en el archivo FIREBASE_SETUP.md.
     4) Activa Authentication → Sign-in method → habilita:
          - Correo electrónico/contraseña
          - Anónimo
     5) En Authentication → Users, crea manualmente el usuario
        administrador (correo + contraseña) y pon ese mismo correo
        en ADMIN_EMAIL más abajo.
     Mientras firebaseConfig no esté configurado, esta sección
     mostrará un aviso y el resto de la página seguirá funcionando
     con normalidad.
  ============================================================ */
</script>

<script type="module">
  import { initializeApp } from "https://www.gstatic.com/firebasejs/10.12.2/firebase-app.js";
  import {
    getFirestore, collection, addDoc, updateDoc, deleteDoc, doc,
    onSnapshot, query, orderBy, serverTimestamp
  } from "https://www.gstatic.com/firebasejs/10.12.2/firebase-firestore.js";
  import {
    getAuth, signInAnonymously, signInWithEmailAndPassword, signOut, onAuthStateChanged
  } from "https://www.gstatic.com/firebasejs/10.12.2/firebase-auth.js";

  /* -------- 1. PEGA AQUÍ TU CONFIGURACIÓN DE FIREBASE -------- */
  const firebaseConfig = {
    apiKey: "TU_API_KEY",
    authDomain: "TU_PROYECTO.firebaseapp.com",
    projectId: "TU_PROYECTO",
    storageBucket: "TU_PROYECTO.appspot.com",
    messagingSenderId: "TU_SENDER_ID",
    appId: "TU_APP_ID"
  };

  /* Correo del usuario administrador (creado en Firebase Auth) */
  const ADMIN_EMAIL = "admin@washme.com";

  const casesGrid = document.getElementById('casesGrid');
  const casesEmpty = document.getElementById('casesEmpty');
  const adminStatus = document.getElementById('adminStatus');
  const addCaseBtn = document.getElementById('addCaseBtn');
  const adminToggleBtn = document.getElementById('adminToggleBtn');

  const loginModal = document.getElementById('loginModal');
  const adminEmailInput = document.getElementById('adminEmailInput');
  const adminPasswordInput = document.getElementById('adminPasswordInput');
  const loginError = document.getElementById('loginError');
  const confirmLoginBtn = document.getElementById('confirmLoginBtn');
  const cancelLoginBtn = document.getElementById('cancelLoginBtn');
  const closeLoginX = document.getElementById('closeLoginX');

  const caseModal = document.getElementById('caseModal');
  const caseModalTitle = document.getElementById('caseModalTitle');
  const caseImageInput = document.getElementById('caseImageInput');
  const caseImagePreview = document.getElementById('caseImagePreview');
  const caseTitleInput = document.getElementById('caseTitleInput');
  const caseTextInput = document.getElementById('caseTextInput');
  const caseError = document.getElementById('caseError');
  const saveCaseBtn = document.getElementById('saveCaseBtn');
  const cancelCaseBtn = document.getElementById('cancelCaseBtn');
  const closeCaseX = document.getElementById('closeCaseX');

  const isConfigured = firebaseConfig.apiKey && firebaseConfig.apiKey.indexOf('TU_') !== 0;

  if(!isConfigured){
    casesEmpty.textContent = 'Esta sección aún no está conectada a Firebase. Sigue las instrucciones en FIREBASE_SETUP.md para activarla.';
    casesEmpty.style.display = 'block';
  } else {
    const app = initializeApp(firebaseConfig);
    const db = getFirestore(app);
    const auth = getAuth(app);

    let cases = [];
    let currentUid = null;
    let isAdmin = false;

    function escapeHtml(str){
      const div = document.createElement('div');
      div.textContent = str || '';
      return div.innerHTML;
    }

    function updateAdminUI(){
      adminStatus.style.display = isAdmin ? 'inline-flex' : 'none';
      addCaseBtn.style.display = isAdmin ? 'inline-flex' : 'none';
      adminToggleBtn.textContent = isAdmin ? 'Cerrar sesión admin' : 'Acceder como administrador';
    }

    function renderCases(){
      casesGrid.innerHTML = '';
      casesEmpty.style.display = cases.length === 0 ? 'block' : 'none';
      if(cases.length === 0){
        casesEmpty.textContent = 'Aún no hay casos publicados. Muy pronto verás aquí nuestros mejores trabajos.';
      }

      cases.forEach(c => {
        const votes = c.votes || {};
        const myVote = (currentUid && votes[currentUid]) || { liked:false, hearted:false, rating:null };

        let likes = 0, hearts = 0, ratingSum = 0, ratingCount = 0;
        Object.values(votes).forEach(v => {
          if(v.liked) likes++;
          if(v.hearted) hearts++;
          if(v.rating){ ratingSum += v.rating; ratingCount++; }
        });
        const avg = ratingCount > 0 ? (ratingSum / ratingCount).toFixed(1) : null;

        const card = document.createElement('article');
        card.className = 'case-card';
        card.dataset.id = c.id;

        let starsHtml = '';
        for(let i = 1; i <= 5; i++){
          starsHtml += '<button type="button" class="star' + (myVote.rating && i <= myVote.rating ? ' filled' : '') + '" data-star="' + i + '">★</button>';
        }

        card.innerHTML =
          '<div class="case-img-wrap">' +
            (isAdmin ?
              '<div class="case-admin-actions">' +
                '<button class="icon-btn edit-btn" title="Editar">✎</button>' +
                '<button class="icon-btn danger delete-btn" title="Eliminar">🗑</button>' +
              '</div>' : '') +
            '<img src="' + c.image + '" alt="' + escapeHtml(c.title) + '">' +
          '</div>' +
          '<div class="case-body">' +
            '<span class="case-date">' + escapeHtml(c.date) + '</span>' +
            '<h3>' + escapeHtml(c.title) + '</h3>' +
            '<p>' + escapeHtml(c.text) + '</p>' +
            '<div class="case-reactions">' +
              '<div class="react-buttons">' +
                '<button class="react-btn like' + (myVote.liked ? ' active' : '') + '" data-type="like">👍 <span>' + likes + '</span></button>' +
                '<button class="react-btn heart' + (myVote.hearted ? ' active' : '') + '" data-type="heart">❤️ <span>' + hearts + '</span></button>' +
              '</div>' +
              '<div class="stars">' + starsHtml +
                '<span class="stars-avg">' + (avg ? avg + ' ★ (' + ratingCount + ')' : 'Sin calificar') + '</span>' +
              '</div>' +
            '</div>' +
          '</div>';

        casesGrid.appendChild(card);
      });
    }

    /* -------- Suscripción en tiempo real a Firestore -------- */
    onSnapshot(query(collection(db, 'casos'), orderBy('createdAt', 'desc')), (snapshot) => {
      cases = snapshot.docs.map(d => ({ id: d.id, ...d.data() }));
      renderCases();
    }, (err) => {
      console.error('Error leyendo casos de éxito:', err);
      casesEmpty.textContent = 'No se pudieron cargar los casos de éxito. Revisa la configuración de Firebase.';
      casesEmpty.style.display = 'block';
    });

    /* -------- Sesión: administrador o visitante anónimo -------- */
    onAuthStateChanged(auth, (user) => {
      if(!user){
        signInAnonymously(auth).catch(err => console.error('Error de sesión anónima:', err));
        return;
      }
      currentUid = user.uid;
      isAdmin = !user.isAnonymous && user.email === ADMIN_EMAIL;
      updateAdminUI();
      renderCases();
    });

    /* -------- Reacciones (like / corazón / estrellas) — abiertas a todos -------- */
    casesGrid.addEventListener('click', async (e) => {
      const card = e.target.closest('.case-card');
      if(!card || !currentUid) return;
      const id = card.dataset.id;
      const c = cases.find(x => x.id === id);
      if(!c) return;
      const votes = c.votes || {};
      const myVote = votes[currentUid] || { liked:false, hearted:false, rating:null };

      const reactBtn = e.target.closest('.react-btn');
      if(reactBtn){
        const type = reactBtn.dataset.type;
        const field = type === 'like' ? 'liked' : 'hearted';
        const newValue = !myVote[field];
        try{
          await updateDoc(doc(db, 'casos', id), { ['votes.' + currentUid + '.' + field]: newValue });
        }catch(err){ console.error('No se pudo guardar tu reacción:', err); }
        return;
      }

      const starBtn = e.target.closest('.star');
      if(starBtn){
        const stars = parseInt(starBtn.dataset.star, 10);
        try{
          await updateDoc(doc(db, 'casos', id), { ['votes.' + currentUid + '.rating']: stars });
        }catch(err){ console.error('No se pudo guardar tu calificación:', err); }
        return;
      }

      if(e.target.closest('.edit-btn') && isAdmin){
        openCaseModal(c);
        return;
      }
      if(e.target.closest('.delete-btn') && isAdmin){
        if(confirm('¿Eliminar este caso de éxito? Esta acción no se puede deshacer.')){
          try{ await deleteDoc(doc(db, 'casos', id)); }
          catch(err){ alert('No se pudo eliminar. Revisa tu conexión o permisos.'); }
        }
      }
    });

    /* -------- Login administrador (correo + contraseña reales) -------- */
    function openLoginModal(){
      adminEmailInput.value = '';
      adminPasswordInput.value = '';
      loginError.classList.remove('show');
      loginModal.classList.add('open');
      adminEmailInput.focus();
    }
    function closeLoginModal(){ loginModal.classList.remove('open'); }

    adminToggleBtn.addEventListener('click', async () => {
      if(isAdmin){
        await signOut(auth);
      } else {
        openLoginModal();
      }
    });
    cancelLoginBtn.addEventListener('click', closeLoginModal);
    closeLoginX.addEventListener('click', closeLoginModal);
    loginModal.addEventListener('click', (e) => { if(e.target === loginModal) closeLoginModal(); });

    confirmLoginBtn.addEventListener('click', async () => {
      try{
        await signInWithEmailAndPassword(auth, adminEmailInput.value.trim(), adminPasswordInput.value);
        closeLoginModal();
      }catch(err){
        loginError.classList.add('show');
      }
    });
    adminPasswordInput.addEventListener('keydown', (e) => { if(e.key === 'Enter') confirmLoginBtn.click(); });

    /* -------- Agregar / editar caso (solo admin) -------- */
    let pendingImageData = null;
    let editingCaseId = null;

    function openCaseModal(existing){
      editingCaseId = existing ? existing.id : null;
      pendingImageData = existing ? existing.image : null;
      caseModalTitle.textContent = existing ? 'Editar caso de éxito' : 'Agregar caso de éxito';
      caseTitleInput.value = existing ? existing.title : '';
      caseTextInput.value = existing ? existing.text : '';
      caseError.classList.remove('show');
      if(existing){
        caseImagePreview.src = existing.image;
        caseImagePreview.style.display = 'block';
      } else {
        caseImagePreview.src = '';
        caseImagePreview.style.display = 'none';
      }
      caseImageInput.value = '';
      caseModal.classList.add('open');
    }
    function closeCaseModal(){ caseModal.classList.remove('open'); }

    addCaseBtn.addEventListener('click', () => { if(isAdmin) openCaseModal(null); });
    cancelCaseBtn.addEventListener('click', closeCaseModal);
    closeCaseX.addEventListener('click', closeCaseModal);
    caseModal.addEventListener('click', (e) => { if(e.target === caseModal) closeCaseModal(); });

    function fileToCompressedDataURL(file, maxWidth, quality){
      return new Promise((resolve, reject) => {
        const reader = new FileReader();
        reader.onload = (e) => {
          const img = new Image();
          img.onload = () => {
            const scale = Math.min(1, maxWidth / img.width);
            const canvas = document.createElement('canvas');
            canvas.width = Math.round(img.width * scale);
            canvas.height = Math.round(img.height * scale);
            const ctx = canvas.getContext('2d');
            ctx.drawImage(img, 0, 0, canvas.width, canvas.height);
            resolve(canvas.toDataURL('image/jpeg', quality));
          };
          img.onerror = reject;
          img.src = e.target.result;
        };
        reader.onerror = reject;
        reader.readAsDataURL(file);
      });
    }

    caseImageInput.addEventListener('change', async (e) => {
      const file = e.target.files[0];
      if(!file) return;
      try{
        /* Comprimida para caber en un documento de Firestore (límite 1 MB) */
        const dataUrl = await fileToCompressedDataURL(file, 700, 0.72);
        pendingImageData = dataUrl;
        caseImagePreview.src = dataUrl;
        caseImagePreview.style.display = 'block';
      }catch(err){
        alert('No se pudo cargar la imagen. Intenta con otra foto.');
      }
    });

    saveCaseBtn.addEventListener('click', async () => {
      if(!isAdmin) return;
      const title = caseTitleInput.value.trim();
      const text = caseTextInput.value.trim();

      if(!title || !pendingImageData){
        caseError.classList.add('show');
        return;
      }
      caseError.classList.remove('show');
      saveCaseBtn.disabled = true;

      try{
        if(editingCaseId){
          await updateDoc(doc(db, 'casos', editingCaseId), { title, text, image: pendingImageData });
        } else {
          await addDoc(collection(db, 'casos'), {
            image: pendingImageData,
            title,
            text,
            date: new Date().toLocaleDateString('es-MX', { day:'numeric', month:'short', year:'numeric' }),
            votes: {},
            createdAt: serverTimestamp()
          });
        }
        closeCaseModal();
      }catch(err){
        alert('No se pudo guardar el caso. Revisa tu conexión o los permisos de Firestore.');
      }finally{
        saveCaseBtn.disabled = false;
      }
    });
  }
</script>

</body>
</html>
