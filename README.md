# mevbrende.github.io
<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Мы в бренде — Байерский сервис</title>
<link href="https://fonts.googleapis.com/css2?family=Unbounded:wght@300;400;600;700&family=Manrope:wght@400;500;600&display=swap" rel="stylesheet"/>
<style>
:root {
  --p:   #6B3FA0;
  --plt: #9B6FD0;
  --lav: #EDE6FA;
  --bg:  #F8F5FF;
  --w:   #FFFFFF;
  --ink: #1A1025;
  --gr:  #6B6080;
  --brd: #DDD5F0;
  --r:   14px;
}
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }
body { font-family: 'Manrope', sans-serif; background: var(--bg); color: var(--ink); line-height: 1.6; }

/* NAV */
nav {
  display: flex; align-items: center; justify-content: space-between;
  padding: 0 5%; height: 64px;
  background: var(--w); border-bottom: 1px solid var(--brd);
  position: sticky; top: 0; z-index: 99;
}
.logo { font-family: 'Unbounded', sans-serif; font-size: 1.05rem; font-weight: 700; color: var(--p); text-decoration: none; letter-spacing: -0.02em; }
.nav-menu { display: flex; gap: 2.4rem; list-style: none; }
.nav-menu a { font-size: 0.8rem; font-weight: 500; color: var(--gr); text-decoration: none; letter-spacing: 0.04em; transition: color .2s; }
.nav-menu a:hover { color: var(--p); }
.nav-cta { background: var(--p); color: #fff; font-family: 'Manrope', sans-serif; font-size: 0.8rem; font-weight: 600; padding: 0.5rem 1.3rem; border-radius: 50px; text-decoration: none; transition: background .2s; }
.nav-cta:hover { background: var(--plt); }

/* HERO */
#hero {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: auto auto;
  min-height: calc(100vh - 64px);
  overflow: hidden;
}
.hero-left {
  grid-column: 1; grid-row: 1 / 3;
  display: flex; flex-direction: column; justify-content: center;
  padding: 6rem 4rem 6rem 5%;
  border-right: 1px solid var(--brd);
  position: relative;
}
.hero-left::before {
  content: '';
  position: absolute;
  width: 500px; height: 500px;
  background: radial-gradient(circle, rgba(107,63,160,0.08) 0%, transparent 70%);
  top: -100px; left: -100px;
  pointer-events: none;
}
.hero-tag {
  display: inline-flex; align-items: center; gap: 0.5rem;
  font-size: 0.68rem; font-weight: 600; letter-spacing: 0.18em; text-transform: uppercase;
  color: var(--p); background: var(--lav); padding: 0.3rem 0.9rem;
  border-radius: 50px; margin-bottom: 1.8rem; width: fit-content;
}
.hero-tag span { width: 6px; height: 6px; background: var(--p); border-radius: 50%; }
h1 {
  font-family: 'Unbounded', sans-serif;
  font-size: clamp(2rem, 3.2vw, 3.6rem);
  font-weight: 300; line-height: 1.15; color: var(--ink);
  margin-bottom: 1.4rem; letter-spacing: -0.02em;
}
h1 strong { font-weight: 700; color: var(--p); display: block; }
.hero-desc { font-size: 0.97rem; color: var(--gr); max-width: 440px; margin-bottom: 2.4rem; }
.btns { display: flex; gap: 0.8rem; flex-wrap: wrap; }
.btn-main {
  display: inline-flex; align-items: center; gap: 0.5rem;
  background: var(--p); color: #fff;
  font-family: 'Manrope', sans-serif; font-size: 0.88rem; font-weight: 600;
  padding: 0.85rem 1.8rem; border-radius: 50px; text-decoration: none;
  transition: background .2s, transform .15s;
}
.btn-main:hover { background: var(--plt); transform: translateY(-1px); }
.btn-ghost {
  display: inline-flex; align-items: center; gap: 0.5rem;
  color: var(--p); font-family: 'Manrope', sans-serif; font-size: 0.88rem; font-weight: 500;
  padding: 0.85rem 1.8rem; border-radius: 50px; text-decoration: none;
  border: 1.5px solid var(--brd); transition: border-color .2s, background .2s;
}
.btn-ghost:hover { border-color: var(--plt); background: var(--lav); }
.hero-stats {
  display: flex; gap: 2.5rem; margin-top: 3.5rem;
  padding-top: 2.5rem; border-top: 1px solid var(--brd);
}
.stat-n { font-family: 'Unbounded', sans-serif; font-size: 2rem; font-weight: 700; color: var(--p); line-height: 1; }
.stat-l { font-size: 0.75rem; color: var(--gr); font-weight: 500; margin-top: 0.2rem; }

.hero-right-top {
  grid-column: 2; grid-row: 1;
  background: var(--p); padding: 3.5rem 4rem 3.5rem 3.5rem;
  display: flex; flex-direction: column; justify-content: flex-end;
  position: relative; overflow: hidden; min-height: 52%;
}
.hero-right-top::before { content: ''; position: absolute; width: 360px; height: 360px; border: 1px solid rgba(255,255,255,0.1); border-radius: 50%; top: -80px; right: -80px; }
.hero-right-top::after { content: ''; position: absolute; width: 220px; height: 220px; border: 1px solid rgba(255,255,255,0.07); border-radius: 50%; bottom: 40px; left: 40px; }
.big-label { font-family: 'Unbounded', sans-serif; font-size: clamp(3.5rem, 6vw, 7rem); font-weight: 700; color: rgba(255,255,255,0.08); line-height: 1; position: absolute; top: 2rem; left: 2.5rem; letter-spacing: -0.04em; pointer-events: none; }
.hero-right-top-content { position: relative; z-index: 1; }
.hero-right-top-content p { font-size: 0.8rem; font-weight: 600; letter-spacing: 0.15em; text-transform: uppercase; color: rgba(255,255,255,0.5); margin-bottom: 0.8rem; }
.hero-right-top-content h2 { font-family: 'Unbounded', sans-serif; font-size: clamp(1.3rem, 2.2vw, 2rem); font-weight: 300; color: #fff; line-height: 1.25; }
.hero-right-top-content h2 b { font-weight: 700; }

.hero-right-bottom {
  grid-column: 2; grid-row: 2;
  background: var(--w); padding: 2.5rem 3.5rem;
  border-top: 1px solid var(--brd);
  display: grid; grid-template-columns: 1fr 1fr; gap: 1.5rem;
}
.feat { display: flex; align-items: flex-start; gap: 0.8rem; }
.feat-ico { width: 36px; height: 36px; flex-shrink: 0; background: var(--lav); border-radius: 9px; display: flex; align-items: center; justify-content: center; }
.feat strong { display: block; font-size: 0.83rem; font-weight: 600; color: var(--ink); }
.feat span { font-size: 0.75rem; color: var(--gr); }

/* MARQUEE */
.marquee-wrap { background: var(--p); overflow: hidden; padding: 0.9rem 0; white-space: nowrap; }
.marquee-track { display: inline-block; animation: marquee 22s linear infinite; }
.marquee-track span { font-family: 'Unbounded', sans-serif; font-size: 0.72rem; font-weight: 600; letter-spacing: 0.12em; text-transform: uppercase; color: rgba(255,255,255,0.7); padding: 0 2.5rem; }
.marquee-track span.dot { color: rgba(255,255,255,0.3); padding: 0; }
@keyframes marquee { from { transform: translateX(0); } to { transform: translateX(-50%); } }

/* SECTIONS */
.section { padding: 6rem 5%; }
.sec-eyebrow { font-size: 0.68rem; font-weight: 600; letter-spacing: 0.18em; text-transform: uppercase; color: var(--plt); margin-bottom: 0.6rem; }
h2.sec-h { font-family: 'Unbounded', sans-serif; font-size: clamp(1.6rem, 2.8vw, 2.6rem); font-weight: 300; color: var(--ink); line-height: 1.2; margin-bottom: 0.6rem; letter-spacing: -0.02em; }
h2.sec-h b { font-weight: 700; color: var(--p); }
.sec-lead { font-size: 0.95rem; color: var(--gr); max-width: 500px; margin-bottom: 3rem; }

/* SERVICES */
#services { background: var(--w); }
.services-layout { display: grid; grid-template-columns: 280px 1fr; gap: 4rem; align-items: start; }
.services-intro { position: sticky; top: 84px; }
.services-intro p { font-size: 0.9rem; color: var(--gr); margin-top: 0.8rem; margin-bottom: 2rem; line-height: 1.7; }
.s-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; }
.s-card { background: var(--bg); border: 1px solid var(--brd); border-radius: var(--r); padding: 1.6rem; transition: border-color .2s, box-shadow .2s; }
.s-card:hover { border-color: var(--plt); box-shadow: 0 4px 20px rgba(107,63,160,0.07); }
.s-ico { width: 40px; height: 40px; background: var(--lav); border-radius: 10px; display: flex; align-items: center; justify-content: center; margin-bottom: 1rem; }
.s-card h3 { font-family: 'Unbounded', sans-serif; font-size: 0.78rem; font-weight: 600; color: var(--ink); margin-bottom: 0.4rem; }
.s-card p { font-size: 0.8rem; color: var(--gr); line-height: 1.6; }

/* STEPS */
#steps { background: var(--ink); }
#steps .sec-eyebrow { color: rgba(255,255,255,0.35); }
#steps h2.sec-h { color: #fff; }
#steps h2.sec-h b { color: var(--lav); }
#steps .sec-lead { color: rgba(255,255,255,0.45); }
.steps-grid { display: grid; grid-template-columns: repeat(4, 1fr); gap: 1px; background: rgba(255,255,255,0.08); border: 1px solid rgba(255,255,255,0.08); border-radius: var(--r); overflow: hidden; }
.step-card { background: var(--ink); padding: 2rem 1.8rem; transition: background .2s; }
.step-card:hover { background: #261A40; }
.step-num { font-family: 'Unbounded', sans-serif; font-size: 2.5rem; font-weight: 700; color: rgba(255,255,255,0.08); line-height: 1; margin-bottom: 1.2rem; }
.step-card h4 { font-family: 'Unbounded', sans-serif; font-size: 0.78rem; font-weight: 600; color: #fff; margin-bottom: 0.5rem; }
.step-card p { font-size: 0.78rem; color: rgba(255,255,255,0.45); line-height: 1.6; }

/* CONTACT */
#contact { background: var(--bg); }
.contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1.5rem; }
.contact-main { background: var(--p); border-radius: 20px; padding: 3.5rem; position: relative; overflow: hidden; display: flex; flex-direction: column; justify-content: space-between; }
.contact-main::before { content: ''; position: absolute; width: 300px; height: 300px; border: 1px solid rgba(255,255,255,0.1); border-radius: 50%; bottom: -80px; right: -80px; }
.contact-main-text { position: relative; z-index: 1; }
.contact-main p.eyebrow { font-size: 0.68rem; font-weight: 600; letter-spacing: 0.18em; text-transform: uppercase; color: rgba(255,255,255,0.45); margin-bottom: 0.8rem; }
.contact-main h3 { font-family: 'Unbounded', sans-serif; font-size: clamp(1.4rem, 2.5vw, 2.2rem); font-weight: 300; color: #fff; line-height: 1.2; margin-bottom: 0.8rem; }
.contact-main h3 b { font-weight: 700; }
.contact-main .sub { font-size: 0.88rem; color: rgba(255,255,255,0.55); position: relative; z-index: 1; margin-top: 0.6rem; }
.btn-white { display: inline-flex; align-items: center; gap: 0.5rem; background: #fff; color: var(--p); font-family: 'Manrope', sans-serif; font-size: 0.88rem; font-weight: 700; padding: 0.85rem 1.8rem; border-radius: 50px; text-decoration: none; margin-top: 2rem; position: relative; z-index: 1; width: fit-content; transition: opacity .2s; }
.btn-white:hover { opacity: 0.88; }
.contact-side { display: flex; flex-direction: column; gap: 1rem; }
.c-card { background: var(--w); border: 1px solid var(--brd); border-radius: var(--r); padding: 1.8rem; flex: 1; display: flex; flex-direction: column; justify-content: space-between; }
.c-card-label { font-size: 0.68rem; font-weight: 600; letter-spacing: 0.15em; text-transform: uppercase; color: var(--gr); margin-bottom: 0.5rem; }
.c-card h4 { font-family: 'Unbounded', sans-serif; font-size: 0.95rem; font-weight: 600; color: var(--ink); margin-bottom: 0.4rem; }
.c-card p { font-size: 0.8rem; color: var(--gr); margin-bottom: 1.2rem; }
.c-link { display: inline-flex; align-items: center; gap: 0.5rem; font-size: 0.82rem; font-weight: 600; text-decoration: none; padding: 0.6rem 1.2rem; border-radius: 50px; width: fit-content; transition: opacity .2s; }
.c-link:hover { opacity: 0.8; }
.c-link-vk { background: #0077FF; color: #fff; }
.c-link-tg { background: var(--lav); color: var(--p); }

/* FOOTER */
footer { background: var(--ink); padding: 3rem 5% 2rem; }
.footer-top { display: flex; justify-content: space-between; align-items: flex-start; gap: 2rem; margin-bottom: 2rem; flex-wrap: wrap; }
.footer-logo { font-family: 'Unbounded', sans-serif; font-size: 1rem; font-weight: 700; color: #fff; text-decoration: none; display: block; margin-bottom: 0.6rem; }
.footer-desc { font-size: 0.78rem; color: rgba(255,255,255,0.35); max-width: 260px; line-height: 1.6; }
.footer-col h5 { font-family: 'Unbounded', sans-serif; font-size: 0.72rem; font-weight: 600; color: rgba(255,255,255,0.35); letter-spacing: 0.1em; text-transform: uppercase; margin-bottom: 0.8rem; }
.footer-col a, .footer-col p { display: block; font-size: 0.8rem; color: rgba(255,255,255,0.55); text-decoration: none; margin-bottom: 0.4rem; cursor: pointer; }
.footer-col a:hover { color: #fff; }
.footer-bottom { border-top: 1px solid rgba(255,255,255,0.08); padding-top: 1.5rem; display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 0.8rem; }
.footer-bottom span { font-size: 0.72rem; color: rgba(255,255,255,0.25); }
.footer-legal-links { display: flex; gap: 1.5rem; }
.footer-legal-links a { font-size: 0.72rem; color: rgba(255,255,255,0.35); text-decoration: none; cursor: pointer; }
.footer-legal-links a:hover { color: rgba(255,255,255,0.7); }

/* MODAL */
.modal-overlay {
  position: fixed; inset: 0;
  background: rgba(26,16,37,0.7);
  backdrop-filter: blur(4px);
  z-index: 999;
  display: flex; align-items: center; justify-content: center;
  padding: 1.5rem;
  opacity: 0; pointer-events: none;
  transition: opacity .25s;
}
.modal-overlay.open { opacity: 1; pointer-events: all; }
.modal {
  background: var(--w);
  border-radius: 20px;
  width: 100%; max-width: 680px;
  max-height: 85vh;
  display: flex; flex-direction: column;
  overflow: hidden;
  transform: translateY(16px);
  transition: transform .25s;
}
.modal-overlay.open .modal { transform: translateY(0); }
.modal-head {
  padding: 1.8rem 2rem 1.2rem;
  border-bottom: 1px solid var(--brd);
  display: flex; align-items: center; justify-content: space-between;
  flex-shrink: 0;
}
.modal-head h3 { font-family: 'Unbounded', sans-serif; font-size: 0.95rem; font-weight: 600; color: var(--ink); }
.modal-close {
  width: 32px; height: 32px;
  background: var(--bg); border: 1px solid var(--brd);
  border-radius: 50%; display: flex; align-items: center; justify-content: center;
  cursor: pointer; font-size: 1rem; color: var(--gr);
  flex-shrink: 0; transition: background .2s;
}
.modal-close:hover { background: var(--lav); }
.modal-body { padding: 1.8rem 2rem; overflow-y: auto; flex: 1; }
.modal-body h4 { font-family: 'Unbounded', sans-serif; font-size: 0.8rem; font-weight: 600; color: var(--ink); margin: 1.4rem 0 0.5rem; }
.modal-body h4:first-child { margin-top: 0; }
.modal-body p { font-size: 0.83rem; color: var(--gr); line-height: 1.7; margin-bottom: 0.6rem; }
.modal-body ul { padding-left: 1.2rem; margin-bottom: 0.6rem; }
.modal-body ul li { font-size: 0.83rem; color: var(--gr); line-height: 1.7; }

/* COOKIE BANNER */
.cookie-banner {
  position: fixed; bottom: 1.5rem; left: 50%; transform: translateX(-50%);
  width: calc(100% - 3rem); max-width: 600px;
  background: var(--ink);
  border-radius: 14px;
  padding: 1.2rem 1.5rem;
  display: flex; align-items: center; justify-content: space-between; gap: 1rem;
  z-index: 998;
  box-shadow: 0 8px 40px rgba(0,0,0,0.25);
  flex-wrap: wrap;
  transition: opacity .3s, transform .3s;
}
.cookie-banner.hidden { opacity: 0; transform: translateX(-50%) translateY(20px); pointer-events: none; }
.cookie-banner p { font-size: 0.78rem; color: rgba(255,255,255,0.6); flex: 1; min-width: 200px; }
.cookie-banner p a { color: rgba(255,255,255,0.8); text-decoration: underline; cursor: pointer; }
.cookie-btn { background: var(--p); color: #fff; font-family: 'Manrope', sans-serif; font-size: 0.78rem; font-weight: 600; padding: 0.5rem 1.2rem; border-radius: 50px; border: none; cursor: pointer; white-space: nowrap; transition: background .2s; flex-shrink: 0; }
.cookie-btn:hover { background: var(--plt); }

/* MOBILE */
@media (max-width: 960px) {
  #hero { grid-template-columns: 1fr; grid-template-rows: auto auto auto; }
  .hero-left { grid-column: 1; grid-row: 1; border-right: none; border-bottom: 1px solid var(--brd); padding: 3rem 5%; }
  .hero-right-top { grid-column: 1; grid-row: 2; min-height: 220px; }
  .hero-right-bottom { grid-column: 1; grid-row: 3; }
  .services-layout { grid-template-columns: 1fr; gap: 2rem; }
  .services-intro { position: static; }
  .steps-grid { grid-template-columns: 1fr 1fr; }
  .contact-grid { grid-template-columns: 1fr; }
  .nav-menu { display: none; }
}
@media (max-width: 560px) {
  .s-grid { grid-template-columns: 1fr; }
  .steps-grid { grid-template-columns: 1fr; }
  .hero-right-bottom { grid-template-columns: 1fr; }
  .hero-stats { gap: 1.5rem; }
  .footer-top { flex-direction: column; }
}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#hero" class="logo">Мы в бренде</a>
  <ul class="nav-menu">
    <li><a href="#services">Услуги</a></li>
    <li><a href="#steps">Как работаем</a></li>
    <li><a href="#contact">Контакты</a></li>
  </ul>
  <a href="https://vk.com/" target="_blank" class="nav-cta">Написать нам</a>
</nav>

<!-- HERO -->
<div id="hero">
  <div class="hero-left">
    <div class="hero-tag"><span></span>Байерский сервис</div>
    <h1>Покупки<br>за рубежом —<br><strong>легко и выгодно</strong></h1>
    <p class="hero-desc">Доставляем одежду, обувь, косметику и аксессуары из США и Европы. Только оригиналы. Вы выбираете — мы делаем всё остальное.</p>
    <div class="btns">
      <a href="https://vk.com/" target="_blank" class="btn-main">
        <svg width="16" height="16" viewBox="0 0 24 24"><path d="M12.87 16.5s.26-.03.4-.18c.12-.14.12-.4.12-.4s-.02-1.22.55-1.4c.56-.17 1.28 1.18 2.04 1.7.58.39 1.02.3 1.02.3l2.04-.03s1.07-.06.56-1c-.04-.07-.3-.65-1.56-1.83-1.31-1.24-1.14-1.04.45-3.18.97-1.3 1.36-2.09 1.24-2.43-.12-.32-.82-.24-.82-.24l-2.3.01s-.17-.02-.3.06c-.12.08-.2.26-.2.26s-.37 1.01-.87 1.87c-1.05 1.78-1.47 1.87-1.64 1.76-.4-.26-.3-1.04-.3-1.6 0-1.74.26-2.47-.51-2.65-.26-.06-.45-.1-1.1-.11-.84-.01-1.56 0-1.96.2-.27.13-.47.43-.35.45.16.02.51.1.7.36.23.34.22 1.1.22 1.1s.13 2.04-.31 2.3c-.3.17-.72-.18-1.62-1.79-.48-.84-.84-1.77-.84-1.77s-.07-.17-.19-.27c-.15-.11-.35-.14-.35-.14l-2.18.01s-.33.01-.45.15c-.11.13-.01.4-.01.4s1.7 3.97 3.62 5.97c1.76 1.83 3.76 1.71 3.76 1.71h.91z" fill="white"/></svg>
        ВКонтакте
      </a>
      <a href="#steps" class="btn-ghost">Как это работает</a>
    </div>
    <div class="hero-stats">
      <div><div class="stat-n">100%</div><div class="stat-l">Оригиналы</div></div>
      <div><div class="stat-n">США</div><div class="stat-l">и Европа</div></div>
      <div><div class="stat-n">Прямые</div><div class="stat-l">закупки</div></div>
    </div>
  </div>
  <div class="hero-right-top">
    <div class="big-label">BRAND</div>
    <div class="hero-right-top-content">
      <p>Наш принцип</p>
      <h2>Вы выбираете —<br><b>мы привезём</b></h2>
    </div>
  </div>
  <div class="hero-right-bottom">
    <div class="feat">
      <div class="feat-ico"><svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="#6B3FA0" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"/></svg></div>
      <div><strong>Только оригиналы</strong><span>Напрямую из официальных магазинов</span></div>
    </div>
    <div class="feat">
      <div class="feat-ico"><svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="#6B3FA0" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg></div>
      <div><strong>Ежедневные выкупы</strong><span>Обрабатываем заказы каждый день</span></div>
    </div>
    <div class="feat">
      <div class="feat-ico"><svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="#6B3FA0" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2"/><circle cx="12" cy="7" r="4"/></svg></div>
      <div><strong>Личный подход</strong><span>Индивидуальное сопровождение</span></div>
    </div>
    <div class="feat">
      <div class="feat-ico"><svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="#6B3FA0" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="1" y="3" width="15" height="13"/><polygon points="16 8 20 8 23 11 23 16 16 16 16 8"/><circle cx="5.5" cy="18.5" r="2.5"/><circle cx="18.5" cy="18.5" r="2.5"/></svg></div>
      <div><strong>Полное сопровождение</strong><span>От выкупа до доставки вам</span></div>
    </div>
  </div>
</div>

<!-- MARQUEE -->
<div class="marquee-wrap">
  <div class="marquee-track">
    <span>США и Европа</span><span class="dot">·</span><span>Оригинальные товары</span><span class="dot">·</span><span>Ежедневные выкупы</span><span class="dot">·</span><span>Одежда и обувь</span><span class="dot">·</span><span>Косметика</span><span class="dot">·</span><span>Товары для детей</span><span class="dot">·</span><span>Аксессуары</span><span class="dot">·</span><span>Личный подход</span><span class="dot">·</span>
    <span>США и Европа</span><span class="dot">·</span><span>Оригинальные товары</span><span class="dot">·</span><span>Ежедневные выкупы</span><span class="dot">·</span><span>Одежда и обувь</span><span class="dot">·</span><span>Косметика</span><span class="dot">·</span><span>Товары для детей</span><span class="dot">·</span><span>Аксессуары</span><span class="dot">·</span><span>Личный подход</span><span class="dot">·</span>
  </div>
</div>

<!-- SERVICES -->
<section class="section" id="services">
  <div class="services-layout">
    <div class="services-intro">
      <div class="sec-eyebrow">Услуги</div>
      <h2 class="sec-h">Что мы<br><b>доставляем</b></h2>
      <p>Выкупаем любые товары из США и Европы — от брендовой одежды до косметики и гаджетов.</p>
      <a href="https://vk.com/" target="_blank" class="btn-main">Сделать заказ</a>
    </div>
    <div class="s-grid">
      <div class="s-card"><div class="s-ico"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#6B3FA0" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M20.38 3.46L16 2a4 4 0 0 1-8 0L3.62 3.46a2 2 0 0 0-1.34 2.23l.58 3.57a1 1 0 0 0 .99.84H6v10c0 1.1.9 2 2 2h8a2 2 0 0 0 2-2V10h2.15a1 1 0 0 0 .99-.84l.58-3.57a2 2 0 0 0-1.34-2.23z"/></svg></div><h3>Одежда и обувь</h3><p>Nike, Zara, Gap, Tommy Hilfiger и сотни других брендов</p></div>
      <div class="s-card"><div class="s-ico"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#6B3FA0" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M20.84 4.61a5.5 5.5 0 0 0-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 0 0-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 0 0 0-7.78z"/></svg></div><h3>Косметика и уход</h3><p>Оригинальная косметика и парфюмерия мировых брендов</p></div>
      <div class="s-card"><div class="s-ico"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#6B3FA0" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M17 21v-2a4 4 0 0 0-4-4H5a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 0 0-3-3.87"/><path d="M16 3.13a4 4 0 0 1 0 7.75"/></svg></div><h3>Товары для детей</h3><p>Одежда, обувь и игрушки из зарубежных магазинов</p></div>
      <div class="s-card"><div class="s-ico"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#6B3FA0" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="2" y="7" width="20" height="14" rx="2"/><path d="M16 21V5a2 2 0 0 0-2-2h-4a2 2 0 0 0-2 2v16"/></svg></div><h3>Аксессуары</h3><p>Сумки, украшения и аксессуары от известных брендов</p></div>
      <div class="s-card"><div class="s-ico"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#6B3FA0" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="5" y="2" width="14" height="20" rx="2"/><line x1="12" y1="18" x2="12.01" y2="18"/></svg></div><h3>Техника и гаджеты</h3><p>Электроника, которую сложно найти в России</p></div>
      <div class="s-card"><div class="s-ico"><svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#6B3FA0" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg></div><h3>Любой товар</h3><p>Пришлите ссылку — выкупим из любого магазина</p></div>
    </div>
  </div>
</section>

<!-- STEPS -->
<section class="section" id="steps">
  <div class="sec-eyebrow">Как мы работаем</div>
  <h2 class="sec-h">4 шага до <b>вашей покупки</b></h2>
  <p class="sec-lead">Всё просто — вы выбираете, мы занимаемся остальным</p>
  <div class="steps-grid">
    <div class="step-card"><div class="step-num">01</div><h4>Выбираете товар</h4><p>В нашей группе ВКонтакте или самостоятельно на зарубежных сайтах</p></div>
    <div class="step-card"><div class="step-num">02</div><h4>Пишете нам</h4><p>Уточняем детали, размер и итоговую стоимость с доставкой</p></div>
    <div class="step-card"><div class="step-num">03</div><h4>Выкупаем товар</h4><p>Берём на себя оплату, таможню и всё оформление</p></div>
    <div class="step-card"><div class="step-num">04</div><h4>Получаете заказ</h4><p>Выбираете удобный способ доставки и получаете покупку</p></div>
  </div>
</section>

<!-- CONTACT -->
<section class="section" id="contact">
  <div class="sec-eyebrow">Контакты</div>
  <h2 class="sec-h" style="margin-bottom:2rem;">Готовы <b>помочь вам</b></h2>
  <div class="contact-grid">
    <div class="contact-main">
      <div class="contact-main-text">
        <p class="eyebrow">Напишите нам</p>
        <h3>Вы выбираете —<br><b>мы доставим</b></h3>
        <p class="sub">Присоединяйтесь к группе ВКонтакте — там актуальные акции, новинки и быстрая связь с нами</p>
      </div>
      <a href="https://vk.com/" target="_blank" class="btn-white">
        <svg width="16" height="16" viewBox="0 0 24 24"><path d="M12.87 16.5s.26-.03.4-.18c.12-.14.12-.4.12-.4s-.02-1.22.55-1.4c.56-.17 1.28 1.18 2.04 1.7.58.39 1.02.3 1.02.3l2.04-.03s1.07-.06.56-1c-.04-.07-.3-.65-1.56-1.83-1.31-1.24-1.14-1.04.45-3.18.97-1.3 1.36-2.09 1.24-2.43-.12-.32-.82-.24-.82-.24l-2.3.01s-.17-.02-.3.06c-.12.08-.2.26-.2.26s-.37 1.01-.87 1.87c-1.05 1.78-1.47 1.87-1.64 1.76-.4-.26-.3-1.04-.3-1.6 0-1.74.26-2.47-.51-2.65-.26-.06-.45-.1-1.1-.11-.84-.01-1.56 0-1.96.2-.27.13-.47.43-.35.45.16.02.51.1.7.36.23.34.22 1.1.22 1.1s.13 2.04-.31 2.3c-.3.17-.72-.18-1.62-1.79-.48-.84-.84-1.77-.84-1.77s-.07-.17-.19-.27c-.15-.11-.35-.14-.35-.14l-2.18.01s-.33.01-.45.15c-.11.13-.01.4-.01.4s1.7 3.97 3.62 5.97c1.76 1.83 3.76 1.71 3.76 1.71h.91z" fill="#6B3FA0"/></svg>
        Открыть группу ВКонтакте
      </a>
    </div>
    <div class="contact-side">
      <div class="c-card">
        <div><div class="c-card-label">ВКонтакте</div><h4>Группа ВКонтакте</h4><p>Новинки, акции и быстрая связь с командой</p></div>
        <a href="https://vk.com/" target="_blank" class="c-link c-link-vk"><svg width="16" height="16" viewBox="0 0 24 24"><path d="M12.87 16.5s.26-.03.4-.18c.12-.14.12-.4.12-.4s-.02-1.22.55-1.4c.56-.17 1.28 1.18 2.04 1.7.58.39 1.02.3 1.02.3l2.04-.03s1.07-.06.56-1c-.04-.07-.3-.65-1.56-1.83-1.31-1.24-1.14-1.04.45-3.18.97-1.3 1.36-2.09 1.24-2.43-.12-.32-.82-.24-.82-.24l-2.3.01s-.17-.02-.3.06c-.12.08-.2.26-.2.26s-.37 1.01-.87 1.87c-1.05 1.78-1.47 1.87-1.64 1.76-.4-.26-.3-1.04-.3-1.6 0-1.74.26-2.47-.51-2.65-.26-.06-.45-.1-1.1-.11-.84-.01-1.56 0-1.96.2-.27.13-.47.43-.35.45.16.02.51.1.7.36.23.34.22 1.1.22 1.1s.13 2.04-.31 2.3c-.3.17-.72-.18-1.62-1.79-.48-.84-.84-1.77-.84-1.77s-.07-.17-.19-.27c-.15-.11-.35-.14-.35-.14l-2.18.01s-.33.01-.45.15c-.11.13-.01.4-.01.4s1.7 3.97 3.62 5.97c1.76 1.83 3.76 1.71 3.76 1.71h.91z" fill="white"/></svg>Написать</a>
      </div>
      <div class="c-card">
        <div><div class="c-card-label">Telegram</div><h4>Telegram</h4><p>Задайте вопрос или оформите заказ в мессенджере</p></div>
        <a href="https://t.me/" target="_blank" class="c-link c-link-tg"><svg width="16" height="16" viewBox="0 0 24 24" fill="none"><path d="M22 2L11 13" stroke="#6B3FA0" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/><path d="M22 2L15 22l-4-9-9-4 20-7z" stroke="#6B3FA0" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>Написать</a>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-top">
    <div>
      <a href="#hero" class="footer-logo">Мы в бренде</a>
      <p class="footer-desc">Байерский сервис. Доставка оригинальных товаров из США и Европы в Россию.</p>
    </div>
    <div class="footer-col">
      <h5>Навигация</h5>
      <a href="#services">Услуги</a>
      <a href="#steps">Как работаем</a>
      <a href="#contact">Контакты</a>
    </div>
    <div class="footer-col">
      <h5>Документы</h5>
      <a onclick="openModal('privacy')">Политика конфиденциальности</a>
      <a onclick="openModal('offer')">Публичная оферта</a>
      <a onclick="openModal('agreement')">Пользовательское соглашение</a>
    </div>
    <div class="footer-col">
      <h5>Реквизиты</h5>
      <p>ИП Фамилия Имя Отчество</p>
      <p>ИНН: XXXXXXXXXXXX</p>
      <p>ОГРНИП: XXXXXXXXXXXXXXX</p>
      <p style="margin-top:0.4rem;">Россия</p>
    </div>
  </div>
  <div class="footer-bottom">
    <span>© 2024 Мы в бренде. Все права защищены.</span>
    <div class="footer-legal-links">
      <a onclick="openModal('privacy')">Политика конфиденциальности</a>
      <a onclick="openModal('offer')">Публичная оферта</a>
    </div>
  </div>
</footer>

<!-- COOKIE BANNER -->
<div class="cookie-banner" id="cookieBanner">
  <p>Мы используем файлы cookie для улучшения работы сайта. Продолжая использование сайта, вы соглашаетесь с нашей <a onclick="openModal('privacy')">Политикой конфиденциальности</a>.</p>
  <button class="cookie-btn" onclick="acceptCookies()">Принять</button>
</div>

<!-- MODAL: PRIVACY -->
<div class="modal-overlay" id="modal-privacy" onclick="closeModalOutside(event,'modal-privacy')">
  <div class="modal">
    <div class="modal-head">
      <h3>Политика конфиденциальности</h3>
      <div class="modal-close" onclick="closeModal('privacy')">✕</div>
    </div>
    <div class="modal-body">
      <h4>1. Общие положения</h4>
      <p>Настоящая Политика конфиденциальности определяет порядок обработки и защиты персональных данных пользователей сайта «Мы в бренде» (далее — Оператор) в соответствии с Федеральным законом № 152-ФЗ «О персональных данных».</p>
      <p>Используя сайт, вы выражаете согласие с условиями настоящей Политики.</p>

      <h4>2. Состав персональных данных</h4>
      <p>Оператор может обрабатывать следующие персональные данные пользователей:</p>
      <ul>
        <li>Имя и фамилия</li>
        <li>Номер телефона</li>
        <li>Адрес электронной почты</li>
        <li>Адрес доставки</li>
        <li>Данные, собираемые автоматически (IP-адрес, тип браузера, cookie-файлы)</li>
      </ul>

      <h4>3. Цели обработки персональных данных</h4>
      <p>Персональные данные обрабатываются в целях:</p>
      <ul>
        <li>Оказания услуг по выкупу и доставке товаров</li>
        <li>Связи с пользователем по вопросам заказа</li>
        <li>Улучшения качества обслуживания</li>
        <li>Соблюдения требований законодательства РФ</li>
      </ul>

      <h4>4. Порядок обработки персональных данных</h4>
      <p>Оператор принимает необходимые организационные и технические меры для защиты персональных данных от несанкционированного доступа, изменения, раскрытия или уничтожения.</p>
      <p>Персональные данные не передаются третьим лицам, за исключением случаев, предусмотренных законодательством РФ, либо с явного согласия пользователя (например, для организации доставки).</p>

      <h4>5. Cookie-файлы</h4>
      <p>Сайт использует файлы cookie для улучшения работы и анализа посещаемости. Вы можете отключить cookie в настройках браузера, однако это может повлиять на функциональность сайта.</p>

      <h4>6. Права пользователя</h4>
      <p>Пользователь вправе: запросить доступ к своим персональным данным; потребовать их исправления или удаления; отозвать согласие на обработку, направив запрос через мессенджер или по реквизитам Оператора.</p>

      <h4>7. Контакты</h4>
      <p>По вопросам обработки персональных данных обращайтесь через группу ВКонтакте или Telegram, указанные на сайте.</p>

      <h4>8. Изменения Политики</h4>
      <p>Оператор оставляет за собой право изменять настоящую Политику. Актуальная редакция размещена на данном сайте.</p>
    </div>
  </div>
</div>

<!-- MODAL: PUBLIC OFFER -->
<div class="modal-overlay" id="modal-offer" onclick="closeModalOutside(event,'modal-offer')">
  <div class="modal">
    <div class="modal-head">
      <h3>Публичная оферта</h3>
      <div class="modal-close" onclick="closeModal('offer')">✕</div>
    </div>
    <div class="modal-body">
      <h4>1. Предмет оферты</h4>
      <p>Настоящая публичная оферта является официальным предложением ИП «Мы в бренде» (далее — Исполнитель) любому физическому лицу (далее — Заказчик) заключить договор на оказание байерских услуг на условиях, изложенных ниже.</p>
      <p>Акцептом (принятием) настоящей оферты является оформление заказа через мессенджеры, указанные на сайте.</p>

      <h4>2. Описание услуги</h4>
      <p>Исполнитель оказывает услуги по выкупу товаров в зарубежных интернет-магазинах и их доставке на территорию Российской Федерации по запросу Заказчика. Исполнитель действует от своего имени в интересах Заказчика.</p>

      <h4>3. Стоимость и оплата</h4>
      <p>Стоимость услуг складывается из стоимости товара, стоимости международной доставки и вознаграждения Исполнителя. Итоговая стоимость согласовывается индивидуально до оформления заказа. Оплата производится в рублях РФ по согласованным реквизитам.</p>

      <h4>4. Сроки исполнения</h4>
      <p>Сроки выкупа и доставки зависят от страны отправления, наличия товара и выбранного способа доставки, и согласовываются с Заказчиком индивидуально.</p>

      <h4>5. Права и обязанности сторон</h4>
      <p>Исполнитель обязуется: выкупить товар согласно заявке; уведомлять Заказчика о статусе заказа; обеспечить доставку в согласованные сроки.</p>
      <p>Заказчик обязуется: предоставить точные данные для заказа; произвести оплату в установленные сроки; принять товар при доставке.</p>

      <h4>6. Ограничение ответственности</h4>
      <p>Исполнитель не несёт ответственности за задержки, вызванные работой таможенных органов, форс-мажорными обстоятельствами, действиями третьих лиц (транспортные компании, магазины). Исполнитель не является продавцом товаров — продавцом выступает зарубежный магазин.</p>

      <h4>7. Возврат и обмен</h4>
      <p>Вопросы возврата решаются индивидуально в соответствии с политикой зарубежного магазина-продавца и законодательством РФ. Вознаграждение Исполнителя при отказе от товара не возвращается, если заказ уже был выкуплен.</p>

      <h4>8. Применимое право</h4>
      <p>Настоящая оферта регулируется законодательством Российской Федерации.</p>
    </div>
  </div>
</div>

<!-- MODAL: USER AGREEMENT -->
<div class="modal-overlay" id="modal-agreement" onclick="closeModalOutside(event,'modal-agreement')">
  <div class="modal">
    <div class="modal-head">
      <h3>Пользовательское соглашение</h3>
      <div class="modal-close" onclick="closeModal('agreement')">✕</div>
    </div>
    <div class="modal-body">
      <h4>1. Общие условия</h4>
      <p>Используя данный сайт, вы соглашаетесь с настоящим Пользовательским соглашением. Если вы не согласны с условиями, пожалуйста, покиньте сайт.</p>

      <h4>2. Использование сайта</h4>
      <p>Сайт предназначен исключительно для информационных целей. Вся информация на сайте носит ознакомительный характер и не является публичной офертой, за исключением раздела «Публичная оферта».</p>
      <p>Запрещается: копировать материалы сайта без разрешения; использовать сайт в незаконных целях; предпринимать действия, нарушающие работу сайта.</p>

      <h4>3. Интеллектуальная собственность</h4>
      <p>Все материалы сайта (тексты, изображения, логотипы, дизайн) являются собственностью «Мы в бренде» и защищены законодательством об авторском праве. Использование материалов без письменного разрешения запрещено.</p>

      <h4>4. Ограничение ответственности</h4>
      <p>Сайт предоставляется «как есть». Оператор не гарантирует бесперебойную работу сайта и не несёт ответственности за возможные убытки, связанные с использованием или невозможностью использования сайта.</p>
      <p>Оператор не несёт ответственности за содержание внешних сайтов, на которые ведут ссылки с данного ресурса (ВКонтакте, Telegram и др.).</p>

      <h4>5. Персональные данные</h4>
      <p>Обработка персональных данных осуществляется в соответствии с Политикой конфиденциальности, размещённой на сайте.</p>

      <h4>6. Изменение соглашения</h4>
      <p>Оператор вправе изменять условия настоящего соглашения в одностороннем порядке. Актуальная версия всегда размещена на сайте. Продолжение использования сайта означает согласие с изменёнными условиями.</p>

      <h4>7. Применимое право и споры</h4>
      <p>Соглашение регулируется законодательством РФ. Все споры разрешаются путём переговоров, а при недостижении согласия — в судебном порядке по месту нахождения Оператора.</p>
    </div>
  </div>
</div>

<script>
function openModal(id) {
  document.getElementById('modal-' + id).classList.add('open');
  document.body.style.overflow = 'hidden';
}
function closeModal(id) {
  document.getElementById('modal-' + id).classList.remove('open');
  document.body.style.overflow = '';
}
function closeModalOutside(e, id) {
  if (e.target === document.getElementById('modal-' + id)) closeModal(id);
}
document.addEventListener('keydown', function(e) {
  if (e.key === 'Escape') {
    ['privacy','offer','agreement'].forEach(closeModal);
  }
});
function acceptCookies() {
  document.getElementById('cookieBanner').classList.add('hidden');
  localStorage.setItem('cookiesAccepted', '1');
}
if (localStorage.getItem('cookiesAccepted')) {
  document.getElementById('cookieBanner').classList.add('hidden');
}
</script>
</body>
</html>
