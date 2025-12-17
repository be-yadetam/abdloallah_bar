[Finish.html](https://github.com/user-attachments/files/24222024/Finish.html)
<!doctype html>
<html lang="fa" dir="rtl">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>یادبود سرباز شهید عبدالله برء</title>
  <meta name="theme-color" content="#070a12" />

  <!-- فونت جایگزین (اگر B Nazanin نصب نبود) -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Vazirmatn:wght@200;300;400;600;700;800&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg0:#050711;
      --bg1:#060a18;
      --panel: rgba(13, 18, 36, .78);
      --panel2: rgba(10, 14, 28, .92);
      --line: rgba(148,163,184,.24);
      --text:#e5e7eb;
      --muted:#9ca3af;
      --gold:#facc15;
      --radius: 22px;
      --shadow: 0 26px 90px rgba(0,0,0,.72);
    }

    /* ✅ فونت بی‌نازنین (اگر روی دستگاه نصب باشد) */
    @font-face{
      font-family:"B Nazanin";
      src: local("B Nazanin"), local("BNazanin");
      font-display: swap;
    }

    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family:"B Nazanin","BNazanin","Vazirmatn", system-ui, -apple-system, "Segoe UI", sans-serif;
      color:var(--text);
      background: radial-gradient(1200px 700px at 20% 0%, rgba(250,204,21,.08), transparent 60%),
                  radial-gradient(900px 520px at 100% 0%, rgba(34,197,94,.10), transparent 55%),
                  radial-gradient(900px 520px at 50% 120%, rgba(56,189,248,.09), transparent 60%),
                  linear-gradient(180deg, var(--bg1), var(--bg0));
      overflow-x:hidden;
    }

    /* ✅ بک‌گراند عکس شهید (با حفظ رنگ‌بندی قبلی) */
    .bgPhoto{
      position:fixed; inset:0;
      z-index:-6;
      background-size:cover;
      background-position:center;
      background-repeat:no-repeat;
      opacity:.14;
      filter: contrast(1.05) saturate(1.05);
      pointer-events:none;
    }
    .bgPhoto:after{
      content:"";
      position:absolute; inset:0;
      background:
        radial-gradient(1200px 700px at 20% 0%, rgba(250,204,21,.10), transparent 60%),
        radial-gradient(900px 520px at 100% 0%, rgba(34,197,94,.12), transparent 55%),
        radial-gradient(900px 520px at 50% 120%, rgba(56,189,248,.11), transparent 60%),
        linear-gradient(180deg, rgba(6,10,24,.35), rgba(5,7,17,.88));
    }

    canvas#stars{
      position:fixed; inset:0;
      z-index:-3;
      opacity:.55;
      pointer-events:none;
    }

    .glow{
      position:fixed; inset:-30%;
      z-index:-4; pointer-events:none;
      background:
        radial-gradient(circle at 10% 10%, rgba(250,204,21,.10), transparent 55%),
        radial-gradient(circle at 90% 15%, rgba(34,197,94,.12), transparent 58%),
        radial-gradient(circle at 50% 105%, rgba(56,189,248,.10), transparent 62%);
      filter: blur(22px);
      animation: float 24s ease-in-out infinite alternate;
      opacity:.75;
    }
    @keyframes float{
      0%{transform:translate3d(0,0,0)}
      50%{transform:translate3d(0,-18px,0)}
      100%{transform:translate3d(0,16px,0)}
    }

    @media (prefers-reduced-motion: reduce){
      .glow{animation:none}
      .shine{animation:none}
      .ring{animation:none}
    }

    .wrap{width:min(1040px, 92vw); margin: 22px auto 40px;}

    .shell{
      border-radius: calc(var(--radius) + 8px);
      background: linear-gradient(180deg, rgba(255,255,255,.03), rgba(255,255,255,.015));
      border: 1px solid rgba(255,255,255,.06);
      box-shadow: var(--shadow);
      overflow:hidden;
      position:relative;
    }
    .shell:before{
      content:"";
      position:absolute; inset:10px;
      border-radius: var(--radius);
      border: 1px solid rgba(250,204,21,.20);
      pointer-events:none;
    }

    header{
      display:flex;
      justify-content:space-between;
      gap:14px;
      align-items:center;
      padding: 16px 18px;
      background: rgba(5,8,20,.88);
      border-bottom: 1px solid var(--line);
      position:sticky; top:0; z-index:5;
      backdrop-filter: blur(10px);
    }
    .brand{display:flex; align-items:center; gap:12px; flex-wrap:wrap;}
    .mark{
      width:38px; height:38px; border-radius:999px;
      display:grid; place-items:center;
      border: 1px solid rgba(250,204,21,.60);
      background: radial-gradient(circle at 30% 20%, rgba(250,204,21,.22), transparent 65%);
      box-shadow: 0 0 18px rgba(250,204,21,.20);
      font-size:18px;
    }
    .brand h1{margin:0; font-size:15px; letter-spacing:.14em; text-indent:.14em; font-weight:700;}
    .brand p{margin:2px 0 0; font-size:11px; color:var(--muted);}
    .basmala{font-size:11px; color:#fef9c3; letter-spacing:.12em; text-align:left; white-space:nowrap;}
    .basmala b{color:var(--gold); font-weight:700}

    @media (max-width:720px){
      header{flex-direction:column; align-items:flex-start}
      .basmala{white-space:normal; line-height:1.8}
    }

    .hero{
      padding: 18px 18px 8px;
      background:
        radial-gradient(900px 420px at 50% 0%, rgba(250,204,21,.06), transparent 60%),
        radial-gradient(720px 360px at 10% 80%, rgba(34,197,94,.08), transparent 58%),
        radial-gradient(720px 360px at 90% 85%, rgba(56,189,248,.07), transparent 58%);
      border-bottom: 1px solid var(--line);
    }

    /* ✅ عکس بالا کوچکتر + متن زیرش */
    .heroGrid{
      display:grid;
      grid-template-columns: 1fr;
      gap:14px;
      align-items:start;
    }
    .portraitCard{
      width:min(260px, 86vw);
      margin: 0 auto;
      background: linear-gradient(135deg, rgba(250,204,21,.10), rgba(255,255,255,.02));
      border:1px solid rgba(255,255,255,.08);
      border-radius: 28px;
      padding:10px;
      position:relative;
      overflow:hidden;
      box-shadow: 0 20px 60px rgba(0,0,0,.55);
    }
    .portrait{
      aspect-ratio: 3/4;
      border-radius: 22px;
      overflow:hidden;
      background:#040712;
      border:1px solid rgba(148,163,184,.18);
      position:relative;
    }
    .portrait iframe{width:100%; height:100%; border:0; display:block; filter: contrast(1.05) saturate(1.03);}
    .portrait:after{
      content:"";
      position:absolute; inset:0;
      pointer-events:none;
      box-shadow: inset 0 0 34px rgba(0,0,0,.72);
    }
    .ring{
      position:absolute; inset:-40%;
      background: conic-gradient(from 220deg, rgba(250,204,21,.85), rgba(34,197,94,.55), rgba(56,189,248,.55), rgba(250,204,21,.85));
      filter: blur(20px);
      opacity:.40;
      animation: spin 26s linear infinite;
      z-index:0;
    }
    @keyframes spin{to{transform:rotate(360deg)}}
    .shine{
      position:absolute; inset:-60% -40%;
      background: linear-gradient(120deg, transparent 35%, rgba(255,255,255,.10), transparent 70%);
      transform: rotate(18deg);
      animation: sweep 7.5s ease-in-out infinite;
      pointer-events:none;
      z-index:1;
    }
    @keyframes sweep{
      0%{transform:translateX(-18%) rotate(18deg); opacity:.0}
      35%{opacity:.55}
      70%{opacity:.18}
      100%{transform:translateX(18%) rotate(18deg); opacity:0}
    }

    .heroText{padding: 0 2px;}
    .name{font-size:26px; font-weight:800; margin:0 0 6px; letter-spacing:.20em; text-indent:.20em;}
    .role{margin:0 0 10px; font-size:13px; color:var(--muted);}

    .metaRow{display:flex; flex-wrap:wrap; gap:8px; margin: 10px 0 10px;}
    .chip{
      font-size:11px;
      padding:6px 10px;
      border-radius:999px;
      background: rgba(5,8,20,.72);
      border: 1px solid rgba(148,163,184,.22);
      color: var(--muted);
    }
    .chip b{color:var(--text); font-weight:600}

    .quote{
      margin:0;
      padding: 12px 12px;
      border-radius: 18px;
      background: linear-gradient(135deg, rgba(250,204,21,.09), rgba(255,255,255,.02));
      border: 1px solid rgba(250,204,21,.22);
      line-height:2;
      font-size:13px;
    }
    .quote em{color:#fff7d1; font-style:normal; font-weight:700;}
    .dates{margin:10px 0 0; font-size:13px; color:var(--text);}
    .dates span{color:var(--gold); font-weight:700}

    .actions{display:flex; flex-wrap:wrap; gap:10px; margin-top: 12px;}
    .btn{
      display:inline-flex; align-items:center; gap:8px;
      padding:9px 12px;
      border-radius: 999px;
      border: 1px solid rgba(148,163,184,.24);
      background: rgba(5,8,20,.68);
      color: var(--text);
      text-decoration:none;
      cursor:pointer;
      transition: transform .15s ease, border-color .15s ease, background .15s ease;
      font-size:12px;
    }
    .btn:hover{
      transform: translateY(-1px);
      border-color: rgba(250,204,21,.40);
      background: rgba(250,204,21,.08);
    }
    .btn.primary{border-color: rgba(250,204,21,.55); background: rgba(250,204,21,.10);}

    .countdown{
      margin: 12px 18px 14px;
      padding: 12px 14px;
      border-radius: 18px;
      background: var(--panel);
      border: 1px solid rgba(250,204,21,.40);
      display:flex;
      justify-content:space-between;
      align-items:center;
      gap:10px;
      box-shadow: 0 12px 30px rgba(0,0,0,.45);
    }
    .countdown small{color:var(--muted); font-size:11px}
    .countVal{font-weight:800; color: var(--gold); font-size:14px; white-space:nowrap;}
    @media (max-width:650px){ .countdown{flex-direction:column; align-items:flex-start} }

    main{padding: 0 18px 18px}
    @media (max-width:720px){ main{padding: 0 12px 16px} }

    details.section{
      margin-top: 10px;
      border-radius: 18px;
      background: linear-gradient(135deg, var(--panel), var(--panel2));
      border: 1px solid var(--line);
      box-shadow: 0 18px 50px rgba(0,0,0,.52);
      overflow:hidden;
    }
    details.section[open]{
      border-color: rgba(250,204,21,.45);
      box-shadow: 0 22px 70px rgba(0,0,0,.65);
    }
    summary{
      list-style:none;
      cursor:pointer;
      padding: 12px 12px;
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:10px;
      user-select:none;
    }
    summary::-webkit-details-marker{display:none}

    .sumLeft{display:flex; align-items:center; gap:10px;}
    .ico{
      width:34px; height:34px;
      border-radius:999px;
      display:grid; place-items:center;
      border:1px solid rgba(250,204,21,.55);
      background: radial-gradient(circle at 30% 20%, rgba(250,204,21,.18), transparent 65%);
      font-size:16px;
    }
    .sumTitle{display:flex; flex-direction:column; gap:3px;}
    .sumTitle b{font-size:13px;}
    .sumTitle span{font-size:11px; color:var(--muted);}
    .chev{color: var(--muted); transition: transform .18s ease, color .18s ease; font-size:14px;}
    details[open] .chev{transform: rotate(180deg); color: var(--gold);}

    .body{border-top: 1px solid rgba(148,163,184,.18); padding: 12px 12px 14px;}
    .text{font-size:13px; line-height:2; color: var(--text); white-space: pre-line; text-align: justify;}
    .divider{height:1px; background: linear-gradient(to left, transparent, rgba(148,163,184,.45), transparent); margin: 8px 0 10px;}

    .mediaBox{
      border-radius: 14px;
      overflow:hidden;
      border: 1px solid rgba(148,163,184,.28);
      background:#040712;
      box-shadow: 0 10px 26px rgba(0,0,0,.45);
    }
    .mediaBox iframe{width:100%; border:0; display:block;}

    /* صوت‌ها کوچکتر و منظم‌تر */
    .audio iframe{height: 58px}
    .video iframe{height: 260px}
    @media (max-width:560px){ .video iframe{height: 210px} }
    .file iframe{height: 420px}
    @media (max-width:560px){ .file iframe{height: 360px} }

    .audGrid{
      display:grid;
      grid-template-columns: repeat(4, minmax(0,1fr));
      gap:6px;
      align-items:stretch;
    }
    @media (max-width:980px){ .audGrid{grid-template-columns: repeat(3, minmax(0,1fr));} }
    @media (max-width:760px){ .audGrid{grid-template-columns: repeat(2, minmax(0,1fr));} }
    @media (max-width:520px){ .audGrid{grid-template-columns: 1fr} }

    /* ✅ گالری: نمایش کامل تصویر (بدون کراپ) */
    .grid{
      display:grid;
      grid-template-columns: repeat(4, minmax(0,1fr));
      gap:10px;
    }
    @media (max-width:920px){ .grid{grid-template-columns: repeat(3,1fr);} }
    @media (max-width:650px){ .grid{grid-template-columns: repeat(2,1fr);} }

    .ph{
      border-radius: 16px;
      overflow:hidden;
      border:1px solid rgba(148,163,184,.22);
      background:#040712;
      height: 220px;               /* ارتفاع ثابت برای نظم */
      box-shadow: 0 10px 24px rgba(0,0,0,.48);
      display:grid;
      place-items:center;
    }
    .ph img{
      width:100%;
      height:100%;
      object-fit:contain;          /* ✅ کل عکس نمایش داده می‌شود */
      display:block;
    }
    .ph iframe{width:100%; height:100%; border:0; display:block;} /* fallback */

    .niyat{
      margin-top: 12px;
      padding: 14px 14px 12px;
      border-radius: 18px;
      background: linear-gradient(135deg, rgba(250,204,21,.10), rgba(255,255,255,.02));
      border: 1px solid rgba(250,204,21,.35);
      box-shadow: 0 12px 32px rgba(0,0,0,.45);
    }
    .niyat h3{
      margin:0 0 8px;
      font-size:14px;
      color: var(--gold);
      display:flex; align-items:center; gap:8px;
    }
    .niyatGrid{
      display:grid;
      grid-template-columns: repeat(2, minmax(0,1fr));
      gap:10px;
    }
    @media (max-width:640px){ .niyatGrid{grid-template-columns: 1fr} }
    .ni{
      display:flex; gap:10px; align-items:flex-start;
      padding: 10px 10px;
      border-radius: 16px;
      background: rgba(5,8,20,.62);
      border: 1px solid rgba(148,163,184,.18);
    }
    .ni input{ margin-top:3px; transform: scale(1.15); accent-color: var(--gold); }
    .ni label{ cursor:pointer; line-height:1.9; font-size:13px; color:var(--text) }
    .thanks{
      margin-top: 10px;
      font-size:12px;
      color:#bbf7d0;
      opacity:0;
      transform: translateY(4px);
      transition: opacity .25s ease, transform .25s ease;
      line-height:1.9;
    }
    .thanks.show{opacity:1; transform: translateY(0)}

    footer{
      padding: 12px 18px;
      border-top: 1px solid var(--line);
      background: rgba(5,8,20,.90);
      display:flex;
      justify-content:space-between;
      gap:10px;
      flex-wrap:wrap;
      color: var(--muted);
      font-size:11px;
    }
    footer b{color: var(--gold)}

    .dock{
      position: fixed;
      bottom: 14px;
      left: 50%;
      transform: translateX(-50%);
      z-index: 9;
      display:none;
      gap:8px;
      padding: 8px;
      border-radius: 999px;
      background: rgba(5,8,20,.78);
      border: 1px solid rgba(148,163,184,.18);
      backdrop-filter: blur(10px);
      box-shadow: 0 18px 60px rgba(0,0,0,.55);
    }
    .dock a, .dock button{
      border:0;
      background: transparent;
      color: var(--text);
      cursor:pointer;
      padding: 8px 10px;
      border-radius: 999px;
      font-size:12px;
      display:inline-flex; align-items:center; gap:6px;
    }
    .dock a:hover, .dock button:hover{background: rgba(250,204,21,.10);}
    @media (max-width:820px){ .dock{display:flex} }

    .noteWarn{
      margin-top:10px;
      padding:10px 12px;
      border-radius:14px;
      border:1px solid rgba(250,204,21,.28);
      background: rgba(250,204,21,.06);
      color:#fef9c3;
      font-size:12px;
      line-height:1.9;
      display:none;
    }
    .noteWarn.show{display:block;}
  </style>
</head>

<body>
  <div class="bgPhoto" id="bgPhoto" aria-hidden="true"></div>
  <div class="glow"></div>
  <canvas id="stars"></canvas>

  <div class="wrap">
    <div class="shell" id="top">
      <header>
        <div class="brand">
          <div class="mark">✨</div>
          <div>
            <h1>یادبود شهید عبدالله برء</h1>
            <p>صفحه مجازی زیارت و دل‌نوشته برای سرباز شهید راه اسلام و میهن</p>
          </div>
        </div>
        <div class="basmala"><b>بِسْمِ رَبِّ الشُّهَدَاءِ وَالصِّدِّیقِین</b></div>
      </header>

      <section class="hero">
        <div class="heroGrid">
          <div class="portraitCard">
            <div class="ring"></div>
            <div class="shine"></div>
            <div class="portrait" id="heroPortrait" title="برای دیدن عکس بعدی کلیک کنید">
              <iframe id="heroPhoto" allow="autoplay"></iframe>
            </div>
          </div>

          <div class="heroText">
            <h2 class="name">عبدالله برء</h2>
            <p class="role">سرباز شهید راه اسلام و میهن</p>

            <p class="quote">
              <em>«امروز روز حق است؛ سربازی امروز مثل زمان امام حسین (ع) می‌باشد.»</em><br>
              او راه جبهه و شهادت را با آگاهی و اختیار انتخاب کرد؛ این صفحه برای آن است
              که نام و یادش، همراه دل‌نوشته‌های زائران، زنده بماند.
            </p>

            <p class="dates">
              <span>اعزام:</span> ۱۵ / ۱۰ / ۱۳۶۰ &nbsp;&nbsp;|&nbsp;&nbsp;
              <span>شهادت:</span> ۲۲ / ۱۰ / ۱۳۶۱
            </p>

            <div class="metaRow">
              <div class="chip"><b>محل خدمت:</b> جزیره مینو، آبادان</div>
              <div class="chip"><b>ویژگی:</b> مومن غیرتمند</div>
              <div class="chip">فرزند رامهرمز</div>
            </div>

            <div class="actions">
              <a class="btn" href="#will" data-open="will">📜 وصیت‌نامه</a>
              <a class="btn" href="#bio" data-open="bio">📖 زندگی‌نامه</a>
              <a class="btn" href="#media" data-open="media">🎬 کلیپ</a>
              <a class="btn" href="#gallery" data-open="gallery">🖼️ عکس‌ها</a>
              <a class="btn" href="#audios" data-open="audios">🎧 صوت‌ها</a>
              <a class="btn primary" href="#notes" data-open="notes">💌 دل‌نوشته</a>
              <a class="btn" href="#khademContact">🤝 ارتباط</a>
              <button class="btn" id="shareBtn" type="button">🔗 کپی لینک صفحه</button>
            </div>
          </div>
        </div>

        <div class="countdown" aria-live="polite">
          <div>
            <div style="font-size:13px; font-weight:700;">⏳ تا سالگرد بعدی شهادت</div>
            <small id="countNote">محاسبه بر اساس ۲۲ دی (هجری شمسی)</small>
          </div>
          <div class="countVal"><span id="countDays">...</span> روز باقی مانده</div>
        </div>
      </section>

      <main>
        <!-- 1) وصیت نامه -->
        <details class="section" id="will">
          <summary>
            <div class="sumLeft">
              <div class="ico">📜</div>
              <div class="sumTitle">
                <b>وصیت‌نامه شهید</b>
                <span>متن کامل وصیت‌نامه – ۱۳ / ۳ / ۱۳۶۱</span>
              </div>
            </div>
            <div class="chev">⌄</div>
          </summary>
          <div class="body">
            <div class="divider"></div>
            <div class="text">
به نام حق

وصیتنامه سرباز شهید عبداله برء  :                                     ۱۳ / ۳ / ۱۳۶۱

با درود فراوان به رهبر انقلاب اسلامی ایران؛ امام خمینی و سلام به شهیدان از صدر اسلام تا کنون و سلام بر امام زمان (عج) که منتظر ظهورش هستیم، ان‌شاءالله.
این انقلاب که بر پایهٔ اصول اسلامی است، زمینه‌ساز حکومت عدل الهی می‌باشد و آن‌ها که شهید شدند، به‌خاطر رضای خدا و همین حکومت عدل الهی شهید شدند و ما الحمدلله در زمانی خدمت می‌کنیم که این خدمت ما برای میهن و نظام جمهوری اسلامی است و برای این خدمتمان افتخار می‌کنیم.

از تمام مردم ایران می‌خواهم که همیشه پشتیبان این انقلاب اسلامی و پشتیبان ولایت فقیه باشند و ما نیز تا آخرین قطرهٔ خونمان پشتیبان اسلام عزیز هستیم و تا نابودی استکبار جهانی، به‌سرکردگی آمریکا و مزدورانش ایستاده‌ایم و آن‌ها را از بین می‌بریم.

امیدوارم که خداوند شهدای انقلاب را با شهدای کربلا محشور کند و از شما تقاضا دارم برای سلامتی امام همیشه دعا کنید و ما نیز به قرآن گوش فرا داده‌ایم و پیرو آیه‌های آن هستیم.

من مبلغ ۶۰۰ ریال به محسن پسر اسد آمون بدهکار هستم که آن مبلغ را بپردازید. خداوند در قرآن می‌فرماید:

«وَ ما لَکُم لا تُقاتِلونَ فی سَبیلِ اللهِ وَ المُستَضعَفینَ مِنَ الرِّجالِ وَ النِّساءِ وَ الوِلدانِ»

اسلام پیروز است و صدامیان نابود هستند.
خدایا خدایا تا انقلاب مهدی (عج) خمینی را نگهدار.
            </div>

            <div class="divider"></div>
            <div class="text">پیوست وصیت‌نامه</div>
            <div class="mediaBox file" style="margin-top:8px;">
              <iframe id="willAttach" loading="lazy" allow="autoplay"></iframe>
            </div>
          </div>
        </details>

        <!-- 2) زندگی نامه -->
        <details class="section" id="bio">
          <summary>
            <div class="sumLeft">
              <div class="ico">📖</div>
              <div class="sumTitle">
                <b>زندگینامه شهید</b>
                <span>روایت مسیر زندگی تا شهادت</span>
              </div>
            </div>
            <div class="chev">⌄</div>
          </summary>
          <div class="body">
            <div class="divider"></div>
            <div class="text">
به نام حق
اذا جاء نصرالله...

شهید، فرزند پدری است پیر و از کار افتاده و پدر ایشان در سال‌های کودکی از داشتن پدر و مادر محروم شده و سپس با زندگی بسیار سختی بزرگ شده بود و بعد از چند سال ازدواج کرد.
مادر شهید، تنها فرزند پدری بود که در زمان شهریور ۱۳۲۰ در جنگ دشت شیر کشته شد.

برادرِ بزرگ شهید یکی از چند فرزند این پدر بود که از ۸ سالگی نزد مردم چوپانی می‌کرد و در اواخر هر سال که ۱۲ ماه است، مزد او ۴ یا ۵ بزغاله بود. بعد از مدتی شهید به کارگری پرداخت و پس از کارگری بود که وی عازم خدمت سربازی گردید.

عده‌ای از مردم می‌گفتند: «تو که با این رنج و مشقت بزرگ شده‌ای چطور می‌خواهی به سربازی بروی؟»
ولی شهید می‌گفت: «امروز روز حق است. سربازی امروز مثل زمان امام حسین (ع) می‌باشد. کاش من بعد از این همه بدبختی‌ها که به این سن رسیده‌ام، روبروی دشمن بجنگم و شربت شهادت را بنوشم.»

وی در تاریخ ۱۵ / ۱۰ / ۶۰ عازم سربازی شد و سه ماه دورهٔ آموزشی خود را در جهرم گذراند و بعد از آن در جزیرهٔ مینو آبادان خدمت خود را انجام داد. وی یک‌بار – که دفعهٔ آخرش بود – به مرخصی آمد و با تمام فامیل و آشناهایش عکس گرفت و به اقوامش گفته بود: «شاید من بعد از این مرخصی شهید شوم؛ این عکس‌ها به‌عنوان یادگاری نزد شما باشند.» زمانی که برای آخرین بار به مرخصی آمد، بوی شهادت از این برادر می‌آمد؛ نزد هر کس می‌رفت خداحافظی می‌کرد.

در اثنای این مرخصی، پدر و مادرش برای وی نامزد کردند. شهید بعد از اینکه به محل خدمت رفت طی نامه‌ای به پدر و مادر خود گفت: «حالا که بعد از این همه بدبختی و فلاکت آرزوی عروسی مرا دارید، بگذارید بعد از اینکه از خدمت آمدم، مراسم عقد و عروسی را بگذارید.»

وی آخرین نامهٔ خویش را در تاریخ ۲۱ / ۱۰ / ۶۱ به پدر و مادر نوشت و بالاخره در تاریخ ۲۲ / ۱۰ / ۱۳۶۱ به درجهٔ رفیع شهادت نائل آمد.

روحش شاد و راهش مستدام و پررهرو.
واحد فرهنگی بنیاد شهید رامهرمز
            </div>

            <div class="divider"></div>
            <div class="text">پیوست زندگینامه</div>
            <div class="mediaBox file" style="margin-top:8px;">
              <iframe id="bioAttach" loading="lazy" allow="autoplay"></iframe>
            </div>
          </div>
        </details>

        <!-- 3) کلیپ -->
        <details class="section" id="media">
          <summary>
            <div class="sumLeft">
              <div class="ico">🎬</div>
              <div class="sumTitle">
                <b>کلیپ یادبود</b>
                <span>پخش کلیپ تصویری</span>
              </div>
            </div>
            <div class="chev">⌄</div>
          </summary>
          <div class="body">
            <div class="divider"></div>
            <div class="text">کلیپ یادبود</div>
            <div class="mediaBox video" style="margin-top:8px;">
              <iframe id="memVideo" allow="autoplay"></iframe>
            </div>
          </div>
        </details>

        <!-- 4) عکس‌ها -->
        <details class="section" id="gallery">
          <summary>
            <div class="sumLeft">
              <div class="ico">🖼️</div>
              <div class="sumTitle">
                <b>گالری تصاویر</b>
                <span>قاب‌هایی از شهید و خانواده</span>
              </div>
            </div>
            <div class="chev">⌄</div>
          </summary>
          <div class="body">
            <div class="divider"></div>
            <div class="text" style="margin-bottom:10px;">گالری شهید</div>
            <div class="grid" id="gridShahid"></div>

            <div class="divider" style="margin-top:14px;"></div>
            <div class="text" style="margin-bottom:10px;">گالری خانواده</div>
            <div class="grid" id="gridFamily"></div>
          </div>
        </details>

        <!-- 5) صوت‌ها (✅ باز و بسته شونده مثل بقیه) -->
        <details class="section" id="audios">
          <summary>
            <div class="sumLeft">
              <div class="ico">🎧</div>
              <div class="sumTitle">
                <b>صوت‌های معنوی</b>
                <span>برای باز کردن، کلیک کنید</span>
              </div>
            </div>
            <div class="chev">⌄</div>
          </summary>

          <div class="body">
            <div class="divider"></div>
            <div class="text" style="font-size:12px; color:var(--muted);">
              اگر پلیرها نمایش داده نشدند، از لینک‌های مستقیم همین پایین استفاده کنید.
            </div>

            <div id="spiritualAudios" class="audGrid" style="margin-top:10px;"></div>
            <div id="spiritualLinks" class="text" style="margin-top:10px; font-size:12px; color:var(--muted);"></div>
          </div>
        </details>

        <!-- 6) دلنوشته -->
        <details class="section" id="notes">
          <summary>
            <div class="sumLeft">
              <div class="ico">💌</div>
              <div class="sumTitle">
                <b>دل‌نوشته زائران</b>
                <span>ثبت + مشاهده + ویرایش نوشته‌های خودتان</span>
              </div>
            </div>
            <div class="chev">⌄</div>
          </summary>

          <div class="body">
            <div class="divider"></div>
            <div class="text">
اینجا می‌توانید دل‌نوشته یا دعای خود را ثبت کنید.
نوشته‌های قبلی نیز پایین‌تر نمایش داده می‌شوند (از جدید به قدیم).
برای ویرایش نوشته‌ی خودتان، «کلید ویرایش» را نگه دارید.
            </div>

            <div class="divider"></div>

            <div class="mediaBox" style="margin-top:8px;">
              <iframe
                id="notesApp"
                style="width:100%; height:900px; border:0;"
                loading="lazy"
                allow="clipboard-write"
              ></iframe>
            </div>

            <div id="notesWarn" class="noteWarn">
              اگر دل‌نوشته داخل صفحه باز نشد، احتمالاً اجازه‌ی نمایش داخل iframe داده نشده.
              از لینک مستقیم استفاده کنید:
              <br>
              <a id="notesOpenBtn" class="btn primary" target="_blank" rel="noopener" style="margin-top:8px; display:inline-flex;">باز کردن دل‌نوشته</a>
            </div>

            <div class="text" style="margin-top:10px; font-size:12px; color:var(--muted);">
              لینک مستقیم دل‌نوشته:
              <a id="notesOpen" target="_blank" rel="noopener" style="color:var(--gold); text-decoration:none;">اینجا کلیک کنید</a>
            </div>

            <section class="niyat" id="niyat">
              <h3>🌸 امروز برای شهید چه آوردی؟</h3>
              <div class="niyatGrid">
                <div class="ni"><input id="n1" type="checkbox"><label for="n1">خواندم یک فاتحه 🍃</label></div>
                <div class="ni"><input id="n2" type="checkbox"><label for="n2">فرستادم یک صلوات 🌹</label></div>
                <div class="ni"><input id="n3" type="checkbox"><label for="n3">انجام می‌دهم یک کار خیر به نیت شهید 🤲</label></div>
                <div class="ni"><input id="n4" type="checkbox"><label for="n4">امروز یک نفر را بخشیدم و حلال کردم 🤍</label></div>
              </div>
              <div class="thanks" id="thanks">
                ممنونم برادر / خواهر مومنم 🌷<br>
                ان‌شاءالله بماند به روزی که همدیگر را ملاقات کنیم.
              </div>
            </section>
          </div>
        </details>

        <!-- 7) ارتباط -->
        <section class="niyat" id="khademContact">
          <h3>🤝 ارتباط با ما</h3>

          <div style="display:flex; flex-wrap:wrap; gap:10px; margin-top:10px;">
            <a class="btn primary" id="tgLink2" target="_blank" rel="noopener">تلگرام</a>
            <a class="btn" id="igLink2" target="_blank" rel="noopener">اینستاگرام</a>
            <a class="btn" id="waLink" target="_blank" rel="noopener">واتساپ</a>
            <a class="btn" id="eitaaLink" target="_blank" rel="noopener">ایتا</a>
          </div>

          <div class="text" style="margin-top:10px; font-size:12px; color:var(--muted);">
            تلگرام: <span style="color:var(--gold)">@ba_khatereha0</span><br>
            ایتا: <span style="color:var(--gold)">@ba_khatereha0</span><br>
            واتساپ: <a id="waText" target="_blank" rel="noopener" style="color:var(--gold); text-decoration:none;">لینک</a>
          </div>
        </section>

      </main>

      <footer>
        <span>این صفحه با <b>QR</b> کنار مزار شهید قابل مشاهده است.</span>
        <span>اللهم اجعل محیانا محیا محمد و آل محمد و مماتنا ممات محمد و آل محمد.</span>
      </footer>
    </div>
  </div>

  <nav class="dock" aria-label="دسترسی سریع">
    <a href="#top">⬆️ بالا</a>
    <a href="#will" data-open="will">📜 وصیت</a>
    <a href="#audios" data-open="audios">🎧 صوت</a>
    <a href="#khademContact">🤝 ارتباط</a>
    <button type="button" id="dockShare">🔗 لینک</button>
  </nav>

  <script>
    /***********************
     * CONFIG
     ***********************/
    const CONFIG = {
      heroRotateMs: 10000,

      heroPhotoUrls: [
        "https://drive.google.com/file/d/1yy50o_IMX0l267AQWo8mW99ZUQd64iVJ/view?usp=sharing",
        "https://drive.google.com/file/d/1QAdl-ElJadkdnegFWFc8WGtgAlHj-AAf/view?usp=sharing"
      ],

      memorialVideoUrl: "https://drive.google.com/file/d/1ULaWWoHVT5OILPoD32QbdDyO61-31GBl/view?usp=sharing",

      willAttachUrl: "https://drive.google.com/file/d/1ZqvLFKjcVCvvA67BCaEJ2f9G5N5iVTEj/view?usp=sharing",
      bioAttachUrl:  "https://drive.google.com/file/d/1aDY7bvWxB0FCxsgo5DUmnrkJzh4Em1GQ/view?usp=sharing",

      spiritualAudioUrls: [
        "https://drive.google.com/file/d/1QqghFpRPw17yBCF6xqBG-Oj2H6gqg3zo/view?usp=sharing",
        "https://drive.google.com/file/d/16nQEsuQoZwBITSRJZujWcHqNvFvAHwGM/view?usp=sharing",
        "https://drive.google.com/file/d/1kiYnCfKqEhUNdY2SFjZhIAIduerAv4EK/view?usp=sharing",
        "https://drive.google.com/file/d/1e--I4xNb-atHtZiQ4-1HKnVTx3RPWHIT/view?usp=sharing",
        "https://drive.google.com/file/d/1yzqBE7BaMvZElcGP3uv1ss1NOlMIC2VZ/view?usp=sharing",
        "https://drive.google.com/file/d/12h8tr9wsuTcDVdCmV-x2F1ZK59NZUPE_/view?usp=sharing",
        "https://drive.google.com/file/d/1JK2w0z3yzvG0v2c2wrfRdCd5VrwLTUTz/view?usp=sharing",
        "https://drive.google.com/file/d/1fPMU6zCEecLj8NDZOpwaCdMZnAf2SqRz/view?usp=sharing",
        "https://drive.google.com/file/d/1aBlYaA1sUGDPnYU2BQCGHJASERcX6lDX/view?usp=sharing",
        "https://drive.google.com/file/d/1Xyv406O85A1rpwlaSdcBMf_zRbSTDMrH/view?usp=sharing",
        "https://drive.google.com/file/d/1opLY2Ip_mJ2k2R1uPpv8i_0fuxU1K8rI/view?usp=sharing",
        "https://drive.google.com/file/d/1xKgcvg4llrqE_OScikScF4hRPbQKZxZO/view?usp=sharing",
        "https://drive.google.com/file/d/14YGVP9PhsxC3mj36HXuatzieLGUv6RtI/view?usp=sharing"
      ],

      galleryFamilyUrls: [
        "https://drive.google.com/file/d/1y28kGjk4Cx7nooLO1I6voi4Y3eJKtm_oce9kZJFDDgk/view?usp=sharing",
        "https://drive.google.com/file/d/1oUKfiWWePwZ5vfyLF_cD4TR2IeX3_iRh/view?usp=sharing",
        "https://drive.google.com/file/d/17OKBou8WjMwMT8gHiPwrsc05LXN1v3-S/view?usp=sharing",
        "https://drive.google.com/file/d/12RReRu1QgYKYpsiExmX2J8PmvEP1L3Hl/view?usp=sharing",
        "https://drive.google.com/file/d/1Qvd9E-1bVT-HQICkQ-n74x1VkNshFq_U/view?usp=sharing",
        "https://drive.google.com/file/d/1lagXKRK0DX9Of70Zk77cO0hqMlgWRjRs/view?usp=sharing",
        "https://drive.google.com/file/d/1-iFYG1s5oegttrTUHUW7LUD1Ko4OoTp6/view?usp=sharing",
        "https://drive.google.com/file/d/1zOPeAWZ6eUXbCN8M_rGzP26EP8d5efcF/view?usp=sharing",
        "https://drive.google.com/file/d/1Yny37j1EKNL0ArUNTqTe-MLbbHDSOaKs/view?usp=sharing",
        "https://drive.google.com/file/d/1hDghA9IJYZnYTcwgCVLjXhspr6Wri3ZQ/view?usp=sharing",
        "https://drive.google.com/file/d/1TJXov5Iq-Juaf2ShOqs9zdQEz5QOiw9O/view?usp=sharing",
        "https://drive.google.com/file/d/1wJuW75_7Dj7DTCCQHrhDEn4k8yhIbFDK/view?usp=sharing"
      ],

      galleryShahidUrls: [
        "https://drive.google.com/file/d/1yy50o_IMX0l267AQWo8mW99ZUQd64iVJ/view?usp=sharing",
        "https://drive.google.com/file/d/1QAdl-ElJadkdnegFWFc8WGtgAlHj-AAf/view?usp=sharing",
        "https://drive.google.com/file/d/1D1Vta_EE5eDSGUfZ3eeAc3pNh9a6-Wtd/view?usp=sharing",
        "https://drive.google.com/file/d/18ZA4taJH5TJrMIBM6r_-9qgFMIuHGk4w/view?usp=sharing",
        "https://drive.google.com/file/d/19_SBr4n-blDu9tWJBHE-u5Km-GFnEkor/view?usp=sharing",
        "https://drive.google.com/file/d/1V4TFFJO3TjRXCKzH6uY8fmS7QBr9VmlM/view?usp=sharing"
      ],

      notesAppUrl: "https://script.google.com/macros/s/AKfycbyuu4F9Z67c3KenycK8A3RcL18ZH0R8Rovd1dBqnAGWJDltlvOpZScEoW0tYZgFN-TC/exec",

      telegramHandle: "@ba_khatereha0",
      telegramUrl: "https://t.me/ba_khatereha0",
      instagramUrl: "https://www.instagram.com/ba_khatereha04?igsh=MXZwaG5vazVnZXAybw==",

      whatsappUrl: "https://wa.me/message/ZPIGMPOYZJKBK1",
      eitaaHandle: "@ba_khatereha0",
      eitaaUrl: "https://eitaa.com/ba_khatereha0",

      anniversaryJalali: { jm: 10, jd: 22 },

      /* بک‌گراند */
      backgroundPhotoUrl: "https://drive.google.com/file/d/1yy50o_IMX0l267AQWo8mW99ZUQd64iVJ/view?usp=sharing"
    };

    /***********************
     * Helpers (Drive)
     ***********************/
    function getDriveId(urlOrId){
      if(!urlOrId) return "";
      const s = String(urlOrId).trim();
      if(!s.includes("drive.google.com")) return s;
      const m = s.match(/\/d\/([^/]+)/);
      return m ? m[1] : s;
    }
    const drivePreview = (urlOrId) => `https://drive.google.com/file/d/${getDriveId(urlOrId)}/preview`;

    function driveImageCandidates(urlOrId){
      const id = getDriveId(urlOrId);
      return [
        `https://drive.google.com/thumbnail?id=${id}&sz=w2400`,
        `https://drive.google.com/uc?export=view&id=${id}`,
        `https://drive.google.com/uc?export=download&id=${id}`
      ];
    }

    function setBackgroundFromDrive(urlOrId){
      const el = document.getElementById("bgPhoto");
      if (!el) return;
      const candidates = driveImageCandidates(urlOrId);
      let i = 0;
      function tryNext(){
        if (i >= candidates.length) return;
        const src = candidates[i++];
        const img = new Image();
        img.onload = () => { el.style.backgroundImage = `url("${src}")`; };
        img.onerror = tryNext;
        img.src = src;
      }
      tryNext();
    }
    setBackgroundFromDrive(CONFIG.backgroundPhotoUrl);

    /***********************
     * HERO rotate (دو عکس بالا + همه عکس‌های شهید)
     ***********************/
    function buildHeroList(){
      const list = [
        ...(CONFIG.heroPhotoUrls || []),
        ...(CONFIG.galleryShahidUrls || [])
      ];
      const seen = new Set();
      const unique = [];
      for (const u of list){
        const id = getDriveId(u);
        if (!id) continue;
        if (seen.has(id)) continue;
        seen.add(id);
        unique.push(u);
      }
      return unique.length ? unique : (CONFIG.heroPhotoUrls || []);
    }

    const HERO_LIST = buildHeroList();
    const heroIframe = document.getElementById("heroPhoto");
    const heroPortrait = document.getElementById("heroPortrait");
    let heroIndex = 0;

    function setHero(i){
      const len = HERO_LIST.length || 1;
      heroIndex = ((i % len) + len) % len;
      heroIframe.src = drivePreview(HERO_LIST[heroIndex]);
    }
    setHero(0);

    if (HERO_LIST.length > 1){
      setInterval(() => setHero(heroIndex + 1), CONFIG.heroRotateMs);
      heroPortrait.style.cursor = "pointer";
      heroPortrait.addEventListener("click", () => setHero(heroIndex + 1));
    } else {
      heroPortrait.removeAttribute("title");
    }

    /***********************
     * Video / Attachments
     ***********************/
    document.getElementById("memVideo").src = drivePreview(CONFIG.memorialVideoUrl);
    document.getElementById("willAttach").src = drivePreview(CONFIG.willAttachUrl);
    document.getElementById("bioAttach").src  = drivePreview(CONFIG.bioAttachUrl);

    /***********************
     * Notes iframe + لینک
     ***********************/
    const notesOpen = document.getElementById("notesOpen");
    const notesOpenBtn = document.getElementById("notesOpenBtn");
    notesOpen.href = CONFIG.notesAppUrl;
    notesOpenBtn.href = CONFIG.notesAppUrl;

    const notesApp = document.getElementById("notesApp");
    notesApp.src = CONFIG.notesAppUrl + (CONFIG.notesAppUrl.includes("?") ? "&" : "?") + "embed=1";

    const notesWarn = document.getElementById("notesWarn");
    let notesLoaded = false;
    notesApp.addEventListener("load", () => { notesLoaded = true; });
    setTimeout(() => { if (!notesLoaded) notesWarn.classList.add("show"); }, 7000);

    /***********************
     * Contact links
     ***********************/
    const tg2 = document.getElementById("tgLink2");
    const ig2 = document.getElementById("igLink2");
    const waLink = document.getElementById("waLink");
    const waText = document.getElementById("waText");
    const eitaaLink = document.getElementById("eitaaLink");

    tg2.href = CONFIG.telegramUrl;
    tg2.textContent = `تلگرام: ${CONFIG.telegramHandle}`;

    ig2.href = CONFIG.instagramUrl;
    ig2.textContent = "اینستاگرام";

    waLink.href = CONFIG.whatsappUrl;
    waLink.textContent = "واتساپ";
    waText.href = CONFIG.whatsappUrl;

    eitaaLink.href = CONFIG.eitaaUrl;
    eitaaLink.textContent = `ایتا: ${CONFIG.eitaaHandle}`;

    /***********************
     * Galleries (✅ img + fallback iframe)
     ***********************/
    function mountGallery(urls, elId){
      const root = document.getElementById(elId);
      root.innerHTML = "";

      (urls || []).forEach(u => {
        const box = document.createElement("div");
        box.className = "ph";

        const candidates = driveImageCandidates(u);
        const img = document.createElement("img");
        img.alt = "تصویر";
        img.loading = "lazy";
        img.referrerPolicy = "no-referrer";

        let idx = 0;
        function tryNext(){
          if (idx >= candidates.length){
            // fallback: iframe
            box.innerHTML = "";
            const iframe = document.createElement("iframe");
            iframe.src = drivePreview(u);
            iframe.allow = "autoplay";
            iframe.loading = "lazy";
            box.appendChild(iframe);
            return;
          }
          img.src = candidates[idx++];
        }

        img.onload = () => {};
        img.onerror = () => tryNext();

        box.appendChild(img);
        root.appendChild(box);
        tryNext();
      });
    }
    mountGallery(CONFIG.galleryShahidUrls, "gridShahid");
    mountGallery(CONFIG.galleryFamilyUrls, "gridFamily");

    /***********************
     * Spiritual audios (حذف تکراری‌ها) + لینک مستقیم
     ***********************/
    function dedupeDriveUrls(urls){
      const seen = new Set();
      const out = [];
      for (const u of (urls || [])){
        const id = getDriveId(u);
        if (!id) continue;
        if (seen.has(id)) continue;
        seen.add(id);
        out.push(u);
      }
      return out;
    }

    function mountAudioList(urls, elId, linksId){
      const root = document.getElementById(elId);
      const linksRoot = document.getElementById(linksId);

      const list = dedupeDriveUrls(urls);

      root.innerHTML = "";
      list.forEach((u, idx) => {
        const box = document.createElement("div");
        box.className = "mediaBox audio";

        const iframe = document.createElement("iframe");
        iframe.src = drivePreview(u);
        iframe.allow = "autoplay";
        iframe.loading = "lazy";
        iframe.title = `صوت معنوی ${idx+1}`;

        box.appendChild(iframe);
        root.appendChild(box);
      });

      const links = list.map((u, i) =>
        `<a href="${u}" target="_blank" rel="noopener" style="color:var(--gold); text-decoration:none;">صوت ${i+1}</a>`
      ).join(" • ");
      linksRoot.innerHTML = `لینک‌های مستقیم: ${links}`;
    }
    mountAudioList(CONFIG.spiritualAudioUrls, "spiritualAudios", "spiritualLinks");

    /***********************
     * UX: فقط یک بخش باز بماند + بازکردن با لینک‌ها
     ***********************/
    const allDetails = Array.from(document.querySelectorAll("details.section"));
    allDetails.forEach(d => {
      d.addEventListener("toggle", () => {
        if (d.open) allDetails.forEach(x => x !== d && (x.open = false));
      });
    });

    document.querySelectorAll("[data-open]").forEach(a => {
      a.addEventListener("click", () => {
        const id = a.getAttribute("data-open");
        const el = document.getElementById(id);
        if (el && el.tagName.toLowerCase() === "details") el.open = true;
      });
    });

    function openFromHash(){
      const id = (location.hash || "").replace("#","");
      if(!id) return;
      const el = document.getElementById(id);
      if (el && el.tagName.toLowerCase() === "details") el.open = true;
    }
    window.addEventListener("hashchange", openFromHash);
    openFromHash();

    /***********************
     * نیت روزانه با ذخیره در مرورگر
     ***********************/
    const niKey = "niyat_state_v1";
    const checks = ["n1","n2","n3","n4"].map(id => document.getElementById(id));
    const thanks = document.getElementById("thanks");

    function loadNiyat(){
      try{
        const data = JSON.parse(localStorage.getItem(niKey) || "{}");
        checks.forEach((c,i)=> c.checked = !!data[i]);
        if (checks.some(c=>c.checked)) thanks.classList.add("show");
      }catch{}
    }
    function saveNiyat(){
      const data = {};
      checks.forEach((c,i)=> data[i] = c.checked);
      localStorage.setItem(niKey, JSON.stringify(data));
      if (checks.some(c=>c.checked)) thanks.classList.add("show");
      else thanks.classList.remove("show");
    }
    checks.forEach(c => c.addEventListener("change", saveNiyat));
    loadNiyat();

    /***********************
     * Share: کپی لینک
     ***********************/
    async function copyLink(){
      const url = location.href.split("#")[0] + "#top";
      try{
        await navigator.clipboard.writeText(url);
        alert("لینک صفحه کپی شد ✅");
      }catch{
        prompt("اگر کپی خودکار نشد، لینک را دستی کپی کنید:", url);
      }
    }
    document.getElementById("shareBtn").addEventListener("click", copyLink);
    document.getElementById("dockShare").addEventListener("click", copyLink);

    /***********************
     * Countdown جلالی → میلادی
     ***********************/
    function div(a,b){ return ~~(a/b); }
    const breaks = [-61, 9, 38, 199, 426, 686, 756, 818, 1111, 1181, 1210, 1635, 2060, 2097, 2192, 2262, 2324, 2394, 2456, 3178];

    function jalCal(jy){
      let bl = breaks.length, gy = jy + 621, leapJ = -14, jp = breaks[0], jm, jump, leap, n, i;
      if (jy < jp || jy >= breaks[bl-1]) return {leap:0, gy, march:0};
      for (i=1; i<bl; i++){
        jm = breaks[i];
        jump = jm - jp;
        if (jy < jm) break;
        leapJ += div(jump, 33) * 8 + div((jump % 33), 4);
        jp = jm;
      }
      n = jy - jp;
      leapJ += div(n, 33) * 8 + div((n % 33) + 3, 4);
      if (jump % 33 === 4 && jump - n === 4) leapJ++;
      let leapG = div(gy,4) - div((div(gy,100) + 1)*3,4) - 150;
      let march = 20 + leapJ - leapG;
      if (jump - n < 6) n = n - jump + div(jump + 4, 33) * 33;
      leap = ((n + 1) % 33 - 1) % 4;
      if (leap === -1) leap = 4;
      return {leap, gy, march};
    }
    function g2d(gy, gm, gd){
      let d = div((gy + div(gm - 8, 6) + 100100) * 1461, 4)
            + div(153 * ((gm + 9) % 12) + 2, 5)
            + gd - 34840408;
      d = d - div(div(gy + 100100 + div(gm - 8, 6), 100) * 3, 4) + 752;
      return d;
    }
    function d2g(jdn){
      let j = 4 * jdn + 139361631;
      j = j + div(div(4*jdn + 183187720, 146097) * 3, 4) * 4 - 3908;
      let i = div((j % 1461), 4) * 5 + 308;
      let gd = div((i % 153), 5) + 1;
      let gm = (div(i, 153) % 12) + 1;
      let gy = div(j, 1461) - 100100 + div(8 - gm, 6);
      return {gy, gm, gd};
    }
    function j2d(jy, jm, jd){
      let r = jalCal(jy);
      return g2d(r.gy, 3, r.march) + (jm - 1) * 31 - div(jm, 7) * (jm - 7) + jd - 1;
    }
    function toGregorian(jy, jm, jd){
      const g = d2g(j2d(jy, jm, jd));
      return new Date(g.gy, g.gm - 1, g.gd);
    }
    function d2j(jdn){
      let gy = d2g(jdn).gy, jy = gy - 621, r = jalCal(jy), jdn1f = g2d(gy, 3, r.march), jd, jm, k;
      k = jdn - jdn1f;
      if (k >= 0){
        if (k <= 185){ jm = 1 + div(k, 31); jd = (k % 31) + 1; return {jy, jm, jd}; }
        else { k -= 186; }
      } else {
        jy -= 1; k += 179; if (r.leap === 1) k += 1;
      }
      jm = 7 + div(k, 30); jd = (k % 30) + 1; return {jy, jm, jd};
    }
    function toJalaliDate(date){
      const gy = date.getFullYear(), gm = date.getMonth()+1, gd = date.getDate();
      return d2j(g2d(gy, gm, gd));
    }
    function updateCountdown(){
      const now = new Date();
      const jNow = toJalaliDate(now);
      const {jm, jd} = CONFIG.anniversaryJalali;
      let targetJY = jNow.jy;
      const passed = (jNow.jm > jm) || (jNow.jm === jm && jNow.jd > jd);
      if (passed) targetJY += 1;
      const target = toGregorian(targetJY, jm, jd);
      const ms = target.setHours(12,0,0,0) - now.setHours(12,0,0,0);
      const days = Math.max(0, Math.ceil(ms / (1000*60*60*24)));
      document.getElementById("countDays").textContent = days;
    }
    updateCountdown();
    setInterval(updateCountdown, 1000*60*30);

    /***********************
     * Stars canvas
     ***********************/
    const canvas = document.getElementById("stars");
    const ctx = canvas.getContext("2d");
    let W, H, dots;

    function resize(){
      W = canvas.width = Math.floor(window.innerWidth * devicePixelRatio);
      H = canvas.height = Math.floor(window.innerHeight * devicePixelRatio);
      canvas.style.width = window.innerWidth + "px";
      canvas.style.height = window.innerHeight + "px";
      const count = Math.floor((window.innerWidth * window.innerHeight) / 18000);
      dots = Array.from({length: Math.max(70, count)}, () => ({
        x: Math.random()*W,
        y: Math.random()*H,
        r: (Math.random()*1.4 + 0.3) * devicePixelRatio,
        a: Math.random()*0.7 + 0.15,
        s: Math.random()*0.35 + 0.05
      }));
    }
    function tick(){
      ctx.clearRect(0,0,W,H);
      for (const d of dots){
        d.a += (Math.random()-0.5)*0.02;
        d.a = Math.max(0.06, Math.min(0.95, d.a));
        d.y += d.s * devicePixelRatio;
        if (d.y > H+10) d.y = -10;
        ctx.globalAlpha = d.a;
        ctx.beginPath();
        ctx.arc(d.x, d.y, d.r, 0, Math.PI*2);
        ctx.fillStyle = "#ffffff";
        ctx.fill();
      }
      ctx.globalAlpha = 1;
      requestAnimationFrame(tick);
    }
    window.addEventListener("resize", resize);
    resize();
    tick();
  </script>
</body>
</html>
