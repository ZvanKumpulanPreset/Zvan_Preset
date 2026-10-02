# Zvan_Preset
Kumpulan Preset Alight motion
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>AM Preset Hub</title>

  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      background:
        radial-gradient(circle at top, #29134d 0%, #0b0b12 45%, #050509 100%);
      color: #fff;
      min-height: 100vh;
    }

    header {
      padding: 35px 20px 20px;
      max-width: 1100px;
      margin: auto;
    }

    .logo {
      font-size: 34px;
      font-weight: 900;
      letter-spacing: -1px;
    }

    .subtitle {
      color: #9d9daa;
      margin-top: 8px;
      line-height: 1.5;
    }

    .toolbar {
      max-width: 1100px;
      margin: auto;
      padding: 10px 20px 25px;
      display: flex;
      gap: 10px;
      flex-wrap: wrap;
    }

    input,
    select {
      background: #12121c;
      border: 1px solid #29293a;
      color: white;
      border-radius: 12px;
      padding: 13px 15px;
      font-size: 14px;
      outline: none;
    }

    input {
      flex: 1;
      min-width: 230px;
    }

    select {
      min-width: 150px;
    }

    .grid {
      max-width: 1100px;
      margin: auto;
      padding: 0 20px 50px;

      display: grid;
      grid-template-columns:
        repeat(auto-fit, minmax(260px, 1fr));

      gap: 18px;
    }

    .card {
      background: rgba(18, 18, 28, 0.95);
      border: 1px solid #29293a;
      border-radius: 20px;
      overflow: hidden;
      transition: 0.2s;
    }

    .card:hover {
      transform: translateY(-4px);
      border-color: #8b5cf6;
      box-shadow: 0 15px 40px rgba(0,0,0,.35);
    }

    .preview {
      height: 180px;

      display: flex;
      align-items: center;
      justify-content: center;

      position: relative;

      background:
        linear-gradient(
          135deg,
          #32145c,
          #15152a 55%,
          #5a28a0
        );
    }

    .preview-title {
      font-size: 24px;
      font-weight: 900;
      opacity: .9;
    }

    .category {
      position: absolute;
      top: 12px;
      left: 12px;

      padding: 6px 9px;

      background: rgba(0,0,0,.55);
      border-radius: 8px;

      font-size: 12px;
    }

    .content {
      padding: 17px;
    }

    .content h2 {
      font-size: 19px;
      margin-bottom: 7px;
    }

    .author {
      color: #9999a8;
      font-size: 13px;
    }

    .buttons {
      display: flex;
      gap: 9px;
      margin-top: 16px;
    }

    .button {
      flex: 1;

      text-decoration: none;
      text-align: center;

      padding: 11px 10px;

      border-radius: 11px;

      color: white;
      background: #1b1b29;

      border: 1px solid #303044;

      font-size: 13px;
      font-weight: bold;
    }

    .button:hover {
      background: #28283a;
    }

    .open {
      background: #8b5cf6;
      border-color: #8b5cf6;
    }

    .open:hover {
      background: #7444d8;
    }

    .empty {
      grid-column: 1 / -1;

      text-align: center;
      padding: 60px 20px;

      color: #777786;
    }

    .info {
      max-width: 1100px;
      margin: 0 auto 40px;

      padding: 0 20px;

      color: #777786;
      font-size: 13px;
      line-height: 1.6;
    }

    @media (max-width: 600px) {
      .logo {
        font-size: 29px;
      }

      .preview {
        height: 160px;
      }
    }
  </style>
</head>

<body>

<header>

  <div class="logo">
    AM Preset Hub
  </div>

  <div class="subtitle">
    Kumpulan preset Alight Motion.
    Pilih preset lalu buka halaman share untuk mengimpornya.
  </div>

</header>


<div class="toolbar">

  <input
    type="text"
    id="search"
    placeholder="🔍 Cari preset..."
  >

  <select id="category">

    <option value="">
      Semua kategori
    </option>

  </select>

</div>


<div
  id="presetContainer"
  class="grid">
</div>


<div class="info">

  Klik <b>Buka di AM</b> untuk membuka halaman
  share Alight Motion. Jika preset mendukung import,
  gunakan tombol <b>Import Package</b> pada halaman tersebut.

</div>


<script>

/*
  ============================================
  DATA PRESET
  ============================================

  Untuk menambahkan preset baru,
  cukup tambahkan object baru ke array ini.

  "open" = link share Alight Motion
*/

const presets = [

  {
    title: "Preset API",
    author: "Alight Motion Share",
    category: "Effect",

    open:
      "https://alightcreative.com/am/share/u/41X9Pn6xkgMpvaPUXkcUfejw8Wv1/p/lmavjIRVQp-8a4941c48ec34ccd"
  },


  {
    title: "PRESETS ‼️",
    author: "Alight Motion Share",
    category: "Effect",

    open:
      "https://alightcreative.com/am/share/u/c4PPnYawaYgrwVYYJ4TZVw1Eced2/p/hFdvZIM09q-d14edbb54f8d70a7"
  },


  {
    title: "PRESET CC",
    author: "Alight Motion Share",
    category: "Color",

    open:
      "https://alightcreative.com/am/share/u/NNIswyk5w8Wp2aa5raZqGEOySHK2/p/Z4apjQomUr-7245d4bae49f5d34"
  },


  {
    title: "PRESET AM",
    author: "Alight Motion Share",
    category: "Video",

    open:
      "https://alightcreative.com/am/share/u/mZxA76g6xLXXrfq7HDqu6iOy6eB3/p/ffb47716-e5b4-428d-b150-cc40ac9d0880"
  },


  {
    title: "Preset Base",
    author: "a.mpreset",
    category: "Base",

    open:
      "https://alightcreative.com/am/share/u/NAz9dgUxwsStf3KInRZ28mlFoiV2/p/uKpVw8Daih-a3c3127452ce79ba"
  },


  {
    title: "Preset Link 1",
    author: "Alight Motion Share",
    category: "Transition",

    open:
      "https://alightcreative.com/am/share/u/tVaooeRWJSNoBCe0RpSQ3RTah6t2/p/vncrcZUWbT-1dc2368f51623a72"
  },


  {
    title: "PRESET XML — 5MB",
    author: "GAK ADA 5MB",
    category: "XML",

    open:
      "https://alightcreative.com/am/share/u/bBjlKaHXJcZFcxPkOTEZxbr6JgR2/p/kULhOC6koV-25f36912fc387aeb"
  },


  {
    title: "New Project Package Preset XML",
    author: "Rahul Mizi",
    category: "XML",

    open:
      "https://alightcreative.com/am/share/u/noGIygefA1RZkbXNAKAO47CPA7q2/p/siBf9mTep1-323ec66cf307a3cc"
  }

];


/*
  ============================================
  ELEMENT HTML
  ============================================
*/

const container =
  document.getElementById("presetContainer");

const search =
  document.getElementById("search");

const category =
  document.getElementById("category");


/*
  ============================================
  BUAT FILTER KATEGORI
  ============================================
*/

const categories = [
  ...new Set(
    presets.map(
      preset => preset.category
    )
  )
];

categories.forEach(cat => {

  const option =
    document.createElement("option");

  option.value = cat;
  option.textContent = cat;

  category.appendChild(option);

});


/*
  ============================================
  ESCAPE HTML
  ============================================
*/

function escapeHTML(text) {

  return String(text)
    .replaceAll("&", "&amp;")
    .replaceAll("<", "&lt;")
    .replaceAll(">", "&gt;")
    .replaceAll('"', "&quot;")
    .replaceAll("'", "&#039;");

}


/*
  ============================================
  RENDER PRESET
  ============================================
*/

function renderPresets() {

  const keyword =
    search.value
      .toLowerCase()
      .trim();

  const selectedCategory =
    category.value;


  const filtered =
    presets.filter(preset => {

      const text =
        (
          preset.title +
          " " +
          preset.author +
          " " +
          preset.category
        ).toLowerCase();

      const matchesSearch =
        text.includes(keyword);

      const matchesCategory =
        !selectedCategory ||
        preset.category === selectedCategory;

      return (
        matchesSearch &&
        matchesCategory
      );

    });


  container.innerHTML = "";


  if (filtered.length === 0) {

    container.innerHTML = `
      <div class="empty">
        Preset tidak ditemukan.
      </div>
    `;

    return;
  }


  filtered.forEach(preset => {

    const card =
      document.createElement("article");

    card.className = "card";


    card.innerHTML = `

      <div class="preview">

        <div class="preview-title">
          ▶ PRESET
        </div>

        <div class="category">
          ${escapeHTML(preset.category)}
        </div>

      </div>


      <div class="content">

        <h2>
          ${escapeHTML(preset.title)}
        </h2>

        <div class="author">
          ${escapeHTML(preset.author)}
        </div>


        <div class="buttons">

          <a
            class="button"
            href="${preset.open}"
            target="_blank"
            rel="noopener noreferrer"
          >
            Preview
          </a>


          <a
            class="button open"
            href="${preset.open}"
            target="_blank"
            rel="noopener noreferrer"
          >
            Buka di AM ↗
          </a>

        </div>

      </div>

    `;


    container.appendChild(card);

  });

}


/*
  ============================================
  EVENT SEARCH
  ============================================
*/

search.addEventListener(
  "input",
  renderPresets
);


category.addEventListener(
  "change",
  renderPresets
);


/*
  ============================================
  START
  ============================================
*/

renderPresets();

</script>

</body>
</html>
