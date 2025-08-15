<!DOCTYPE html>
<html lang="az">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Portfolio – Ad Soyad</title>
  <meta name="description" content="Şəkil və videolar üçün yüngül, pulsuz portfolio saytı." />
  <style>
    :root{
      --bg:#0b0b0e; --card:#121218; --muted:#9aa0a6; --text:#e7e9ea; --accent:#7c5cff; --ring:#2a2a35;
    }
    *{box-sizing:border-box}
    html,body{margin:0;padding:0;background:var(--bg);color:var(--text);font:16px/1.6 system-ui,-apple-system,Segoe UI,Roboto,Inter,Arial}
    a{color:inherit;text-decoration:none}
    img{max-width:100%;display:block}
    .wrap{max-width:1100px;margin:0 auto;padding:24px}
    header{display:flex;gap:16px;align-items:center;justify-content:space-between;position:sticky;top:0;background:linear-gradient(180deg,rgba(11,11,14,.98),rgba(11,11,14,.8));backdrop-filter: blur(8px);padding:16px 24px;border-bottom:1px solid var(--ring);z-index:10}
    .brand{display:flex;align-items:center;gap:12px}
    .logo{width:44px;height:44px;border-radius:14px;background:conic-gradient(from 180deg,var(--accent),#37d0ff,#22d39c);box-shadow:0 0 0 4px #00000020}
    nav{display:flex;gap:16px;flex-wrap:wrap}
    nav a{padding:8px 12px;border-radius:10px;border:1px solid var(--ring)}
    nav a:hover, nav a.active{background:var(--card);border-color:#3a3a46}

    .hero{display:grid;grid-template-columns:1.2fr .8fr;gap:24px;align-items:center;margin-top:28px}
    .hero .card{background:var(--card);border:1px solid var(--ring);border-radius:20px;padding:24px}
    .title{font-size:clamp(28px,6vw,44px);line-height:1.2;margin:0 0 8px}
    .muted{color:var(--muted)}
    .btn{display:inline-flex;align-items:center;gap:10px;background:var(--accent);color:white;padding:12px 16px;border-radius:12px;border:0;cursor:pointer;font-weight:600}
    .btn.secondary{background:transparent;color:var(--text);border:1px solid var(--ring)}

    section{margin:40px 0}
    .section-title{font-size:24px;margin:0 0 16px}

    /* Gallery */
    .grid{display:grid;gap:14px}
    .grid.cols-3{grid-template-columns:repeat(3,1fr)}
    @media (max-width:900px){.hero{grid-template-columns:1fr}.grid.cols-3{grid-template-columns:repeat(2,1fr)}}
    @media (max-width:560px){.grid.cols-3{grid-template-columns:1fr}}
    .card.img{position:relative;overflow:hidden;background:#0f0f14;border-radius:18px;border:1px solid var(--ring)}
    .card.img img{width:100%;height:260px;object-fit:cover;transition:transform .35s ease}
    .card.img:hover img{transform:scale(1.03)}
    .tag{position:absolute;left:10px;top:10px;background:#00000080;padding:6px 10px;border-radius:999px;border:1px solid var(--ring);font-size:12px}
    .caption{padding:10px 12px;display:flex;justify-content:space-between;align-items:center;font-size:14px}

    /* Video list */
    .video-list{display:grid;grid-template-columns:repeat(2,1fr);gap:16px}
    @media (max-width:900px){.video-list{grid-template-columns:1fr}}
    .video{aspect-ratio:16/9;border:1px solid var(--ring);border-radius:16px;overflow:hidden;background:#0f0f14}
    iframe{width:100%;height:100%;border:0}

    /* About + Contact */
    .two{display:grid;grid-template-columns:1.2fr .8fr;gap:18px}
    @media (max-width:900px){.two{grid-template-columns:1fr}}
    .card{background:var(--card);border:1px solid var(--ring);border-radius:20px;padding:18px}
    .list{display:flex;flex-direction:column;gap:10px}

    /* Lightbox */
    dialog#lightbox{width:min(92vw,1100px);border:0;border-radius:16px;padding:0;overflow:hidden;background:#000}
    dialog::backdrop{background:rgba(0,0,0,.8)}
    .lb-toolbar{position:absolute;top:10px;right:10px;z-index:3;display:flex;gap:8px}
    .icon-btn{background:#0000007a;border:1px solid #ffffff22;color:#fff;padding:8px 10px;border-radius:10px;cursor:pointer}
    .lb-wrap{position:relative}
    .lb-img{width:100%;height:auto;max-height:88vh;display:block;margin:auto}
    .lb-cap{position:absolute;left:0;right:0;bottom:0;background:linear-gradient(180deg,transparent,rgba(0,0,0,.7));color:#fff;padding:16px;font-size:14px}

    footer{border-top:1px solid var(--ring);margin-top:44px;padding:18px;color:var(--muted);text-align:center}
  </style>
</head>
<body>
  <header class="wrap">
    <div class="brand">
      <div class="logo" aria-hidden="true"></div>
      <div>
        <strong>Ad Soyad</strong><br/>
        <span class="muted">3D Artist · Motion · Designer</span>
      </div>
    </div>
    <nav>
      <a href="#isler" class="active">İşlər</a>
      <a href="#videolar">Videolar</a>
      <a href="#haqqimda">Haqqımda</a>
      <a href="#elaqe">Əlaqə</a>
    </nav>
  </header>

  <main class="wrap">
    <section class="hero" id="isler">
      <div class="card">
        <h1 class="title">Salam! Mən <span style="color:var(--accent)">Ad Soyad</span> — 3D modelləşdirmə və motion dizayn işləri.</h1>
        <p class="muted">Aşağıda seçilmiş portfoliodan şəkillər və video işlər var. Daha çoxu üçün əlaqə saxla.</p>
        <div style="display:flex;gap:10px;margin-top:10px">
          <a class="btn" href="#elaqe">Əlaqə</a>
          <a class="btn secondary" href="#videolar">Showreel</a>
        </div>
      </div>
      <div class="card">
        <div class="list">
          <div><strong>Proqramlar:</strong> 3ds Max, Blender, After Effects, Premiere Pro</div>
          <div><strong>Sahələr:</strong> Produkt vizualizasiya, Motion, Reklam</div>
          <div><strong>Şəhər:</strong> Bakı, Azərbaycan</div>
          <div><strong>Status:</strong> Freelancer · İşbirliyinə açıq</div>
        </div>
      </div>
    </section>

    <!-- GALLERY -->
    <section>
      <h2 class="section-title">Seçilmiş işlər</h2>
      <div class="grid cols-3" id="gallery">
        <!-- Şəkilləri /img qovluğuna qoy və aşağıdakı src-ləri dəyiş. Alt yazıları "data-cap"-də yaz. -->
        <figure class="card img"><span class="tag">3D</span>
          <img loading="lazy" src="img/work-1.jpg" alt="İş 1" data-cap="Produkt vizualizasiya – 2025" />
          <figcaption class="caption"><span>İş 1</span><button class="icon-btn" data-open>Göstər</button></figcaption>
        </figure>
        <figure class="card img"><span class="tag">Render</span>
          <img loading="lazy" src="img/work-2.jpg" alt="İş 2" data-cap="Arxitektura render – 2025" />
          <figcaption class="caption"><span>İş 2</span><button class="icon-btn" data-open>Göstər</button></figcaption>
        </figure>
        <figure class="card img"><span class="tag">Motion</span>
          <img loading="lazy" src="img/work-3.jpg" alt="İş 3" data-cap="Animasiya kadrı – 2024" />
          <figcaption class="caption"><span>İş 3</span><button class="icon-btn" data-open>Göstər</button></figcaption>
        </figure>
        <!-- Daha çox kart əlavə edə bilərsən -->
      </div>
    </section>

    <!-- VIDEOS -->
    <section id="videolar">
      <h2 class="section-title">Videolar</h2>
      <div class="video-list">
        <!-- YouTube və ya Vimeo linkinin ID-sini qoy. Məs: https://youtu.be/VIDEO_ID -->
        <div class="video"><iframe src="https://www.youtube.com/embed/dQw4w9WgXcQ" title="Showreel" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen loading="lazy"></iframe></div>
        <div class="video"><iframe src="https://player.vimeo.com/video/76979871?h=fb4c5a7b6b" title="Case Study" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen loading="lazy"></iframe></div>
      </div>
    </section>

    <section id="haqqimda" class="two">
      <div class="card">
        <h2 class="section-title">Haqqımda</h2>
        <p>Qısa bio: Təxminən 5 ildir 3D və motion sahəsində işləyirəm. Məqsədim markalara məhsullarını daha yaxşı təqdim edən vizual həllər yaratmaqdır.</p>
        <p><strong>Mükafatlar / Nəticələr:</strong> 3 layihə ilə 1M+ baxış, 20+ müştəri, 50+ tamamlanmış iş.</p>
      </div>
      <div class="card" id="elaqe">
        <h2 class="section-title">Əlaqə</h2>
        <ul class="list">
          <li><strong>Email:</strong> <a href="mailto:sizinmail@domain.com">sizinmail@domain.com</a></li>
          <li><strong>Telefon/WhatsApp:</strong> <a href="tel:+994000000000">+994 00 000 00 00</a></li>
          <li><strong>Instagram:</strong> <a href="#">instagram.com/istifadəçi</a></li>
          <li><strong>Behance:</strong> <a href="#">behance.net/istifadəçi</a></li>
        </ul>
      </div>
    </section>

    <footer>
      © <span id="year"></span> Ad Soyad — Bütün hüquqlar qorunur.
    </footer>
  </main>

  <!-- Lightbox Modal -->
  <dialog id="lightbox">
    <div class="lb-toolbar">
      <button class="icon-btn" id="lbClose" aria-label="Bağla">✕</button>
      <a class="icon-btn" id="lbDownload" download>Yüklə</a>
    </div>
    <div class="lb-wrap">
      <img id="lbImg" class="lb-img" alt="Geniş şəkil" />
      <div class="lb-cap" id="lbCap"></div>
    </div>
  </dialog>

  <script>
    // İl
    document.getElementById('year').textContent = new Date().getFullYear()

    // Lightbox aç/bağla
    const dlg = document.getElementById('lightbox')
    const lbImg = document.getElementById('lbImg')
    const lbCap = document.getElementById('lbCap')
    const lbDownload = document.getElementById('lbDownload')
    const gallery = document.getElementById('gallery')

    gallery?.addEventListener('click', (e)=>{
      const btn = e.target.closest('[data-open]')
      if(!btn) return
      const fig = btn.closest('figure')
      const img = fig.querySelector('img')
      lbImg.src = img.src
      lbImg.alt = img.alt
      lbCap.textContent = img.dataset.cap || img.alt
      lbDownload.href = img.src
      if(typeof dlg.showModal === 'function') dlg.showModal()
    })
    document.getElementById('lbClose')?.addEventListener('click', ()=> dlg.close())
    dlg?.addEventListener('click', (e)=>{ if(e.target === dlg) dlg.close() })

    // Klaviatura ilə bağlama
    document.addEventListener('keydown', (e)=>{ if(e.key==='Escape' && dlg.open) dlg.close() })
  </script>
</body>
</html>
