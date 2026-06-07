<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Chen Zhao · GitHub 主页</title>
    <!-- 使用现代、干净的字体，提升可读性与美观度 -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,500;14..32,600;14..32,700&display=swap" rel="stylesheet">
    <!-- 可选：简单的 Font Awesome 6 (免费图标库) 丰富视觉 -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(145deg, #f9fafc 0%, #f1f5f9 100%);
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 2rem 1rem;
        }

        /* 主卡片风格 — 干净、现代、轻微玻璃态 */
        .github-card {
            max-width: 880px;
            width: 100%;
            background: rgba(255,255,255,0.96);
            backdrop-filter: blur(0px);
            border-radius: 2rem;
            box-shadow: 0 20px 35px -12px rgba(0,0,0,0.1), 0 1px 2px rgba(0,0,0,0.02);
            overflow: hidden;
            transition: transform 0.2s ease, box-shadow 0.2s ease;
            border: 1px solid rgba(255,255,255,0.5);
        }

        .github-card:hover {
            transform: translateY(-3px);
            box-shadow: 0 28px 40px -16px rgba(0,0,0,0.15);
        }

        /* 头部区域 */
        .profile-header {
            padding: 2rem 2rem 1.2rem 2rem;
            text-align: center;
            background: linear-gradient(135deg, #ffffff 0%, #fef9f0 100%);
            border-bottom: 1px solid #eef2f6;
        }

        .avatar-placeholder {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 96px;
            height: 96px;
            background: linear-gradient(135deg, #1e2b3c, #2c4c6e);
            border-radius: 50%;
            box-shadow: 0 10px 18px -6px rgba(0,0,0,0.2);
            margin-bottom: 1rem;
            transition: all 0.2s;
        }

        .avatar-placeholder i {
            font-size: 3.4rem;
            color: white;
            filter: drop-shadow(0 2px 4px rgba(0,0,0,0.1));
        }

        .profile-header h1 {
            font-size: 2.2rem;
            font-weight: 700;
            letter-spacing: -0.01em;
            background: linear-gradient(120deg, #1f3b4c, #2b5f8a);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            margin-bottom: 0.25rem;
        }

        .wave {
            display: inline-block;
            animation: waveAnim 1.2s ease-in-out infinite;
            transform-origin: 70% 70%;
        }

        @keyframes waveAnim {
            0% { transform: rotate(0deg); }
            20% { transform: rotate(14deg); }
            40% { transform: rotate(-8deg); }
            60% { transform: rotate(10deg); }
            80% { transform: rotate(-2deg); }
            100% { transform: rotate(0deg); }
        }

        .tagline {
            font-size: 1rem;
            color: #4b6a85;
            margin-top: 0.5rem;
            font-weight: 500;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
            flex-wrap: wrap;
        }

        .tagline i {
            color: #2c6b9e;
            font-size: 0.9rem;
        }

        /* 主要内容区 */
        .profile-content {
            padding: 1.8rem 2rem 2rem 2rem;
        }

        /* 关于我部分 */
        .section {
            margin-bottom: 2rem;
        }

        .section-title {
            font-size: 1.35rem;
            font-weight: 600;
            color: #1e2f3c;
            display: flex;
            align-items: center;
            gap: 0.65rem;
            border-left: 4px solid #2c7cb6;
            padding-left: 1rem;
            margin-bottom: 1.25rem;
        }

        .section-title i {
            color: #2c7cb6;
            font-size: 1.3rem;
        }

        .about-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 1.25rem;
            background: #f8fafd;
            border-radius: 1.5rem;
            padding: 1.4rem 1.6rem;
            border: 1px solid #e6edf4;
        }

        .info-item {
            flex: 1;
            min-width: 180px;
            display: flex;
            align-items: center;
            gap: 0.75rem;
            font-size: 1rem;
            color: #1e3a5f;
        }

        .info-item i {
            width: 2rem;
            font-size: 1.35rem;
            color: #2c7cb6;
            text-align: center;
        }

        .info-item strong {
            font-weight: 600;
            color: #0f2c3f;
        }

        .info-item span {
            color: #2c4c6e;
        }

        .badge-container {
            display: flex;
            flex-wrap: wrap;
            gap: 0.75rem;
            margin-top: 0.5rem;
        }

        .badge {
            background: white;
            border-radius: 60px;
            padding: 0.3rem 1rem;
            font-size: 0.8rem;
            font-weight: 500;
            box-shadow: 0 1px 2px rgba(0,0,0,0.03);
            border: 1px solid #dce5ec;
            color: #1e4663;
            transition: all 0.15s;
        }

        .badge i {
            margin-right: 6px;
            font-size: 0.75rem;
        }

        .badge:hover {
            background: #eef4fa;
            border-color: #bdd4e8;
            transform: translateY(-1px);
        }

        /* 个人主页卡片风格 */
        .website-card {
            background: linear-gradient(110deg, #eef5fc 0%, #ffffff 100%);
            border-radius: 1.5rem;
            padding: 1.2rem 1.5rem;
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 1rem;
            border: 1px solid #dfe9f2;
            margin-bottom: 1.8rem;
            transition: all 0.2s;
        }

        .website-info {
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .website-icon {
            background: #1f4662;
            width: 48px;
            height: 48px;
            border-radius: 28px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.5rem;
            box-shadow: 0 6px 12px -6px rgba(0,0,0,0.2);
        }

        .website-text h3 {
            font-size: 1.2rem;
            font-weight: 600;
            color: #1b3b4f;
        }

        .website-text p {
            font-size: 0.85rem;
            color: #4f6f8c;
        }

        .btn-website {
            background: #1f4662;
            color: white;
            padding: 0.6rem 1.3rem;
            border-radius: 40px;
            text-decoration: none;
            font-weight: 500;
            font-size: 0.9rem;
            transition: 0.2s;
            display: inline-flex;
            align-items: center;
            gap: 8px;
            border: none;
            cursor: pointer;
            box-shadow: 0 2px 6px rgba(0,0,0,0.05);
        }

        .btn-website:hover {
            background: #123a52;
            transform: scale(0.98);
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }

        /* 建设中区域 */
        .building {
            background: #fef9e6;
            border-radius: 1.2rem;
            padding: 1rem 1.5rem;
            display: flex;
            align-items: center;
            gap: 1rem;
            flex-wrap: wrap;
            justify-content: space-between;
            border-left: 5px solid #f5b042;
            margin-top: 0.75rem;
        }

        .building-message {
            display: flex;
            align-items: center;
            gap: 12px;
            font-weight: 500;
            color: #ad7a2b;
        }

        .building-message i {
            font-size: 1.6rem;
        }

        .progress-indicator {
            background: #e9e0ce;
            border-radius: 40px;
            height: 8px;
            width: 160px;
            overflow: hidden;
        }

        .progress-fill {
            width: 68%;
            height: 100%;
            background: linear-gradient(90deg, #f5b042, #f0a02a);
            border-radius: 40px;
        }

        /* 脚注社交链接 */
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-top: 2rem;
            padding-top: 1rem;
            border-top: 1px solid #e2e9f0;
        }

        .social-icon {
            color: #3f627f;
            font-size: 1.5rem;
            transition: 0.2s;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            text-decoration: none;
            font-size: 1rem;
            font-weight: 500;
            background: #f0f4f9;
            padding: 0.4rem 1rem;
            border-radius: 60px;
        }

        .social-icon i {
            font-size: 1.2rem;
        }

        .social-icon:hover {
            background: #e3ecf3;
            color: #1f4b6e;
            transform: translateY(-2px);
        }

        /* 响应式 */
        @media (max-width: 620px) {
            .profile-header {
                padding: 1.5rem;
            }
            .profile-content {
                padding: 1.5rem;
            }
            .about-grid {
                flex-direction: column;
                gap: 0.8rem;
            }
            .website-card {
                flex-direction: column;
                align-items: flex-start;
            }
            .social-links {
                flex-wrap: wrap;
            }
            .section-title {
                font-size: 1.2rem;
            }
        }
        
        /* 小点缀 */
        .dot-pulse {
            display: inline-block;
            width: 6px;
            height: 6px;
            border-radius: 50%;
            background-color: #f5b042;
            box-shadow: 0 0 0 0 #f5b042;
            animation: pulse-dot 1.2s infinite;
            margin-left: 6px;
        }
        
        @keyframes pulse-dot {
            0% { transform: scale(0.8); opacity: 0.6;}
            70% { transform: scale(1.2); opacity: 1;}
            100% { transform: scale(0.8); opacity: 0.6;}
        }

        footer {
            text-align: center;
            font-size: 0.7rem;
            padding: 1rem 2rem 1.2rem;
            color: #6b8a9e;
            background: #fafcff;
            border-top: 1px solid #ecf3f9;
        }
    </style>
</head>
<body>
<div class="github-card">
    <div class="profile-header">
        <div class="avatar-placeholder">
            <i class="fas fa-code"></i>
        </div>
        <h1>
            Hi 👋, I'm Chen Zhao
            <span class="wave">👨‍💻</span>
        </h1>
        <div class="tagline">
            <i class="fas fa-map-marker-alt"></i> 
            <span>Digital Creator · 全栈爱好者 · 探索无限可能</span>
            <span class="dot-pulse"></span>
        </div>
    </div>

    <div class="profile-content">
        <!-- 🚀 About Me 区域，精致现代 -->
        <div class="section">
            <div class="section-title">
                <i class="fas fa-user-astronaut"></i>
                <span>✦ 关于我 / About Me</span>
            </div>
            <div class="about-grid">
                <div class="info-item">
                    <i class="fas fa-globe"></i>
                    <div><strong>🌐 个人主页</strong><br><span>czhao.xyz</span></div>
                </div>
                <div class="info-item">
                    <i class="fas fa-rocket"></i>
                    <div><strong>🚀 当前状态</strong><br><span>持续创作 · 构建数字花园</span></div>
                </div>
                <div class="info-item">
                    <i class="fas fa-heart" style="color:#d45b6a;"></i>
                    <div><strong>💡 热爱领域</strong><br><span>Web开发 · 开源 · 交互设计</span></div>
                </div>
                <div class="info-item">
                    <i class="fas fa-coffee"></i>
                    <div><strong>⚡ 日常</strong><br><span>写码 · 阅读 · 探索新技术</span></div>
                </div>
            </div>
        </div>

        <!-- 特色标签 / 技能组 -->
        <div class="section">
            <div class="section-title">
                <i class="fas fa-cubes"></i>
                <span>🛠️ 技术栈 & 兴趣</span>
            </div>
            <div class="badge-container">
                <span class="badge"><i class="fab fa-js"></i> JavaScript/TS</span>
                <span class="badge"><i class="fab fa-react"></i> React & Next.js</span>
                <span class="badge"><i class="fab fa-python"></i> Python</span>
                <span class="badge"><i class="fas fa-database"></i> Node.js</span>
                <span class="badge"><i class="fab fa-github"></i> Git & CI/CD</span>
                <span class="badge"><i class="fas fa-palette"></i> UI/UX 灵感</span>
                <span class="badge"><i class="fas fa-cloud"></i> 云原生概念</span>
            </div>
        </div>

        <!-- 个人主页模块 重点展示 -->
        <div class="website-card">
            <div class="website-info">
                <div class="website-icon">
                    <i class="fas fa-house-chimney"></i>
                </div>
                <div class="website-text">
                    <h3>✨ 个人数字空间 · Chen Zhao ✨</h3>
                    <p>作品集 · 技术笔记 · 思考沉淀</p>
                </div>
            </div>
            <a href="https://czhao.xyz" target="_blank" rel="noopener noreferrer" class="btn-website">
                <i class="fas fa-arrow-up-right-from-square"></i> 访问主页
            </a>
        </div>

        <!-- 持续建设中的动态卡片 - 更有趣的展示 -->
        <div class="building">
            <div class="building-message">
                <i class="fas fa-hard-hat"></i>
                <span><strong>🚧 持续建设中 · Construction in Progress</strong></span>
                <i class="fas fa-spinner fa-pulse"></i>
            </div>
            <div class="progress-indicator">
                <div class="progress-fill"></div>
            </div>
            <div style="font-size:0.75rem; color:#a08654;">
                更多精彩内容即将呈现 ✨
            </div>
        </div>

        <!-- 额外小模块：最新动态或 Quote，给人活跃印象 -->
        <div class="section" style="margin-top: 0.5rem;">
            <div class="section-title">
                <i class="fas fa-newspaper"></i>
                <span>📌 最近旅程</span>
            </div>
            <div style="background:#ffffff; border-radius:1.2rem; padding:0.6rem 0 0.2rem 0;">
                <div style="display:flex; align-items: center; gap:12px; flex-wrap:wrap; justify-content: space-between;">
                    <div style="display: flex; gap: 1rem; flex-wrap: wrap;">
                        <span style="background:#eef2f7; padding: 0.3rem 0.9rem; border-radius:40px; font-size:0.8rem;"><i class="far fa-calendar-alt"></i> 2026 重构主页体验</span>
                        <span style="background:#eef2f7; padding: 0.3rem 0.9rem; border-radius:40px; font-size:0.8rem;"><i class="fas fa-code-branch"></i> 开源贡献进行时</span>
                        <span style="background:#eef2f7; padding: 0.3rem 0.9rem; border-radius:40px; font-size:0.8rem;"><i class="fas fa-mug-hot"></i> 博客计划 · 技术深思</span>
                    </div>
                    <div style="font-size:0.8rem; color:#2c7cb6;">
                        <i class="fas fa-sync-alt"></i> 不断迭代中...
                    </div>
                </div>
            </div>
        </div>

        <!-- 社交链接，让你主页更有连接性，虽然 GitHub profile 常用但美观 -->
        <div class="social-links">
            <a href="https://github.com/ChenZhao" class="social-icon" target="_blank" rel="noopener noreferrer"><i class="fab fa-github"></i> GitHub</a>
            <a href="#" class="social-icon" target="_blank" rel="noopener noreferrer"><i class="fab fa-twitter"></i> Twitter</a>
            <a href="#" class="social-icon" target="_blank" rel="noopener noreferrer"><i class="fab fa-linkedin-in"></i> LinkedIn</a>
            <a href="mailto:hello@czhao.xyz" class="social-icon"><i class="far fa-envelope"></i> 邮件</a>
        </div>
        
        <!-- 小脚注 优雅提示 -->
        <footer>
            <i class="fas fa-laptop-code"></i> 保持好奇 · 终身学习 · 代码构建未来  
            <span style="display:inline-block; margin-left:8px;">✨ czhao.xyz 持续丰富中 ✨</span>
        </footer>
    </div>
</div>

<!-- 可选：增加简单 hover 效果交互，或者保持原样即可 -->
</body>
</html>
