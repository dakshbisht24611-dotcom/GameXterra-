<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>GameXterra | Gaming Hub</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    body {
      background-color: #0b0e14;
      color: #e2e8f0;
      line-height: 1.6;
    }

    header {
      background-color: #131823;
      padding: 1rem 5%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 2px solid #7c3aed;
      position: sticky;
      top: 0;
      z-index: 100;
    }

    .logo {
      font-size: 1.6rem;
      font-weight: 800;
      color: #fff;
      letter-spacing: 1px;
    }

    .logo span {
      color: #8b5cf6;
    }

    nav a {
      color: #cbd5e1;
      text-decoration: none;
      margin-left: 1.5rem;
      font-weight: 600;
      transition: color 0.3s;
    }

    nav a:hover {
      color: #8b5cf6;
    }

    .hero {
      text-align: center;
      padding: 5rem 1.5rem;
      background: linear-gradient(135deg, #1e1b4b 0%, #0b0e14 100%);
    }

    .hero h1 {
      font-size: 2.8rem;
      margin-bottom: 1rem;
      color: #fff;
    }

    .hero p {
      font-size: 1.1rem;
      color: #94a3b8;
      max-width: 600px;
      margin: 0 auto 2rem;
    }

    .btn {
      display: inline-block;
      background-color: #7c3aed;
      color: #fff;
      padding: 0.8rem 2rem;
      border-radius: 6px;
      text-decoration: none;
      font-weight: bold;
      transition: background 0.3s;
    }

    .btn:hover {
      background-color: #6d28d9;
    }

    .container {
      max-width: 1100px;
      margin: 3rem auto;
      padding: 0 1.5rem;
    }

    .section-title {
      font-size: 1.8rem;
      margin-bottom: 1.5rem;
      border-left: 4px solid #8b5cf6;
      padding-left: 0.8rem;
    }

    .filters {
      margin-bottom: 1.5rem;
      display: flex;
      gap: 0.6rem;
      flex-wrap: wrap;
    }

    .filter-btn {
      background: #1e293b;
      color: #e2e8f0;
      border: 1px solid #334155;
      padding: 0.5rem 1rem;
      border-radius: 20px;
      cursor: pointer;
      font-weight: 600;
    }

    .filter-btn.active, .filter-btn:hover {
      background: #7c3aed;
      border-color: #7c3aed;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 1.5rem;
    }

    .card {
      background-color: #131823;
      border: 1px solid #1e293b;
      border-radius: 10px;
      overflow: hidden;
      transition: transform 0.2s;
    }

    .card:hover {
      transform: translateY(-5px);
      border-color: #8b5cf6;
    }

    .card-banner {
      height: 150px;
      background: linear-gradient(45deg, #312e81, #4c1d95);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 2.5rem;
    }

    .card-body {
      padding: 1.2rem;
    }

    .tag {
      font-size: 0.75rem;
      background: #2e1065;
      color: #c4b5fd;
      padding: 0.2rem 0.6rem;
      border-radius: 4px;
      text-transform: uppercase;
      font-weight: bold;
    }

    .card h3 {
      margin: 0.6rem 0;
      color: #fff;
    }

    .card p {
      font-size: 0.9rem;
      color: #94a3b8;
      margin-bottom: 1rem;
    }

    footer {
      text-align: center;
      padding: 2rem;
      background-color: #131823;
      color: #64748b;
      margin-top: 4rem;
      border-top: 1px solid #1e293b;
    }
  </style>
</head>
<body>

  <header>
    <div class="logo">Game<span>Xterra</span></div>
    <nav>
      <a href="#games">Games</a>
      <a href="#news">News</a>
    </nav>
  </header>

  <section class="hero">
    <h1>Welcome to GameXterra</h1>
    <p>Your destination for browser games, top reviews, and the latest gaming updates.</p>
    <a href="#games" class="btn">Explore Games</a>
  </section>

  <div class="container" id="games">
    <h2 class="section-title">Featured Games</h2>

    <div class="filters">
      <button class="filter-btn active" onclick="filterGames('all', this)">All</button>
      <button class="filter-btn" onclick="filterGames('action', this)">Action</button>
      <button class="filter-btn" onclick="filterGames('rpg', this)">RPG</button>
      <button class="filter-btn" onclick="filterGames('arcade', this)">Arcade</button>
    </div>

    <div class="grid" id="game-grid">
      <div class="card" data-category="action">
        <div class="card-banner">⚔️</div>
        <div class="card-body">
          <span class="tag">Action</span>
          <h3>Cyber Strike</h3>
          <p>Fast-paced futuristic shooter set in a neon metropolis.</p>
          <a href="#" class="btn">Play Now</a>
        </div>
      </div>

      <div class="card" data-category="rpg">
        <div class="card-banner">🐉</div>
        <div class="card-body">
          <span class="tag">RPG</span>
          <h3>Shadow Realms</h3>
          <p>Explore vast dungeons, collect loot, and defeat ancient bosses.</p>
          <a href="#" class="btn">Play Now</a>
        </div>
      </div>

      <div class="card" data-category="arcade">
        <div class="card-banner">🚀</div>
        <div class="card-body">
          <span class="tag">Arcade</span>
          <h3>Star Blaster</h3>
          <p>Classic space survival shooter with endless wave challenges.</p>
          <a href="#" class="btn">Play Now</a>
        </div>
      </div>
    </div>
  </div>

  <div class="container" id="news">
    <h2 class="section-title">Latest Updates</h2>
    <div class="card">
      <div class="card-body">
        <span class="tag">Announcement</span>
        <h3>GameXterra Launches Online!</h3>
        <p>Stay tuned as we add playable mini-games, leaderboards, and community reviews every week.</p>
      </div>
    </div>
  </div>

  <footer>
    <p>&copy; 2026 GameXterra. All rights reserved.</p>
  </footer>

  <script>
    function filterGames(category, btn) {
      document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
      btn.classList.add('active');

      document.querySelectorAll('#game-grid .card').forEach(card => {
        if (category === 'all' || card.dataset.category === category) {
          card.style.display = 'block';
        } else {
          card.style.display = 'none';
        }
      });
    }
  </script>

</body>
</html>
