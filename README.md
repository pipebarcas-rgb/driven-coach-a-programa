<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Cancha Llena — Driven Coach</title>
<meta name="description" content="Tu próximo grupo de entrenamiento lleno y pagado antes de arrancar. 8–12 personas en 2–3 semanas. Sin publicidad. Sin cursos. Solo básquet.">
<link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@600;700;800&family=Barlow:wght@400;500;600&display=swap" rel="stylesheet">
<style>
* { box-sizing: border-box; margin: 0; padding: 0; }

:root {
  --bg: #0C0F0D;
  --surface: #141A16;
  --green: #1F8C5A;
  --green-dim: rgba(31,140,90,0.12);
  --green-border: rgba(31,140,90,0.28);
  --text: #E8F0EC;
  --muted: #7a9c83;
  --dim: #3a5a43;
}

body {
  font-family: 'Barlow', sans-serif;
  background: var(--bg);
  color: var(--text);
  line-height: 1.5;
}

/* ─── HERO ─── */
.hero {
  padding: 4rem 1.4rem 3.5rem;
  max-width: 580px;
  margin: 0 auto;
}

.hero-eyebrow {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 0.16em;
  text-transform: uppercase;
  color: var(--green);
  margin-bottom: 1rem;
}

.hero-title {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: clamp(42px, 12vw, 68px);
  font-weight: 800;
  line-height: 0.92;
  text-transform: uppercase;
  margin-bottom: 1.4rem;
}

.hero-title span { color: var(--green); }

.hero-sub {
  font-size: 17px;
  color: var(--muted);
  line-height: 1.55;
  margin-bottom: 0.6rem;
  max-width: 440px;
}

.hero-sub strong { color: var(--text); }

.hero-nota {
  font-size: 12px;
  color: var(--dim);
  margin-bottom: 2rem;
}

.cta-btn {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  background: var(--green);
  color: #fff;
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 15px;
  font-weight: 700;
  letter-spacing: 0.07em;
  text-transform: uppercase;
  padding: 0.9rem 2rem;
  border-radius: 6px;
  text-decoration: none;
  transition: background 0.15s;
}
.cta-btn:hover { background: #197a4d; }

.hero-cupos {
  font-size: 11px;
  color: var(--dim);
  margin-top: 0.8rem;
}

/* ─── COMO FUNCIONA ─── */
.como {
  background: var(--surface);
  padding: 2.8rem 1.4rem;
}

.como-inner { max-width: 580px; margin: 0 auto; }

.section-label {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: var(--green);
  margin-bottom: 1.2rem;
}

.steps { display: flex; flex-direction: column; gap: 0; }

.step {
  display: flex;
  gap: 1rem;
  padding: 1rem 0;
  border-bottom: 0.5px solid rgba(255,255,255,0.05);
  align-items: flex-start;
}
.step:last-child { border-bottom: none; }

.step-num {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 28px;
  font-weight: 800;
  color: var(--green);
  line-height: 1;
  min-width: 32px;
  padding-top: 2px;
}

.step-body {}

.step-title {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 18px;
  font-weight: 700;
  color: var(--text);
  margin-bottom: 3px;
  text-transform: uppercase;
  letter-spacing: 0.02em;
}

.step-desc {
  font-size: 13px;
  color: var(--muted);
  line-height: 1.55;
}

/* ─── CASO MARQUIS ─── */
.caso {
  padding: 2.8rem 1.4rem;
  max-width: 580px;
  margin: 0 auto;
}

.caso-box {
  background: var(--green-dim);
  border: 0.5px solid var(--green-border);
  border-radius: 12px;
  padding: 1.6rem 1.4rem;
}

.caso-label {
  font-size: 10px;
  font-weight: 600;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: var(--green);
  margin-bottom: 1rem;
}

.caso-stat {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: clamp(38px, 10vw, 52px);
  font-weight: 800;
  color: var(--text);
  line-height: 1;
  margin-bottom: 0.4rem;
}

.caso-stat-sub {
  font-size: 13px;
  color: var(--muted);
  margin-bottom: 1.2rem;
}

.caso-detail {
  font-size: 13px;
  color: var(--muted);
  line-height: 1.6;
  border-top: 0.5px solid rgba(255,255,255,0.06);
  padding-top: 1rem;
}

.caso-detail strong { color: var(--text); }

/* ─── PARA QUIEN ─── */
.para-quien {
  background: var(--surface);
  padding: 2.8rem 1.4rem;
}
.para-quien-inner { max-width: 580px; margin: 0 auto; }

.check-list { display: flex; flex-direction: column; gap: 0.6rem; margin-top: 0.6rem; }

.check-item {
  display: flex;
  gap: 0.7rem;
  font-size: 14px;
  color: var(--muted);
  line-height: 1.5;
  align-items: flex-start;
}
.check-item .mark { color: var(--green); flex-shrink: 0; font-weight: 700; }

.no-list { margin-top: 1.4rem; }
.no-label {
  font-size: 10px;
  font-weight: 600;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--dim);
  margin-bottom: 0.7rem;
}
.no-item {
  display: flex;
  gap: 0.7rem;
  font-size: 13px;
  color: #4a6a54;
  margin-bottom: 0.4rem;
  line-height: 1.5;
  align-items: flex-start;
}
.no-item .mark { flex-shrink: 0; }

/* ─── PRECIO ─── */
.precio {
  padding: 2.8rem 1.4rem;
  max-width: 580px;
  margin: 0 auto;
}

.precio-box {
  background: var(--surface);
  border-radius: 12px;
  padding: 1.6rem 1.4rem;
  margin-bottom: 1rem;
}

.precio-row {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  padding: 0.7rem 0;
  border-bottom: 0.5px solid rgba(255,255,255,0.05);
}
.precio-row:last-child { border-bottom: none; }

.precio-campo {
  font-size: 11px;
  font-weight: 600;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--dim);
}

.precio-valor {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 18px;
  font-weight: 700;
  color: var(--text);
  text-align: right;
}

.precio-valor.green { color: var(--green); }

.garantia-box {
  background: var(--green-dim);
  border: 0.5px solid var(--green-border);
  border-radius: 10px;
  padding: 1.2rem 1.3rem;
  margin-bottom: 1.6rem;
}

.garantia-title {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 14px;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.04em;
  color: var(--green);
  margin-bottom: 0.4rem;
}

.garantia-text {
  font-size: 13px;
  color: var(--muted);
  line-height: 1.55;
}

.cta-final {
  display: block;
  text-align: center;
  background: var(--green);
  color: #fff;
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 17px;
  font-weight: 700;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  padding: 1.1rem 2rem;
  border-radius: 6px;
  text-decoration: none;
  transition: background 0.15s;
}
.cta-final:hover { background: #197a4d; }

.cupos-finales {
  text-align: center;
  font-size: 11px;
  color: var(--dim);
  margin-top: 0.7rem;
}

/* ─── QUIEN SOY ─── */
.quien {
  background: var(--surface);
  padding: 2.8rem 1.4rem;
}
.quien-inner {
  max-width: 580px;
  margin: 0 auto;
  display: flex;
  gap: 1.4rem;
  align-items: flex-start;
}

.quien-avatar {
  width: 68px;
  height: 68px;
  border-radius: 50%;
  background: #1F8C5A22;
  border: 1.5px solid var(--green-border);
  flex-shrink: 0;
  overflow: hidden;
}

.quien-avatar img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center top;
}

.quien-body {}
.quien-name {
  font-family: 'Barlow Condensed', sans-serif;
  font-size: 20px;
  font-weight: 700;
  color: var(--text);
  margin-bottom: 2px;
}
.quien-rol {
  font-size: 10px;
  font-weight: 600;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--green);
  margin-bottom: 0.7rem;
}
.quien-bio {
  font-size: 13px;
  color: var(--muted);
  line-height: 1.6;
}

/* ─── FOOTER ─── */
footer {
  padding: 2rem 1.4rem;
  text-align: center;
  font-size: 11px;
  color: var(--dim);
  border-top: 0.5px solid rgba(255,255,255,0.04);
}

footer a { color: var(--dim); text-decoration: none; }
footer a:hover { color: var(--muted); }

@media (max-width: 400px) {
  .quien-inner { flex-direction: column; }
}
</style>
</head>
<body>

<!-- ─── HERO ─── -->
<div class="hero">
  <div class="hero-eyebrow">Driven Coach · Puerto Montt</div>
  <h1 class="hero-title">Tu grupo<br><span>lleno y pagado</span><br>antes de arrancar</h1>
  <p class="hero-sub">
    <strong>8–12 personas en 2–3 semanas.</strong><br>
    Felipe hace todo el marketing. Vos solo entrenás y respondés mensajes con scripts listos.
  </p>
  <div class="hero-nota">Sin entrada. Sin cursos. Sin publicidad que tengas que manejar.</div>
  <a href="https://wa.me/56961171595?text=Hola%20Felipe%2C%20vi%20lo%20de%20Cancha%20Llena%20y%20quiero%20saber%20si%20aplico" class="cta-btn">
    Quiero saber si aplico →
  </a>
  <div class="hero-cupos">Solo 3 cupos disponibles en esta fase</div>
</div>

<!-- ─── COMO FUNCIONA ─── -->
<div class="como">
  <div class="como-inner">
    <div class="section-label">Cómo funciona</div>
    <div class="steps">

      <div class="step">
        <div class="step-num">1</div>
        <div class="step-body">
          <div class="step-title">Armamos la oferta de tu grupo</div>
          <div class="step-desc">Definimos el nombre, precio, días, lugar y qué incluye. Una sola página. Clara. Lista para vender.</div>
        </div>
      </div>

      <div class="step">
        <div class="step-num">2</div>
        <div class="step-body">
          <div class="step-title">Felipe corre los ads en Meta</div>
          <div class="step-desc">Creo la imagen y el copy. Lanzo la campaña apuntada a tu zona. Los leads llegan directo a tu WhatsApp con un mensaje pre-cargado. Vos no tocás nada.</div>
        </div>
      </div>

      <div class="step">
        <div class="step-num">3</div>
        <div class="step-body">
          <div class="step-title">Respondés con los scripts que te mando</div>
          <div class="step-desc">Tenés 4 scripts listos: bienvenida, precio, seguimiento y cierre. No improvisás. No sabés qué decir. Solo copiás y pegás.</div>
        </div>
      </div>

      <div class="step">
        <div class="step-num">4</div>
        <div class="step-body">
          <div class="step-title">El grupo se llena. Empieza el entrenamiento.</div>
          <div class="step-desc">Primer pago = cupo confirmado. Cuando tenés los 8–12 confirmados, se cierra la inscripción y arrancás.</div>
        </div>
      </div>

    </div>
  </div>
</div>

<!-- ─── CASO MARQUIS ─── -->
<div class="caso">
  <div class="section-label">Caso real</div>
  <div class="caso-box">
    <div class="caso-label">Marquis Johnson · Puerto Montt</div>
    <div class="caso-stat">$240.000 CLP</div>
    <div class="caso-stat-sub">en 7 días — sin publicidad</div>
    <div class="caso-detail">
      Coach de básquet en Puerto Montt. Entrenaba alumnos de forma informal. <strong>Sin ads, solo con landing y scripts</strong>, lanzó su primer grupo estructurado y cobró $240.000 CLP en la primera semana.
    </div>
  </div>
</div>

<!-- ─── PARA QUIEN ─── -->
<div class="para-quien">
  <div class="para-quien-inner">

    <div class="section-label">Este servicio es para vos si...</div>
    <div class="check-list">
      <div class="check-item"><span class="mark">✓</span>Ya entrenás gente y cobras por sesión ($15.000–$30.000 CLP)</div>
      <div class="check-item"><span class="mark">✓</span>Tenés entre 3 y 20 alumnos activos</div>
      <div class="check-item"><span class="mark">✓</span>Tenés WhatsApp o Instagram con algo de actividad</div>
      <div class="check-item"><span class="mark">✓</span>Querés llenar un grupo sin depender del boca a boca</div>
      <div class="check-item"><span class="mark">✓</span>No querés aprender marketing — solo entrenar</div>
    </div>

    <div class="no-list">
      <div class="no-label">No aplica si...</div>
      <div class="no-item"><span class="mark">—</span>Sos coach pero todavía no tenés alumnos que te paguen</div>
      <div class="no-item"><span class="mark">—</span>No estás en Chile o Argentina</div>
    </div>

  </div>
</div>

<!-- ─── PRECIO ─── -->
<div class="precio">
  <div class="section-label">La oferta</div>

  <div class="precio-box">
    <div class="precio-row">
      <div class="precio-campo">Entrada</div>
      <div class="precio-valor green">$0</div>
    </div>
    <div class="precio-row">
      <div class="precio-campo">Costo de ads (Meta)</div>
      <div class="precio-valor">Felipe los pone</div>
    </div>
    <div class="precio-row">
      <div class="precio-campo">Cobro cuando hay resultado</div>
      <div class="precio-valor">25% de lo que facture el grupo</div>
    </div>
    <div class="precio-row">
      <div class="precio-campo">Duración del lanzamiento</div>
      <div class="precio-valor">2–3 semanas</div>
    </div>
    <div class="precio-row">
      <div class="precio-campo">Cupos disponibles</div>
      <div class="precio-valor green">3 coaches — fase validación</div>
    </div>
  </div>

  <div class="garantia-box">
    <div class="garantia-title">Garantía total</div>
    <div class="garantia-text">
      Si el grupo no se llena, no me pagás nada. Felipe absorbe el costo de los ads. Sin resultado, sin cobro.
    </div>
  </div>

  <a href="https://wa.me/56961171595?text=Hola%20Felipe%2C%20vi%20lo%20de%20Cancha%20Llena%20y%20quiero%20saber%20si%20aplico" class="cta-final">
    Escribirme por WhatsApp →
  </a>
  <div class="cupos-finales">3 cupos · Se cierran cuando se completan</div>
</div>

<!-- ─── QUIEN SOY ─── -->
<div class="quien">
  <div class="quien-inner">
    <div class="quien-avatar">
      <img src="data:image/jpeg;base64,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" alt="Felipe Bartsch">
    </div>
    <div class="quien-body">
      <div class="quien-name">Felipe Bartsch</div>
      <div class="quien-rol">Driven Coach · Puerto Montt</div>
      <div class="quien-bio">
        Ayudo a coaches de básquet a llenar sus grupos sin que tengan que aprender marketing. Yo hago los ads, la landing y los scripts. El coach solo entrena.
      </div>
    </div>
  </div>
</div>

<!-- ─── FOOTER ─── -->
<footer>
  <div>Driven Coach · Puerto Montt, Chile</div>
  <div style="margin-top: 0.3rem;">
    <a href="https://wa.me/56961171595">WhatsApp</a>
    &nbsp;·&nbsp;
    <a href="/cdn-cgi/l/email-protection#147c7b78755470667d62717a777b75777c3a7778"><span class="__cf_
