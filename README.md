# MANUALES-DE-USO
Manuales de uso 
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Manuales de Uso</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;700;800&display=swap" rel="stylesheet">
<style>
:root {
  --bg: #FFF8F0;
  --bg-a: rgba(255,120,150,.22);
  --bg-b: rgba(110,90,255,.2);
  --bg-c: rgba(0,200,160,.18);
  --card: #fff;
  --ink: #1B1740;
  --muted: #625F85;
  --line: rgba(27,23,64,.1);
  --accent: #6C4BFF;
  --accent-ink: #fff;
  --field: #F3F0FF;
  --danger: #E5304F;
  --chip: #fff;
  --shadow: 0 2px 0 rgba(27,23,64,.06), 0 16px 34px -14px rgba(27,23,64,.28);
  --sans: "Plus Jakarta Sans", system-ui, -apple-system, sans-serif;
}
@media (prefers-color-scheme: dark) {
  :root {
    --bg: #141029;
    --card: #201A3F;
    --ink: #F6F3FF;
    --muted: #B1ADD6;
    --line: rgba(246,243,255,.12);
    --accent: #9A83FF;
    --field: #2B2552;
    --chip: #2B2552;
    --shadow: 0 2px 0 rgba(0,0,0,.2), 0 16px 34px -14px rgba(0,0,0,.6);
  }
}
*, *::before, *::after { box-sizing: border-box; }
body {
  margin: 0;
  color: var(--ink);
  font-family: var(--sans);
  min-height: 100vh;
  background: radial-gradient(circle at 8% 0%, var(--bg-a), transparent 40%),
              radial-gradient(circle at 95% 10%, var(--bg-b), transparent 42%),
              radial-gradient(circle at 50% 100%, var(--bg-c), transparent 45%),
              var(--bg);
  background-attachment: fixed;
}
.wrap { max-width: 1100px; margin: 0 auto; padding: 36px 20px 72px; }
.hero { display: flex; align-items: center; gap: 16px; margin-bottom: 24px; }
.hero .big { font-size: 52px; animation: wig 3s ease-in-out infinite; }
@keyframes wig { 0%,100%{transform:rotate(-6deg)} 50%{transform:rotate(6deg) translateY(-4px)} }
h1 { margin: 0; font-size: clamp(32px, 5vw, 48px); font-weight: 800; letter-spacing: -.03em; }
h1 span { background: linear-gradient(90deg, #6C4BFF, #FF4F8B, #FF9A3D); -webkit-background-clip: text; background-clip: text; color: transparent; }
.sub { margin: 6px 0 0; color: var(--muted); font-size: 1rem; }
.bar { display: flex; flex-wrap: wrap; gap: 10px; margin-bottom: 16px; }
.search { flex: 1 1 220px; }
input, textarea { font: inherit; color: var(--ink); background: var(--field); border: 2px solid transparent; border-radius: 14px; padding: 13px 16px; width: 100%; }
input:focus, textarea:focus { outline: none; border-color: var(--accent); }
textarea { resize: vertical; min-height: 80px; }
.btn { font: inherit; font-weight: 700; border: 0; border-radius: 14px; padding: 13px 20px; cursor: pointer; background: var(--chip); color: var(--ink); box-shadow: var(--shadow); }
.btn.primary { background: linear-gradient(135deg, #6C4BFF, #FF4F8B); color: #fff; }
.btn.on { background: var(--ink); color: var(--bg); }
.btn.danger { background: transparent; color: var(--danger); box-shadow: none; }
.chips { display: flex; flex-wrap: wrap; gap: 8px; margin-bottom: 24px; }
.chip { font: inherit; font-weight: 700; font-size: .88rem; border: 0; border-radius: 999px; padding: 8px 16px; cursor: pointer; background: var(--chip); color: var(--ink); box-shadow: var(--shadow); }
.chip[aria-pressed="true"] { background: var(--ink); color: var(--bg); }
.grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(260px, 1fr)); gap: 20px; }
.card { background: var(--card); border-radius: 24px; overflow: hidden; box-shadow: var(--shadow); display: flex; flex-direction: column; transition: transform .25s; }
.card:hover { transform: translateY(-5px); }
.cover { aspect-ratio: 4/3; display: grid; place-items: center; position: relative; background-size: cover; background-position: center; }
.cover .sticker { font-size: 54px; filter: drop-shadow(0 8px 12px rgba(0,0,0,0.15)); }
.badge { position: absolute; left: 12px; bottom: 12px; background: rgba(255,255,255,0.92); color: #1B1740; border-radius: 999px; font-weight: 800; font-size: .75rem; padding: 6px 12px; backdrop-filter: blur(4px); }
.info { padding: 18px 20px 20px; display: flex; flex-direction: column; gap: 8px; flex: 1; }
.info h2 { margin: 0; font-size: 1.15rem; font-weight: 800; }
.info p { margin: 0; color: var(--muted); font-size: .9rem; line-height: 1.45; display: -webkit-box; -webkit-line-clamp: 2; -webkit-box-orient: vertical; overflow: hidden; }
.tip { background: #FFF3B8; color: #4A3A00; border-radius: 12px; padding: 8px 12px; font-size: .84rem; font-weight: 600; margin-top: 4px; }
.act { margin-top: auto; padding-top: 12px; display: flex; gap: 8px; flex-wrap: wrap; }
.act a, .act button { font: inherit; font-weight: 700; font-size: .88rem; text-decoration: none; border: 0; border-radius: 12px; padding: 9px 14px; cursor: pointer; background: var(--ink); color: var(--bg); }
.act button { background: var(--field); color: var(--ink); }
.act a.off { opacity: .4; pointer-events: none; }
.empty { grid-column: 1/-1; text-align: center; padding: 56px 20px; border: 2px dashed var(--line); border-radius: 24px; color: var(--muted); }
.empty b { display: block; font-size: 48px; margin-bottom: 8px; }
.empty strong { display: block; color: var(--ink); font-size: 1.2rem; margin-bottom: 4px; }
dialog { border: 0; border-radius: 24px; padding: 0; width: min(520px, calc(100vw - 32px)); background: var(--card); color: var(--ink); box-shadow: 0 24px 60px rgba(0,0,0,.3); }
dialog::backdrop { background: rgba(15,10,40,.5); backdrop-filter: blur(2px); }
form { padding: 24px; display: flex; flex-direction: column; gap: 14px; }
form h3 { margin: 0 0 4px; font-size: 1.4rem; font-weight: 800; }
label, .lb { display: flex; flex-direction: column; gap: 6px; font-weight: 700; font-size: .86rem; }
.opts { display: flex; flex-wrap: wrap; gap: 6px; }
.opts input { position: absolute; opacity: 0; width: 0; height: 0; }
.opts label { cursor: pointer; flex-direction: row; }
.opts span { display: grid; place-items: center; min-width: 40px; height: 40px; border-radius: 12px; background: var(--field); font-size: 20px; border: 2px solid transparent; }
.opts .t { font-size: .82rem; padding: 0 12px; }
.opts input:checked + span { border-color: var(--ink); }
.pv { height: 90px; border-radius: 12px; background: var(--field) center/cover; display: none; }
.row { display: flex; gap: 10px; justify-content: flex-end; margin-top: 8px; }
.row .danger { margin-right: auto; }
</style>
</head>
<body>
<main class="wrap">
  <div class="hero">
    <span class="big" aria-hidden="true">📚</span>
    <div>
      <h1>Manuales <span>de uso</span></h1>
      <p class="sub">Organiza tus manuales en un solo sitio ✨</p>
    </div>
  </div>
  <div class="bar">
    <input class="search" id="q" type="search" placeholder="🔍 Buscar manual…" aria-label="Buscar manual">
    <button class="btn" id="edit" aria-pressed="false">✏️ Editar</button>
    <button class="btn primary" id="add">➕ Nuevo manual</button>
  </div>
  <div class="chips" id="chips"></div>
  <section class="grid" id="grid"></section>
</main>

<dialog id="dlg">
  <form id="f" method="dialog">
    <h3 id="ft">Nuevo manual</h3>
    <label>Título<input id="t" required maxlength="80" placeholder="Ej. Cómo usar la impresora"></label>
    <div><div class="lb">Categoría</div><div class="opts" id="ct"></div></div>
    <label>Descripción<textarea id="d" maxlength="240" placeholder="¿De qué trata este manual?"></textarea></label>
    <label>💡 Consejo rápido<input id="tp" maxlength="120" placeholder="Un truco para recordar"></label>
    <label>Enlace al manual (Drive, Web, PDF)<input id="u" inputmode="url" placeholder="https://…"></label>
    <div>
      <div class="lb">Imagen de portada (opcional)</div>
      <div class="pv" id="pv"></div>
      <input id="im" type="file" accept="image/*">
      <button type="button" class="btn danger" id="rmimg" hidden>Quitar imagen</button>
    </div>
    <div><div class="lb">Emoji</div><div class="opts" id="ic"></div></div>
    <div><div class="lb">Color de portada</div><div class="opts" id="co"></div></div>
    <div class="row">
      <button type="button" class="btn danger" id="del" hidden>Eliminar</button>
      <button type="button" class="btn" id="cancel">Cancelar</button>
      <button type="submit" class="btn primary">Guardar</button>
    </div>
  </form>
</dialog>

<script>
var ICONS = ["📘","📱","🛠️","🧾","📦","⚙️","🎁","🛒","💳","🧹","🔐","⏰"];
var COLORS = [
  "linear-gradient(135deg,#6C4BFF,#B39BFF)",
  "linear-gradient(135deg,#FF4F6D,#FFA05A)",
  "linear-gradient(135deg,#00B894,#8CF0C4)",
  "linear-gradient(135deg,#0A84FF,#6FE0FF)",
  "linear-gradient(135deg,#FFB000,#FFE35C)",
  "linear-gradient(135deg,#E83FFB,#FF92D8)"
];
var CATS = ["🚀 Primeros pasos", "🛒 Caja y ventas", "📦 Productos", "👥 Equipo", "✨ Otros"];

var $ = function(id) { return document.getElementById(id); };
var items = [], editing = false, cur = null, img = "", filt = -1, LS = "manuales_v1";

// Cargar manuales iniciales si está vacío
var INITIAL_DATA = [
  { id: "m1", ts: 1, title: "Manual de Bienvenida", desc: "Guía rápida para empezar.", tip: "Revisa la sección de equipo", url: "https://google.com", icon: 0, color: 0, cat: 0 },
  { id: "m2", ts: 2, title: "Uso del Terminal POS", desc: "Cómo cobrar y emitir tickets.", tip: "Guarda copia de todo", url: "", icon: 3, color: 1, cat: 1 }
];

function mkOptions(box, name, list, fn) {
  box.textContent = "";
  list.forEach(function(v, i) {
    var l = document.createElement("label");
    l.innerHTML = '<input type="radio" name="' + name + '" value="' + i + '"><span></span>';
    fn(l.querySelector("span"), v);
    box.appendChild(l);
  });
}

mkOptions($("ic"), "emoji", ICONS, function(s, v) { s.textContent = v; });
mkOptions($("co"), "color", COLORS, function(s, v) { s.style.background = v; s.style.width = "40px"; });
mkOptions($("ct"), "cat", CATS, function(s, v) { s.className = "t"; s.textContent = v; });

function renderChips() {
  var b = $("chips"); b.textContent = "";
  ["✨ Todos"].concat(CATS).forEach(function(n, i) {
    var c = document.createElement("button");
    c.className = "chip"; c.textContent = n;
    c.setAttribute("aria-pressed", String(filt === i - 1));
    c.onclick = function() { filt = i - 1; renderChips(); render(); };
    b.appendChild(c);
  });
}

function safeUrl(u) {
  u = (u || "").trim();
  if (!u) return "";
  if (!/^https?:\/\//i.test(u)) u = "https://" + u;
  return u;
}

function render() {
  var g = $("grid"), q = $("q").value.trim().toLowerCase();
  g.textContent = "";
  
  var list = items.filter(function(m) {
    return (filt < 0 || m.cat === filt) && (!q || ((m.title || "") + " " + (m.desc || "")).toLowerCase().indexOf(q) > -1);
  });

  if (!list.length) {
    var e = document.createElement("div"); e.className = "empty";
    e.innerHTML = '<b>' + (items.length ? "🕵️" : "📭") + '</b><strong>' + 
      (items.length ? "Sin resultados" : "No hay manuales") + '</strong><span>' + 
      (items.length ? "Prueba con otra búsqueda." : "Pulsa «Nuevo manual» para añadir el primero.") + '</span>';
    g.appendChild(e);
    return;
  }

  list.forEach(function(m) {
    var c = document.createElement("article"); c.className = "card";
    var ic = ICONS[m.icon] || ICONS[0], url = safeUrl(m.url);
    
    c.innerHTML = '<div class="cover"><span class="sticker"></span><div class="badge" hidden></div></div>' +
                  '<div class="info"><h2></h2><p></p><div class="tip" hidden></div><div class="act"></div></div>';
    
    var cv = c.querySelector(".cover");
    cv.style.background = COLORS[m.color] || COLORS[0];
    cv.querySelector(".sticker").textContent = ic;
    
    if (m.img) {
      cv.style.backgroundImage = "url(" + m.img + ")";
      cv.querySelector(".sticker").style.display = "none";
    }

    if (CATS[m.cat]) {
      var bd = c.querySelector(".badge");
      bd.hidden = false; bd.textContent = CATS[m.cat];
    }

    c.querySelector("h2").textContent = m.title || "Sin título";
    var p = c.querySelector("p");
    if (m.desc) p.textContent = m.desc; else p.hidden = true;
    
    if (m.tip) {
      var t = c.querySelector(".tip");
      t.hidden = false; t.textContent = "💡 " + m.tip;
    }

    var act = c.querySelector(".act"), a = document.createElement("a");
    a.textContent = "📖 Abrir manual";
    if (url) { a.href = url; a.target = "_blank"; a.rel = "noopener"; } 
    else { a.className = "off"; }
    act.appendChild(a);

    if (editing) {
      var b = document.createElement("button");
      b.textContent = "✏️ Editar";
      b.onclick = function() { openDlg(m); };
      act.appendChild(b);
    }

    g.appendChild(c);
  });
}

function setPv() {
  var p = $("pv");
  p.style.display = img ? "block" : "none";
  p.style.backgroundImage = img ? "url(" + img + ")" : "none";
  $("rmimg").hidden = !img;
}

function openDlg(m) {
  cur = m || null;
  $("ft").textContent = m ? "Editar manual" : "Nuevo manual";
  $("t").value = m ? m.title || "" : "";
  $("d").value = m ? m.desc || "" : "";
  $("u").value = m ? m.url || "" : "";
  $("tp").value = m ? m.tip || "" : "";
  $("im").value = "";
  img = m ? m.img || "" : "";
  setPv();

  var i = m && ICONS[m.icon] ? m.icon : 0;
  var c = m && COLORS[m.color] ? m.color : 0;
  var k = m && CATS[m.cat] ? m.cat : 0;

  document.querySelector('input[name="emoji"][value="' + i + '"]').checked = true;
  document.querySelector('input[name="color"][value="' + c + '"]').checked = true;
  document.querySelector('input[name="cat"][value="' + k + '"]').checked = true;

  var d = $("del");
  d.hidden = !m;
  d.textContent = "Eliminar";
  delete d.dataset.sure;
  $("dlg").showModal();
  $("t").focus();
}

$("im").onchange = function() {
  var f = this.files[0]; if (!f) return;
  var r = new FileReader();
  r.onload = function() {
    var im = new Image();
    im.onload = function() {
      var w = Math.min(480, im.width), h = Math.round(im.height * w / im.width);
      var cv = document.createElement("canvas");
      cv.width = w; cv.height = h;
      cv.getContext("2d").drawImage(im, 0, 0, w, h);
      img = cv.toDataURL("image/jpeg", 0.7);
      setPv();
    };
    im.src = r.result;
  };
  r.readAsDataURL(f);
};

$("rmimg").onclick = function() { img = ""; $("im").value = ""; setPv(); };

function persist() {
  try { localStorage.setItem(LS, JSON.stringify(items)); } catch(e) {}
}

$("f").onsubmit = function(e) {
  e.preventDefault();
  var getVal = function(n) { return +document.querySelector('input[name="' + n + '"]:checked').value; };
  var item = {
    id: cur ? cur.id : "m_" + Date.now(),
    ts: cur ? cur.ts : Date.now(),
    title: $("t").value.trim(),
    desc: $("d").value.trim(),
    tip: $("tp").value.trim(),
    url: $("u").value.trim(),
    img: img,
    icon: getVal("emoji"),
    color: getVal("color"),
    cat: getVal("cat")
  };

  var idx = items.findIndex(function(x) { return x.id === item.id; });
  if (idx > -1) items[idx] = item; else items.unshift(item);

  persist();
  render();
  $("dlg").close();
};

$("cancel").onclick = function() { $("dlg").close(); };

$("del").onclick = function() {
  if (this.dataset.sure) {
    items = items.filter(function(x) { return x.id !== cur.id; });
    persist(); render(); $("dlg").close();
  } else {
    this.dataset.sure = "1";
    this.textContent = "Confirmar eliminación";
  }
};

$("add").onclick = function() { openDlg(null); };

$("edit").onclick = function() {
  editing = !editing;
  this.classList.toggle("on", editing);
  this.textContent = editing ? "✅ Listo" : "✏️ Editar";
  render();
};

$("q").oninput = render;

// Inicialización
try {
  var stored = localStorage.getItem(LS);
  items = stored ? JSON.parse(stored) : INITIAL_DATA;
} catch(e) {
  items = INITIAL_DATA;
}

renderChips();
render();
</script>
</body>
</html>