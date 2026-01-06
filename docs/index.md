---
layout: blank
---

<head>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        *{margin:0; padding:0; box-sizing:border-box; transition:all 0.3s}
        .container{max-width:480px; width:100%}
        body{
            font-family:'Inter',sans-serif;
            line-height:1.6;
            padding:20px;
            min-height:100vh;
            display:flex;
            justify-content:center;
            align-items:center;
        }
        a{text-decoration:none !important; color:inherit}
        a:hover{text-decoration:none !important}
        .theme-toggle{
            position:fixed;
            top:20px;
            right:20px;
            border:none;
            width:50px; 
            height:50px;
            border-radius:50%;
            cursor:pointer;
            display:flex;
            align-items:center;
            justify-content:center;
            font-size:1.2rem;
            z-index:100;
            backdrop-filter:blur(6px)
        }
        .theme-toggle:hover{transform:scale(1.1)}
        .footer{
            text-align:center;
            margin-top:30px;
            opacity:0.7;
            font-size:0.9rem
        }
        .profile-card{
            border-radius:20px;
            padding:30px;
            text-align:center;
            backdrop-filter:blur(16px);
            margin-bottom:16px;
        }
        .profile-img{
            width:160px;
            height:160px;
            border-radius:50%;
            object-fit:cover;
            margin:0 auto 10px;
        }
        .profile-name{font-size:1.8rem; font-weight:700; margin-bottom:4px}
        .profile-bio{font-size:1rem; opacity:0.8; max-width:95%; margin:0 auto}
        .social-links{display:flex; justify-content:center; gap:15px; margin-top:20px}
        .icon-mask{
            width: 24px;
            height: 24px;
            mask: var(--icon-url) no-repeat center;
            mask-size: contain;
        }
        .social-icon{
            width:45px;
            height:45px;
            border-radius:50%;
            display:flex;
            align-items:center;
            justify-content:center;
            font-size:1.4rem;
        }
        .social-icon:hover{transform:translateY(-3px);}
        .link-container{
            display:flex;
            flex-direction:column;
            gap:16px;
        }
        .link-content{flex:1;text-align:left}
        .link-title{font-weight:600; font-size:1.1rem; margin-bottom:4px}
        .link-description{font-size:0.9rem; opacity:0.7}
        .link-item{
            border-radius:16px;
            padding:18px 24px;
            display:flex;
            align-items:center;
            border:1px solid rgba(255,255,255,0.1);
            backdrop-filter:blur(10px)
        }
        .link-item:hover{
            border-color:var(--brand-color);
            transform:translateX(12px);
            .link-mask{
                width:42px;
                height:42px;
            }
        }
        .link-icon{
            width:42px;
            height:42px;
            margin-right:24px;
            display:flex;
            align-items:center;
            justify-content:center;
            font-size:1.2rem;
        }
        .link-mask{
            width: 32px;
            height: 32px;
            mask: var(--icon-url) no-repeat center;
            mask-size: contain;
            background:var(--brand-color);
        }
        /* Dark Theme */
        body{
            color:#d2d2d2;
            background-color: #121212;
            &::before{background:url("https://github.com/AmyMialee/AmyMialee/blob/main/docs/checkerdark.png?raw=true")repeat;}
            .theme-toggle{background:rgba(255,255,255,0.2); color:rgb(234,198,73)}
            .theme-toggle:hover{background:rgba(255,255,255,0.2)}
            .profile-card{
                background:rgba(60,60,60,0.15);
                border:1px solid rgba(255,255,255,0.1);
                box-shadow:0 10px 30px rgba(0,0,0,0.48);
            }
            .profile-img{
                border:4px solid rgba(255,255,255,0.2);
                background:rgba(42,42,42,0.5)
            }
            .profile-name{color:#d8d8d8}
            .social-icon{
                background:rgba(255,255,255,0.075);
                box-shadow:0 4px 8px rgba(0,0,0,0.2);
                color:#717b7f
            }
            .social-icon:hover{
                background-color:var(--brand-color);
                color:white;
                .icon-mask{background-color:white}
            }
            .icon-mask{background:#717b7f}
            .link-item{
                color:#d2d2d2 !important;
                background:rgba(60,60,60,0.15);
                border:1px solid rgba(255,255,255,0.1);
                box-shadow:0 10px 30px rgba(0,0,0,0.48);
                border-left:4px solid var(--brand-color);
            }
            .link-item:hover{background:rgba(60,60,60,0.45)}
        }
        /* Light Theme */
        body.light{
            color:#0b0020;
            background-color: #9073C7;
            &::before{background:url("https://github.com/AmyMialee/AmyMialee/blob/main/docs/checker.png?raw=true")repeat;}
            .theme-toggle{background:rgba(61,61,61,0.2); color:rgb(57,57,57)}
            .theme-toggle:hover{background:rgba(255,255,255,0.2)}
            .profile-card{
                background:rgba(255,255,255,0.15);
                border:1px solid rgba(0,0,0,0.1);
                box-shadow:0 10px 30px rgba(0,0,0,0.24);
            }
            .profile-img{
                border:4px solid rgb(240,244,255,0.2);
                background:rgba(239,239,239,0.5)
            }
            .profile-name{color:#373737}
            .social-icon{
                background:rgba(255,255,255,0.2);
                box-shadow:0 4px 8px rgba(0,0,0,0.075);
                color:#495154
            }
            .social-icon:hover{
                background-color:var(--brand-color);
                color:white;
                .icon-mask{background-color:white}
            }
            .icon-mask{background:#495154}
            .link-item{
                color:#0b0020 !important;
                background:rgba(255,255,255,0.15);
                border:1px solid rgba(0,0,0,0.1);
                box-shadow:0 10px 30px rgba(0,0,0,0.24);
                border-left:4px solid var(--brand-color);
            }
            .link-item:hover{background:rgba(255,255,255,0.45)}
        }
        /* Animated Scroll */
        @keyframes bgScroll {
            from { background-position: 0 0; }
            to { background-position: 120px 120px; }
        }
        body::before {
            content: "";
            position: fixed;
            top: -150%;
            left: -150%;
            width: 300%;
            height: 300%;
            z-index: -1;
            transform: rotate(10deg);
            animation: bgScroll 6s linear infinite;
            pointer-events: none;
        }
        /* Open Animation */
        @keyframes fadeInUp{from{transform:translateX(20px)}to{transform:translateX(0)}}
        .container{animation:fadeInUp 4.5s ease forwards}
        /* Thin Screen Adjustment */
        @media(max-width:500px){.profile-card{padding:20px}.link-item{padding:16px 20px}body{padding:15px}}
    </style>
</head>
<body>
    <button class="theme-toggle" id="themeToggle" title="Toggle Dark/Light Theme"><i class="fas fa-sun"></i></button>
    <div class="container">
        <div class="profile-card">
            <img src="https://avatars.githubusercontent.com/u/10999535?v=4?ixlib=rb-4.0.3&auto=format&fit=crop&w=774&q=80" alt="Profile Picture" class="profile-img">
            <h1 class="profile-name">AmyMialee</h1>
            <p class="profile-bio">Games Development Graduate and Modder</p>
            <div class="social-links">
                <a href="https://www.patreon.com/cw/AmyMialee" class="social-icon" target="_blank" title="Patreon" style="--brand-color: #f96854;"><span class="icon-mask" style="--icon-url: url('https://cdn.simpleicons.org/patreon/white')"></span></a>
                <a href="https://discord.gg/aEghXGbm3J" class="social-icon" target="_blank" title="Discord" style="--brand-color: #5865f2;"><span class="icon-mask" style="--icon-url: url('https://cdn.simpleicons.org/discord/white')"></span></a>
                <a href="https://twitch.tv/amymialee" class="social-icon" target="_blank" title="Twitch" style="--brand-color: #8956fb;"><span class="icon-mask" style="--icon-url: url('https://cdn.simpleicons.org/twitch/white')"></span></a>
                <!--<a href="https://youtube.com/@amymialee" class="social-icon" target="_blank" title="YouTube" style="--brand-color: #ff0000;"><span class="icon-mask" style="--icon-url: url&#40;'https://cdn.simpleicons.org/youtube/white'&#41;"></span></a>-->
                <a href="https://modrinth.com/user/AmyMialee" class="social-icon" target="_blank" title="Modrinth" style="--brand-color: #1bd96a;"><span class="icon-mask" style="--icon-url: url('https://cdn.simpleicons.org/modrinth/white')"></span></a>
                <!--<a href="https://curseforge.com/members/amymialee/projects" class="social-icon" target="_blank" title="CurseForge" style="--brand-color: #f58220;"><span class="icon-mask" style="--icon-url: url('https://cdn.simpleicons.org/curseforge/white')"></span></a>-->
                <!--<a href="https://bsky.app/profile/amymialee.xyz" class="social-icon" target="_blank" title="BlueSky" style="--brand-color: #1185fe;"><span class="icon-mask" style="--icon-url: url('https://cdn.simpleicons.org/bluesky/white')"></span></a>-->
                <!--<a href="https://twitter.com/amy_mialee" class="social-icon" target="_blank" title="Twitter" style="--brand-color: #26a7de;"><span class="icon-mask" style="--icon-url: url('https://cdn.simpleicons.org/x/white')"></span></a>-->
                <a href="https://github.com/AmyMialee" class="social-icon" target="_blank" title="GitHub" style="--brand-color: #6e5494;"><span class="icon-mask" style="--icon-url: url('https://cdn.simpleicons.org/github/white')"></span></a>
            </div>
        </div>
        <div class="link-container">
            <a href="https://www.patreon.com/cw/AmyMialee" class="link-item" target="_blank" title="Patreon" style="--brand-color: #f96854;">
                <div class="link-icon"><span class="link-mask" style="--icon-url: url('https://cdn.simpleicons.org/patreon/white')"></span></div>
                <div class="link-content"><div class="link-title">Patreon</div><div class="link-description">Support my work and get access to my Projects</div></div>
            </a>
            <a href="https://discord.gg/aEghXGbm3J" class="link-item" target="_blank" title="Discord" style="--brand-color: #5865f2;">
                <div class="link-icon"><span class="link-mask" style="--icon-url: url('https://cdn.simpleicons.org/discord/white')"></span></div>
                <div class="link-content"><div class="link-title">Discord</div><div class="link-description">Join my Discord Server</div></div>
            </a>
            <a href="https://www.twitch.tv/AmyMialee" class="link-item" target="_blank" title="Twitch" style="--brand-color: #8956fb;">
                <div class="link-icon"><span class="link-mask" style="--icon-url: url('https://cdn.simpleicons.org/twitch/white')"></span></div>
                <div class="link-content"><div class="link-title">Twitch</div><div class="link-description">Follow me on Twitch</div></div>
            </a>
            <a href="https://www.youtube.com/@AmyMialee" class="link-item" target="_blank" title="YouTube" style="--brand-color: #ff0000;">
                <div class="link-icon"><span class="link-mask" style="--icon-url: url('https://cdn.simpleicons.org/youtube/white')"></span></div>
                <div class="link-content"><div class="link-title">YouTube</div><div class="link-description">Subscribe to me on YouTube</div></div>
            </a>
            <a href="https://modrinth.com/user/AmyMialee" class="link-item" target="_blank" title="Modrinth" style="--brand-color: #1bd96a;">
                <div class="link-icon"><span class="link-mask" style="--icon-url: url('https://cdn.simpleicons.org/modrinth/white')"></span></div>
                <div class="link-content"><div class="link-title">Modrinth</div><div class="link-description">Download my mods on Modrinth</div></div>
            </a>
            <a href="https://curseforge.com/members/amymialee/projects" class="link-item" target="_blank" title="CurseForge" style="--brand-color: #f58220;">
                <div class="link-icon"><span class="link-mask" style="--icon-url: url('https://cdn.simpleicons.org/curseforge/white')"></span></div>
                <div class="link-content"><div class="link-title">CurseForge</div><div class="link-description">Download my mods on CurseForge</div></div>
            </a>
            <a href="https://bsky.app/profile/amymialee.xyz" class="link-item" target="_blank" title="BlueSky" style="--brand-color: #1185fe;">
                <div class="link-icon"><span class="link-mask" style="--icon-url: url('https://cdn.simpleicons.org/bluesky/white')"></span></div>
                <div class="link-content"><div class="link-title">BlueSky</div><div class="link-description">Follow me on BlueSky</div></div>
            </a>
            <a href="https://twitter.com/amy_mialee" class="link-item" target="_blank" title="Twitter" style="--brand-color: #26a7de;">
                <div class="link-icon"><span class="link-mask" style="--icon-url: url('https://cdn.simpleicons.org/x/white')"></span></div>
                <div class="link-content"><div class="link-title">Twitter</div><div class="link-description">Follow me on Twitter</div></div>
            </a>
            <a href="https://github.com/AmyMialee" class="link-item" target="_blank" title="GitHub" style="--brand-color: #6e5494;">
                <div class="link-icon"><span class="link-mask" style="--icon-url: url('https://cdn.simpleicons.org/github/white')"></span></div>
                <div class="link-content"><div class="link-title">GitHub</div><div class="link-description">Follow me on GitHub</div></div>
            </a>
        </div>
        <div class="footer">
            <p>© <span id="currentYear"></span> AmyMialee</p>
        </div>
    </div>
    <script>
        const themeToggle = document.getElementById('themeToggle');
        const swap = () => {
            document.body.classList.toggle('light');
            const isLight = document.body.classList.contains('light');
            localStorage.setItem('theme', isLight ? 'light' : 'dark');
            themeToggle.innerHTML = isLight ? '<i class="fas fa-moon"></i>' : '<i class="fas fa-sun"></i>';
        };
        themeToggle.addEventListener('click', swap);
        if (localStorage.getItem('theme') === 'light'){swap();}
        document.getElementById('currentYear').textContent = new Date().getFullYear().toString();
    </script>
</body>