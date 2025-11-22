  :root {
      --bg: #0f172a;
      --card: #020617;
      --accent: #38bdf8;
      --accent-soft: rgba(56, 189, 248, 0.15);
      --text: #e5e7eb;
      --muted: #9ca3af;
      --border: #1f2937;
      --heading: #f9fafb;
    }
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }
    body {
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI",
        sans-serif;
      background: radial-gradient(circle at top, #1f2937 0, #020617 55%, #000 100%);
      color: var(--text);
      min-height: 100vh;
      display: flex;
      justify-content: center;
      padding: 2rem 1rem;
    }
    .page {
      width: 100%;
      max-width: 900px;
      background: linear-gradient(145deg, #020617 0%, #020617 60%, #111827 100%);
      border-radius: 18px;
      border: 1px solid rgba(148, 163, 184, 0.2);
      padding: 2.5rem 2rem;
      box-shadow:
        0 25px 60px rgba(0, 0, 0, 0.7),
        0 0 0 1px rgba(15, 23, 42, 0.7);
      position: relative;
      overflow: hidden;
    }
    .page::before {
      content: "";
      position: absolute;
      inset: -40%;
      background:
        radial-gradient(circle at 10% -10%, rgba(56, 189, 248, 0.12), transparent 60%),
        radial-gradient(circle at 110% 110%, rgba(94, 234, 212, 0.14), transparent 55%);
      opacity: 0.7;
      pointer-events: none;
    }
    .content {
      position: relative;
      z-index: 1;
    }
    /* Header */
    .badge {
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      padding: 0.25rem 0.6rem;
      font-size: 0.75rem;
      border-radius: 999px;
      background: rgba(15, 23, 42, 0.9);
      border: 1px solid rgba(148, 163, 184, 0.4);
      color: var(--muted);
      margin-bottom: 0.75rem;
    }
    .badge-dot {
      width: 6px;
      height: 6px;
      border-radius: 999px;
      background: #22c55e;
      box-shadow: 0 0 0 4px rgba(34, 197, 94, 0.25);
    }
    h1 {
      font-size: clamp(2.25rem, 4vw, 2.8rem);
      color: var(--heading);
      margin-bottom: 0.4rem;
      display: flex;
      align-items: center;
      gap: 0.6rem;
    }
    h1 span.emoji {
      font-size: 2.2rem;
    }
    .subtitle {
      color: var(--muted);
      max-width: 40rem;
      line-height: 1.6;
      margin-bottom: 1.8rem;
    }
    hr {
      border: none;
      border-top: 1px solid var(--border);
      margin: 1.8rem 0;
    }
    h2 {
      font-size: 1.3rem;
      margin-bottom: 0.8rem;
      color: var(--heading);
      display: flex;
      align-items: center;
      gap: 0.4rem;
    }
    /* Məqsədim */
    .goals-list {
      list-style: none;
      display: grid;
      gap: 0.4rem;
      padding-left: 0;
    }
    .goals-list li {
      position: relative;
      padding-left: 1.4rem;
      color: var(--text);
      font-size: 0.97rem;
    }
    .goals-list li::before {
      content: "•";
      position: absolute;
      left: 0.2rem;
      top: 0.1rem;
      color: var(--accent);
    }
    /* Languages & Tools */
    .section-card {
      background: radial-gradient(circle at top left, var(--accent-soft), transparent 60%);
      border-radius: 14px;
      border: 1px solid rgba(148, 163, 184, 0.4);
      padding: 1.2rem 1rem 1.3rem;
      margin-top: 0.4rem;
    }
    .lang-title {
      text-align: center;
      font-size: 1.1rem;
      margin-bottom: 1rem;
      color: var(--heading);
    }
    .tools-row {
      display: flex;
      justify-content: center;
      gap: 1.5rem;
      flex-wrap: wrap;
    }
    .tool-icon {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 0.4rem;
      font-size: 0.8rem;
      color: var(--muted);
    }
    .tool-icon img {
      transition: transform 0.2s ease, box-shadow 0.2s ease;
      border-radius: 12px;
      padding: 0.25rem;
      background: rgba(15, 23, 42, 0.8);
      box-shadow:
        0 8px 20px rgba(15, 23, 42, 0.9),
        0 0 0 1px rgba(15, 23, 42, 0.7);
    }
    .tool-icon:hover img {
      transform: translateY(-4px) scale(1.03);
      box-shadow:
        0 14px 30px rgba(15, 23, 42, 0.85),
        0 0 0 1px rgba(56, 189, 248, 0.3);
    }
    /* Günlük qeydlər cədvəli */
    .notes-table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 0.4rem;
      font-size: 0.9rem;
      overflow: hidden;
      border-radius: 12px;
      border: 1px solid var(--border);
      background: rgba(15, 23, 42, 0.8);
    }
    .notes-table thead {
      background: linear-gradient(
        90deg,
        rgba(56, 189, 248, 0.16),
        rgba(59, 130, 246, 0.16)
      );
    }
    .notes-table th,
    .notes-table td {
      padding: 0.55rem 0.8rem;
      text-align: left;
      border-bottom: 1px solid rgba(30, 64, 175, 0.35);
    }
    .notes-table th {
      font-weight: 600;
      color: var(--heading);
      font-size: 0.85rem;
      letter-spacing: 0.03em;
      text-transform: uppercase;
    }
    .notes-table td {
      color: var(--text);
    }
    .notes-table tbody tr:nth-child(odd) {
      background: rgba(15, 23, 42, 0.9);
    }
    .notes-table tbody tr:nth-child(even) {
      background: rgba(15, 23, 42, 0.75);
    }
    .notes-table tbody tr:hover {
      background: rgba(15, 23, 42, 0.98);
    }
    .link-pill {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 2.1rem;
      height: 1.6rem;
      border-radius: 999px;
      background: rgba(56, 189, 248, 0.1);
      color: var(--accent);
      font-size: 0.85rem;
    }
    .notes-hint {
      margin-top: 0.6rem;
      font-size: 0.83rem;
      color: var(--muted);
      font-style: italic;
    }
    /* Motivasiya */
    blockquote {
      border-left: 3px solid var(--accent);
      padding-left: 0.9rem;
      margin-top: 0.4rem;
      color: var(--muted);
      font-size: 0.92rem;
    }
    blockquote p {
      margin-bottom: 0.4rem;
    }
    /* Contact */
    .contact-title {
      text-align: center;
      font-size: 1.1rem;
      margin-bottom: 0.8rem;
    }
    .contact-row {
      display: flex;
      justify-content: center;
      gap: 1.1rem;
      align-items: center;
      flex-wrap: wrap;
    }
    .contact-row a img {
      transition: transform 0.2s ease, filter 0.2s ease;
      filter: drop-shadow(0 8px 18px rgba(15, 23, 42, 0.9));
    }
    .contact-row a:hover img {
      transform: translateY(-3px) scale(1.05);
      filter: drop-shadow(0 10px 24px rgba(56, 189, 248, 0.6));
    }
    .footer-note {
      margin-top: 1.4rem;
      text-align: center;
      font-size: 0.9rem;
      color: var(--muted);
    }
    .footer-note span {
      color: var(--accent);
    }
    @media (max-width: 640px) {
      .page {
        padding: 1.8rem 1.3rem;
      }
      .tools-row {
        gap: 1rem;
      }
      .notes-table th,
      .notes-table td {
        padding: 0.5rem 0.6rem;
      }
    }
  </style>
</head>
<body>
  <main class="page">
    <div class="content">
      <!-- Header -->
      <div class="badge">
        <span class="badge-dot"></span>
        <span>Front-end öyrənmə yolculuğu</span>
      </div>
      <h1><span class="emoji">🌟</span>Days of Code</h1>
      <p class="subtitle">
        Bu repo mənim Front-end Development öyrənmə yolculuğumu sənədləşdirmək üçün
        yaradılıb. Hər gün yeni mövzu, kod parçaları, tapşırıqlar və öyrəndiyim
        bilikləri burada qeyd edirəm.
      </p>
      <hr />
      <!-- Məqsədim -->
      <section>
        <h2>🎯 Məqsədim</h2>
        <ul class="goals-list">
          <li>Front-end development bacarıqlarımı inkişaf etdirmək</li>
          <li>HTML, CSS, JavaScript və React öyrənmək</li>
          <li>Hər gün ən azı bir faydalı kod yazmaq</li>
          <li>Öyrəndiklərimi sənədləşdirmək və paylaşmaq</li>
        </ul>
      </section>
      <hr />
      <!-- Languages & Tools -->
      <section>
        <div class="section-card">
          <h3 class="lang-title">💻 Languages and Tools</h3>
          <div class="tools-row">
            <a
              class="tool-icon"
              href="https://www.w3schools.com/cpp/"
              target="_blank"
              rel="noreferrer"
            >
              <img
                src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg"
                alt="cplusplus"
                width="40"
                height="40"
              />
              <span>C++</span>
            </a>
            <a
              class="tool-icon"
              href="https://developer.mozilla.org/en-US/docs/Web/JavaScript"
              target="_blank"
              rel="noreferrer"
            >
              <img
                src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg"
                alt="javascript"
                width="40"
                height="40"
              />
              <span>JavaScript</span>
            </a>
            <a
              class="tool-icon"
              href="https://www.python.org"
              target="_blank"
              rel="noreferrer"
            >
              <img
                src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg"
                alt="python"
                width="40"
                height="40"
              />
              <span>Python</span>
            </a>
            <a
              class="tool-icon"
              href="https://www.w3.org/html/"
              target="_blank"
              rel="noreferrer"
            >
              <img
                src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg"
                alt="html5"
                width="40"
                height="40"
              />
              <span>HTML5</span>
            </a>
          </div>
        </div>
      </section>
      <hr />
      <!-- Günlük qeydlər -->
      <section>
        <h2>📘 Günlük Öyrənmə Qeydləri</h2>
        <table class="notes-table">
          <thead>
            <tr>
              <th>Gün</th>
              <th>Mövzu</th>
              <th>Link</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>Day 01</td>
              <td>HTML əsasları</td>
              <td><span class="link-pill">🔹</span></td>
            </tr>
            <tr>
              <td>Day 02</td>
              <td>CSS struktur və style</td>
              <td><span class="link-pill">🔹</span></td>
            </tr>
            <tr>
              <td>Day 03</td>
              <td>Flexbox və Layout</td>
              <td><span class="link-pill">🔹</span></td>
            </tr>
            <tr>
              <td>Day 04</td>
              <td>JavaScript giriş</td>
              <td><span class="link-pill">🔹</span></td>
            </tr>
            <tr>
              <td>...</td>
              <td>...</td>
              <td><span class="link-pill">🔹</span></td>
            </tr>
          </tbody>
        </table>
        <p class="notes-hint">
          Günlər artdıqca bu cədvəli öz layihələrin və qeydlərinlə yeniləyə bilərsən.
        </p>
      </section>
      <hr />
      <!-- Sənədləşdirdiklərim -->
      <section>
        <h2>⭐ Mən bu repoda nəyi sənədləşdirirəm?</h2>
        <ul class="goals-list">
          <li>HTML/CSS əsasları</li>
          <li>JavaScript fundamental anlayışlar</li>
          <li>Kod yazarkən qarşılaşdığım problemlər və həll yollarım</li>
          <li>Öz miniprojektlərim</li>
          <li>Qeydlər və dərs nəticələri</li>
        </ul>
      </section>
      <hr />
      <!-- Motivasiya -->
      <section>
        <h2>🧠 Motivasiya</h2>
        <blockquote>
          <p><em>"Hər gün bir az kod yazmaq — bir gün böyük inkişaf deməkdir."</em></p>
          <p><em>"Consistency is better than perfection."</em></p>
        </blockquote>
      </section>
      <hr />
      <!-- Contact -->
      <section>
        <h3 class="contact-title">⚡ Contact</h3>
        <div class="contact-row">
          <a href="https://instagram.com/rehman.mammadov" target="_blank">
            <img
              src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/instagram.svg"
              alt="Instagram"
              height="34"
              width="44"
            />
          </a>
          <a href="https://discord.com/users/594201367669768217" target="_blank">
            <img
              src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/discord.svg"
              alt="Discord"
              height="34"
              width="44"
            />
          </a>
        </div>
        <p class="footer-note">
          💙 Əgər bu yolculuq sənə də ilham verirsə — bir <span>⭐</span> verə bilərsən!
        </p>
      </section>
    </div>
  </main>
</body>
</html>
