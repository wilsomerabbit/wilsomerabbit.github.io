---
title:
date: 2026-02-12
type: "index"
comments: false
---

<!-- 自我介紹區 -->
<div class="section-block about-section">
  <div class="about-content">
    <div class="about-left">
      <div class="about-intro">
        <div class="about-text">
          <h2>Aurora</h2>
          <p class="about-tagline">@Rebecca_0411</p>
        </div>
      </div>
      <p class="about-desc">
        🐢嗨！我是 Aurora，歡迎來到我的小空間。🐢<br>
        有的時候會寫程式、玩西洋棋。<br>
        偶爾也會開發一些有趣的專案。<br>
        頭貼跟名字常換，可能會找不到我:D
      </p>
    </div>
    <div class="about-right">
      <img src="/img/about-side.jpg" class="about-side-img" alt="" />
    </div>
  </div>
</div>

<hr class="section-divider" />

<!-- Project 大分類 -->
<div class="section-block project-section">
  <h2 class="section-title"><i class="fas fa-code" style="color:#3b82f6"></i> Project</h2>
  <p class="section-subtitle"></p>

  <!-- Discord 機器人區 -->
  <div class="project-item bot-section">
    <h3 class="project-item-title"><i class="fab fa-discord" style="color:#5865F2"></i> Discord Bot</h3>
    <p class="section-subtitle">這裡放一些我寫的dc機器人</p>
  <div class="bot-layout">
    <div class="discord-invite-card">
      <div class="discord-invite-header">Invite to join</div>
      <div class="discord-invite-body">
        <img src="img/discord-avatar.jpg" class="discord-invite-avatar" alt="千早愛音" />
        <div class="discord-invite-info">
          <div class="discord-invite-name">千早愛音</div>
          <div class="discord-invite-status">
            <span class="status-dot online"></span> Online
          </div>
        </div>
      </div>
      <a href="https://discord.com/oauth2/authorize?client_id=1468680591145828362" class="discord-invite-join" target="_blank">Join</a>
    </div>
    <div class="bot-description">
      <div class="bot-feature-card">
        <div class="bot-feature-title">MyGo圖搜尋機器人</div>
        <div class="bot-feature-item">
          <span>支援 /random 隨機抽選圖片功能</span>
        </div>
      </div>
      <a href="#" class="bot-doc-link" target="_blank"><i class="fas fa-book"></i> 點我進入 千早愛音Bot使用說明</a>
    </div>
  </div>
  </div>
</div>

<hr class="section-divider" />

<!-- 西洋棋區 -->
<div class="section-block chess-section">
  <h2 class="section-title"><i class="fas fa-chess" style="color:#769656"></i> Chess</h2>
  <p class="section-subtitle">My chess profile</p>
  <a href="https://www.chess.com/member/wilsome" class="chess-banner-link" target="_blank">
    <img src="/img/chess-profile.png" class="chess-banner-img" alt="Chess.com Profile" />
  </a>
  <div class="chess-info">
    <div class="chess-rating-card">
      <div class="chess-rating-label"><i class="fas fa-clock"></i> Rapid Rating</div>
      <div class="chess-rating-value" id="chess-rapid-rating">載入中...</div>
    </div>
    <p class="chess-desc">點圖片可以跳轉到我的chess.com介面，有在玩的歡迎加好友！</p>
  </div>
</div>

<script>
fetch('https://api.chess.com/pub/player/wilsome/stats')
  .then(r => r.json())
  .then(data => {
    const el = document.getElementById('chess-rapid-rating');
    if (data.chess_rapid && data.chess_rapid.last) {
      el.textContent = data.chess_rapid.last.rating;
    } else {
      el.textContent = 'N/A';
    }
  })
  .catch(() => {
    document.getElementById('chess-rapid-rating').textContent = 'N/A';
  });
</script>

<hr class="section-divider" />

<!-- 請我喝杯拿鐵（贊助區） -->
<div class="section-block sponsor-section">
  <a href="#" class="sponsor-title-link" target="_blank">
    <h2 class="section-title"><i class="fas fa-mug-hot" style="color:#ef4444"></i> 請我喝杯拿鐵↗</h2>
  </a>
  <p class="sponsor-desc">如果你喜歡我的內容或專案，可以請我喝杯拿鐵來支持我繼續創作！</p>
  <a href="#" class="sponsor-banner-link" target="_blank">
    <img src="/img/sponsor-banner.jpg" class="sponsor-banner-img" alt="贊助" />
  </a>
  <p class="sponsor-hint">點圖片可以進入贊助連結</p>
</div>
