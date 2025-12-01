<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>ManhuaGod — Read (Demo)</title>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <header class="site-header">
    <div class="container header-inner">
      <a class="logo" href="/">ManhuaGod</a>
      <nav class="nav">
        <input id="search" placeholder="Search titles..." aria-label="Search" />
        <div id="auth-area" class="auth-area">
          <button id="btn-login" class="btn">Login</button>
        </div>
      </nav>
    </div>
  </header>

  <main class="container">
    <section class="hero">
      <h1>Welcome to ManhuaGod (Demo)</h1>
      <p>This is a demo using Supabase for auth + comments. Replace placeholder content with legally-owned or licensed works only.</p>
    </section>

    <section>
      <div class="grid-controls">
        <label>Filter:
          <select id="filter">
            <option value="all">All</option>
            <option value="action">Action</option>
            <option value="romance">Romance</option>
            <option value="comedy">Comedy</option>
          </select>
        </label>
      </div>

      <div id="gallery" class="gallery" aria-live="polite"></div>
    </section>
  </main>

  <footer class="site-footer">
    <div class="container">
      <small>ManhuaGod — demo template • No copyrighted content included</small>
    </div>
  </footer>

  <!-- Reader & Comments Modal -->
  <div id="reader" class="reader" aria-hidden="true">
    <div class="reader-inner">
      <button id="reader-close" class="reader-close" aria-label="Close">✕</button>
      <div id="reader-title" class="reader-title"></div>
      <div id="reader-pages" class="reader-pages"></div>

      <hr />

      <section id="comments-section" class="comments-section">
        <h3>Comments</h3>
        <div id="comment-form-area"></div>
        <div id="comments-list"></div>
      </section>
    </div>
  </div>

  <!-- Auth Modal -->
  <div id="auth-modal" class="modal" aria-hidden="true">
    <div class="modal-inner">
      <button id="auth-close" class="modal-close" aria-label="Close">✕</button>
      <h3 id="auth-title">Sign in</h3>
      <div id="auth-form">
        <input id="auth-email" type="email" placeholder="Email" />
        <input id="auth-password" type="password" placeholder="Password" />
        <button id="auth-submit" class="btn">Sign in</button>
        <div style="margin-top:8px">
          <a id="auth-toggle" href="#" style="color:var(--accent)">Create an account</a>
        </div>
        <div style="margin-top:8px;color:var(--muted);font-size:13px">
          Tip: Use a real email for full auth flows. This demo uses email/password.
        </div>
      </div>
    </div>
  </div>

  <!-- Supabase config (filled) -->
  <script src="supabase-config.js"></script>

  <!-- Supabase JS (UMD) -->
  <script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js/dist/umd/supabase.min.js"></script>

  <script type="module" src="script.js"></script>
</body>
</html>
