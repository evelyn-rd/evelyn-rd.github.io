<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Taller de Motos | Civac y Barona</title>
<style>
:root{
  --navy:#0b2447;--ink:#04070d;--bg:#ffffff;--bg2:#eef2f8;--text:#0e1726;--muted:#4b5a73;
  --card:#ffffff;--line:#d5dce8;--accent:#2f7bff;--ok:#1fa75a;
  box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px);
}
:root:not([data-theme="light"]){color-scheme:light dark}
@media (prefers-color-scheme:dark){
  :root:not([data-theme="light"]){--bg:#070d18;--bg2:#0c1626;--text:#eaf0fb;--muted:#9fb0cb;--card:#101c31;--line:#22314d}
}
:root[data-theme="dark"]{--bg:#070d18;--bg2:#0c1626;--text:#eaf0fb;--muted:#9fb0cb;--card:#101c31;--line:#22314d}
*,*::before,*::after{box-sizing:border-box}
html{scroll-behavior:smooth;scroll-padding-top:env(safe-area-inset-top,0px)}
body{margin:0;background:var(--bg);color:var(--text);font:400 1rem/1.6 "Segoe UI",Inter,system-ui,-apple-system,Roboto,Helvetica,Arial,sans-serif}
h1,h2,h3{line-height:1.1;margin:0;letter-spacing:-.02em}
h2{font-size:clamp(1.7rem,4.5vw,2.5rem);margin-bottom:.6rem}
p{margin:0 0 1rem}
a{color:inherit}
.wrap{width:min(1100px,100% - 2.5rem);margin-inline:auto}
section{padding:4.5rem 0}
.alt{background:var(--bg2)}
.lead{color:var(--muted);max-width:60ch}
.btn{display:inline-flex;align-items:center;gap:.5rem;padding:.9rem 1.5rem;border-radius:10px;border:2px solid transparent;font:700 1rem inherit;font-family:inherit;text-decoration:none;cursor:pointer;transition:transform .15s,background .15s}
.btn:hover{transform:translateY(-2px)}
.btn:focus-visible,input:focus-visible,select:focus-visible,textarea:focus-visible,.stars label:focus-within{outline:3px solid var(--accent);outline-offset:2px}
.btn-wa{background:#25d366;color:#04210f}
.btn-fb{background:#1877f2;color:#fff}
.btn-line{border-color:#fff;color:#fff}
.btn-main{background:var(--accent);color:#fff}

/* Hero */
.hero{background:linear-gradient(160deg,var(--ink) 0%,var(--navy) 100%);color:#fff;padding:0 0 5rem;position:relative;overflow:hidden}
.top{display:flex;justify-content:space-between;align-items:center;padding:1.2rem 0}
.logo{font-weight:800;font-size:1.15rem;display:flex;gap:.6rem;align-items:center}
.logo svg{width:32px;height:32px}
.hero-grid{display:grid;grid-template-columns:1.3fr 1fr;gap:2rem;align-items:center;padding-top:3rem}
.hero h1{font-size:clamp(2.3rem,7vw,4.4rem);font-weight:800}
.hero p.sub{font-size:1.2rem;color:#c3d1ea;max-width:46ch;margin:1.2rem 0 2rem}
.cta-row{display:flex;flex-wrap:wrap;gap:.8rem}
.gauge{width:100%;max-width:360px;justify-self:center}
.needle{transform-origin:150px 150px;animation:rev 2.2s cubic-bezier(.2,.8,.2,1) both}
@keyframes rev{from{transform:rotate(-120deg)}to{transform:rotate(35deg)}}
@media (prefers-reduced-motion:reduce){.needle{animation:none;transform:rotate(35deg)}.btn{transition:none}html{scroll-behavior:auto}}

/* Beneficios */
.cols{display:grid;grid-template-columns:repeat(3,1fr);gap:1.5rem;margin-top:2.2rem}
.ben{padding:1.6rem;border:1px solid var(--line);border-radius:14px;background:var(--card)}
.ico{width:52px;height:52px;border-radius:12px;background:var(--navy);display:grid;place-items:center;margin-bottom:1rem}
.ico svg{width:28px;height:28px;stroke:#fff;fill:none;stroke-width:1.8;stroke-linecap:round;stroke-linejoin:round}
.ben h3{font-size:1.2rem;margin-bottom:.4rem}
.ben p{color:var(--muted);margin:0}

/* Piezas */
.parts{display:grid;grid-template-columns:repeat(auto-fill,minmax(210px,1fr));gap:1.2rem;margin-top:2rem}
.part{border:1px solid var(--line);border-radius:14px;background:var(--card);padding:1.2rem;display:flex;flex-direction:column;gap:.5rem}
.part .pi{height:90px;border-radius:10px;background:linear-gradient(135deg,var(--navy),var(--ink));display:grid;place-items:center}
.part .pi svg{width:46px;height:46px;stroke:#fff;fill:none;stroke-width:1.6;stroke-linecap:round;stroke-linejoin:round}
.part h3{font-size:1.05rem}
.part small{color:var(--muted)}
.part .btn{margin-top:auto;padding:.6rem 1rem;font-size:.95rem;background:var(--navy);color:#fff}

/* Sobre mí */
.about{display:grid;grid-template-columns:1fr 1.4fr;gap:2.5rem;align-items:center}
.stats{display:grid;grid-template-columns:repeat(2,1fr);gap:1rem}
.stat{background:var(--navy);color:#fff;border-radius:14px;padding:1.4rem}
.stat b{display:block;font-size:2.2rem;line-height:1}
.stat span{color:#c3d1ea;font-size:.95rem}

/* Formularios */
.form{max-width:640px;margin-top:1.8rem;display:grid;gap:1rem}
label.f{display:grid;gap:.35rem;font-weight:600;font-size:.95rem}
input,select,textarea{font:inherit;width:100%;padding:.8rem 1rem;border-radius:10px;border:1.5px solid var(--line);background:var(--card);color:var(--text)}
textarea{min-height:110px;resize:vertical}
.two{display:grid;grid-template-columns:1fr 1fr;gap:1rem}
.stars{display:flex;flex-direction:row-reverse;justify-content:flex-end;gap:.2rem}
.stars input{position:absolute;opacity:0;width:1px;height:1px}
.stars label{font-size:2.2rem;line-height:1;cursor:pointer;color:var(--line);padding:0 .1rem;border-radius:6px}
.stars input:checked~label,.stars label:hover,.stars label:hover~label{color:#f5b301}
.note{font-size:.9rem;color:var(--muted)}
.msg{padding:.9rem 1rem;border-radius:10px;background:var(--ok);color:#fff;font-weight:600;display:none}
.msg.show{display:block}
.err{color:#d93a3a;font-size:.9rem;display:none}
.err.show{display:block}

/* Footer */
footer{background:var(--ink);color:#c3d1ea;padding:3rem 0 2rem}
.foot{display:flex;flex-wrap:wrap;justify-content:space-between;gap:1.5rem;align-items:center}
.soc{display:flex;gap:.8rem}
.soc a{width:46px;height:46px;border-radius:50%;background:var(--navy);display:grid;place-items:center}
.soc svg{width:22px;height:22px;fill:#fff}
.soc a:hover{background:var(--accent)}
.copy{margin-top:2rem;font-size:.9rem;border-top:1px solid #1a2a47;padding-top:1.2rem}

@media (max-width:800px){
  .hero-grid,.about,.cols{grid-template-columns:1fr}
  .gauge{max-width:260px;order:-1}
  section{padding:3.2rem 0}
  .two{grid-template-columns:1fr}
}
</style>
</head>
<body>

<header class="hero">
  <div class="wrap">
    <div class="top">
      <div class="logo">
        <svg viewBox="0 0 32 32" fill="none" stroke="#fff" stroke-width="2" stroke-linecap="round" aria-hidden="true"><circle cx="7" cy="22" r="5"/><circle cx="25" cy="22" r="5"/><path d="M7 22l6-9h7l5 9M13 13l-2-3h-3M20 13l2-3h3"/></svg>
        Taller de Motos
      </div>
      <a class="btn btn-wa" href="#contacto" data-wa>WhatsApp</a>
    </div>
    <div class="hero-grid">
      <div>
        <h1>Tu moto en manos que sí saben.</h1>
        <p class="sub">Servicio, mantenimiento y refacciones para tu moto, con precio claro y entrega a tiempo. Dos talleres: Civac y Barona.</p>
        <div class="cta-row">
          <a class="btn btn-wa" href="#" data-wa>Escríbenos por WhatsApp</a>
          <a class="btn btn-fb" href="#" data-fb target="_blank" rel="noopener">Facebook</a>
          <a class="btn btn-line" href="#piezas">Ver piezas</a>
        </div>
      </div>
      <svg class="gauge" viewBox="0 0 300 200" role="img" aria-label="Tacómetro">
        <path d="M30 170 A120 120 0 0 1 270 170" fill="none" stroke="#2f7bff" stroke-width="14" stroke-linecap="round" opacity=".35"/>
        <path d="M30 170 A120 120 0 0 1 200 62" fill="none" stroke="#2f7bff" stroke-width="14" stroke-linecap="round"/>
        <g class="needle"><line x1="150" y1="150" x2="150" y2="48" stroke="#fff" stroke-width="5" stroke-linecap="round"/></g>
        <circle cx="150" cy="150" r="12" fill="#fff"/>
        <text x="150" y="190" text-anchor="middle" fill="#c3d1ea" font-size="14" font-family="Segoe UI,Arial,sans-serif">Listo para rodar</text>
      </svg>
    </div>
  </div>
</header>

<main>
<section id="beneficios">
  <div class="wrap">
    <h2>Por qué traer tu moto con nosotros</h2>
    <p class="lead">Trabajamos como nos gustaría que trabajaran en nuestra moto.</p>
    <div class="cols">
      <article class="ben">
        <div class="ico"><svg viewBox="0 0 24 24"><path d="M14.7 6.3a4 4 0 0 0-5.4 5.4L3 18l3 3 6.3-6.3a4 4 0 0 0 5.4-5.4l-2.5 2.5-2.5-.5-.5-2.5z"/></svg></div>
        <h3>Diagnóstico honesto</h3>
        <p>Te explicamos qué falla y qué no. Solo cambiamos lo necesario y te avisamos antes de cobrar algo extra.</p>
      </article>
      <article class="ben">
        <div class="ico"><svg viewBox="0 0 24 24"><circle cx="12" cy="12" r="9"/><path d="M12 7v5l3 2"/></svg></div>
        <h3>Entrega a tiempo</h3>
        <p>Sabes cuándo queda tu moto. Si el trabajo se alarga, te escribimos por WhatsApp para que no andes preguntando.</p>
      </article>
      <article class="ben">
        <div class="ico"><svg viewBox="0 0 24 24"><path d="M12 3l8 3v6c0 5-3.5 8-8 9-4.5-1-8-4-8-9V6z"/><path d="M8.5 12l2.5 2.5 4.5-5"/></svg></div>
        <h3>Piezas con garantía</h3>
        <p>Vendemos refacciones de calidad para las marcas más comunes y te las instalamos si lo prefieres.</p>
      </article>
    </div>
  </div>
</section>

<section id="piezas" class="alt">
  <div class="wrap">
    <h2>Piezas que vendemos</h2>
    <p class="lead">Toca «Pedir» en la pieza que necesitas y te llevamos directo al formulario. Te confirmamos disponibilidad y precio por WhatsApp.</p>
    <div class="parts" id="parts"></div>
  </div>
</section>

<section id="sobre-mi">
  <div class="wrap about">
    <div class="stats">
      <div class="stat"><b>2</b><span>talleres: Civac y Barona</span></div>
      <div class="stat"><b>10+</b><span>años en el oficio</span></div>
      <div class="stat"><b>1,000+</b><span>motos atendidas</span></div>
      <div class="stat"><b>100%</b><span>trato directo contigo</span></div>
    </div>
    <div>
      <h2>Sobre mí</h2>
      <p>Soy mecánico de motos desde que tuve mi primera, y empecé arreglándola yo mismo en la cochera. Hoy atiendo dos talleres, pero sigo creyendo lo mismo: a tu moto se le habla claro, se le trabaja bien y se te entrega como si fuera la mía.</p>
      <p>Si ruedas todos los días al trabajo o los fines de semana por carretera, aquí te ayudamos a que no te deje tirado.</p>
      <a class="btn btn-main" href="#contacto">Hablemos de tu moto</a>
    </div>
  </div>
</section>

<section id="calificanos" class="alt">
  <div class="wrap">
    <h2>Califica la atención</h2>
    <p class="lead">Elige el taller que te atendió y cuéntanos cómo te fue. Tu opinión nos ayuda a mejorar.</p>
    <form class="form" id="rateForm" novalidate>
      <label class="f">Taller
        <select id="rTaller" required>
          <option value="">Selecciona un taller</option>
          <option>Civac</option>
          <option>Barona</option>
        </select>
      </label>
      <div class="f" style="display:grid;gap:.35rem;font-weight:600;font-size:.95rem">
        Tu calificación
        <div class="stars" role="radiogroup" aria-label="Calificación de 1 a 5 estrellas">
          <input type="radio" name="star" id="s5" value="5"><label for="s5" title="5 estrellas" aria-label="5 estrellas">★</label>
          <input type="radio" name="star" id="s4" value="4"><label for="s4" title="4 estrellas" aria-label="4 estrellas">★</label>
          <input type="radio" name="star" id="s3" value="3"><label for="s3" title="3 estrellas" aria-label="3 estrellas">★</label>
          <input type="radio" name="star" id="s2" value="2"><label for="s2" title="2 estrellas" aria-label="2 estrellas">★</label>
          <input type="radio" name="star" id="s1" value="1"><label for="s1" title="1 estrella" aria-label="1 estrella">★</label>
        </div>
      </div>
      <label class="f">Tu nombre (opcional)<input id="rNombre" autocomplete="name"></label>
      <label class="f">Comentario<textarea id="rCom" placeholder="¿Qué te gustó o qué podemos mejorar?"></textarea></label>
      <p class="err" id="rErr">Selecciona un taller y una calificación.</p>
      <button class="btn btn-main" type="submit">Enviar calificación</button>
      <p class="msg" id="rOk" role="status">¡Gracias! Se abrió WhatsApp para enviar tu calificación.</p>
    </form>
  </div>
</section>

<section id="contacto">
  <div class="wrap">
    <h2>Contáctanos o pide una pieza</h2>
    <p class="lead">Llena el formulario y te respondemos por WhatsApp.</p>
    <form class="form" id="contactForm" novalidate>
      <div class="two">
        <label class="f">Nombre<input id="cNombre" required autocomplete="name"></label>
        <label class="f">Teléfono<input id="cTel" type="tel" required autocomplete="tel"></label>
      </div>
      <div class="two">
        <label class="f">¿Qué necesitas?
          <select id="cTipo">
            <option>Servicio o reparación</option>
            <option>Pedido de pieza</option>
            <option>Cotización</option>
            <option>Otro</option>
          </select>
        </label>
        <label class="f">Taller de preferencia
          <select id="cTaller"><option>Civac</option><option>Barona</option></select>
        </label>
      </div>
      <label class="f">Moto (marca, modelo y año)<input id="cMoto" placeholder="Ej. Italika FT150, 2021"></label>
      <label class="f">Mensaje o pieza que buscas<textarea id="cMsg" placeholder="Cuéntanos qué le pasa a tu moto o qué pieza necesitas."></textarea></label>
      <p class="err" id="cErr">Escribe tu nombre y teléfono.</p>
      <button class="btn btn-wa" type="submit">Enviar por WhatsApp</button>
      <p class="note">Al enviar se abre WhatsApp con tu mensaje listo. También puedes escribirnos por <a href="#" data-fb target="_blank" rel="noopener">Facebook</a>.</p>
    </form>
  </div>
</section>
</main>

<footer>
  <div class="wrap">
    <div class="foot">
      <div>
        <div class="logo" style="color:#fff">Taller de Motos</div>
        <p style="margin:.4rem 0 0">Sucursales: Civac y Barona</p>
      </div>
      <div class="soc">
        <a href="#" data-wa aria-label="WhatsApp"><svg viewBox="0 0 24 24"><path d="M12 2a10 10 0 0 0-8.6 15.1L2 22l5-1.3A10 10 0 1 0 12 2zm5.8 14.2c-.2.7-1.4 1.3-2 1.4-.5.1-1.2.1-3.7-.9-3.1-1.3-5.1-4.5-5.3-4.7-.1-.2-1.200-1.600-1.200-3s.7-2.100 1-2.400c.2-.3.5-.3.7-.3h.5c.2 0 .4 0 .6.5l.8 2c.1.200.1.400 0 .6l-.4.600c-.1.200-.3.300-.1.600.2.300.8 1.300 1.700 2.100 1.200 1 2.100 1.300 2.400 1.500.3.100.5.100.6-.1l.9-1.100c.2-.3.4-.2.600-.1l1.900.9c.3.1.5.2.5.3.1.100.1.800-.1 1.400z"/></svg></a>
        <a href="#" data-fb target="_blank" rel="noopener" aria-label="Facebook"><svg viewBox="0 0 24 24"><path d="M13.5 22v-8h2.7l.4-3.200h-3.100V8.800c0-.9.300-1.500 1.600-1.500h1.700V4.400c-.3 0-1.300-.1-2.400-.1-2.400 0-4.100 1.500-4.100 4.200v2.300H7.600V14h2.700v8z"/></svg></a>
        <a href="#" data-ig target="_blank" rel="noopener" aria-label="Instagram"><svg viewBox="0 0 24 24"><path d="M7.500 2h9A5.500 5.500 0 0 1 22 7.500v9a5.500 5.500 0 0 1-5.500 5.500h-9A5.500 5.500 0 0 1 2 16.500v-9A5.500 5.500 0 0 1 7.500 2zm0 2A3.500 3.500 0 0 0 4 7.500v9A3.500 3.500 0 0 0 7.500 20h9a3.500 3.500 0 0 0 3.500-3.500v-9A3.500 3.500 0 0 0 16.500 4zM12 7a5 5 0 1 1 0 10 5 5 0 0 1 0-10zm0 2a3 3 0 1 0 0 6 3 3 0 0 0 0-6zm5.200-3.200a1.200 1.200 0 1 1 0 2.400 1.200 1.200 0 0 1 0-2.400z"/></svg></a>
      </div>
    </div>
    <div class="copy">© <span id="yr"></span> Taller de Motos. Todos los derechos reservados.</div>
  </div>
</footer>

<script>
// ====== CONFIGURA AQUÍ ======
const CONFIG = {
  whatsapp: "527446908659",           // Número con código de país, sin + ni espacios
  facebook: "https://www.facebook.com/share/1EpH3uoUc2/",
  instagram: "https://www.instagram.com/ventobaronairon?vrfl=Y2ptNW9mNDNicDh5"
};
// ============================

const PARTS = [
  {n:"Llantas", d:"Para calle y trabajo", i:'<circle cx="12" cy="12" r="9"/><circle cx="12" cy="12" r="3"/><path d="M12 3v6M12 15v6M3 12h6M15 12h6"/>'},
  {n:"Pastillas y discos de freno", d:"Frenado seguro", i:'<circle cx="12" cy="12" r="9"/><circle cx="12" cy="12" r="4"/><path d="M12 3v2M12 19v2M3 12h2M19 12h2"/>'},
  {n:"Kit de arrastre", d:"Cadena, corona y piñón", i:'<circle cx="7" cy="12" r="4"/><circle cx="17" cy="12" r="3"/><path d="M7 8h10M7 16h10"/>'},
  {n:"Baterías", d:"Arranque confiable", i:'<rect x="3" y="7" width="18" height="12" rx="2"/><path d="M7 7V5h3v2M14 7V5h3v2M8 13h4M10 11v4"/>'},
  {n:"Aceites y filtros", d:"Mantenimiento básico", i:'<path d="M12 3s6 6.500 6 11a6 6 0 0 1-12 0c0-4.500 6-11 6-11z"/>'},
  {n:"Bujías y eléctrico", d:"Encendido y luces", i:'<path d="M13 2L5 14h6l-1 8 8-12h-6z"/>'},
  {n:"Clutch y cables", d:"Embrague y aceleración", i:'<path d="M4 20c4-2 4-6 8-8s6-6 8-8M4 20l3-1M20 4l-1 3"/>'},
  {n:"Espejos y accesorios", d:"Cascos, guantes y más", i:'<ellipse cx="12" cy="8" rx="6" ry="4"/><path d="M12 12v8M8 20h8"/>'}
];

const $ = s => document.querySelector(s);
const wa = txt => "https://wa.me/" + CONFIG.whatsapp + (txt ? "?text=" + encodeURIComponent(txt) : "");
const open = url => window.open(url, "_blank", "noopener");

// Enlaces de redes
document.querySelectorAll("[data-wa]").forEach(a => { a.href = wa("Hola, quiero información sobre sus servicios."); a.target = "_blank"; a.rel = "noopener"; });
document.querySelectorAll("[data-fb]").forEach(a => a.href = CONFIG.facebook);
document.querySelectorAll("[data-ig]").forEach(a => a.href = CONFIG.instagram);
$("#yr").textContent = new Date().getFullYear();

// Piezas
$("#parts").innerHTML = PARTS.map(p => `
  <article class="part">
    <div class="pi"><svg viewBox="0 0 24 24" aria-hidden="true">${p.i}</svg></div>
    <h3>${p.n}</h3><small>${p.d}</small>
    <button class="btn" type="button" data-pieza="${p.n}">Pedir</button>
  </article>`).join("");
$("#parts").addEventListener("click", e => {
  const b = e.target.closest("[data-pieza]"); if (!b) return;
  $("#cTipo").value = "Pedido de pieza";
  $("#cMsg").value = "Quiero pedir: " + b.dataset.pieza;
  $("#contacto").scrollIntoView({behavior: "smooth"});
  setTimeout(() => $("#cNombre").focus({preventScroll: true}), 500);
});

// Formulario de contacto / pedido
$("#contactForm").addEventListener("submit", e => {
  e.preventDefault();
  const nombre = $("#cNombre").value.trim(), tel = $("#cTel").value.trim();
  $("#cErr").classList.toggle("show", !nombre || !tel);
  if (!nombre || !tel) return;
  const t = `Hola, soy ${nombre} (tel. ${tel}).\nSolicitud: ${$("#cTipo").value}\nTaller: ${$("#cTaller").value}\nMoto: ${$("#cMoto").value.trim() || "No indicada"}\nMensaje: ${$("#cMsg").value.trim() || "—"}`;
  open(wa(t));
});

// Calificación de atención
$("#rateForm").addEventListener("submit", e => {
  e.preventDefault();
  const taller = $("#rTaller").value, star = document.querySelector('input[name="star"]:checked');
  const bad = !taller || !star;
  $("#rErr").classList.toggle("show", bad);
  if (bad) return;
  const t = `Calificación de atención\nTaller: ${taller}\nEstrellas: ${star.value}/5\nNombre: ${$("#rNombre").value.trim() || "Anónimo"}\nComentario: ${$("#rCom").value.trim() || "—"}`;
  $("#rOk").classList.add("show");
  open(wa(t));
  e.target.reset();
});
</script>
</body>
</html>
