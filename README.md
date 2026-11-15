<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<meta name="color-scheme" content="light dark">
<meta name="description" content="Basic Skills Training Center — SLLC Implementation Manual course (Chapters 4–14), with quizzes, final exam and certificate.">
<title>SLLC Implementation Manual — Basic Skills Training Center</title>
<link rel="icon" href='data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16"><circle cx="8" cy="8" r="7" fill="%231B2A4A"/><path d="M8 3 L11 6 L8 9 L5 6 Z" fill="%23C9A227"/></svg>'>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,500;12..96,700&family=Inter:wght@400;500;600;700&family=Playfair+Display:ital,wght@0,600;1,600&display=swap" rel="stylesheet">
<script>
try{
  var t = JSON.parse(localStorage.getItem('sllc-academy-v3') || '{}').theme;
  if (t === 'light' || t === 'dark') document.documentElement.setAttribute('data-theme', t);
}catch(e){}
</script>
<style>
:root{
  --bg:#F5F7F9; --surface:#FFFFFF; --surface2:#E8EDF2; --fg:#14201C; --muted:#52645E; --line:#D3DED9;
  --accent:#1B2A4A; --accent-fg:#FFFFFF; --accent-soft:#E6EBF2;
  --c0:#46605A; --c1:#C0432E; --c2:#B9860B; --c3:#2B63B8; --c4:#2E8B4E; --c5:#7A4FA3;
  --ok:#1F7A45; --bad:#B3321F; --hl:#FFF1B8; --gold:#C9A227;
  --fd:'Bricolage Grotesque','Inter',system-ui,sans-serif;
  --fb:'Inter',system-ui,-apple-system,'Segoe UI',sans-serif;
  --fs:'Playfair Display',Georgia,serif;
}
@media (prefers-color-scheme:dark){
  :root:not([data-theme="light"]){
    --bg:#0D1513; --surface:#151F1C; --surface2:#1C2925; --fg:#E7F0EC; --muted:#9DB0A9; --line:#2A3A35;
    --accent:#4FC3A6; --accent-fg:#06201A; --accent-soft:#16352E;
    --c0:#8FB0A6; --c1:#EE7B66; --c2:#E5B84A; --c3:#6FA1EE; --c4:#5CC27E; --c5:#B28BDA;
    --ok:#5CC27E; --bad:#F08B79; --hl:#4A4220; --gold:#D9B24C; color-scheme:dark;
  }
}
:root[data-theme="dark"]{
  --bg:#0D1513; --surface:#151F1C; --surface2:#1C2925; --fg:#E7F0EC; --muted:#9DB0A9; --line:#2A3A35;
  --accent:#4FC3A6; --accent-fg:#06201A; --accent-soft:#16352E;
  --c0:#8FB0A6; --c1:#EE7B66; --c2:#E5B84A; --c3:#6FA1EE; --c4:#5CC27E; --c5:#B28BDA;
  --ok:#5CC27E; --bad:#F08B79; --hl:#4A4220; --gold:#D9B24C; color-scheme:dark;
}
*{box-sizing:border-box}
html{scroll-behavior:smooth}
@media (prefers-reduced-motion:reduce){
  html{scroll-behavior:auto}
  *,*::before,*::after{animation-duration:.001ms!important;transition-duration:.001ms!important}
}
body{
  background:var(--bg); color:var(--fg); font:16px/1.65 var(--fb); margin:0;
  padding-left:max(16px,env(safe-area-inset-left,0px));
  padding-right:max(16px,env(safe-area-inset-right,0px));
}
body::before{content:"";position:fixed;inset:0 0 auto;height:0;height:env(safe-area-inset-top,0px);z-index:40;background:var(--surface)}
a{color:var(--accent)}
button,select,textarea,input{font:inherit;color:inherit}
:focus-visible{outline:3px solid var(--accent);outline-offset:2px}
.sr-only{position:absolute;width:1px;height:1px;padding:0;margin:-1px;overflow:hidden;clip:rect(0 0 0 0);white-space:nowrap;border:0}
.skip{position:absolute;left:-9999px;top:0;z-index:100;background:var(--accent);color:var(--accent-fg);padding:10px 16px;border-radius:0 0 8px 0;font-weight:600;text-decoration:none}
.skip:focus{left:0}

/* ---------- brand mark ---------- */
.brand-mark{display:flex;align-items:center;gap:10px;text-decoration:none;color:var(--fg)}
.brand-mark .mark{flex:none;display:block}
.brand-mark .words{display:flex;flex-direction:column;line-height:1.1;min-width:0}
.brand-mark .words strong{font:700 16px/1.1 var(--fd);letter-spacing:-.01em}
.brand-mark .words span{font:600 10.5px/1.2 var(--fb);letter-spacing:.14em;text-transform:uppercase;color:var(--muted);white-space:nowrap}

/* ---------- header ---------- */
.top{
  position:sticky;top:0;top:env(safe-area-inset-top,0px);z-index:30;background:var(--surface);
  border-bottom:1px solid var(--line);
  margin:0 calc(-1*max(16px,env(safe-area-inset-left,0px)));
  padding:10px max(16px,env(safe-area-inset-right,0px)) 10px max(16px,env(safe-area-inset-left,0px));
  display:flex;align-items:center;gap:12px;
}
.prog{flex:1;display:flex;align-items:center;gap:10px;min-width:0;justify-content:flex-end}
.bar{height:8px;background:var(--surface2);border-radius:99px;overflow:hidden;flex:0 1 200px;width:100%}
.bar>b{display:block;height:100%;background:var(--accent);width:0;transition:width .4s cubic-bezier(0.4, 0, 0.2, 1)}
.pct{font-size:13px;color:var(--muted);font-variant-numeric:tabular-nums;white-space:nowrap}
.icon-btn{background:transparent;border:1px solid var(--line);border-radius:8px;width:40px;height:40px;display:grid;place-items:center;cursor:pointer;font-size:17px;flex:none}
.icon-btn:hover{background:var(--surface2)}
#menuBtn{display:none}

/* ---------- buttons ---------- */
.btn{background:var(--accent);color:var(--accent-fg);border:0;border-radius:8px;padding:9px 16px;font-weight:600;cursor:pointer;min-height:40px;text-decoration:none;display:inline-flex;align-items:center;justify-content:center;gap:6px;transition:filter .15s}
.btn:hover{filter:brightness(1.08)}
.btn.ghost{background:transparent;color:var(--accent);border:1px solid var(--accent)}
.btn.ghost:hover{background:var(--accent-soft);filter:none}
.btn.sm{padding:5px 12px;min-height:32px;font-size:14px}
.btn.ok{background:var(--ok);color:#fff}
.btn.bad{background:var(--bad);color:#fff}
.btn:disabled{opacity:.45;cursor:not-allowed}

/* ---------- layout ---------- */
.shell{display:grid;grid-template-columns:300px minmax(0,1fr);gap:32px;max-width:1240px;margin:0 auto;padding-block:24px 150px}
nav#side{position:sticky;top:calc(64px + env(safe-area-inset-top,0px));align-self:start;max-height:calc(100vh - 150px);overflow:auto;font-size:14px;scrollbar-width:thin}
main{min-width:0;max-width:760px;min-height:400px;}
main:focus{outline:none}

/* ---------- sidebar ---------- */
.navtop{display:flex;flex-direction:column;gap:2px;padding-bottom:10px;border-bottom:1px solid var(--line);margin-bottom:10px}
.navh{font-size:11px;text-transform:uppercase;letter-spacing:.09em;color:var(--muted);margin:8px 0 4px;padding-left:8px;font-weight:600}
nav#side details{border-top:1px solid var(--line);padding:6px 0}
nav#side summary{display:flex;gap:8px;align-items:center;cursor:pointer;font-weight:600;padding:6px 8px;border-radius:6px;list-style:none;user-select:none}
nav#side summary:hover{background:var(--surface2)}
nav#side summary::-webkit-details-marker{display:none}
nav#side summary .ttl{flex:1;min-width:0}
nav#side .cnt{font-size:12px;color:var(--muted);font-variant-numeric:tabular-nums;flex:none}
.sw{width:10px;height:10px;border-radius:3px;flex:none;display:block}
nav#side a.li{display:flex;gap:8px;align-items:flex-start;padding:6px 8px 6px 26px;text-decoration:none;color:var(--fg);border-radius:6px;line-height:1.35}
nav#side a.li:hover{background:var(--surface2)}
nav#side a.li[aria-current="page"]{background:var(--accent-soft);font-weight:600}
nav#side .navtop a.li{padding-left:8px;font-weight:600}
.ck{width:16px;height:16px;border:1.5px solid var(--line);border-radius:50%;flex:none;margin-top:2px;display:grid;place-items:center;font-size:10px;line-height:1;color:transparent}
.ck.on{background:var(--ok);border-color:var(--ok);color:#fff}
.locked-note{font-size:13px;color:var(--muted);background:var(--surface2);border:1px dashed var(--line);border-radius:10px;padding:12px;margin-top:10px;line-height:1.5}

/* ---------- typography ---------- */
.crumb{font-size:13px;color:var(--muted);text-transform:uppercase;letter-spacing:.08em;display:flex;gap:8px;align-items:center;margin-bottom:6px}
h1{font:700 32px/1.12 var(--fd); font:700 clamp(28px,5vw,40px)/1.12 var(--fd);letter-spacing:-.02em;margin:0 0 8px;text-wrap:balance}
h2{font:700 24px/1.2 var(--fd); font:700 clamp(22px,3.4vw,28px)/1.2 var(--fd);letter-spacing:-.01em;margin:0 0 10px;text-wrap:balance}
h3{font:700 21px/1.25 var(--fd);margin:34px 0 8px;text-wrap:balance}
h4{font:700 14px/1.3 var(--fb);text-transform:uppercase;letter-spacing:.07em;margin:18px 0 6px}
p{margin:0 0 14px}
ul,ol{padding-left:22px;margin:0 0 16px}
li{margin-bottom:6px}
.lead{font-size:18px;color:var(--muted);max-width:64ch}
.meta{color:var(--muted);font-size:14px;margin-bottom:22px}
.muted{color:var(--muted)}
.callout{background:var(--accent-soft);border-radius:10px;padding:14px 16px;margin:20px 0}
.callout p:last-child{margin:0}
.callout.warn{background:var(--surface2);border:1px solid var(--line)}

/* ---------- status badge ---------- */
.status-badge{display:inline-flex;align-items:center;gap:6px;font-size:11px;font-weight:700;text-transform:uppercase;letter-spacing:.09em;padding:3px 10px;border-radius:99px;line-height:1.6}
.status-badge.pending{background:var(--hl);color:var(--fg)}
.status-badge.approved{background:var(--ok);color:#fff}
.status-badge.rejected{background:var(--bad);color:#fff}

/* ---------- cards / CTA ---------- */
.cta{display:flex;flex-wrap:wrap;gap:10px;margin:18px 0 26px}
.cards{display:grid;grid-template-columns:repeat(auto-fill,minmax(230px,1fr));gap:12px;margin:16px 0 24px}
.card{display:flex;flex-direction:column;gap:6px;padding:14px;border:1px solid var(--line);border-radius:12px;background:var(--surface);text-decoration:none;color:var(--fg);transition:all .2s}
.card:hover{border-color:var(--accent);transform:translateY(-2px);box-shadow:0 4px 12px rgba(0,0,0,0.05)}
.card .sw{width:12px;height:12px;margin-bottom:2px}

/* ---------- tables ---------- */
.tw{overflow-x:auto;margin:16px 0;border:1px solid var(--line);border-radius:10px;background:var(--surface)}
table{border-collapse:collapse;width:100%;min-width:680px;font-size:14px;line-height:1.5}
th,td{text-align:left;vertical-align:top;padding:10px 12px;border-bottom:1px solid var(--line)}
th{background:var(--surface2);font-size:12px;text-transform:uppercase;letter-spacing:.06em;font-weight:600}
tr:last-child td{border-bottom:0}
tbody tr:hover{background:var(--bg)}
td.rh{font-weight:600}
.chip{display:inline-block;font-size:11px;font-weight:600;text-transform:uppercase;letter-spacing:.06em;background:var(--accent-soft);color:var(--accent);border-radius:99px;padding:1px 8px;vertical-align:middle}
.rowactions{display:flex;flex-wrap:wrap;gap:6px}

/* ---------- tabs ---------- */
.tabs{display:flex;flex-wrap:wrap;gap:6px;margin:16px 0}
.tab{background:var(--surface);border:1px solid var(--line);border-radius:99px;padding:6px 14px;font-size:14px;font-weight:600;cursor:pointer;color:var(--muted);transition:all .15s}
.tab:hover{background:var(--surface2)}
.tab[aria-pressed="true"]{background:var(--accent);border-color:var(--accent);color:var(--accent-fg)}
.tab .n{font-variant-numeric:tabular-nums;opacity:.8;margin-left:4px}

/* ---------- widgets & forms ---------- */
.widget,.practice{background:var(--surface);border:1px solid var(--line);border-radius:12px;padding:16px;margin:22px 0}
.widget h4:first-child,.practice h4:first-child{margin-top:0}
.widget h4,.practice h4{color:var(--accent)}
label{display:block;font-weight:600;font-size:14px;margin-top:4px}
input[type="text"],input[type="email"],input[type="password"],select,textarea{
  width:100%;background:var(--bg);border:1px solid var(--line);border-radius:8px;padding:10px;margin:6px 0 12px;transition:border-color .15s;
}
input:focus,textarea:focus{outline:none;border-color:var(--accent);box-shadow:0 0 0 3px var(--accent-soft)}
textarea{resize:vertical;min-height:96px;font-family:var(--fb);font-size:15px}
[aria-invalid="true"]{border-color:var(--bad)!important}
.err{color:var(--bad);font-size:13px;margin:-6px 0 10px}
.hint{font-size:13px;color:var(--muted);margin:0 0 12px}
fieldset{border:1px solid var(--line);border-radius:10px;padding:12px;margin:0 0 14px}
legend{font-weight:600;padding:0 6px;font-size:15px}
.opt{display:flex;gap:10px;align-items:flex-start;padding:7px 6px;border-radius:8px;cursor:pointer;font-weight:400;margin:0}
.opt:hover{background:var(--surface2)}
.opt input{margin:4px 0 0;flex:none}
.fb{margin:10px 0 0;font-size:14px}
.fb.ok{color:var(--ok)}
.fb.bad{color:var(--bad)}

/* ---------- exam / quiz ---------- */
.q-block{border:1px solid var(--line);border-radius:12px;padding:14px 16px;margin:14px 0;background:var(--surface)}
.q-block .qn{font-size:12px;text-transform:uppercase;letter-spacing:.08em;color:var(--muted);margin:0 0 6px;font-weight:700}
.q-block legend{padding:0;font-size:15.5px;font-weight:600;margin:0 0 8px;display:block}
.q-block .why{margin-top:10px;font-size:13.5px}
.q-block.correct{border-color:var(--ok);background:linear-gradient(0deg,var(--accent-soft),transparent)}
.q-block.wrong{border-color:var(--bad)}
.score-line{display:flex;flex-wrap:wrap;align-items:center;gap:12px;margin:14px 0}
.score-big{font:700 34px/1 var(--fd);font-variant-numeric:tabular-nums}
.score-big small{font:600 14px/1 var(--fb);color:var(--muted);margin-left:6px}

/* ---------- lesson nav ---------- */
.lesson-nav{display:flex;flex-wrap:wrap;gap:10px;justify-content:space-between;align-items:center;margin:28px 0 0;padding-top:18px;border-top:1px solid var(--line)}
.lesson-nav a{max-width:46%;overflow:hidden;text-overflow:ellipsis;white-space:nowrap;display:block}

/* ---------- signature pad ---------- */
.sig-pad-wrap{position:relative;border:2px dashed var(--line);border-radius:12px;background:var(--surface);margin:10px 0 16px;touch-action:none;overflow:hidden;box-shadow:inset 0 2px 4px rgba(0,0,0,0.02)}
.sig-pad-wrap canvas{display:block;width:100%;height:180px;cursor:crosshair;border-radius:10px}
.sig-pad-wrap .placeholder{position:absolute;top:50%;left:50%;transform:translate(-50%,-50%);color:var(--muted);font-size:14px;pointer-events:none;text-align:center;opacity:0.6}
.sig-preview{max-width:240px;max-height:100px;display:block;margin:10px 0;background:#fff;padding:6px;border-radius:6px;border:1px solid var(--line);box-shadow:0 2px 8px rgba(0,0,0,0.05)}

/* =====================================================
   CERTIFICATE
   ===================================================== */
.cert-container {
  width:100%;
  overflow-x:auto;
  padding: 20px 0;
}
.cert{
  position:relative;
  margin:0 auto;
  width: 100%;
  max-width: 900px;
  padding: 40px 60px;
  padding: clamp(40px, 6vw, 70px) clamp(20px, 5vw, 60px);
  border-radius: 8px;
  text-align: center;
  background-color: #FDFBF7;
  background-image: 
    radial-gradient(circle at 50% 0%, rgba(201, 162, 39, 0.08) 0%, transparent 70%),
    url('data:image/svg+xml;utf8,<svg width="100" height="100" xmlns="http://www.w3.org/2000/svg"><path d="M0 0h100v100H0z" fill="none"/><path d="M50 50m-40 0a40 40 0 1 0 80 0a40 40 0 1 0 -80 0" stroke="%23C9A227" stroke-width="0.5" fill="none" opacity="0.1"/></svg>');
  box-shadow: 0 10px 40px rgba(0,0,0,0.08), 0 0 0 1px rgba(201, 162, 39, 0.3);
  color: #1B2A4A;
  font-family: var(--fb);
  -webkit-print-color-adjust: exact;
  print-color-adjust: exact;
}
.cert::before{
  content:"";position:absolute;inset:15px;
  border: 3px solid #C9A227; border-radius: 4px;
  pointer-events:none;
}
.cert::after{
  content:"";position:absolute;inset:22px;
  border: 1px solid rgba(27, 42, 74, 0.2); border-radius: 2px;
  pointer-events:none;
}
.cert-orn{
  position:absolute; width:20px; height:20px; background:#C9A227;
  transform:rotate(45deg); border-radius:2px; z-index:1;
  box-shadow: 0 0 0 4px #FDFBF7;
}
.cert-orn.tl{top:5px;left:5px}
.cert-orn.tr{top:5px;right:5px}
.cert-orn.bl{bottom:5px;left:5px}
.cert-orn.br{bottom:5px;right:5px}

.cert-logo{width:100%;max-width:380px;height:auto;margin:0 auto 20px;display:block}

.cert-kicker{
  display:inline-block; margin: 0 0 18px;
  font: 600 11px/1 var(--fb); letter-spacing:.3em; text-transform:uppercase;
  color: #fff; background: #1B2A4A;
  padding: 10px 24px 9px; border-radius: 99px;
}
.cert-title{
  font: 600 32px/1.1 var(--fs);
  font: 600 clamp(28px, 5vw, 42px)/1.1 var(--fs);
  color: #1B2A4A; margin:0 0 10px;
  letter-spacing: -0.02em;
}
.cert-rule{
  display:flex; align-items:center; justify-content:center; gap:12px;
  max-width: 300px; margin: 16px auto 24px;
  color: #C9A227; font-size: 12px;
}
.cert-rule::before, .cert-rule::after{
  content:""; height:1px; flex:1;
  background: linear-gradient(90deg, transparent, #C9A227, transparent);
}
.cert-presents{
  font-size:13px; text-transform:uppercase; letter-spacing:.18em;
  color: #52645E; margin:0 0 8px;
}
.cert-name{
  display:inline-block;
  font: 600 36px/1.15 var(--fs);
  font: 600 clamp(30px, 6vw, 54px)/1.15 var(--fs);
  color: #1B2A4A; margin: 0 0 20px;
  padding: 0 20px 12px;
  border-bottom: 2px solid #C9A227;
  max-width: 100%; overflow-wrap: anywhere;
}
.cert-body{
  max-width: 600px; margin: 0 auto 10px;
  font-size: 16px; color: #333; line-height: 1.7;
}
.cert-body strong { color: #1B2A4A; }

.cert-foot{
  display: grid;
  grid-template-columns: 1fr auto 1fr;
  align-items: end;
  gap: 20px 40px;
  margin-top: 50px;
  max-width: 700px;
  margin-inline: auto;
}
.cert-sign{
  display:flex; flex-direction:column; align-items:center; gap:4px; min-width:0;
}
.sigdate{
  font: 600 15px/1.3 var(--fb); color: #1B2A4A;
  min-height: 1.3em; margin-bottom: 8px;
}
.sig-img{
  max-height: 70px; max-width: 100%; object-fit: contain; margin-bottom: 4px;
}
.sig-img-empty{
  height: 70px; width: 100%; margin-bottom: 4px;
  border-bottom: 1px solid #1B2A4A;
}
.sigline{
  width: 100%; height: 1px; background: #1B2A4A; opacity: 0.3;
}
.siglabel{
  font-size: 11px; text-transform: uppercase; letter-spacing: .15em;
  color: #52645E; font-weight: 600; text-align: center;
}
.cert-seal{
  width: 100px; width: clamp(90px, 16vw, 130px); height: auto; display: block;
  filter: drop-shadow(0 6px 12px rgba(0,0,0,0.15));
  margin-bottom: -10px;
}
.cert-id{
  margin: 30px auto 0; font-size: 11px; letter-spacing: .15em;
  text-transform: uppercase; color: #888;
}

/* ---------- toasts ---------- */
.toasts{position:fixed;left:50%;transform:translateX(-50%);bottom:max(16px,env(safe-area-inset-bottom,0px));z-index:60;display:flex;flex-direction:column;gap:8px;width:min(92vw,420px);pointer-events:none}
.toast{background:var(--surface);color:var(--fg);border:1px solid var(--line);border-left:4px solid var(--accent);padding:10px 14px;border-radius:10px;font-size:14px;box-shadow:0 10px 30px rgb(0 0 0/.18);animation:tin .2s ease-out;transition:opacity .3s}
.toast.ok{border-left-color:var(--ok)}
.toast.bad{border-left-color:var(--bad)}
@keyframes tin{from{opacity:0;transform:translateY(10px)}to{opacity:1;transform:none}}

/* ---------- responsive ---------- */
@media (max-width:900px){
  .shell{grid-template-columns:minmax(0,1fr);padding-block:18px 120px}
  #menuBtn{display:inline-flex}
  nav#side{display:none;position:fixed;inset:0;top:calc(58px + env(safe-area-inset-top,0px));max-height:none;background:var(--bg);z-index:29;padding:12px max(16px,env(safe-area-inset-right,0px)) 160px max(16px,env(safe-area-inset-left,0px));overflow:auto}
  body.menu nav#side{display:block}
  body.menu{overflow:hidden}
  .pct{display:none}
  .bar{flex:1}
  .brand-mark .words span{font-size:9px}
}
@media (max-width:600px){
  .cert-foot{grid-template-columns:1fr;gap:30px}
  .cert-sign{width:100%;max-width:280px;margin:0 auto}
  .brand-mark .words span{display:none}
}
@media (max-width:520px){
  .lesson-nav a{max-width:100%}
}

/* ---------- print ---------- */
@media print{
  @page { size: landscape; margin: 0; }
  .top,nav#side,.skip,.toasts,.no-print{display:none!important}
  body{background:#fff;color:#000;padding:0;margin:0;}
  body::before{display:none}
  .shell{display:block;max-width:none;padding:0}
  main{max-width:none}
  .cert-container { padding: 0; overflow: visible; }
  .cert{
    box-shadow: none; border-radius: 0;
    width: 100%; max-width: 100%;
    height: 100vh;
    padding: 40px 60px;
    box-sizing: border-box;
    page-break-inside: avoid;
    background-color: #FDFBF7 !important;
  }
  .cert::before{border-color: #C9A227 !important}
  .cert-orn { display: none; }
  a{color:#000;text-decoration:none}
}
</style>
</head>
<body>
<a class="skip" href="#main">Skip to content</a>

<header class="top">
  <button id="menuBtn" class="btn ghost sm" aria-expanded="false" aria-controls="side" data-action="menu">Menu</button>
  <a class="brand-mark" href="#/home" aria-label="Basic Skills Training Center — home">
    <svg class="mark" viewBox="0 0 100 100" width="44" height="44" aria-hidden="true">
      <circle cx="50" cy="50" r="48" fill="#1B2A4A" stroke="#C9A227" stroke-width="3"/>
      <circle cx="50" cy="50" r="42" fill="none" stroke="#FFFFFF" stroke-width="1" opacity="0.4"/>
      <path d="M20 75 Q35 80 50 75 Q65 80 80 75 L80 85 Q65 90 50 85 Q35 90 20 85 Z" fill="#FFFFFF" opacity="0.9"/>
      <path d="M50 75 L50 85" stroke="#1B2A4A" stroke-width="1.5"/>
      <path d="M50 72 L50 45 L45 40" stroke="#C9A227" stroke-width="3" fill="none" stroke-linecap="round"/>
      <path d="M50 50 L56 42" stroke="#C9A227" stroke-width="3" fill="none" stroke-linecap="round"/>
      <circle cx="45" cy="38" r="8" fill="#2E8B57"/>
      <circle cx="55" cy="40" r="7" fill="#2E8B57"/>
      <circle cx="50" cy="32" r="9" fill="#2E8B57"/>
      <circle cx="38" cy="46" r="6" fill="#2E8B57"/>
      <circle cx="62" cy="48" r="6" fill="#2E8B57"/>
      <path d="M65 25 L67 29 L71 29 L68 32 L69 36 L65 34 L61 36 L62 32 L59 29 L63 29 Z" fill="#C9A227"/>
    </svg>
    <span class="words"><strong>Basic Skills</strong><span>Training Center</span></span>
  </a>
  <div class="prog">
    <div class="bar" id="pbar" role="progressbar" aria-label="Course progress" aria-valuemin="0" aria-valuemax="100" aria-valuenow="0"><b id="pfill"></b></div>
    <span class="pct" id="pct">0%</span>
  </div>
  <button class="icon-btn" id="themeBtn" data-action="theme" aria-label="Change colour theme">◐</button>
</header>

<div class="shell">
  <nav id="side" aria-label="Course outline"></nav>
  <main id="main" tabindex="-1">
    <div style="text-align:center;padding:50px;color:var(--muted)">Loading course...</div>
  </main>
</div>

<div class="toasts" id="toasts" aria-live="polite" aria-atomic="false"></div>

<noscript>
  <div class="callout bad" style="margin:20px;">
    <h2>JavaScript Required</h2>
    <p>This course requires JavaScript to run. Please enable JavaScript in your browser.</p>
  </div>
</noscript>

<script>
(function () {
  'use strict';

  const $  = (s, r = document) => r.querySelector(s);
  const $$ = (s, r = document) => Array.from(r.querySelectorAll(s));
  const esc = s => String(s).replace(/[&<>"']/g, c => ({ '&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;' }[c]));

  const MODULES = [
    {
      id: 'm4', title: 'Student Participation and Inclusion', color: 'var(--c1)',
      chapter: 'Chapter 4',
      blurb: 'Who attends, who is included, and how.',
      lessons: [
        {
          id: 'm4l1', title: 'Identifying students who need support', mins: 6,
          body: `
            <p>Not every child who needs help will ask for it, and the quietest children are often the ones furthest behind. The club starts with a simple, respectful identification process.</p>
            <h4>Three quick signals</h4>
            <ul>
              <li><strong>Reading:</strong> the child cannot read the words or letters you would expect for their grade.</li>
              <li><strong>Writing:</strong> written work is much shorter, less legible, or more hesitant than peers'.</li>
              <li><strong>Participation:</strong> the child avoids reading aloud, hides books, or is silent in discussion.</li>
            </ul>
            <h4>Tools you can use</h4>
            <ul>
              <li>A short <strong>letter and sound check</strong> — point to letters and ask for the sound.</li>
              <li>A <strong>one-minute read</strong> from a short passage, counting correct words.</li>
              <li>A <strong>writing sample</strong> — a five-minute "quick write" on a familiar topic.</li>
            </ul>
            <p>Identification should never feel like a test the child can fail. Say clearly: <em>"This helps me help you."</em></p>
            <div class="callout"><p><strong>Remember:</strong> the aim of identification is placement, not labelling. Children's needs change, and so should their group.</p></div>`,
          check: {
            q: 'The main purpose of identifying students who need support is…',
            opts: ['To label weak learners', 'To place them in the right group and support them', 'To report them to parents'],
            a: 1,
            why: 'Identification guides support and grouping — it is not a judgement about the child.'
          }
        },
        {
          id: 'm4l2', title: 'Inclusion of children with disabilities', mins: 7,
          body: `
            <p>Inclusive literacy clubs assume that every child can learn to read and write — with the right access. Exclusion usually comes from barriers in the environment, not from the child.</p>
            <h4>Common barriers and simple responses</h4>
            <div class="tw"><table>
              <thead><tr><th>Barrier</th><th>Simple response</th></tr></thead>
              <tbody>
                <tr><td class="rh">Low vision</td><td>Large-print texts, seat near light, use a pointer, allow oral responses.</td></tr>
                <tr><td class="rh">Hearing loss</td><td>Sit close, face the child when speaking, use gestures and visuals.</td></tr>
                <tr><td class="rh">Physical disability</td><td>Accessible seating, table height, reachable bookshelf.</td></tr>
                <tr><td class="rh">Learning disability</td><td>More time, multisensory activities, repeated practice, one instruction at a time.</td></tr>
                <tr><td class="rh">Speech difficulties</td><td>Allow alternative response modes (pointing, writing, drawing).</td></tr>
              </tbody>
            </table></div>
            <p>The club should be the most inclusive space in the school — a place where children are not filtered out by a test they cannot access.</p>
            <div class="callout"><p><strong>Key idea:</strong> adapt the activity, not the child. Every activity can be offered in at least two ways.</p></div>`,
          check: {
            q: 'When a child with low vision joins the club, the best first response is…',
            opts: ['Excuse them from reading activities', 'Provide large-print materials, seating near light and a pointer', 'Seat them at the back to avoid distraction'],
            a: 1,
            why: 'The barrier is access, not ability — large print, good light and a pointer remove it.'
          }
        },
        {
          id: 'm4l3', title: 'Safe and accessible learning environments', mins: 5,
          body: `
            <p>Children participate fully only when they feel physically and emotionally safe. A safe club has four visible features.</p>
            <ul>
              <li><strong>Physical safety:</strong> safe furniture, clear space, no blocked exits, adequate light and ventilation.</li>
              <li><strong>Emotional safety:</strong> no mocking of mistakes, no public shaming, encouraging voice.</li>
              <li><strong>Social safety:</strong> clear anti-bullying rules that apply to volunteers and students.</li>
              <li><strong>Accessibility:</strong> materials reachable by all heights, seating for children with disabilities, quiet corner for those who need it.</li>
            </ul>
            <p>Children should know what to do if they feel unsafe. Agree a simple reporting route: tell the club facilitator, tell the club patron, or drop a note in a closed box.</p>`,
          check: {
            q: 'Which of these is the strongest sign of an emotionally safe club?',
            opts: ['Children are silent while the volunteer reads', 'Children try hard and make mistakes without fear', 'Children only speak when called on'],
            a: 1,
            why: 'A safe club encourages participation — mistakes are treated as learning, not failure.'
          }
        }
      ],
      quiz: {
        title: 'Chapter 4 quiz — Participation and inclusion',
        questions: [
          { q: 'The best reason to identify struggling readers early is to…', opts: ['Separate them from the class', 'Place them in the right group and support them', 'Report them to the woreda'], a: 1, why: 'Identification is about support and grouping, not labelling.' },
          { q: 'Which adjustment supports a child with low vision?', opts: ['Excusing them from reading', 'Seating near light with large print and a pointer', 'Reading for them so they do not have to'], a: 1, why: 'Access adaptations remove the barrier without lowering expectations.' },
          { q: 'A safe learning environment requires…', opts: ['Quiet children', 'Physical, emotional and social safety', 'A strict discipline policy only'], a: 1, why: 'Safety has physical, emotional and social dimensions and must be visible.' }
        ]
      }
    },
    {
      id: 'm5', title: 'Volunteers and Reading Buddy Programme', color: 'var(--c3)',
      chapter: 'Chapter 5',
      blurb: 'Recruiting, supporting and keeping good volunteers.',
      lessons: [
        {
          id: 'm5l1', title: 'Volunteer recruitment', mins: 6,
          body: `
            <p>Volunteers extend what a teacher alone can offer, and a well-chosen volunteer changes a child's trajectory. Recruitment is deliberate, not improvised.</p>
            <h4>Where volunteers come from</h4>
            <ul>
              <li>Parents and caregivers (especially those who work nearby).</li>
              <li>Upper-primary and secondary students (Reading Buddies).</li>
              <li>Retired teachers, youth groups and faith-based groups.</li>
              <li>PTSA members, community elders and local professionals.</li>
            </ul>
            <h4>Messages that attract the right people</h4>
            <ul>
              <li><em>"Two hours a week is enough to help a child read."</em></li>
              <li><em>"You do not need to be a teacher — you need patience and reliability."</em></li>
              <li><em>"We train, support and value every volunteer."</em></li>
            </ul>
            <h4>Selection signals</h4>
            <p>Reliability, warmth, ability to follow safeguarding rules, respect for children, and willingness to learn. References and safeguarding checks are essential.</p>`,
          check: {
            q: 'Which is the best recruitment message for volunteers?',
            opts: ['Only qualified teachers may apply', 'Two hours a week — with training and support — can help a child read', 'Volunteers must commit for three years'],
            a: 1,
            why: 'Realistic, encouraging messages attract reliable volunteers without over-promising.'
          }
        },
        {
          id: 'm5l2', title: 'Volunteer responsibilities and support', mins: 6,
          body: `
            <p>Volunteers do not replace teachers. They extend and enrich what teachers have begun.</p>
            <h4>Core responsibilities</h4>
            <ul>
              <li>Attend sessions on time and prepared.</li>
              <li>Work with the group or buddy assigned by the facilitator.</li>
              <li>Follow the safeguarding code of conduct and confidentiality rules.</li>
            </ul>
            <h4>Ongoing support</h4>
            <ul>
              <li>Weekly check-ins with the club facilitator.</li>
              <li>Access to simple activity cards and reading materials.</li>
              <li>Peer sharing sessions to discuss successes and challenges.</li>
            </ul>
            <div class="callout"><p><strong>Appreciation:</strong> Volunteers work without pay. A sincere thank you, a certificate of recognition, and community acknowledgment keep motivation high.</p></div>`,
          check: {
            q: 'What is the most effective form of ongoing support for volunteers?',
            opts: ['Weekly check-ins, simple activity cards and peer sharing', 'Strict monitoring with unannounced inspections', 'Leaving them to work independently without guidance'],
            a: 0,
            why: 'Regular guidance and ready-to-use materials ensure volunteers feel confident and effective.'
          }
        }
      ],
      quiz: {
        title: 'Chapter 5 quiz — Volunteers and Buddy Programme',
        questions: [
          { q: 'Who makes ideal reading buddies in school?', opts: ['Only university graduates', 'Upper-primary or secondary students with good reading skills', 'School administrators'], a: 1, why: 'Upper-primary students act as relatable mentors when properly prepared.' },
          { q: 'What is the primary role of a volunteer?', opts: ['To replace the classroom teacher', 'To extend and enrich reading practice', 'To test and grade students'], a: 1, why: 'Volunteers provide targeted practice and encouragement, complementing teachers.' }
        ]
      }
    },
    {
      id: 'm6', title: 'Teaching Reading and Comprehension Strategies', color: 'var(--c2)',
      chapter: 'Chapter 6',
      blurb: 'Phonics, fluency, vocabulary, and active comprehension.',
      lessons: [
        {
          id: 'm6l1', title: 'The core pillars of early reading', mins: 8,
          body: `
            <p>Reading is not a single skill; it rests on interconnected pillars that must be nurtured together.</p>
            <ul>
              <li><strong>Phonemic Awareness:</strong> Hearing and manipulating sounds in spoken words.</li>
              <li><strong>Phonics:</strong> Linking letters to sounds to decode written words.</li>
              <li><strong>Fluency:</strong> Reading smoothly, accurately, and with proper expression.</li>
              <li><strong>Vocabulary:</strong> Knowing the meanings of words heard and read.</li>
              <li><strong>Comprehension:</strong> Understanding, reflecting on, and extracting meaning from text.</li>
            </ul>
            <div class="callout"><p><strong>Practice:</strong> Every club session should include time for code-based practice (letters/sounds) and meaning-based practice (stories/discussion).</p></div>`,
          check: {
            q: 'Which pillar focuses specifically on linking written letters to their corresponding sounds?',
            opts: ['Vocabulary', 'Phonics', 'Fluency'],
            a: 1,
            why: 'Phonics connects graphemes (letters) to phonemes (sounds).'
          }
        },
        {
          id: 'm6l2', title: 'Active comprehension techniques', mins: 7,
          body: `
            <p>Reading aloud without understanding is not reading. Active comprehension happens before, during, and after reading.</p>
            <h4>Key questioning strategies</h4>
            <ul>
              <li><strong>Before reading:</strong> Look at the cover and pictures. Ask: <em>"What do you think happens next?"</em></li>
              <li><strong>During reading:</strong> Pause and check understanding. Ask: <em>"Why did the character do that?"</em></li>
              <li><strong>After reading:</strong> Retell the main points and connect the story to real life.</li>
            </ul>`,
          check: {
            q: 'When should prediction and questioning take place?',
            opts: ['Only after finishing the entire book', 'Before, during, and after reading', 'Only when children struggle with a word'],
            a: 1,
            why: 'Active comprehension is a continuous cognitive process throughout the reading journey.'
          }
        }
      ],
      quiz: {
        title: 'Chapter 6 quiz — Reading strategies',
        questions: [
          { q: 'What are the two main dimensions every club session should balance?', opts: ['Code-based practice and meaning-based practice', 'Silent reading and rigorous testing', 'Singing and drawing'], a: 0, why: 'Balanced literacy combines decoding skills with comprehension.' },
          { q: 'Asking "What do you think will happen next?" before reading helps build…', opts: ['Decoding speed', 'Active prediction and comprehension', 'Handwriting posture'], a: 1, why: 'Predicting engages prior knowledge and focuses attention.' }
        ]
      }
    },
    {
      id: 'm7', title: 'Teaching Writing and Vocabulary Development', color: 'var(--c4)',
      chapter: 'Chapter 7',
      blurb: 'From letter formation to creative expression and word mastery.',
      lessons: [
        {
          id: 'm7l1', title: 'Building vocabulary intentionally', mins: 6,
          body: `
            <p>Children need rich vocabulary to understand advanced texts. New words should be taught explicitly and used repeatedly in context.</p>
            <h4>Four steps to teach a new word</h4>
            <ol>
              <li>Say the word clearly and have children repeat it.</li>
              <li>Provide a simple, child-friendly definition.</li>
              <li>Give an example of the word used in a sentence.</li>
              <li>Ask children to make their own sentence using the word.</li>
            </ol>`,
          check: {
            q: 'What is the most effective way to help children retain a new vocabulary word?',
            opts: ['Copying it 50 times in a notebook', 'Hearing its definition and using it in spoken sentences', 'Memorizing the dictionary'],
            a: 1,
            why: 'Active usage and contextual examples cement vocabulary in long-term memory.'
          }
        },
        {
          id: 'm7l2', title: 'Supported writing activities', mins: 7,
          body: `
            <p>Writing reinforces reading. Start small and build confidence progressively.</p>
            <ul>
              <li><strong>Shared writing:</strong> Facilitator writes down what children dictate.</li>
              <li><strong>Guided writing:</strong> Writing sentences together on the chalkboard.</li>
              <li><strong>Independent writing:</strong> Quick writes, journaling, and creative storytelling.</li>
            </ul>`,
          check: {
            q: 'Shared writing is especially useful because…',
            opts: ['It requires no chalkboard', 'It connects spoken language to written symbols with facilitator support', 'It replaces reading practice entirely'],
            a: 1,
            why: 'Shared writing demonstrates how thoughts become written text safely.'
          }
        }
      ],
      quiz: {
        title: 'Chapter 7 quiz — Writing and vocabulary',
        questions: [
          { q: 'In shared writing, who composes the sentences?', opts: ['Only the facilitator', 'The children dictate while the facilitator writes', 'The school director'], a: 1, why: 'Children generate the ideas while the adult models transcription.' },
          { q: 'Why is vocabulary instruction critical for reading?', opts: ['It makes books heavier', 'Meaningful word knowledge unlocks text comprehension', 'It speeds up handwriting'], a: 1, why: 'You cannot comprehend words whose meanings are unknown.' }
        ]
      }
    },
    {
      id: 'm8', title: 'Formative Assessment and Progress Monitoring', color: 'var(--c5)',
      chapter: 'Chapter 8',
      blurb: 'Tracking growth without stress using simple observation tools.',
      lessons: [
        {
          id: 'm8l1', title: 'Formative vs. summative assessment', mins: 6,
          body: `
            <p>Assessment in literacy clubs is meant to guide instruction, not to rank or penalize children.</p>
            <ul>
              <li><strong>Formative assessment:</strong> Daily checks during activities to see who needs help right now.</li>
              <li><strong>Summative assessment:</strong> Periodic reviews at the end of a term to measure overall progress.</li>
            </ul>
            <p>Keep observation checklists simple: date, child's name, and 3 key competencies being observed.</p>`,
          check: {
            q: 'Formative assessment is primarily used to…',
            opts: ['Assign final grades for report cards', 'Guide daily teaching and immediate support', 'Punish inattentive students'],
            a: 1,
            why: 'Formative checks provide real-time feedback to adjust instruction.'
          }
        }
      ],
      quiz: {
        title: 'Chapter 8 quiz — Assessment',
        questions: [
          { q: 'What is the primary characteristic of formative assessment in the club?', opts: ['It is high-stakes and timed', 'It is continuous and informs daily support', 'It happens only once a year'], a: 1, why: 'Formative assessment is ongoing and instructional.' }
        ]
      }
    },
    {
      id: 'm9', title: 'Classroom Management and Positive Discipline', color: 'var(--c0)',
      chapter: 'Chapter 9',
      blurb: 'Creating joyful, orderly, and respectful learning spaces.',
      lessons: [
        {
          id: 'm9l1', title: 'Establishing positive routines', mins: 6,
          body: `
            <p>Good management comes from clear routines, engaging activities, and mutual respect rather than fear or harsh punishment.</p>
            <ul>
              <li>Establish clear signals for starting and stopping activities.</li>
              <li>Keep transitions fast and energetic.</li>
              <li>Praise effort and cooperation publicly; correct privately and gently.</li>
            </ul>`,
          check: {
            q: 'What is the foundation of positive classroom management?',
            opts: ['Strict corporal punishment', 'Clear routines, engagement, and mutual respect', 'Complete silence at all times'],
            a: 1,
            why: 'Predictable routines and positive reinforcement foster a secure learning atmosphere.'
          }
        }
      ],
      quiz: {
        title: 'Chapter 9 quiz — Management',
        questions: [
          { q: 'When a child misbehaves during a club activity, the best first step is…', opts: ['Expel them immediately', 'Address the behavior calmly and privately with positive guidance', 'Yout at the entire group'], a: 1, why: 'Private, calm correction preserves dignity and maintains safety.' }
        ]
      }
    },
    {
      id: 'm10', title: 'Teaching Learning Materials (TLM) Creation and Use', color: 'var(--c1)',
      chapter: 'Chapter 10',
      blurb: 'Making low-cost, high-impact reading aids from local resources.',
      lessons: [
        {
          id: 'm10l1', title: 'Creating local TLMs', mins: 7,
          body: `
            <p>You do not need expensive imported books to run a successful literacy club. Local materials are often more relevant and engaging.</p>
            <ul>
              <li><strong>Letter cards & word cards:</strong> Made from cardboard boxes or heavy paper.</li>
              <li><strong>Storybooks:</strong> Written and illustrated by teachers, students, and community members.</li>
              <li><strong>Word walls:</strong> Displaying high-frequency words on classroom walls.</li>
            </ul>`,
          check: {
            q: 'What is a major benefit of locally made TLMs?',
            opts: ['They are expensive', 'They are culturally relevant, affordable, and sustainable', 'They never get damaged'],
            a: 1,
            why: 'Local materials utilize readily available resources and reflect local contexts.'
          }
        }
      ],
      quiz: {
        title: 'Chapter 10 quiz — TLMs',
        questions: [
          { q: 'Which material can be easily repurposed to make letter flashcards?', opts: ['Cardboard boxes', 'Glass bottles', 'Metal sheets'], a: 0, why: 'Cardboard is sturdy, free, and easy to cut into cards.' }
        ]
      }
    },
    {
      id: 'm11', title: 'Community Engagement and Parental Involvement', color: 'var(--c3)',
      chapter: 'Chapter 11',
      blurb: 'Partnering with families and community leaders for sustainable impact.',
      lessons: [
        {
          id: 'm11l1', title: 'Involving parents in literacy', mins: 6,
          body: `
            <p>Children thrive when schools and families work together to champion reading.</p>
            <ul>
              <li>Invite parents to open club days and storytelling sessions.</li>
              <li>Show parents how to support reading at home through simple storytelling and conversation.</li>
              <li>Communicate regularly with community elders and PTSA members.</li>
            </ul>`,
          check: {
            q: 'How can parents support literacy at home without formal reading skills?',
            opts: ['By telling traditional stories and discussing daily experiences', 'By teaching complex grammar rules', 'By purchasing expensive computers'],
            a: 0,
            why: 'Oral storytelling and rich conversation build foundational language and comprehension.'
          }
        }
      ],
      quiz: {
        title: 'Chapter 11 quiz — Community engagement',
        questions: [
          { q: 'Why is parental involvement crucial for the literacy club?', opts: ['Parents can pay monthly taxes', 'It reinforces learning beyond school hours and ensures community ownership', 'It replaces the teacher'],
            a: 1,
            why: 'Family support bridges school and home, reinforcing learning continuity.' }
        ]
      }
    },
    {
      id: 'm12', title: 'Monitoring, Evaluation, and Accountability', color: 'var(--c2)',
      chapter: 'Chapter 12',
      blurb: 'Using data to track attendance, progress, and continuous improvement.',
      lessons: [
        {
          id: 'm12l1', title: 'Tracking club success', mins: 6,
          body: `
            <p>Good data tells you what is working and where adjustments are needed.</p>
            <ul>
              <li>Maintain accurate daily attendance logs (disaggregated by gender and disability).</li>
              <li>Track reading fluency and vocabulary growth quarterly.</li>
              <li>Review feedback boxes and facilitator logs regularly.</li>
            </ul>`,
          check: {
            q: 'Why should attendance records be disaggregated by gender and disability?',
            opts: ['To meet bureaucratic quotas', 'To ensure equitable participation across all groups', 'To make registers heavier'],
            a: 1,
            why: 'Disaggregation highlights inclusion gaps so facilitators can take corrective action.'
          }
        }
      ],
      quiz: {
        title: 'Chapter 12 quiz — M&E',
        questions: [
          { q: 'What is the primary purpose of collecting monitoring data in the club?', opts: ['To punish poor performers', 'To inform continuous improvement and ensure equity', 'To sell reports to corporations'], a: 1, why: 'Data drives evidence-based decisions and program improvement.' }
        ]
      }
    },
    {
      id: 'm13', title: 'Program Sustainability and Transition', color: 'var(--c4)',
      chapter: 'Chapter 13',
      blurb: 'Ensuring clubs thrive long after initial project funding ends.',
      lessons: [
        {
          id: 'm13l1', title: 'Building local ownership', mins: 6,
          body: `
            <p>Sustainability relies on community ownership, trained local volunteers, and school integration.</p>
            <ul>
              <li>Hand over leadership to school clubs, PTSAs, and local champions.</li>
              <li>Reuse local TLMs and share best practices across clusters.</li>
              <li>Establish school-level resource sharing so books and materials remain accessible.</li>
            </ul>`,
          check: {
            q: 'What is the key indicator of program sustainability?',
            opts: ['Continuous reliance on external donors', 'Strong community and school ownership maintaining activities independently', 'Closing down the club after one year'],
            a: 1,
            why: 'Local ownership ensures activities continue indefinitely without external dependency.'
          }
        }
      ],
      quiz: {
        title: 'Chapter 13 quiz — Sustainability',
        questions: [
          { q: 'Who should ultimately drive the sustainability of the literacy club?', opts: ['Foreign donors', 'The local school community, PTSA, and volunteers', 'Only government ministers'], a: 1, why: 'Local stakeholders are permanent fixtures of the school ecosystem.' }
        ]
      }
    },
    {
      id: 'm14', title: 'Final Exam and Certification', color: 'var(--c5)',
      chapter: 'Chapter 14',
      blurb: 'Comprehensive review, final examination, and certificate issuance.',
      lessons: [
        {
          id: 'm14l1', title: 'Final certification readiness', mins: 5,
          body: `
            <p>Congratulations on reaching the final chapter of the SLLC Implementation Manual course!</p>
            <p>You are now ready to take the final certification exam. Passing the exam with a score of 80% or higher will unlock your official certificate of completion, which you can sign, save, and print.</p>
            <div class="callout"><p><strong>Tip:</strong> Review your notes on inclusive practices, reading pillars, formative assessment, and volunteer management before starting the exam.</p></div>`,
          check: {
            q: 'What passing score is required to unlock your certificate of completion?',
            opts: ['50%', '70%', '80%'],
            a: 2,
            why: 'An 80% passing threshold ensures mastery of the implementation manual principles.'
          }
        }
      ],
      quiz: {
        title: 'Final Certification Exam',
        exam: true,
        questions: [
          { q: 'What is the primary goal of the SLLC literacy club?', opts: ['To replace formal schooling', 'To provide joyful, supportive foundational literacy and numeracy practice', 'To test children rigorously'], a: 1, why: 'Clubs build foundational reading and confidence through engaging practice.' },
          { q: 'How should children with diverse learning needs be included?', opts: ['Excluded from group activities', 'Supported with adaptive materials and inclusive teaching strategies', 'Ignored until they catch up'], a: 1, why: 'Inclusive practices adapt the environment and activities to ensure full access.' },
          { q: 'Which assessment type is used daily to guide instruction?', opts: ['Summative exam', 'Formative assessment', 'National standardized testing'], a: 1, why: 'Formative assessment provides ongoing feedback for daily teaching adjustments.' },
          { q: 'Who are ideal reading buddies for younger students?', opts: ['Upper-primary students and community volunteers', 'No one — children must read alone', 'Strict school inspectors'], a: 0, why: 'Trained older students and community members provide excellent peer mentoring.' },
          { q: 'What material is best for creating low-cost TLMs?', opts: ['Imported plastic toys', 'Locally available cardboard, paper, and natural items', 'Expensive electronic tablets'], a: 1, why: 'Local, low-cost materials are sustainable and culturally appropriate.' },
          { q: 'Why is community and parental involvement essential?', opts: ['To collect fines', 'To ensure reading practice continues at home and guarantees sustainability', 'To grade report cards'], a: 1, why: 'Family and community partnership creates a supportive reading culture.' },
          { q: 'What is the correct approach to managing student behavior in the club?', opts: ['Harsh physical punishment', 'Positive discipline, clear routines, and calm redirection', 'Expelling disruptive children'], a: 1, why: 'Positive discipline builds emotional safety and mutual respect.' },
          { q: 'What metric should be tracked in attendance registers for equity?', opts: ['Only total numbers', 'Disaggregation by gender and disability status', 'Only top readers'], a: 1, why: 'Disaggregation ensures no vulnerable group is left behind.' },
          { q: 'How should new vocabulary be introduced?', opts: ['Memorizing lists without context', 'Explicitly stating definitions, giving examples, and using in sentences', 'Skipping unknown words'], a: 1, why: 'Explicit, contextual vocabulary instruction deepens comprehension.' },
          { q: 'What is the ultimate indicator of club sustainability?', opts: ['Permanent dependency on external grants', 'Strong local ownership by schools, volunteers, and the community', 'Stopping all activities after training'], a: 1, why: 'Local leadership and ownership guarantee long-term continuity.' }
        ]
      }
    }
  ];

  /* =========================================================
     State Management
     ========================================================= */
  let state = {
    progress: {}, // { lessonId: true }
    quizzes: {},  // { moduleId: score }
    examScore: null,
    cert: { name: '', date: '', sigData: '', id: '' },
    theme: 'light'
  };

  try {
    const saved = JSON.parse(localStorage.getItem('sllc-academy-v3') || '{}');
    if (saved.progress) state.progress = saved.progress;
    if (saved.quizzes) state.quizzes = saved.quizzes;
    if (saved.examScore !== undefined) state.examScore = saved.examScore;
    if (saved.cert) state.cert = saved.cert;
    if (saved.theme) state.theme = saved.theme;
  } catch (e) {}

  function saveState() {
    try {
      localStorage.setItem('sllc-academy-v3', JSON.stringify(state));
    } catch (e) {}
    updateProgressUI();
  }

  function showToast(msg, type = 'ok') {
    const t = document.createElement('div');
    t.className = `toast ${type}`;
    t.textContent = msg;
    $('#toasts').appendChild(t);
    setTimeout(() => {
      t.style.opacity = '0';
      setTimeout(() => t.remove(), 300);
    }, 3500);
  }

  /* =========================================================
     Progress Calculations
     ========================================================= */
  const allLessons = MODULES.flatMap(m => m.lessons);
  const totalLessonsCount = allLessons.length;

  function getCompletedCount() {
    return allLessons.filter(l => state.progress[l.id]).length;
  }

  function getProgressPct() {
    if (totalLessonsCount === 0) return 0;
    return Math.round((getCompletedCount() / totalLessonsCount) * 100);
  }

  function updateProgressUI() {
    const pct = getProgressPct();
    const pbar = $('#pbar');
    const pfill = $('#pfill');
    const pctEl = $('#pct');
    if (pbar) pbar.setAttribute('aria-valuenow', pct);
    if (pfill) pfill.style.width = pct + '%';
    if (pctEl) pctEl.textContent = pct + '%';
  }

  /* =========================================================
     Navigation & Routing
     ========================================================= */
  function renderNav() {
    const nav = $('#side');
    if (!nav) return;

    let html = `
      <div class="navtop">
        <a class="li" href="#/home">
          <span class="ck ${getCompletedCount() === totalLessonsCount ? 'on' : ''}">✓</span>
          <span class="ttl"><strong>Course Overview</strong></span>
        </a>
      </div>
    `;

    MODULES.forEach(m => {
      const completedL = m.lessons.filter(l => state.progress[l.id]).length;
      const totalL = m.lessons.length;
      const isQuizDone = state.quizzes[m.id] !== undefined;

      html = html + `
        <details ${location.hash.includes(m.id) ? 'open' : ''}>
          <summary>
            <span class="sw" style="background:${m.color}"></span>
            <span class="ttl">${esc(m.chapter)}</span>
            <span class="cnt">${completedL}/${totalL}</span>
          </summary>
          <div style="padding-left:12px">
      `;

      m.lessons.forEach(l => {
        const done = state.progress[l.id];
        const active = location.hash === `#/lesson/${l.id}` ? 'aria-current="page"' : '';
        html = html + `
          <a class="li" href="#/lesson/${l.id}" ${active}>
            <span class="ck ${done ? 'on' : ''}">✓</span>
            <span class="ttl">${esc(l.title)}</span>
          </a>
        `;
      });

      const qActive = location.hash === `#/quiz/${m.id}` ? 'aria-current="page"' : '';
      const qDoneCls = isQuizDone ? 'on' : '';
      html = html + `
            <a class="li" href="#/quiz/${m.id}" ${qActive}>
              <span class="ck ${qDoneCls}">✓</span>
              <span class="ttl"><em>${m.quiz.exam ? 'Final Exam' : 'Chapter Quiz'}</em></span>
            </a>
          </div>
        </details>
      `;
    });

    const certActive = location.hash === '#/certificate' ? 'aria-current="page"' : '';
    const certUnlocked = state.examScore !== null && state.examScore >= 80;
    html = html + `
      <div class="navtop" style="margin-top:10px;border-top:1px solid var(--line);padding-top:10px">
        <a class="li" href="#/certificate" ${certActive}>
          <span class="ck ${certUnlocked ? 'on' : ''}">✓</span>
          <span class="ttl"><strong>Certificate of Completion</strong></span>
        </a>
      </div>
    `;

    nav.innerHTML = html;
  }

  function handleRoute() {
    const hash = location.hash || '#/home';
    const main = $('#main');
    if (!main) return;

    // Close mobile menu if open
    document.body.classList.remove('menu');
    const menuBtn = $('#menuBtn');
    if (menuBtn) menuBtn.setAttribute('aria-expanded', 'false');

    if (hash === '#/home') {
      renderHome(main);
    } else if (hash.startsWith('#/lesson/')) {
      const lessonId = hash.replace('#/lesson/', '');
      renderLesson(lessonId, main);
    } else if (hash.startsWith('#/quiz/')) {
      const modId = hash.replace('#/quiz/', '');
      renderQuiz(modId, main);
    } else if (hash === '#/certificate') {
      renderCertificate(main);
    } else {
      location.hash = '#/home';
    }
    renderNav();
    window.scrollTo({ top: 0, behavior: 'smooth' });
  }

  /* =========================================================
     Views Renderers
     ========================================================= */
  function renderHome(container) {
    const pct = getProgressPct();
    const completed = getCompletedCount();

    let html = `
      <div class="crumb">SLLC Implementation Manual Course</div>
      <h1>Basic Skills Training Center</h1>
      <p class="lead">Chapters 4 to 14 of the Structured Literacy and Language Club (SLLC) Implementation Manual. Master inclusive instruction, reading pillars, formative assessment, community engagement, and program sustainability.</p>
      
      <div class="cards" style="margin:24px 0">
        <div class="card">
          <span class="sw" style="background:var(--accent)"></span>
          <strong>${completed} /${totalLessonsCount} Lessons Completed</strong>
          <span class="muted">${pct}% overall progress</span>
        </div>
        <div class="card">
          <span class="sw" style="background:var(--ok)"></span>
          <strong>Final Exam Status</strong>
          <span class="muted">${state.examScore !== null ? state.examScore + '% Score' : 'Not taken yet'}</span>
        </div>
      </div>

      <h2>Course Outline</h2>
      <p>Select any chapter below to begin or continue your learning journey:</p>
      <div class="cards">
    `;

    MODULES.forEach(m => {
      const comp = m.lessons.filter(l => state.progress[l.id]).length;
      html = html + `
        <a class="card" href="#/lesson/${m.lessons[0].id}">
          <div style="display:flex;align-items:center;gap:8px">
            <span class="sw" style="background:${m.color}"></span>
            <span style="font-size:12px;text-transform:uppercase;font-weight:700;color:var(--muted)">${esc(m.chapter)}</span>
          </div>
          <strong style="font-size:16px">${esc(m.title)}</strong>
          <span class="muted" style="font-size:13px">${comp}/${m.lessons.length} lessons completed</span>
        </a>
      `;
    });

    html = html + `</div>`;
    container.innerHTML = html;
  }

  function renderLesson(lessonId, container) {
    let currentModule = null;
    let currentIndex = -1;
    let lesson = null;

    MODULES.forEach(m => {
      m.lessons.forEach((l, idx) => {
        if (l.id === lessonId) {
          currentModule = m;
          currentIndex = idx;
          lesson = l;
        }
      });
    });

    if (!lesson || !currentModule) {
      container.innerHTML = '<p>Lesson not found.</p>';
      return;
    }

    // Mark as visited/completed
    state.progress[lesson.id] = true;
    saveState();

    // Find prev and next links
    let prevLink = '';
    let nextLink = '';

    if (currentIndex > 0) {
      const prevL = currentModule.lessons[currentIndex - 1];
      prevLink = `<a class="btn ghost sm" href="#/lesson/${prevL.id}">← Previous</a>`;
    } else {
      // Find previous module
      const modIdx = MODULES.findIndex(m => m.id === currentModule.id);
      if (modIdx > 0) {
        const prevM = MODULES[modIdx - 1];
        const lastL = prevM.lessons[prevM.lessons.length - 1];
        prevLink = `<a class="btn ghost sm" href="#/lesson/${lastL.id}">← Previous Chapter</a>`;
      } else {
        prevLink = `<a class="btn ghost sm" href="#/home">← Home</a>`;
      }
    }

    if (currentIndex < currentModule.lessons.length - 1) {
      const nextL = currentModule.lessons[currentIndex + 1];
      nextLink = `<a class="btn sm" href="#/lesson/${nextL.id}">Next Lesson →</a>`;
    } else {
      nextLink = `<a class="btn sm" href="#/quiz/${currentModule.id}">Chapter Quiz →</a>`;
    }

    let checkHtml = '';
    if (lesson.check) {
      const chk = lesson.check;
      checkHtml = `
        <div class="practice" id="checkBlock">
          <h4>Knowledge Check</h4>
          <p><strong>${esc(chk.q)}</strong></p>
          <div style="display:flex;flex-direction:column;gap:6px">
      `;
      chk.opts.forEach((opt, idx) => {
        checkHtml = checkHtml + `
          <label class="opt">
            <input type="radio" name="chk_${lesson.id}" value="${idx}">
            <span>${esc(opt)}</span>
          </label>
        `;
      });
      checkHtml = checkHtml + `
          </div>
          <button class="btn sm" style="margin-top:12px" data-action="check" data-id="${lesson.id}">Submit Answer</button>
          <div class="fb" id="fb_${lesson.id}" style="display:none"></div>
        </div>
      `;
    }

    container.innerHTML = `
      <div class="crumb">${esc(currentModule.chapter)} •${esc(currentModule.title)}</div>
      <h1>${esc(lesson.title)}</h1>
      <div class="meta">Estimated reading time: ${lesson.mins} mins</div>
      <div class="lesson-body">${lesson.body}</div>${checkHtml}
      <div class="lesson-nav">
        ${prevLink}${nextLink}
      </div>
    `;

    // Bind check button
    const checkBtn = $(`[data-action="check"][data-id="${lesson.id}"]`, container);
    if (checkBtn) {
      checkBtn.addEventListener('click', () => {
        const selected = $(`input[name="chk_${lesson.id}"]:checked`, container); const fb = $(`#fb_${lesson.id}`, container);
        if (!selected) {
          showToast('Please select an option first.', 'bad');
          return;
        }
        const val = parseInt(selected.value, 10);
        const correctVal = lesson.check.a;
        fb.style.display = 'block';
        if (val === correctVal) {
          fb.className = 'fb ok';
          fb.innerHTML = `<strong>Correct!</strong> ${esc(lesson.check.why)}`; showToast('Correct answer!', 'ok'); } else { fb.className = 'fb bad'; fb.innerHTML = `<strong>Incorrect.</strong> ${esc(lesson.check.why)}`;
          showToast('Incorrect. Try reviewing the lesson text.', 'bad');
        }
      });
    }
  }

  function renderQuiz(modId, container) {
    const mod = MODULES.find(m => m.id === modId);
    if (!mod) {
      container.innerHTML = '<p>Quiz not found.</p>';
      return;
    }

    const qz = mod.quiz;
    const isExam = qz.exam;
    let questionsHtml = '';

    qz.questions.forEach((q, qIdx) => {
      questionsHtml = questionsHtml + `
        <fieldset class="q-block" data-qidx="${qIdx}">
          <div class="qn">Question ${qIdx + 1} of${qz.questions.length}</div>
          <legend>${esc(q.q)}</legend>
          <div style="display:flex;flex-direction:column;gap:6px">
      `;
      q.opts.forEach((opt, oIdx) => {
        questionsHtml = questionsHtml + `
          <label class="opt">
            <input type="radio" name="q_${modId}_${qIdx}" value="${oIdx}">
            <span>${esc(opt)}</span>
          </label>
        `;
      });
      questionsHtml = questionsHtml + `
          </div>
          <div class="why muted" style="display:none"></div>
        </fieldset>
      `;
    });

    container.innerHTML = `
      <div class="crumb">${esc(mod.chapter)} • Assessment</div>
      <h1>${esc(qz.title)}</h1>
      <p class="lead">${isExam ? 'Answer all questions to complete your final certification exam. You need 80% or higher to pass.' : 'Complete this quick quiz to verify your understanding of the chapter.'}</p>
      
      <form id="quizForm">
        ${questionsHtml}
        <button type="submit" class="btn" style="margin-top:16px">Submit ${isExam ? 'Final Exam' : 'Quiz'}</button>
      </form>
      <div id="quizResult" style="margin-top:20px"></div>
    `;

    $('#quizForm').addEventListener('submit', (e) => {
      e.preventDefault();
      let score = 0;
      let answeredAll = true;

      qz.questions.forEach((q, qIdx) => {
        const sel = $(`input[name="q_${modId}_${qIdx}"]:checked`, container);
        const block = $(`[data-qidx="${qIdx}"]`, container); const whyEl = $('.why', block);  if (!sel) { answeredAll = false; } else { const val = parseInt(sel.value, 10); whyEl.style.display = 'block'; if (val === q.a) { score++; block.className = 'q-block correct'; whyEl.innerHTML = `<strong>Correct.</strong> ${esc(q.why)}`;
          } else {
            block.className = 'q-block wrong';
            whyEl.innerHTML = `<strong>Incorrect.</strong> Correct answer: "${esc(q.opts[q.a])}". ${esc(q.why)}`;
          }
        }
      });

      if (!answeredAll) {
        showToast('Please answer all questions before submitting.', 'bad');
        return;
      }

      const pct = Math.round((score / qz.questions.length) * 100);
      
      if (isExam) {
        state.examScore = pct;
        saveState();
      } else {
        state.quizzes[mod.id] = pct;
        saveState();
      }

      const resDiv = $('#quizResult');
      resDiv.innerHTML = `
        <div class="callout ${pct >= 80 ? '' : 'warn'}">
          <h3>Your Score: ${score} / ${qz.questions.length} (${pct}%)</h3>
