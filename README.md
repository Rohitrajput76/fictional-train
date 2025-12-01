<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>ManhuaGod — Explore Manhua</title>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <header class="site-header">
    <div class="container header-inner">
      <h1 class="logo">🐉 ManhuaGod</h1>
      <nav class="nav">
        <a href="#" data-view="home">Home</a>
        <a href="#" data-view="popular">Popular</a>
        <a href="#" data-view="latest">Latest</a>
        <a href="#" data-view="top">Top Rated</a>
        <a href="#" data-view="discussions">Discussions</a>
        <a href="#" data-view="profile" id="profile-link">My Profile</a>
      </nav>
    </div>
    <div class="hero container">
      <h2>Discover and read popular manhua</h2>
      <div class="search-row">
        <input id="search" type="search" placeholder="Search manhua, author, genre..." />
      </div>
    </div>
  </header>

  <main class="container">
    <!-- View Navigation Tabs -->
    <div class="view-tabs">
      <button class="view-tab active" data-view="browse">Browse</button>
      <button class="view-tab" data-view="rankings">Rankings</button>
      <button class="view-tab" data-view="reviews">Reviews</button>
      <button class="view-tab" data-view="bookmarks">My Bookmarks</button>
    </div>

    <section class="controls-row">
      <div class="controls">
        <label class="control">
          <span>Genre</span>
          <select id="genreSelect">
            <option value="all">All</option>
            <option value="Action">Action</option>
            <option value="Drama">Drama</option>
            <option value="Romance">Romance</option>
            <option value="Comedy">Comedy</option>
          </select>
        </label>
        <label class="control">
          <span>Status</span>
          <select id="statusSelect">
            <option value="all">All</option>
            <option value="Ongoing">Ongoing</option>
            <option value="Completed">Completed</option>
          </select>
        </label>

        <label class="control">
          <span>Sort</span>
          <select id="sortSelect">
            <option value="popular">Most Popular</option>
            <option value="newest">Newest</option>
            <option value="az">Title A–Z</option>
          </select>
        </label>

        <label class="control">
          <span>View</span>
          <div class="view-toggle" id="viewToggle">
            <button data-view="grid" class="active">Grid</button>
            <button data-view="list">List</button>
          </div>
        </label>

        <label class="control">
          <span>Per page</span>
          <select id="perPageSelect"><option>8</option><option>12</option><option>20</option></select>
        </label>

        <button id="openSettings" class="settings-btn">Settings ⚙️</button>
      </div>
    </section>

    <section id="grid" class="grid"></section>
    <div id="rankings-view" style="display:none;"></div>
    <div id="reviews-view" style="display:none;"></div>
    <div id="bookmarks-view" style="display:none;"></div>
    <div id="discussions-view" style="display:none;"></div>
    <div id="pagination" class="pagination"></div>
  </main>

  <div id="modal" class="modal hidden">
    <div class="modal-content">
      <button id="modalClose" class="modal-close">✕</button>
      <div id="modalBody"></div>
    </div>
  </div>

  <div id="settingsModal" class="modal hidden">
    <div class="modal-content">
      <button id="settingsClose" class="modal-close">✕</button>
      <div style="max-width:640px">
        <h3>Settings</h3>
        <div style="margin:12px 0">
          <label><input type="checkbox" id="themeToggle"/> Use light theme</label>
        </div>
        <div style="margin:12px 0">
          <label><input type="checkbox" id="enableReactions"/> Enable reactions on comments</label>
        </div>
        <div style="margin:12px 0">
          <label>Reaction emojis (comma separated)</label>
          <input id="reactionList" style="width:100%;margin-top:6px;padding:8px;border-radius:6px;border:1px solid rgba(255,255,255,0.04)" placeholder="👍,❤️,😂,😮,😢,🔥" />
        </div>
        <div style="margin:12px 0">
          <label>Display name</label>
          <input id="userNameInput" style="width:100%;margin-top:6px;padding:8px;border-radius:6px;border:1px solid rgba(255,255,255,0.04)" placeholder="Your name (used for comments/reactions)" />
        </div>
        <div style="margin:12px 0;color:var(--muted)">Preferences are saved to localStorage in this demo.</div>
      </div>
    </div>
  </div>

  <footer class="site-footer">
    <div class="container">© ManhuaGod — Demo site. No copyrighted content included.</div>
  </footer>

  <script src="script.js"></script>
</body>
</html>          
