<!DOCTYPE html>
<html lang="zh">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.5, user-scalable=yes">
  <title>汕尾 · 海韵之城 | 旅游推荐</title>
  <!-- 字体与图标库 -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@400;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Quicksand', sans-serif;
      background: #f9fbfd;
      color: #1e2f4e;
      line-height: 1.6;
      scroll-behavior: smooth;
    }

    /* 颜色变量 — 海洋调 */
    :root {
      --deep-blue: #1e3c5c;
      --mid-blue: #2b5797;
      --soft-blue: #6ab0e6;
      --light-wave: #c5e0f4;
      --sand: #f8e3c2;
      --coral: #ff7b6b;
      --white-soft: #f4f8fc;
    }

    /* 通用容器 */
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 2rem 1.5rem;
    }

    /* 头部 */
    header {
      background: rgba(255, 255, 255, 0.9);
      backdrop-filter: blur(8px);
      box-shadow: 0 4px 20px rgba(0, 30, 50, 0.08);
      position: sticky;
      top: 0;
      z-index: 100;
    }

    .header-inner {
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 1rem;
    }

    .logo h1 {
      font-size: 1.9rem;
      font-weight: 700;
      color: var(--deep-blue);
      letter-spacing: 1px;
    }

    .logo span {
      color: var(--coral);
      font-weight: 600;
      font-size: 1rem;
      display: block;
      line-height: 1.2;
    }

    .nav-links {
      display: flex;
      gap: 2rem;
      flex-wrap: wrap;
    }

    .nav-links a {
      text-decoration: none;
      font-weight: 600;
      color: var(--mid-blue);
      font-size: 1.2rem;
      transition: 0.2s;
      border-bottom: 2px solid transparent;
      padding-bottom: 4px;
    }

    .nav-links a:hover {
      border-bottom-color: var(--coral);
      color: var(--deep-blue);
    }

    /* 首页大屏 hero */
    .hero {
      background: linear-gradient(rgba(0, 25, 45, 0.5), rgba(20, 40, 70, 0.4)), url('https://images.unsplash.com/photo-1507525428034-b723cf961d3e?ixlib=rb-4.0.3&auto=format&fit=crop&w=2070&q=80');
      background-size: cover;
      background-position: center 30%;
      min-height: 80vh;
      display: flex;
      align-items: center;
      text-align: center;
      color: white;
    }

    .hero-content {
      max-width: 800px;
      margin: 0 auto;
      padding: 2rem;
      background: rgba(0, 0, 0, 0.2);
      border-radius: 30px;
      backdrop-filter: blur(4px);
    }

    .hero-content h2 {
      font-size: 3.8rem;
      font-weight: 700;
      margin-bottom: 0.5rem;
      text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.3);
    }

    .hero-content p {
      font-size: 1.6rem;
      margin-bottom: 2rem;
      font-weight: 300;
    }

    .btn {
      display: inline-block;
      background: var(--coral);
      color: white;
      font-size: 1.3rem;
      padding: 0.8rem 2.5rem;
      border-radius: 50px;
      text-decoration: none;
      font-weight: 600;
      box-shadow: 0 8px 20px rgba(255, 123, 107, 0.4);
      transition: 0.2s;
      border: none;
      cursor: pointer;
    }

    .btn:hover {
      background: #ff5f4b;
      transform: scale(1.02);
      box-shadow: 0 10px 24px rgba(255, 90, 70, 0.5);
    }

    /* 通用 section 标题 */
    .section-title {
      text-align: center;
      margin-bottom: 3rem;
    }

    .section-title h3 {
      font-size: 2.8rem;
      color: var(--deep-blue);
      position: relative;
      display: inline-block;
    }

    .section-title h3:after {
      content: '';
      display: block;
      width: 80px;
      height: 4px;
      background: var(--coral);
      margin: 0.5rem auto 0;
      border-radius: 4px;
    }

    /* 卡片网格 */
    .card-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 2rem;
      margin-top: 2rem;
    }

    .card {
      background: white;
      border-radius: 28px;
      overflow: hidden;
      box-shadow: 0 15px 30px -12px rgba(0, 50, 80, 0.2);
      transition: transform 0.25s, box-shadow 0.3s;
      display: flex;
      flex-direction: column;
    }

    .card:hover {
      transform: translateY(-10px);
      box-shadow: 0 25px 40px -14px rgba(0, 90, 130, 0.3);
    }

    .card-image {
      width: 100%;
      height: 210px;
      object-fit: cover;
      background-color: #b3d9f0;
    }

    .card-content {
      padding: 1.5rem 1.5rem 1.8rem;
      flex: 1;
      display: flex;
      flex-direction: column;
    }

    .card h4 {
      font-size: 1.9rem;
      font-weight: 700;
      color: var(--deep-blue);
      margin-bottom: 0.5rem;
    }

    .card p {
      color: #2f4057;
      margin-bottom: 1.2rem;
      font-size: 1rem;
      line-height: 1.5;
      flex: 1;
    }

    /* 点赞模块 */
    .like-container {
      display: flex;
      align-items: center;
      gap: 0.8rem;
      margin-top: 0.5rem;
    }

    .like-btn {
      background: none;
      border: none;
      font-size: 1.7rem;
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      transition: 0.1s;
      padding: 0;
      line-height: 1;
    }

    .like-btn i {
      transition: 0.1s;
    }

    .fa-solid.fa-heart {
      color: #e74c3c !important;
    }

    .like-count {
      font-size: 1.3rem;
      font-weight: 600;
      color: #1e3c5c;
    }

    /* 美食小标签 (点缀) */
    .food-tag {
      background: var(--light-wave);
      padding: 0.4rem 1rem;
      border-radius: 50px;
      font-size: 0.9rem;
      font-weight: 600;
      color: var(--deep-blue);
      display: inline-block;
      margin-bottom: 0.8rem;
    }

    /* 联系/关于区 */
    .contact-info {
      background: var(--light-wave);
      border-radius: 48px;
      padding: 3rem 2rem;
      text-align: center;
      margin-top: 2rem;
    }

    .contact-info p {
      font-size: 1.4rem;
      margin: 0.5rem 0;
    }

    .contact-info i {
      color: var(--coral);
      width: 2rem;
    }

    .social-icons {
      margin-top: 2rem;
      font-size: 2.2rem;
      word-spacing: 1.5rem;
    }

    .social-icons a {
      color: var(--deep-blue);
      transition: 0.2s;
    }

    .social-icons a:hover {
      color: var(--coral);
    }

    /* 底部footer */
    footer {
      background: var(--deep-blue);
      color: #d4e6f5;
      text-align: center;
      padding: 1.8rem 1rem;
      font-size: 1.1rem;
    }

    footer #currentYear {
      font-weight: 600;
      color: var(--coral);
    }

    /* 响应式微调 */
    @media (max-width: 680px) {
      .hero-content h2 {
        font-size: 2.8rem;
      }

      .hero-content p {
        font-size: 1.2rem;
      }

      .header-inner {
        flex-direction: column;
        text-align: center;
      }

      .nav-links {
        justify-content: center;
        gap: 1.2rem;
      }
    }

    /* 辅助分隔 */
    hr {
      border: none;
      height: 2px;
      background: linear-gradient(to right, transparent, var(--soft-blue), transparent);
      margin: 0.5rem 0;
    }
  </style>
</head>

<body>

  <header>
    <div class="container header-inner">
      <div class="logo">
        <h1>汕尾·漫游<span>Shanwei · 南海明珠</span></h1>
      </div>
      <nav class="nav-links">
        <a href="#home">首页</a>
        <a href="#attractions">景点</a>
        <a href="#food">美食</a>
        <a href="#contact">遇见汕尾</a>
      </nav>
    </div>
  </header>

  <main>
    <!-- 首页英雄区 (home) -->
    <section id="home" class="hero">
      <div class="hero-content">
        <h2>红海湾 · 慢生活</h2>
        <p>🏖️ 沙滩 · 渔歌 · 鲜美之城</p>
        <a href="#attractions" class="btn">探索汕尾 <i class="fa-solid fa-arrow-down-long"></i></a>
      </div>
    </section>

    <!-- 景点推荐 part -->
    <section id="attractions" class="container">
      <div class="section-title">
        <h3>✨ 必访景点</h3>
        <p>山海交融，古韵今风</p>
      </div>

      <div class="card-grid">
        <!-- 卡片 1: 红海湾 -->
        <div class="card">
          <img class="card-image"
            src="https://images.unsplash.com/photo-1559128010-7c1ad6e1b6a5?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80"
            alt="红海湾浪花" loading="lazy">
          <div class="card-content">
            <h4>红海湾</h4>
            <p>遮浪半岛 · 粤东黄金海岸。一边风平浪静，一边波涛汹涌，感受大自然的神奇分界。</p>
            <div class="like-container">
              <button class="like-btn" aria-label="点赞"><i class="fa-regular fa-heart"></i></button>
              <span class="like-count">128</span>
            </div>
          </div>
        </div>

        <!-- 卡片 2: 玄武山 -->
        <div class="card">
          <img class="card-image"
            src="https://images.unsplash.com/photo-1604537466608-1094bc53e09b?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80"
            alt="玄武山元山寺" loading="lazy">
          <div class="card-content">
            <h4>玄武山</h4>
            <p>碣石镇 · 元山寺祈福。岭南名刹，福星垒塔，登高望海，禅意悠然。</p>
            <div class="like-container">
              <button class="like-btn" aria-label="点赞"><i class="fa-regular fa-heart"></i></button>
              <span class="like-count">95</span>
            </div>
          </div>
        </div>

        <!-- 卡片 3: 凤山妈祖 -->
        <div class="card">
          <img class="card-image"
            src="https://images.unsplash.com/photo-1564769625682-9a4dbb2e6cdd?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80"
            alt="凤山妈祖石像" loading="lazy">
          <div class="card-content">
            <h4>凤山祖庙</h4>
            <p>市区 · 妈祖文化胜地。高达16米的妈祖石像，俯瞰品清湖，庇佑渔人。</p>
            <div class="like-container">
              <button class="like-btn" aria-label="点赞"><i class="fa-regular fa-heart"></i></button>
              <span class="like-count">112</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- 美食推荐 part -->
    <section id="food" class="container">
      <div class="section-title">
        <h3>🦐 古早汕尾味</h3>
        <p>从清晨的一碗海鲜粥开始</p>
      </div>

      <div class="card-grid">
        <!-- 美食1: 薄饼 -->
        <div class="card">
          <img class="card-image"
            src="https://images.unsplash.com/photo-1604904612712-6c9e4a140b4b?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80"
            alt="汕尾薄饼" loading="lazy">
          <div class="card-content">
            <span class="food-tag"><i class="fa-regular fa-clock"></i> 特色小吃</span>
            <h4>薄饼</h4>
            <p>咸香酥脆，甜糯缠绵。现烙饼皮裹着叉烧、豆芽、糖葱，一口沦陷。</p>
            <div class="like-container">
              <button class="like-btn" aria-label="点赞"><i class="fa-regular fa-heart"></i></button>
              <span class="like-count">76</span>
            </div>
          </div>
        </div>
        <!-- 美食2: 牛肉丸 -->
        <div class="card">
          <img class="card-image"
            src="https://images.unsplash.com/photo-1603048588665-791ca8aea617?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80"
            alt="汕尾牛肉丸" loading="lazy">
          <div class="card-content">
            <span class="food-tag"><i class="fa-regular fa-clock"></i> 地道肉丸</span>
            <h4>牛肉丸 · 牛杂</h4>
            <p>手打牛肉丸弹牙爆汁，搭配本地秘制沙茶，再喝一口牛杂汤，舒坦。</p>
            <div class="like-container">
              <button class="like-btn" aria-label="点赞"><i class="fa-regular fa-heart"></i></button>
              <span class="like-count">101</span>
            </div>
          </div>
        </div>
        <!-- 美食3: 晨洲蚝 -->
        <div class="card">
          <img class="card-image"
            src="https://images.unsplash.com/photo-1582965072789-4c9cbfb3e43c?ixlib=rb-4.0.3&auto=format&fit=crop&w=800&q=80"
            alt="晨洲生蚝" loading="lazy">
          <div class="card-content">
            <span class="food-tag"><i class="fa-regular fa-star"></i> 海中牛奶</span>
            <h4>晨洲蚝</h4>
            <p>晨洲村养蚝历史百年，肥美无渣，可炭烤、酥炸或做成蚝烙，鲜甜入魂。</p>
            <div class="like-container">
              <button class="like-btn" aria-label="点赞"><i class="fa-regular fa-heart"></i></button>
              <span class="like-count">88</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- 联系/关于板块 (contact) 并嵌入一点互动信息 -->
    <section id="contact" class="container">
      <div class="section-title">
        <h3>🗺️ 遇见·善美汕尾</h3>
        <p>每一帧都是南海的风</p>
      </div>

      <div class="contact-info">
        <p><i class="fa-regular fa-compass"></i> 汕尾市城区 · 海滨大道 渔歌广场</p>
        <p><i class="fa-regular fa-envelope"></i> visit@shanwei.travel</p>
        <p><i class="fa-regular fa-sun"></i> 最佳旅行季：十月至次年四月</p>
        <hr style="width: 60%; margin: 2rem auto;">
        <p style="font-size: 1.2rem;">关注我们，获取更多浪花瞬间</p>
        <div class="social-icons">
          <a href="#"><i class="fa-brands fa-weixin"></i></a>
          <a href="#"><i class="fa-brands fa-weibo"></i></a>
          <a href="#"><i class="fa-brands fa-xiaohongshu"></i></a>
          <a href="#"><i class="fa-brands fa-tiktok"></i></a>
        </div>
      </div>
    </section>
  </main>

  <!-- 底部footer 包含动态年份 -->
  <footer>
    <p>🌊 南海渔韵 · 广东汕尾 | <span id="currentYear"></span> 慢游指南</p>
    <p style="font-size: 0.9rem; opacity: 0.8;">所有图片仅作展示，感受真实汕尾</p>
  </footer>

  <!-- JavaScript 交互: 点赞 + 动态年份 -->
  <script>
    (function () {
      // 设置页脚当前年份
      const yearSpan = document.getElementById('currentYear');
      if (yearSpan) {
        yearSpan.textContent = new Date().getFullYear();
      }

      // 点赞功能 —— 使用事件委托 (避免重复绑定，且能处理动态新增，不过这里没有新增)
      document.body.addEventListener('click', function (e) {
        // 找到被点击的按钮 (like-btn)
        const likeBtn = e.target.closest('.like-btn');
        if (!likeBtn) return; // 不是点赞按钮则退出

        // 防止按钮默认或冒泡干扰
        e.preventDefault();

        // 获取当前按钮所在的like-container
        const container = likeBtn.closest('.like-container');
        if (!container) return;

        // 计数span
        const countSpan = container.querySelector('.like-count');
        if (!countSpan) return;

        // 更新数字 +1
        let current = parseInt(countSpan.innerText, 10);
        // 简单防非数字
        if (isNaN(current)) current = 0;
        countSpan.innerText = current + 1;

        // 改变心形图标为实心红色 (fa-regular -> fa-solid)
        const icon = likeBtn.querySelector('i');
        if (icon) {
          icon.classList.remove('fa-regular');
          icon.classList.add('fa-solid');
          // 颜色已在CSS中设置 .fa-solid.fa-heart {color:#e74c3c}
        }
      });

      // 额外小点缀: 控制台欢迎语 (可忽略)
      console.log('🐚 欢迎来汕尾 ~ 海风已经在召唤');
    })();
  </script>

  <!-- 平滑滚动后备 (已写在css, 但确保兼容) -->
</body>

</html>
