<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Fernwick – Houseplants for real rooms</title>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,500;12..96,800&family=Instrument+Sans:wght@400;500;600&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#E8EEF0; --surface:#F6F9FA; --ink:#13232B; --muted:#4F636D; --line:#C3D0D6;
  --accent:#2447D6; --on-accent:#fff; --moss:#6F8F2E; --blush:#F0C4BB; --sun:#F2D06B;
  color-scheme:light;
  box-sizing:border-box; padding-top:env(safe-area-inset-top,0px); padding-bottom:env(safe-area-inset-bottom,0px);
}
@media (prefers-color-scheme:dark){
  :root:not([data-theme="light"]){
    --bg:#0F1A20; --surface:#17262E; --ink:#E6EEF1; --muted:#9DB0B9; --line:#2B404A;
    --accent:#7F98FF; --on-accent:#0F1A20; --moss:#A5C75A; --blush:#E8A99E; --sun:#E9C75E; color-scheme:dark;
  }
}
:root[data-theme="dark"]{
  --bg:#0F1A20; --surface:#17262E; --ink:#E6EEF1; --muted:#9DB0B9; --line:#2B404A;
  --accent:#7F98FF; --on-accent:#0F1A20; --moss:#A5C75A; --blush:#E8A99E; --sun:#E9C75E; color-scheme:dark;
}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--ink);font:400 1rem/1.55 "Instrument Sans",system-ui,-apple-system,"Segoe UI",sans-serif}
h1,h2,h3{font-family:"Bricolage Grotesque","Instrument Sans",system-ui,sans-serif;margin:0;line-height:1}
button{font:inherit;color:inherit;cursor:pointer}
:focus-visible{outline:3px solid var(--accent);outline-offset:2px}
.wrap{max-width:1120px;margin:0 auto;padding:0 20px}
header.top{position:sticky;top:env(safe-area-inset-top,0px);z-index:5;background:var(--bg);border-bottom:1px solid var(--line)}
header.top .wrap{display:flex;align-items:center;justify-content:space-between;height:60px}
.logo{font:800 1.4rem "Bricolage Grotesque",sans-serif;letter-spacing:-.02em}
.nav{display:flex;gap:10px;align-items:center}
.btn{border:1.5px solid var(--ink);background:transparent;border-radius:999px;padding:8px 16px;font-weight:600}
.btn.primary{background:var(--accent);border-color:var(--accent);color:var(--on-accent)}
.btn:hover{background:var(--ink);color:var(--bg)}
.btn.primary:hover{filter:brightness(1.1);background:var(--accent);color:var(--on-accent)}
.hero{padding:56px 0 40px;display:grid;gap:32px;grid-template-columns:1.2fr 1fr;align-items:center}
.hero h1{font-size:clamp(2.6rem,7.5vw,5.6rem);font-weight:800;letter-spacing:-.04em}
.hero p{font-size:1.15rem;color:var(--muted);max-width:44ch;margin:20px 0 28px}
.stage{background:var(--blush);border-radius:48% 52% 44% 56%/52% 46% 54% 48%;aspect-ratio:1;display:grid;place-items:center;padding:8%}
.filters{display:flex;gap:8px;flex-wrap:wrap;margin:8px 0 24px}
.chip{border:1.5px solid var(--line);background:var(--surface);border-radius:999px;padding:6px 14px;font-weight:500}
.chip[aria-pressed="true"]{background:var(--ink);color:var(--bg);border-color:var(--ink)}
.grid{display:grid;gap:20px;grid-template-columns:repeat(auto-fill,minmax(230px,1fr));padding-bottom:64px}
.card{background:var(--surface);border:1px solid var(--line);border-radius:20px;overflow:hidden;display:flex;flex-direction:column}
.card .art{aspect-ratio:1/.9;display:grid;place-items:center;padding:14px}
.card .body{padding:16px;display:flex;flex-direction:column;gap:6px;flex:1}
.card h3{font-size:1.3rem;font-weight:800}
.card .meta{color:var(--muted);font-size:.9rem}
.card .row{display:flex;align-items:center;justify-content:space-between;margin-top:auto;padding-top:12px}
.price{font-weight:600}
h2.section{font-size:clamp(1.8rem,4vw,2.6rem);font-weight:800;letter-spacing:-.03em;margin:24px 0 16px}
.care{background:var(--ink);color:var(--bg);padding:48px 0}
.care .tiles{display:grid;gap:16px;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));margin-top:20px}
.care .tile{border:1px solid color-mix(in srgb,var(--bg) 30%,transparent);border-radius:16px;padding:18px}
.care .tile p{margin:8px 0 0;opacity:.85}
footer{padding:28px 0;color:var(--muted);font-size:.9rem}
.scrim{position:fixed;inset:0;background:rgba(0,0,0,.45);z-index:10}
.drawer{position:fixed;top:0;right:0;bottom:0;width:min(420px,100%);background:var(--surface);z-index:11;display:flex;flex-direction:column;padding:calc(20px + env(safe-area-inset-top,0px)) 20px calc(20px + env(safe-area-inset-bottom,0px));border-left:1px solid var(--line)}
.drawer .items{flex:1;overflow:auto;display:flex;flex-direction:column;gap:12px;margin:16px 0}
.line{display:grid;grid-template-columns:56px 1fr auto;gap:12px;align-items:center}
.line .thumb{width:56px;height:56px;border-radius:12px;display:grid;place-items:center}
.qty{display:flex;align-items:center;gap:8px;margin-top:4px}
.qty button{width:28px;height:28px;border-radius:50%;border:1.5px solid var(--line);background:transparent;line-height:1}
.total{display:flex;justify-content:space-between;font-weight:600;font-size:1.15rem;border-top:1px solid var(--line);padding-top:14px;margin-bottom:12px}
.empty{color:var(--muted);padding:24px 0}
@media (max-width:760px){.hero{grid-template-columns:1fr}.stage{max-width:320px;margin:0 auto}}
@media (prefers-reduced-motion:no-preference){.sway{transform-origin:50% 100%;animation:sway 5s ease-in-out infinite alternate}}
@keyframes sway{from{transform:rotate(-2.5deg)}to{transform:rotate(2.5deg)}}
</style>
</head>
<body>
<div id="root"></div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/react/18.3.1/umd/react.production.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/react-dom/18.3.1/umd/react-dom.production.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/htm@3.1.1/dist/htm.umd.js"></script>
<script>
const { useState, useMemo, useEffect } = React;
const html = htm.bind(React.createElement);

const PRODUCTS = [
  { id: 1, name: "Monstera", kind: "leaf", light: "Bright, indirect", level: "Easy", price: 38, pot: "#2447D6", bg: "#F0C4BB" },
  { id: 2, name: "Snake plant", kind: "blade", light: "Low to bright", level: "Easy", price: 29, pot: "#F2D06B", bg: "#C9DCB0" },
  { id: 3, name: "Boston fern", kind: "fern", light: "Medium, humid", level: "Fussy", price: 32, pot: "#13232B", bg: "#F2D06B" },
  { id: 4, name: "Golden pothos", kind: "vine", light: "Low to medium", level: "Easy", price: 22, pot: "#F0C4BB", bg: "#B8CCF5" },
  { id: 5, name: "Fiddle-leaf fig", kind: "leaf", light: "Bright, indirect", level: "Fussy", price: 64, pot: "#6F8F2E", bg: "#F0C4BB" },
  { id: 6, name: "ZZ plant", kind: "blade", light: "Low", level: "Easy", price: 34, pot: "#2447D6", bg: "#F2D06B" },
  { id: 7, name: "Maidenhair fern", kind: "fern", light: "Medium, humid", level: "Fussy", price: 27, pot: "#F2D06B", bg: "#C9DCB0" },
  { id: 8, name: "Trailing philodendron", kind: "vine", light: "Low to medium", level: "Easy", price: 24, pot: "#13232B", bg: "#B8CCF5" }
];
const FILTERS = ["All", "Easy", "Fussy", "Low light"];

function Plant({ kind, pot, size = 160, sway = false }) {
  const g = "#3F6B2A", g2 = "#6F8F2E";
  let leaves;
  if (kind === "leaf") leaves = html`<g><path d="M80 90 C40 80 30 40 55 20 C80 35 85 65 80 90Z" fill=${g}/><path d="M80 90 C120 80 135 45 110 22 C85 38 78 65 80 90Z" fill=${g2}/><path d="M80 92 C70 60 78 30 80 8 C95 30 92 65 80 92Z" fill=${g}/></g>`;
  else if (kind === "blade") leaves = html`<g><path d="M70 100 L62 20 L82 100Z" fill=${g}/><path d="M80 100 L88 8 L96 100Z" fill=${g2}/><path d="M90 100 L112 30 L106 100Z" fill=${g}/></g>`;
  else if (kind === "fern") leaves = html`<g fill="none" stroke=${g} strokeWidth="5" strokeLinecap="round"><path d="M80 100 C40 80 30 50 28 30"/><path d="M80 100 C70 70 72 40 80 14"/><path d="M80 100 C120 80 130 50 132 30"/><path d="M80 100 C55 85 50 60 48 44" stroke=${g2}/><path d="M80 100 C105 85 110 60 112 44" stroke=${g2}/></g>`;
  else leaves = html`<g><path d="M80 100 C60 60 40 70 30 110" fill="none" stroke=${g} strokeWidth="4"/><path d="M80 100 C100 50 125 60 130 115" fill="none" stroke=${g2} strokeWidth="4"/><ellipse cx="45" cy="78" rx="12" ry="8" fill=${g}/><ellipse cx="32" cy="104" rx="11" ry="7" fill=${g2}/><ellipse cx="108" cy="68" rx="12" ry="8" fill=${g2}/><ellipse cx="125" cy="98" rx="11" ry="7" fill=${g}/><ellipse cx="80" cy="84" rx="12" ry="8" fill=${g}/></g>`;
  return html`<svg viewBox="0 0 160 160" width=${size} height=${size} role="img" aria-label=${kind + " plant in a pot"}>
    <g className=${sway ? "sway" : ""}>${leaves}</g>
    <path d="M48 100 H112 L104 150 H56Z" fill=${pot}/>
    <rect x="44" y="94" width="72" height="12" rx="4" fill=${pot} opacity=".85"/>
  </svg>`;
}

function Cart({ cart, onClose, onChange }) {
  const lines = PRODUCTS.filter(p => cart[p.id]);
  const total = lines.reduce((s, p) => s + p.price * cart[p.id], 0);
  const [done, setDone] = useState(false);
  useEffect(() => { const k = e => e.key === "Escape" && onClose(); window.addEventListener("keydown", k); return () => window.removeEventListener("keydown", k); }, []);
  return html`<div>
    <div className="scrim" onClick=${onClose}></div>
    <aside className="drawer" role="dialog" aria-label="Your cart">
      <div style=${{display:"flex",justifyContent:"space-between",alignItems:"center"}}>
        <h2 style=${{fontSize:"1.6rem"}}>Your cart</h2>
        <button className="btn" onClick=${onClose}>Close</button>
      </div>
      <div className="items">
        ${done ? html`<p className="empty">Order placed. Your plants ship within two days, and care cards are in the box.</p>`
          : lines.length === 0 ? html`<p className="empty">Your cart is empty. Add a plant from the shop to start.</p>`
          : lines.map(p => html`<div className="line" key=${p.id}>
              <div className="thumb" style=${{background:p.bg}}><${Plant} kind=${p.kind} pot=${p.pot} size=${46}/></div>
              <div><strong>${p.name}</strong>
                <div className="qty">
                  <button aria-label=${"Remove one " + p.name} onClick=${() => onChange(p.id, -1)}>−</button>
                  <span>${cart[p.id]}</span>
                  <button aria-label=${"Add one " + p.name} onClick=${() => onChange(p.id, 1)}>+</button>
                </div></div>
              <span className="price">$${p.price * cart[p.id]}</span>
            </div>`)}
      </div>
      ${!done && html`<div>
        <div className="total"><span>Total</span><span>$${total}</span></div>
        <button className="btn primary" style=${{width:"100%",padding:"12px"}} disabled=${!lines.length}
          onClick=${() => { setDone(true); lines.forEach(p => onChange(p.id, -cart[p.id])); }}>Place order</button>
      </div>`}
    </aside>
  </div>`;
}

function App() {
  const [filter, setFilter] = useState("All");
  const [cart, setCart] = useState({});
  const [open, setOpen] = useState(false);
  const [dark, setDark] = useState(null);

  const change = (id, d) => setCart(c => { const n = Math.max(0, (c[id] || 0) + d); const x = { ...c }; if (n) x[id] = n; else delete x[id]; return x; });
  const count = Object.values(cart).reduce((a, b) => a + b, 0);
  const shown = useMemo(() => PRODUCTS.filter(p =>
    filter === "All" ? true : filter === "Low light" ? p.light.startsWith("Low") : p.level === filter), [filter]);

  useEffect(() => { if (dark !== null) document.documentElement.setAttribute("data-theme", dark ? "dark" : "light"); }, [dark]);
  const isDark = dark === null ? window.matchMedia("(prefers-color-scheme: dark)").matches : dark;

  return html`<div>
    <header className="top"><div className="wrap">
      <span className="logo">Fernwick</span>
      <nav className="nav" aria-label="Main">
        <button className="btn" onClick=${() => setDark(!isDark)}>${isDark ? "Light mode" : "Dark mode"}</button>
        <button className="btn primary" onClick=${() => setOpen(true)}>Cart (${count})</button>
      </nav>
    </div></header>

    <main>
      <section className="wrap hero">
        <div>
          <h1>Plants that survive your actual apartment.</h1>
          <p>Every plant here is picked for a real window, a real schedule, and a person who forgets to water on Sundays.</p>
          <a href="#shop" className="btn primary" style=${{textDecoration:"none",display:"inline-block"}}>Shop plants</a>
        </div>
        <div className="stage"><${Plant} kind="leaf" pot="#2447D6" size=${300} sway=${true}/></div>
      </section>

      <section className="wrap" id="shop">
        <h2 className="section">Shop</h2>
        <div className="filters" role="group" aria-label="Filter plants">
          ${FILTERS.map(f => html`<button key=${f} className="chip" aria-pressed=${filter === f} onClick=${() => setFilter(f)}>${f}</button>`)}
        </div>
        <div className="grid">
          ${shown.map(p => html`<article className="card" key=${p.id}>
            <div className="art" style=${{background:p.bg}}><${Plant} kind=${p.kind} pot=${p.pot}/></div>
            <div className="body">
              <h3>${p.name}</h3>
              <span className="meta">${p.light} · ${p.level} to keep</span>
              <div className="row">
                <span className="price">$${p.price}</span>
                <button className="btn" onClick=${() => change(p.id, 1)}>${cart[p.id] ? "Add another" : "Add to cart"}</button>
              </div>
            </div>
          </article>`)}
        </div>
      </section>

      <section className="care"><div className="wrap">
        <h2 className="section" style=${{marginTop:0}}>Care that fits on a card</h2>
        <div className="tiles">
          <div className="tile"><h3>Water</h3><p>Check the top two inches of soil. If it’s dry, water until it drains.</p></div>
          <div className="tile"><h3>Light</h3><p>Most plants prefer a spot within a few feet of a window, out of harsh afternoon sun.</p></div>
          <div className="tile"><h3>Repot</h3><p>When roots poke out of the drainage holes, move up one pot size in spring.</p></div>
        </div>
      </div></section>
    </main>

    <footer><div className="wrap">Fernwick is a demo storefront built with React. No real orders are placed.</div></footer>
    ${open && html`<${Cart} cart=${cart} onClose=${() => setOpen(false)} onChange=${change}/>`}
  </div>`;
}

ReactDOM.createRoot(document.getElementById("root")).render(html`<${App}/>`);
</script>
</body>
</html>
