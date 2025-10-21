<!doctype html>
<html lang="kk">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Сенің Дүкенің — Киім</title>
  <meta name="description" content="Қазақша киім дүкені — жаңа коллекциялар, жеңілдіктер." />
  <style>
    /* ---------- БАЗАЛЫҚ СТИЛЬ ---------- */
    :root{
      --accent:#2b6cb0;
      --muted:#666;
      --bg:#f7f7fb;
      --card:#ffffff;
      --radius:12px;
      font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }
    *{box-sizing:border-box}
    body{margin:0;background:var(--bg);color:#111;line-height:1.4}
    header{
      background:linear-gradient(90deg,var(--accent),#4aa3d8);
      color:white;padding:18px 20px;display:flex;align-items:center;justify-content:space-between;gap:16px;
    }
    .brand{display:flex;align-items:center;gap:12px;font-weight:700}
    .brand svg{width:38px;height:38px}
    nav{display:flex;gap:14px;align-items:center}
    nav a{color:rgba(255,255,255,0.95);text-decoration:none;font-weight:600}
    .search{display:flex;align-items:center;gap:8px;background:rgba(255,255,255,0.12);padding:8px;border-radius:999px}
    .search input{border:none;background:transparent;color:white;outline:none;width:180px}
    .container{max-width:1100px;margin:22px auto;padding:0 18px}
    .hero{display:grid;grid-template-columns:1fr 380px;gap:18px;align-items:center}
    .hero .panel{background:var(--card);padding:20px;border-radius:var(--radius);box-shadow:0 6px 18px rgba(30,30,40,0.06)}
    .hero h1{margin:0 0 8px;font-size:28px}
    .products{display:grid;grid-template-columns:repeat(auto-fill,minmax(220px,1fr));gap:16px;margin-top:18px}
    .card{background:var(--card);border-radius:14px;padding:12px;box-shadow:0 4px 14px rgba(20,20,30,0.04);display:flex;flex-direction:column}
    .card img{width:100%;height:260px;object-fit:cover;border-radius:10px}
    .card h3{margin:10px 0 6px;font-size:16px}
    .price{font-weight:700}
    .muted{color:var(--muted);font-size:13px}
    .btn{background:var(--accent);color:white;border:none;padding:10px 12px;border-radius:10px;cursor:pointer;font-weight:600}
    .btn.secondary{background:transparent;color:var(--accent);border:1px solid rgba(43,108,176,0.12)}
    .cart-toggle{position:relative}
    .cart-count{position:absolute;top:-6px;right:-10px;background:#ff4d4f;color:white;border-radius:999px;padding:4px 7px;font-size:12px}
    footer{padding:28px 18px;text-align:center;color:var(--muted);font-size:14px;margin-top:28px}
    /* Modal */
    .modal-backdrop{position:fixed;inset:0;background:rgba(0,0,0,0.45);display:none;align-items:center;justify-content:center;padding:20px;z-index:60}
    .modal{background:white;border-radius:12px;max-width:760px;width:100%;padding:18px;box-shadow:0 18px 40px rgba(20,20,30,0.25)}
    .modal .row{display:flex;gap:12px}
    .product-meta{flex:1}
    /* cart */
    .cart-panel{width:340px;background:var(--card);border-radius:12px;padding:14px;box-shadow:0 10px 30px rgba(10,10,20,0.08)}
    .cart-item{display:flex;gap:10px;align-items:center;padding:8px 0;border-bottom:1px dashed #eee}
    .cart-item img{width:64px;height:64px;object-fit:cover;border-radius:8px}
    .cart-footer{margin-top:12px;display:flex;justify-content:space-between;align-items:center}
    /* responsive */
    @media (max-width:880px){
      .hero{grid-template-columns:1fr;gap:12px}
      .hero .panel{order:2}
      .card img{height:200px}
    }
    @media (max-width:520px){
      nav{display:none}
      .search input{width:90px}
      .card img{height:160px}
    }
  </style>
</head>
<body>
  <header>
    <div class="brand">
      <!-- simple logo -->
      <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><rect width="24" height="24" rx="6" fill="white" opacity="0.1"/><path d="M6 17c0-3 3-6 6-6s6 3 6 6" stroke="white" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
      <div>
        <div>Сенің Дүкенің</div>
        <div style="font-size:12px;color:rgba(255,255,255,0.9)">Әдемі киім — қазақша</div>
      </div>
    </div>

    <nav aria-label="Басты меню">
      <a href="#news">Жаңа</a>
      <a href="#women">Әйелдер</a>
      <a href="#men">Ерлер</a>
      <a href="#sale">Жеңілдіктер</a>
    </nav>

    <div style="display:flex;align-items:center;gap:12px">
      <div class="search" role="search" aria-label="Іздеу">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" style="opacity:0.9"><path d="M21 21l-4.35-4.35" stroke="white" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/><circle cx="11" cy="11" r="6" stroke="white" stroke-width="1.5" /></svg>
        <input id="search" placeholder="Іздеу: көйлек, джинс..." />
      </div>

      <button class="btn cart-toggle" id="openCart" aria-label="Себет">
        Себет
        <span class="cart-count" id="cartCount">0</span>
      </button>
    </div>
  </header>

  <main class="container">
    <section class="hero">
      <div class="panel">
        <h1>Жаңа коллекция — Қараша 2025</h1>
        <p class="muted">Үлкен таңдау: көйлектер, костюмдар, сырт киім. Жеткізу Қазақстан бойынша.</p>
        <div style="margin-top:12px;display:flex;gap:10px">
          <button class="btn" onclick="filterCategory('women')">Әйелдер</button>
          <button class="btn secondary" onclick="filterCategory('men')">Ерлер</button>
        </div>
      </div>

      <aside class="panel cart-panel" style="display:flex;flex-direction:column;gap:10px;">
        <h3>Жылдам қарау</h3>
        <div class="muted">Сауда шарттары: қайтару 14 күн ішінде. Төлем — карточка, қолма-қол.</div>
        <div style="margin-top:auto;display:flex;gap:8px">
          <button class="btn" onclick="openCartPanel()">Себетті ашу</button>
          <button class="btn secondary" onclick="checkout()">Тексеру</button>
        </div>
      </aside>
    </section>

    <section style="margin-top:18px">
      <h2 id="productsTitle">Тауарлар</h2>
      <div style="margin-top:8px">
        <label class="muted">Сұрыптау:</label>
        <select id="sort" onchange="applySort(this.value)">
          <option value="default">Әдепкі</option>
          <option value="price-asc">Баға: арзаннан қымбатқа</option>
          <option value="price-desc">Баға: қымбаттан арзанға</option>
        </select>
      </div>

      <div class="products" id="productGrid" aria-live="polite"></div>
    </section>
  </main>

  <div class="modal-backdrop" id="modal">
    <div class="modal" role="dialog" aria-modal="true" aria-hidden="true">
      <div id="modalContent"></div>
      <div style="margin-top:12px;text-align:right">
        <button class="btn secondary" onclick="closeModal()">Жабу</button>
        <button class="btn" id="modalAddBtn">Себетке салу — 0 тг</button>
      </div>
    </div>
  </div>
 <div>
   
   <footer> Байланыс нөмірі: <a href="tel:+777789946613">+7 778 994 66 13</a></div>
  <footer>
    © <span id="year"></span> Сенің Дүк…
