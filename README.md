# MODAWIGAMES
<!DOCTYPE html>
<html lang="nl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MODAWIGAMES | Ultimate Gaming Platform 2025</title>
    <!-- Externe bronnen -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;500;700;900&family=Russo+One&family=Press+Start+2P&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css">
    <style>
        /* ============ BASIS STIJLEN ============ */
        :root {
            /* Kleurenpaletten */
            --default-primary: #6c5ce7;
            --default-secondary: #00cec9;
            --default-accent: #fd79a8;
            --default-dark: #2d3436;
            --default-light: #f5f6fa;
            
            /* Retro thema */
            --retro-primary: #ff9ff3;
            --retro-secondary: #feca57;
            --retro-accent: #ff6b6b;
            --retro-dark: #222f3e;
            --retro-light: #f5f6fa;
            --retro-text: #341f97;
            
            /* Fantasy thema */
            --fantasy-primary: #1dd1a1;
            --fantasy-secondary: #5f27cd;
            --fantasy-accent: #ff9f43;
            --fantasy-dark: #222f3e;
            --fantasy-light: #f5f6fa;
            --fantasy-text: #2e86de;
            
            /* Futuristisch thema */
            --futuristic-primary: #54a0ff;
            --futuristic-secondary: #00d2d3;
            --futuristic-accent: #f368e0;
            --futuristic-dark: #2d3436;
            --futuristic-light: #f5f6fa;
            --futuristic-text: #00cec9;
            
            /* Status kleuren */
            --success: #00b894;
            --warning: #fdcb6e;
            --danger: #d63031;
            --info: #0984e3;
            
            /* Overgangen */
            --transition-fast: all 0.2s ease;
            --transition-medium: all 0.3s ease;
            --transition-slow: all 0.5s ease;
            
            /* Schaduwen */
            --shadow-sm: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);
            --shadow-md: 0 4px 6px rgba(0,0,0,0.16), 0 4px 6px rgba(0,0,0,0.23);
            --shadow-lg: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);
            --shadow-xl: 0 14px 28px rgba(0,0,0,0.25), 0 10px 10px rgba(0,0,0,0.22);
            --shadow-inset: inset 0 2px 4px 0 rgba(0,0,0,0.06);
            
            /* Afgeronde hoeken */
            --radius-sm: 4px;
            --radius-md: 8px;
            --radius-lg: 16px;
            --radius-xl: 32px;
            --radius-full: 9999px;
            
            /* Typografie */
            --font-heading: 'Russo One', sans-serif;
            --font-body: 'Orbitron', sans-serif;
            --font-special: 'Press Start 2P', cursive;
            
            /* Spacing */
            --space-xs: 0.25rem;
            --space-sm: 0.5rem;
            --space-md: 1rem;
            --space-lg: 1.5rem;
            --space-xl: 2rem;
            --space-2xl: 3rem;
            --space-3xl: 4rem;
            
            /* Actieve thema variabelen (standaard) */
            --primary: var(--default-primary);
            --secondary: var(--default-secondary);
            --accent: var(--default-accent);
            --dark: var(--default-dark);
            --light: var(--default-light);
            --text: var(--default-light);
        }

        /* ============ BASIS ELEMENTEN ============ */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
            font-size: 16px;
        }

        body {
            font-family: var(--font-body);
            line-height: 1.6;
            color: var(--text);
            background-color: var(--dark);
            overflow-x: hidden;
            transition: var(--transition-medium);
        }

        h1, h2, h3, h4, h5, h6 {
            font-family: var(--font-heading);
            font-weight: 700;
            line-height: 1.2;
            margin-bottom: var(--space-md);
        }

        h1 { font-size: 3.5rem; }
        h2 { font-size: 2.5rem; }
        h3 { font-size: 2rem; }
        h4 { font-size: 1.5rem; }
        h5 { font-size: 1.25rem; }
        h6 { font-size: 1rem; }

        p {
            margin-bottom: var(--space-md);
            font-weight: 400;
        }

        a {
            color: var(--secondary);
            text-decoration: none;
            transition: var(--transition-fast);
        }

        a:hover {
            color: var(--accent);
        }

        img {
            max-width: 100%;
            height: auto;
            display: block;
        }

        ul, ol {
            margin-bottom: var(--space-md);
            padding-left: var(--space-lg);
        }

        /* ============ LAYOUT COMPONENTEN ============ */
        .container {
            width: 100%;
            max-width: 1440px;
            margin: 0 auto;
            padding: 0 var(--space-lg);
        }

        .section {
            padding: var(--space-3xl) 0;
            position: relative;
        }

        .section-title {
            text-align: center;
            margin-bottom: var(--space-2xl);
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            margin: var(--space-md) auto;
            border-radius: var(--radius-full);
        }

        .grid {
            display: grid;
            gap: var(--space-lg);
        }

        .grid-cols-2 {
            grid-template-columns: repeat(2, 1fr);
        }

        .grid-cols-3 {
            grid-template-columns: repeat(3, 1fr);
        }

        .grid-cols-4 {
            grid-template-columns: repeat(4, 1fr);
        }

        .flex {
            display: flex;
        }

        .flex-col {
            flex-direction: column;
        }

        .items-center {
            align-items: center;
        }

        .justify-center {
            justify-content: center;
        }

        .justify-between {
            justify-content: space-between;
        }

        .gap-sm {
            gap: var(--space-sm);
        }

        .gap-md {
            gap: var(--space-md);
        }

        .gap-lg {
            gap: var(--space-lg);
        }

        /* ============ THEMA SPECIFIEKE STIJLEN ============ */
        /* Standaard thema */
        body.default-theme {
            --primary: var(--default-primary);
            --secondary: var(--default-secondary);
            --accent: var(--default-accent);
            --dark: var(--default-dark);
            --light: var(--default-light);
            --text: var(--default-light);
            background: linear-gradient(135deg, var(--dark), #1a1a2e);
        }

        /* Retro thema */
        body.retro-theme {
            --primary: var(--retro-primary);
            --secondary: var(--retro-secondary);
            --accent: var(--retro-accent);
            --dark: var(--retro-dark);
            --light: var(--retro-light);
            --text: var(--retro-text);
            background: linear-gradient(135deg, var(--dark), #1a1a2e);
        }

        /* Fantasy thema */
        body.fantasy-theme {
            --primary: var(--fantasy-primary);
            --secondary: var(--fantasy-secondary);
            --accent: var(--fantasy-accent);
            --dark: var(--fantasy-dark);
            --light: var(--fantasy-light);
            --text: var(--fantasy-text);
            background: linear-gradient(135deg, var(--dark), #1a1a2e);
        }

        /* Futuristisch thema */
        body.futuristic-theme {
            --primary: var(--futuristic-primary);
            --secondary: var(--futuristic-secondary);
            --accent: var(--futuristic-accent);
            --dark: var(--futuristic-dark);
            --light: var(--futuristic-light);
            --text: var(--futuristic-text);
            background: linear-gradient(135deg, var(--dark), #1a1a2e);
        }

        /* ============ COMPONENTEN ============ */
        /* Knoppen */
        .btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: var(--space-sm) var(--space-lg);
            border-radius: var(--radius-lg);
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: var(--transition-medium);
            border: 2px solid transparent;
            cursor: pointer;
            font-size: 0.9rem;
            position: relative;
            overflow: hidden;
            z-index: 1;
        }

        .btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            z-index: -1;
            transition: var(--transition-medium);
        }

        .btn:hover::before {
            opacity: 0.9;
            transform: scale(1.05);
        }

        .btn-primary {
            color: var(--light);
            box-shadow: var(--shadow-md);
        }

        .btn-primary:hover {
            transform: translateY(-3px);
            box-shadow: var(--shadow-lg);
            color: var(--light);
        }

        .btn-secondary {
            background-color: transparent;
            border-color: var(--primary);
            color: var(--primary);
        }

        .btn-secondary:hover {
            background-color: var(--primary);
            color: var(--light);
            transform: translateY(-3px);
            box-shadow: var(--shadow-md);
        }

        .btn-accent {
            background-color: var(--accent);
            color: var(--light);
        }

        .btn-accent:hover {
            background-color: var(--accent);
            opacity: 0.9;
            transform: translateY(-3px);
            box-shadow: var(--shadow-lg);
        }

        .btn-lg {
            padding: var(--space-md) var(--space-xl);
            font-size: 1.1rem;
        }

        .btn-icon {
            margin-right: var(--space-sm);
        }

        /* Kaarten */
        .card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: var(--radius-lg);
            overflow: hidden;
            transition: var(--transition-medium);
            box-shadow: var(--shadow-sm);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-lg);
            border-color: var(--primary);
        }

        .card-img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .card-body {
            padding: var(--space-lg);
        }

        .card-title {
            font-size: 1.25rem;
            margin-bottom: var(--space-sm);
            color: var(--secondary);
        }

        .card-text {
            color: rgba(255, 255, 255, 0.8);
            font-size: 0.9rem;
            margin-bottom: var(--space-md);
        }

        .card-footer {
            padding: var(--space-md) var(--space-lg);
            background: rgba(0, 0, 0, 0.2);
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        /* Badges */
        .badge {
            display: inline-block;
            padding: var(--space-xs) var(--space-sm);
            border-radius: var(--radius-full);
            font-size: 0.75rem;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .badge-primary {
            background-color: var(--primary);
            color: var(--light);
        }

        .badge-secondary {
            background-color: var(--secondary);
            color: var(--dark);
        }

        .badge-accent {
            background-color: var(--accent);
            color: var(--light);
        }

        .badge-success {
            background-color: var(--success);
            color: var(--light);
        }

        .badge-warning {
            background-color: var(--warning);
            color: var(--dark);
        }

        .badge-danger {
            background-color: var(--danger);
            color: var(--light);
        }

        .badge-info {
            background-color: var(--info);
            color: var(--light);
        }

        /* Progress bars */
        .progress {
            height: 8px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: var(--radius-full);
            overflow: hidden;
            margin-bottom: var(--space-md);
        }

        .progress-bar {
            height: 100%;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            border-radius: var(--radius-full);
            transition: width 1s ease;
        }

        /* Ratings */
        .rating {
            color: var(--warning);
            margin-bottom: var(--space-sm);
        }

        .rating-sm {
            font-size: 0.8rem;
        }

        .rating-lg {
            font-size: 1.2rem;
        }

        /* Tooltips */
        .tooltip {
            position: relative;
            display: inline-block;
        }

        .tooltip .tooltip-text {
            visibility: hidden;
            width: 120px;
            background-color: var(--dark);
            color: var(--light);
            text-align: center;
            border-radius: var(--radius-sm);
            padding: var(--space-xs) 0;
            position: absolute;
            z-index: 1;
            bottom: 125%;
            left: 50%;
            margin-left: -60px;
            opacity: 0;
            transition: var(--transition-medium);
            font-size: 0.8rem;
            box-shadow: var(--shadow-md);
        }

        .tooltip .tooltip-text::after {
            content: "";
            position: absolute;
            top: 100%;
            left: 50%;
            margin-left: -5px;
            border-width: 5px;
            border-style: solid;
            border-color: var(--dark) transparent transparent transparent;
        }

        .tooltip:hover .tooltip-text {
            visibility: visible;
            opacity: 1;
        }

        /* ============ SECTIE SPECIFIEKE STIJLEN ============ */
        /* Header */
        .header {
            background: linear-gradient(135deg, rgba(0, 0, 0, 0.8), rgba(0, 0, 0, 0.5));
            padding: var(--space-md) 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-family: var(--font-special);
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--light);
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: var(--space-sm);
        }

        .logo-icon {
            color: var(--primary);
            font-size: 2rem;
        }

        /* Navigatie */
        .nav-menu {
            display: flex;
            gap: var(--space-md);
        }

        .nav-link {
            color: var(--light);
            font-weight: 500;
            padding: var(--space-sm) var(--space-md);
            border-radius: var(--radius-sm);
            transition: var(--transition-fast);
            position: relative;
        }

        .nav-link::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--primary);
            transition: var(--transition-medium);
        }

        .nav-link:hover {
            color: var(--primary);
        }

        .nav-link:hover::after {
            width: 100%;
        }

        .nav-link.active {
            color: var(--primary);
            font-weight: 700;
        }

        .nav-link.active::after {
            width: 100%;
        }

        /* Hero sectie */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            position: relative;
            overflow: hidden;
            padding-top: 80px;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.3));
            z-index: 1;
        }

        .hero-bg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            z-index: 0;
        }

        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 800px;
            padding: var(--space-xl);
        }

        .hero-title {
            font-size: 4rem;
            margin-bottom: var(--space-md);
            text-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
            animation: fadeInDown 1s ease;
        }

        .hero-subtitle {
            font-size: 1.5rem;
            margin-bottom: var(--space-xl);
            opacity: 0.9;
            animation: fadeInUp 1s ease 0.3s forwards;
            opacity: 0;
        }

        .hero-buttons {
            display: flex;
            gap: var(--space-md);
            justify-content: center;
            animation: fadeIn 1s ease 0.6s forwards;
            opacity: 0;
        }

        /* Nieuws sectie */
        .news-section {
            background-color: rgba(0, 0, 0, 0.3);
            position: relative;
            overflow: hidden;
        }

        .news-section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1542751371-adc38448a05e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80') no-repeat center center/cover;
            opacity: 0.1;
            z-index: -1;
        }

        .news-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: var(--space-lg);
        }

        .news-card {
            background: rgba(45, 52, 54, 0.8);
            border-radius: var(--radius-lg);
            overflow: hidden;
            transition: var(--transition-medium);
            box-shadow: var(--shadow-sm);
        }

        .news-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-lg);
        }

        .news-card-img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .news-card-body {
            padding: var(--space-lg);
        }

        .news-card-date {
            font-size: 0.8rem;
            color: var(--secondary);
            margin-bottom: var(--space-sm);
        }

        .news-card-title {
            font-size: 1.25rem;
            margin-bottom: var(--space-sm);
        }

        .news-card-excerpt {
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.9rem;
            margin-bottom: var(--space-md);
        }

        /* Reviews sectie */
        .reviews-section {
            background-color: rgba(0, 0, 0, 0.5);
        }

        .review-card {
            background: rgba(45, 52, 54, 0.8);
            border-radius: var(--radius-lg);
            padding: var(--space-lg);
            box-shadow: var(--shadow-sm);
            transition: var(--transition-medium);
        }

        .review-card:hover {
            transform: translateY(-5px);
            box-shadow: var(--shadow-md);
        }

        .review-header {
            display: flex;
            align-items: center;
            margin-bottom: var(--space-md);
        }

        .review-avatar {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            object-fit: cover;
            margin-right: var(--space-md);
            border: 3px solid var(--primary);
        }

        .review-game {
            font-size: 1.25rem;
            margin-bottom: var(--space-xs);
        }

        .review-author {
            color: var(--secondary);
            font-size: 0.9rem;
        }

        .review-content {
            margin-bottom: var(--space-md);
            color: rgba(255, 255, 255, 0.8);
        }

        /* Games sectie */
        .games-section {
            background: linear-gradient(135deg, rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.3));
        }

        .game-card {
            background: rgba(45, 52, 54, 0.8);
            border-radius: var(--radius-lg);
            overflow: hidden;
            transition: var(--transition-medium);
            box-shadow: var(--shadow-sm);
        }

        .game-card:hover {
            transform: scale(1.03);
            box-shadow: var(--shadow-lg);
        }

        .game-card-img {
            width: 100%;
            height: 250px;
            object-fit: cover;
        }

        .game-card-body {
            padding: var(--space-lg);
        }

        .game-card-title {
            font-size: 1.5rem;
            margin-bottom: var(--space-sm);
        }

        .game-card-meta {
            display: flex;
            justify-content: space-between;
            margin-bottom: var(--space-md);
        }

        .game-card-genre {
            background-color: var(--primary);
            color: var(--light);
            padding: var(--space-xs) var(--space-sm);
            border-radius: var(--radius-full);
            font-size: 0.8rem;
        }

        .game-card-platforms {
            display: flex;
            gap: var(--space-xs);
        }

        .platform-icon {
            width: 24px;
            height: 24px;
            object-fit: contain;
            opacity: 0.7;
            transition: var(--transition-fast);
        }

        .platform-icon:hover {
            opacity: 1;
            transform: scale(1.2);
        }

        .game-card-description {
            color: rgba(255, 255, 255, 0.7);
            margin-bottom: var(--space-md);
            font-size: 0.9rem;
        }

        /* Community sectie */
        .community-section {
            background: url('https://images.unsplash.com/photo-1511512578047-dba367674e03?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2071&q=80') no-repeat center center/cover;
            position: relative;
        }

        .community-section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(135deg, rgba(108, 92, 231, 0.8), rgba(0, 206, 201, 0.8));
            z-index: 0;
        }

        .community-content {
            position: relative;
            z-index: 1;
            text-align: center;
        }

        .community-stats {
            display: flex;
            justify-content: space-around;
            flex-wrap: wrap;
            gap: var(--space-xl);
            margin: var(--space-2xl) 0;
        }

        .stat-item {
            text-align: center;
        }

        .stat-number {
            font-size: 3rem;
            font-weight: 700;
            color: var(--light);
            margin-bottom: var(--space-xs);
        }

        .stat-label {
            font-size: 1rem;
            color: rgba(255, 255, 255, 0.8);
        }

        /* Leaderboard sectie */
        .leaderboard-section {
            background-color: rgba(0, 0, 0, 0.5);
        }

        .leaderboard-table {
            width: 100%;
            border-collapse: separate;
            border-spacing: 0 var(--space-sm);
        }

        .leaderboard-table th {
            background-color: var(--primary);
            color: var(--light);
            padding: var(--space-md);
            text-align: left;
        }

        .leaderboard-table tr {
            background-color: rgba(255, 255, 255, 0.1);
            transition: var(--transition-fast);
        }

        .leaderboard-table tr:hover {
            background-color: rgba(255, 255, 255, 0.2);
            transform: translateX(5px);
        }

        .leaderboard-table td {
            padding: var(--space-md);
            vertical-align: middle;
        }

        .leaderboard-rank {
            font-weight: 700;
            color: var(--secondary);
            width: 50px;
        }

        .leaderboard-user {
            display: flex;
            align-items: center;
            gap: var(--space-md);
        }

        .leaderboard-avatar {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            object-fit: cover;
        }

        .leaderboard-score {
            font-weight: 700;
            color: var(--accent);
        }

        /* Contact sectie */
        .contact-section {
            background-color: rgba(0, 0, 0, 0.3);
        }

        .contact-form {
            max-width: 600px;
            margin: 0 auto;
            background: rgba(45, 52, 54, 0.8);
            padding: var(--space-xl);
            border-radius: var(--radius-lg);
            box-shadow: var(--shadow-md);
        }

        .form-group {
            margin-bottom: var(--space-lg);
        }

        .form-label {
            display: block;
            margin-bottom: var(--space-sm);
            font-weight: 500;
        }

        .form-control {
            width: 100%;
            padding: var(--space-md);
            background-color: rgba(255, 255, 255, 0.1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: var(--radius-sm);
            color: var(--light);
            transition: var(--transition-fast);
        }

        .form-control:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 2px rgba(108, 92, 231, 0.3);
        }

        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }

        /* Footer */
        .footer {
            background-color: var(--dark);
            padding: var(--space-2xl) 0;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }

        .footer-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: var(--space-xl);
            margin-bottom: var(--space-xl);
        }

        .footer-logo {
            font-family: var(--font-special);
            font-size: 1.5rem;
            margin-bottom: var(--space-md);
            color: var(--light);
        }

        .footer-about {
            max-width: 300px;
        }

        .footer-links h3 {
            font-size: 1.25rem;
            margin-bottom: var(--space-md);
            color: var(--secondary);
        }

        .footer-links ul {
            list-style: none;
            padding: 0;
        }

        .footer-links li {
            margin-bottom: var(--space-sm);
        }

        .footer-links a {
            color: rgba(255, 255, 255, 0.7);
            transition: var(--transition-fast);
        }

        .footer-links a:hover {
            color: var(--primary);
            padding-left: var(--space-xs);
        }

        .footer-social {
            display: flex;
            gap: var(--space-md);
            margin-top: var(--space-md);
        }

        .social-link {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background-color: rgba(255, 255, 255, 0.1);
            color: var(--light);
            transition: var(--transition-fast);
        }

        .social-link:hover {
            background-color: var(--primary);
            color: var(--light);
            transform: translateY(-3px);
        }

        .footer-bottom {
            text-align: center;
            padding-top: var(--space-xl);
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: rgba(255, 255, 255, 0.5);
            font-size: 0.9rem;
        }

        /* ============ ANIMATIES ============ */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }

        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
            100% { transform: translateY(0px); }
        }

        /* ============ THEMA SWITCHER ============ */
        .theme-switcher {
            position: fixed;
            bottom: var(--space-lg);
            right: var(--space-lg);
            z-index: 1000;
            background: rgba(0, 0, 0, 0.7);
            backdrop-filter: blur(10px);
            border-radius: var(--radius-lg);
            padding: var(--space-sm);
            box-shadow: var(--shadow-lg);
            display: flex;
            flex-direction: column;
            gap: var(--space-xs);
        }

        .theme-btn {
            width: 30px;
            height: 30px;
            border-radius: 50%;
            cursor: pointer;
            border: 2px solid transparent;
            transition: var(--transition-medium);
        }

        .theme-btn:hover {
            transform: scale(1.1);
            border-color: var(--light);
        }

        .theme-btn.active {
            border-color: var(--light);
            transform: scale(1.1);
            box-shadow: 0 0 10px rgba(255, 255, 255, 0.5);
        }

        /* ============ RESPONSIVE STIJLEN ============ */
        @media (max-width: 1200px) {
            html {
                font-size: 15px;
            }
            
            .grid-cols-4 {
                grid-template-columns: repeat(3, 1fr);
            }
        }

        @media (max-width: 992px) {
            html {
                font-size: 14px;
            }
            
            .grid-cols-3, .grid-cols-4 {
                grid-template-columns: repeat(2, 1fr);
            }
            
            .hero-title {
                font-size: 3rem;
            }
            
            .hero-subtitle {
                font-size: 1.25rem;
            }
        }

        @media (max-width: 768px) {
            html {
                font-size: 13px;
            }
            
            .header-container {
                flex-direction: column;
                gap: var(--space-md);
            }
            
            .nav-menu {
                flex-wrap: wrap;
                justify-content: center;
            }
            
            .grid-cols-2, .grid-cols-3, .grid-cols-4 {
                grid-template-columns: 1fr;
            }
            
            .hero-title {
                font-size: 2.5rem;
            }
            
            .hero-buttons {
                flex-direction: column;
                align-items: center;
            }
            
            .community-stats {
                gap: var(--space-lg);
            }
        }

        @media (max-width: 576px) {
            html {
                font-size: 12px;
            }
            
            .section {
                padding: var(--space-xl) 0;
            }
            
            .hero-title {
                font-size: 2rem;
            }
            
            .hero-subtitle {
                font-size: 1rem;
            }
            
            .section-title h2 {
                font-size: 1.8rem;
            }
        }

        /* ============ SPECIALE EFFECTEN ============ */
        .parallax {
            background-attachment: fixed;
            background-position: center;
            background-repeat: no-repeat;
            background-size: cover;
            position: relative;
        }

        .parallax::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.6);
            z-index: 0;
        }

        .parallax-content {
            position: relative;
            z-index: 1;
        }

        .floating {
            animation: float 3s ease-in-out infinite;
        }

        .pulse {
            animation: pulse 2s infinite;
        }

        /* ============ GAMIFICATION ELEMENTEN ============ */
        .achievement {
            display: flex;
            align-items: center;
            gap: var(--space-md);
            background: rgba(255, 255, 255, 0.1);
            border-radius: var(--radius-md);
            padding: var(--space-md);
            margin-bottom: var(--space-md);
            transition: var(--transition-fast);
        }

        .achievement:hover {
            background: rgba(255, 255, 255, 0.2);
            transform: translateX(5px);
        }

        .achievement-icon {
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: var(--primary);
            border-radius: var(--radius-md);
            font-size: 1.5rem;
            color: var(--light);
        }

        .achievement-content {
            flex: 1;
        }

        .achievement-title {
            font-weight: 700;
            margin-bottom: var(--space-xs);
        }

        .achievement-desc {
            font-size: 0.9rem;
            color: rgba(255, 255, 255, 0.7);
        }

        .achievement-progress {
            width: 100%;
            height: 5px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: var(--radius-full);
            margin-top: var(--space-sm);
            overflow: hidden;
        }

        .achievement-progress-bar {
            height: 100%;
            background: var(--secondary);
            border-radius: var(--radius-full);
        }

        /* Quest log */
        .quest-log {
            background: rgba(0, 0, 0, 0.5);
            border-radius: var(--radius-lg);
            padding: var(--space-lg);
            margin-bottom: var(--space-xl);
        }

        .quest {
            padding: var(--space-md) 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        .quest:last-child {
            border-bottom: none;
        }

        .quest-header {
            display: flex;
            align-items: center;
            gap: var(--space-md);
            margin-bottom: var(--space-sm);
        }

        .quest-icon {
            width: 30px;
            height: 30px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: var(--primary);
            border-radius: var(--radius-sm);
            color: var(--light);
        }

        .quest-title {
            font-weight: 700;
            flex: 1;
        }

        .quest-reward {
            background: var(--warning);
            color: var(--dark);
            padding: var(--space-xs) var(--space-sm);
            border-radius: var(--radius-full);
            font-size: 0.8rem;
            font-weight: 700;
        }

        .quest-description {
            color: rgba(255, 255, 255, 0.7);
            font-size: 0.9rem;
            margin-bottom: var(--space-sm);
        }

        .quest-progress {
            width: 100%;
            height: 5px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: var(--radius-full);
            overflow: hidden;
        }

        .quest-progress-bar {
            height: 100%;
            background: var(--success);
            border-radius: var(--radius-full);
        }

        /* Live events */
        .live-event {
            background: rgba(255, 0, 0, 0.1);
            border-left: 4px solid var(--danger);
            padding: var(--space-md);
            margin-bottom: var(--space-md);
            display: flex;
            align-items: center;
            gap: var(--space-md);
            border-radius: 0 var(--radius-md) var(--radius-md) 0;
        }

        .live-badge {
            background: var(--danger);
            color: var(--light);
            padding: var(--space-xs) var(--space-sm);
            border-radius: var(--radius-full);
            font-weight: 700;
            font-size: 0.8rem;
            text-transform: uppercase;
        }

        .event-title {
            font-weight: 700;
            margin-bottom: var(--space-xs);
        }

        .event-time {
            font-size: 0.9rem;
            color: rgba(255, 255, 255, 0.7);
        }

        /* User profile card */
        .profile-card {
            background: rgba(45, 52, 54, 0.8);
            border-radius: var(--radius-lg);
            padding: var(--space-lg);
            box-shadow: var(--shadow-md);
            text-align: center;
        }

        .profile-avatar {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid var(--primary);
            margin: 0 auto var(--space-md);
        }

        .profile-name {
            font-size: 1.5rem;
            margin-bottom: var(--space-xs);
        }

        .profile-title {
            color: var(--secondary);
            margin-bottom: var(--space-md);
            font-size: 0.9rem;
        }

        .profile-stats {
            display: flex;
            justify-content: space-around;
            margin: var(--space-lg) 0;
        }

        .stat {
            text-align: center;
        }

        .stat-number {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
        }

        .stat-label {
            font-size: 0.8rem;
            color: rgba(255, 255, 255, 0.7);
        }

        /* ============ TOP 10 LIJSTEN ============ */
        .top10-list {
            counter-reset: top10-counter;
            list-style: none;
            padding: 0;
        }

        .top10-item {
            counter-increment: top10-counter;
            display: flex;
            align-items: center;
            gap: var(--space-md);
            padding: var(--space-md);
            background: rgba(255, 255, 255, 0.05);
            border-radius: var(--radius-md);
            margin-bottom: var(--space-sm);
            transition: var(--transition-fast);
        }

        .top10-item:hover {
            background: rgba(255, 255, 255, 0.1);
            transform: translateX(5px);
        }

        .top10-item::before {
            content: counter(top10-counter);
            font-size: 1.2rem;
            font-weight: 700;
            color: var(--primary);
            min-width: 30px;
            text-align: center;
        }

        .top10-item:nth-child(1)::before {
            color: var(--warning);
            font-size: 1.5rem;
        }

        .top10-item:nth-child(2)::before {
            color: var(--secondary);
        }

        .top10-item:nth-child(3)::before {
            color: var(--accent);
        }

        .top10-content {
            flex: 1;
        }

        .top10-title {
            font-weight: 700;
            margin-bottom: var(--space-xs);
        }

        .top10-meta {
            display: flex;
            gap: var(--space-md);
            font-size: 0.9rem;
            color: rgba(255, 255, 255, 0.7);
        }

        /* ============ INFOGRAFICS ============ */
        .infographic {
            background: rgba(255, 255, 255, 0.05);
            border-radius: var(--radius-lg);
            padding: var(--space-lg);
            margin-bottom: var(--space-xl);
            box-shadow: var(--shadow-sm);
        }

        .infographic-title {
            color: var(--primary);
            margin-bottom: var(--space-lg);
            text-align: center;
            font-size: 1.5rem;
        }

        .infographic-content {
            display: flex;
            flex-wrap: wrap;
            gap: var(--space-lg);
            justify-content: center;
        }

        .infographic-item {
            flex: 1;
            min-width: 200px;
            text-align: center;
        }

        .infographic-number {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--secondary);
            margin-bottom: var(--space-sm);
        }

        .infographic-label {
            font-size: 0.9rem;
            color: rgba(255, 255, 255, 0.7);
        }

        /* ============ AUDIO PLAYER ============ */
        .audio-player {
            background: rgba(255, 255, 255, 0.1);
            border-radius: var(--radius-lg);
            padding: var(--space-md);
            display: flex;
            align-items: center;
            gap: var(--space-md);
            margin-bottom: var(--space-lg);
        }

        .player-controls {
            display: flex;
            gap: var(--space-sm);
        }

        .player-btn {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            background: var(--primary);
            color: var(--light);
            display: flex;
            align-items: center;
            justify-content: center;
            border: none;
            cursor: pointer;
            transition: var(--transition-fast);
        }

        .player-btn:hover {
            background: var(--secondary);
            transform: scale(1.1);
        }

        .player-info {
            flex: 1;
        }

        .player-title {
            font-weight: 700;
            margin-bottom: var(--space-xs);
        }

        .player-artist {
            font-size: 0.9rem;
            color: rgba(255, 255, 255, 0.7);
        }

        .player-progress {
            width: 100%;
            height: 5px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: var(--radius-full);
            margin-top: var(--space-md);
            overflow: hidden;
        }

        .player-progress-bar {
            height: 100%;
            background: var(--secondary);
            border-radius: var(--radius-full);
            width: 30%;
        }

        /* ============ CUSTOM SCROLLBAR ============ */
        ::-webkit-scrollbar {
            width: 10px;
        }

        ::-webkit-scrollbar-track {
            background: rgba(255, 255, 255, 0.1);
        }

        ::-webkit-scrollbar-thumb {
            background: var(--primary);
            border-radius: var(--radius-full);
        }

        ::-webkit-scrollbar-thumb:hover {
            background: var(--secondary);
        }

        /* ============ TOAST MELDINGEN ============ */
        .toast {
            position: fixed;
            bottom: var(--space-lg);
            left: 50%;
            transform: translateX(-50%);
            background: var(--dark);
            color: var(--light);
            padding: var(--space-md) var(--space-lg);
            border-radius: var(--radius-lg);
            box-shadow: var(--shadow-xl);
            display: flex;
            align-items: center;
            gap: var(--space-md);
            z-index: 1100;
            opacity: 0;
            transition: var(--transition-medium);
        }

        .toast.show {
            opacity: 1;
            transform: translateX(-50%) translateY(0);
        }

        .toast.hide {
            opacity: 0;
            transform: translateX(-50%) translateY(100px);
        }

        .toast-icon {
            font-size: 1.5rem;
        }

        .toast-success .toast-icon {
            color: var(--success);
        }

        .toast-warning .toast-icon {
            color: var(--warning);
        }

        .toast-error .toast-icon {
            color: var(--danger);
        }

        .toast-info .toast-icon {
            color: var(--info);
        }

        .toast-message {
            flex: 1;
        }

        .toast-close {
            background: none;
            border: none;
            color: var(--light);
            cursor: pointer;
            font-size: 1rem;
        }

        /* ============ LOADING SCREEN ============ */
        .loading-screen {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: var(--dark);
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            z-index: 9999;
            transition: opacity 0.5s ease;
        }

        .loading-logo {
            font-family: var(--font-special);
            font-size: 3rem;
            margin-bottom: var(--space-xl);
            color: var(--primary);
            text-shadow: 0 0 10px rgba(108, 92, 231, 0.5);
        }

        .loading-spinner {
            width: 50px;
            height: 50px;
            border: 5px solid rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            border-top-color: var(--primary);
            animation: spin 1s linear infinite;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }

        /* ============ MEDIA QUERIES VOOR THEMA'S ============ */
        @media (prefers-color-scheme: light) {
            body.default-theme {
                --light: #2d3436;
                --dark: #f5f6fa;
                --text: #2d3436;
                background: linear-gradient(135deg, var(--dark), #e0e0e0);
            }
        }
    </style>
</head>
<body class="default-theme">
    <!-- Loading screen -->
    <div class="loading-screen">
        <div class="loading-logo">MODAWIGAMES</div>
        <div class="loading-spinner"></div>
    </div>

    <!-- Header -->
    <header class="header">
        <div class="container header-container">
            <a href="#" class="logo">
                <i class="fas fa-gamepad logo-icon"></i>
                MODAWIGAMES
            </a>
            
            <nav class="nav-menu">
                <a href="#home" class="nav-link active"><i class="fas fa-home"></i> Home</a>
                <a href="#news" class="nav-link"><i class="fas fa-newspaper"></i> Nieuws</a>
                <a href="#reviews" class="nav-link"><i class="fas fa-star"></i> Reviews</a>
                <a href="#games" class="nav-link"><i class="fas fa-gamepad"></i> Games</a>
                <a href="#community" class="nav-link"><i class="fas fa-users"></i> Community</a>
                <a href="#leaderboard" class="nav-link"><i class="fas fa-trophy"></i> Leaderboard</a>
            </nav>
        </div>
    </header>

    <!-- Hoofdinhoud -->
    <main>
        <!-- Hero sectie -->
        <section class="hero" id="home">
            <img src="https://images.unsplash.com/photo-1542751371-adc38448a05e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="Gaming background" class="hero-bg">
            
            <div class="hero-content">
                <h1 class="hero-title">Ontdek de Gaming Wereld van 2025</h1>
                <p class="hero-subtitle">De beste reviews, nieuws en community voor echte gamers</p>
                
                <div class="hero-buttons">
                    <a href="#games" class="btn btn-primary btn-lg">
                        <i class="fas fa-gamepad btn-icon"></i> Ontdek Games
                    </a>
                    <a href="#community" class="btn btn-secondary btn-lg">
                        <i class="fas fa-users btn-icon"></i> Word Lid
                    </a>
                </div>
            </div>
        </section>

        <!-- Nieuws sectie -->
        <section class="section news-section" id="news">
            <div class="container">
                <div class="section-title">
                    <h2>Laatste Gaming Nieuws</h2>
                    <p>Blijf op de hoogte van het laatste nieuws in de gaming wereld</p>
                </div>
                
                <div class="news-grid">
                    <!-- Nieuwsartikel 1 -->
                    <div class="news-card">
                        <img src="https://images.unsplash.com/photo-1547036967-23d11aacaee0?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="Game nieuws" class="news-card-img">
                        
                        <div class="news-card-body">
                            <div class="news-card-date">
                                <i class="far fa-calendar"></i> 15 juni 2025
                            </div>
                            <h3 class="news-card-title">Cyber Odyssey 2 aangekondigd</h3>
                            <p class="news-card-excerpt">De langverwachte sequel naar de cyberpunk hit komt in Q1 2025 met cross-platform play en next-gen graphics.</p>
                            
                            <div class="flex justify-between items-center">
                                <span class="badge badge-primary">Exclusief</span>
                                <a href="#" class="btn btn-sm btn-accent">Lees Meer</a>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Nieuwsartikel 2 -->
                    <div class="news-card">
                        <img src="https://images.unsplash.com/photo-1511512578047-dba367674e03?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2071&q=80" alt="Esports nieuws" class="news-card-img">
                        
                        <div class="news-card-body">
                            <div class="news-card-date">
                                <i class="far fa-calendar"></i> 12 juni 2025
                            </div>
                            <h3 class="news-card-title">Nederlands team wint EK</h3>
                            <p class="news-card-excerpt">Team NL heeft goud gewonnen tijdens het Europese kampioenschap Galaxy Warriors met een prijzenpot van €500.000.</p>
                            
                            <div class="flex justify-between items-center">
                                <span class="badge badge-danger">eSports</span>
                                <a href="#" class="btn btn-sm btn-accent">Lees Meer</a>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Nieuwsartikel 3 -->
                    <div class="news-card">
                        <img src="https://images.unsplash.com/photo-1585771724684-38269d6639fd?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="Tech nieuws" class="news-card-img">
                        
                        <div class="news-card-body">
                            <div class="news-card-date">
                                <i class="far fa-calendar"></i> 8 juni 2025
                            </div>
                            <h3 class="news-card-title">Nieuwe console aangekondigd</h3>
                            <p class="news-card-excerpt">Next-gen console belooft 8K gaming met 120fps ondersteuning en revolutionaire AI-technologie.</p>
                            
                            <div class="flex justify-between items-center">
                                <span class="badge badge-info">Tech</span>
                                <a href="#" class="btn btn-sm btn-accent">Lees Meer</a>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="text-center mt-8">
                    <a href="#" class="btn btn-primary">
                        <i class="fas fa-newspaper btn-icon"></i> Bekijk Alle Nieuws
                    </a>
                </div>
            </div>
        </section>

        <!-- Reviews sectie -->
        <section class="section reviews-section" id="reviews">
            <div class="container">
                <div class="section-title">
                    <h2>Laatste Game Reviews</h2>
                    <p>Onze eerlijke beoordelingen van de nieuwste games</p>
                </div>
                
                <div class="grid grid-cols-3 gap-8">
                    <!-- Review 1 -->
                    <div class="review-card">
                        <div class="review-header">
                            <img src="https://randomuser.me/api/portraits/men/32.jpg" alt="Reviewer" class="review-avatar">
                            <div>
                                <h3 class="review-game">Cyber Odyssey</h3>
                                <p class="review-author">Door: GameMasterNL</p>
                            </div>
                        </div>
                        
                        <div class="rating rating-lg">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star-half-alt"></i>
                            <span>4.5/5</span>
                        </div>
                        
                        <div class="review-content">
                            <p>"Een visueel spektakel met een meeslepend verhaal dat je niet snel zult vergeten. De gameplay is vernieuwend en uitdagend."</p>
                        </div>
                        
                        <div class="progress">
                            <div class="progress-bar" style="width: 90%"></div>
                        </div>
                        
                        <a href="#" class="btn btn-primary btn-block">Lees Volledige Review</a>
                    </div>
                    
                    <!-- Review 2 -->
                    <div class="review-card">
                        <div class="review-header">
                            <img src="https://randomuser.me/api/portraits/women/44.jpg" alt="Reviewer" class="review-avatar">
                            <div>
                                <h3 class="review-game">Mythic Realms</h3>
                                <p class="review-author">Door: FantasyQueen</p>
                            </div>
                        </div>
                        
                        <div class="rating rating-lg">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="far fa-star"></i>
                            <span>4/5</span>
                        </div>
                        
                        <div class="review-content">
                            <p>"Een fantastische MMORPG met een enorme wereld om te verkennen. De community is levendig en de endgame content is uitdagend."</p>
                        </div>
                        
                        <div class="progress">
                            <div class="progress-bar" style="width: 80%"></div>
                        </div>
                        
                        <a href="#" class="btn btn-primary btn-block">Lees Volledige Review</a>
                    </div>
                    
                    <!-- Review 3 -->
                    <div class="review-card">
                        <div class="review-header">
                            <img src="https://randomuser.me/api/portraits/men/75.jpg" alt="Reviewer" class="review-avatar">
                            <div>
                                <h3 class="review-game">Galaxy Warriors</h3>
                                <p class="review-author">Door: SpaceExplorer</p>
                            </div>
                        </div>
                        
                        <div class="rating rating-lg">
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <i class="fas fa-star"></i>
                            <span>5/5</span>
                        </div>
                        
                        <div class="review-content">
                            <p>"Absoluut verbluffend! De ruimtegevechten zijn intens en de multiplayer ervaring is onovertroffen. Een must-have voor sci-fi fans."</p>
                        </div>
                        
                        <div class="progress">
                            <div class="progress-bar" style="width: 100%"></div>
                        </div>
                        
                        <a href="#" class="btn btn-primary btn-block">Lees Volledige Review</a>
                    </div>
                </div>
                
                <div class="text-center mt-8">
                    <a href="#" class="btn btn-primary">
                        <i class="fas fa-star btn-icon"></i> Bekijk Alle Reviews
                    </a>
                </div>
            </div>
        </section>

        <!-- Games sectie -->
        <section class="section games-section" id="games">
            <div class="container">
                <div class="section-title">
                    <h2>Populaire Games</h2>
                    <p>Ontdek de meest populaire games van dit moment</p>
                </div>
                
                <div class="grid grid-cols-4 gap-8">
                    <!-- Game 1 -->
                    <div class="game-card">
                        <img src="https://images.unsplash.com/photo-1542751371-adc38448a05e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="Cyber Odyssey" class="game-card-img">
                        
                        <div class="game-card-body">
                            <h3 class="game-card-title">Cyber Odyssey</h3>
                            
                            <div class="game-card-meta">
                                <span class="game-card-genre">RPG</span>
                                
                                <div class="game-card-platforms">
                                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/87/PlayStation_controller.svg/1200px-PlayStation_controller.svg.png" alt="PS5" class="platform-icon" title="PS5">
                                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/71/Xbox_controller_2013.svg/1200px-Xbox_controller_2013.svg.png" alt="Xbox" class="platform-icon" title="Xbox Series X">
                                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/22/Windows_10_Logo.svg/1200px-Windows_10_Logo.svg.png" alt="PC" class="platform-icon" title="PC">
                                </div>
                            </div>
                            
                            <p class="game-card-description">Een episch cyberpunk avontuur in een verre toekomst waar technologie en menselijkheid botsen.</p>
                            
                            <div class="rating rating-sm">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star-half-alt"></i>
                                <span>4.5</span>
                            </div>
                            
                            <div class="flex justify-between mt-4">
                                <a href="#" class="btn btn-sm btn-primary">Details</a>
                                <a href="#" class="btn btn-sm btn-secondary">Koop Nu</a>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Game 2 -->
                    <div class="game-card">
                        <img src="https://images.unsplash.com/photo-1560253023-3ec5d502959f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="Mythic Realms" class="game-card-img">
                        
                        <div class="game-card-body">
                            <h3 class="game-card-title">Mythic Realms</h3>
                            
                            <div class="game-card-meta">
                                <span class="game-card-genre">MMORPG</span>
                                
                                <div class="game-card-platforms">
                                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/87/PlayStation_controller.svg/1200px-PlayStation_controller.svg.png" alt="PS5" class="platform-icon" title="PS5">
                                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/71/Xbox_controller_2013.svg/1200px-Xbox_controller_2013.svg.png" alt="Xbox" class="platform-icon" title="Xbox Series X">
                                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/22/Windows_10_Logo.svg/1200px-Windows_10_Logo.svg.png" alt="PC" class="platform-icon" title="PC">
                                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Nintendo_Switch_Logo.png/1200px-Nintendo_Switch_Logo.png" alt="Switch" class="platform-icon" title="Switch">
                                </div>
                            </div>
                            
                            <p class="game-card-description">Verken een uitgestrekte fantasy wereld met duizenden andere spelers in deze massieve MMORPG.</p>
                            
                            <div class="rating rating-sm">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="far fa-star"></i>
                                <span>4.0</span>
                            </div>
                            
                            <div class="flex justify-between mt-4">
                                <a href="#" class="btn btn-sm btn-primary">Details</a>
                                <a href="#" class="btn btn-sm btn-secondary">Koop Nu</a>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Game 3 -->
                    <div class="game-card">
                        <img src="https://images.unsplash.com/photo-1511512578047-dba367674e03?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2071&q=80" alt="Galaxy Warriors" class="game-card-img">
                        
                        <div class="game-card-body">
                            <h3 class="game-card-title">Galaxy Warriors</h3>
                            
                            <div class="game-card-meta">
                                <span class="game-card-genre">Space Shooter</span>
                                
                                <div class="game-card-platforms">
                                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/87/PlayStation_controller.svg/1200px-PlayStation_controller.svg.png" alt="PS5" class="platform-icon" title="PS5">
                                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/71/Xbox_controller_2013.svg/1200px-Xbox_controller_2013.svg.png" alt="Xbox" class="platform-icon" title="Xbox Series X">
                                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/22/Windows_10_Logo.svg/1200px-Windows_10_Logo.svg.png" alt="PC" class="platform-icon" title="PC">
                                </div>
                            </div>
                            
                            <p class="game-card-description">Vecht in epische ruimtegevechten en verover het universum in deze multiplayer shooter.</p>
                            
                            <div class="rating rating-sm">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <span>5.0</span>
                            </div>
                            
                            <div class="flex justify-between mt-4">
                                <a href="#" class="btn btn-sm btn-primary">Details</a>
                                <a href="#" class="btn btn-sm btn-secondary">Koop Nu</a>
                            </div>
                        </div>
                    </div>
                    
                    <!-- Game 4 -->
                    <div class="game-card">
                        <img src="https://images.unsplash.com/photo-1547036967-23d11aacaee0?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2070&q=80" alt="Neon Dynasty" class="game-card-img">
                        
                        <div class="game-card-body">
                            <h3 class="game-card-title">Neon Dynasty</h3>
                            
                            <div class="game-card-meta">
                                <span class="game-card-genre">FPS</span>
                                
                                <div class="game-card-platforms">
                                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/87/PlayStation_controller.svg/1200px-PlayStation_controller.svg.png" alt="PS5" class="platform-icon" title="PS5">
                                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/71/Xbox_controller_2013.svg/1200px-Xbox_controller_2013.svg.png" alt="Xbox" class="platform-icon" title="Xbox Series X">
                                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/22/Windows_10_Logo.svg/1200px-Windows_10_Logo.svg.png" alt="PC" class="platform-icon" title="PC">
                                    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Nintendo_Switch_Logo.png/1200px-Nintendo_Switch_Logo.png" alt="Switch" class="platform-icon" title="Switch">
                                </div>
                            </div>
                            
                            <p class="game-card-description">Een snelle first-person shooter in een futuristische setting met intense multiplayer gevechten.</p>
                            
                            <div class="rating rating-sm">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="far fa-star"></i>
                                <span>4.0</span>
                            </div>
                            
                            <div class="flex justify-between mt-4">
                                <a href="#" class="btn btn-sm btn-primary">Details</a>
                                <a href="#" class="btn btn-sm btn-secondary">Koop Nu</a>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="text-center mt-8">
                    <a href="#" class="btn btn-primary">
                        <i class="fas fa-gamepad btn-icon"></i> Bekijk Alle Games
                    </a>
                </div>
            </div>
        </section>

        <!-- Community sectie -->
        <section class="section community-section" id="community">
            <div class="container community-content">
                <div class="section-title">
                    <h2>Onze Gaming Community</h2>
                    <p>Sluit je aan bij duizenden gamers wereldwijd</p>
                </div>
                
                <div class="community-stats">
                    <div class="stat-item">
                        <div class="stat-number">25K+</div>
                        <div class="stat-label">Actieve Leden</div>
                    </div>
                    
                    <div class="stat-item">
                        <div class="stat-number">500+</div>
                        <div class="stat-label">Dagelijkse Discussies</div>
                    </div>
                    
                    <div class="stat-item">
                        <div class="stat-number">120</div>
                        <div class="stat-label">Gaming Teams</div>
                    </div>
                    
                    <div class="stat-item">
                        <div class="stat-number">10K+</div>
                        <div class="stat-label">User Guides</div>
                    </div>
                </div>
                
                <div class="flex justify-center gap-4">
                    <a href="#" class="btn btn-primary btn-lg">
                        <i class="fas fa-users btn-icon"></i> Word Lid
                    </a>
                    <a href="#" class="btn btn-secondary btn-lg">
                        <i class="fas fa-comments btn-icon"></i> Naar Forum
                    </a>
                </div>
            </div>
        </section>

        <!-- Leaderboard sectie -->
        <section class="section leaderboard-section" id="leaderboard">
            <div class="container">
                <div class="section-title">
                    <h2>Community Leaderboard</h2>
                    <p>Top gamers van deze maand</p>
                </div>
                
                <div class="infographic">
                    <h3 class="infographic-title">Top 10 Gamers</h3>
                    
                    <ol class="top10-list">
                        <li class="top10-item">
                            <div class="top10-content">
                                <h4 class="top10-title">GameMasterNL</h4>
                                <div class="top10-meta">
                                    <span><i class="fas fa-trophy"></i> Level 42</span>
                                    <span><i class="fas fa-star"></i> 1250 pts</span>
                                </div>
                            </div>
                        </li>
                        
                        <li class="top10-item">
                            <div class="top10-content">
                                <h4 class="top10-title">PixelQueen</h4>
                                <div class="top10-meta">
                                    <span><i class="fas fa-trophy"></i> Level 38</span>
                                    <span><i class="fas fa-star"></i> 1120 pts</span>
                                </div>
                            </div>
                        </li>
                        
                        <li class="top10-item">
                            <div class="top10-content">
                                <h4 class="top10-title">CyberWarrior</h4>
                                <div class="top10-meta">
                                    <span><i class="fas fa-trophy"></i> Level 35</span>
                                    <span><i class="fas fa-star"></i> 980 pts</span>
                                </div>
                            </div>
                        </li>
                        
                        <li class="top10-item">
                            <div class="top10-content">
                                <h4 class="top10-title">FantasyFan</h4>
                                <div class="top10-meta">
                                    <span><i class="fas fa-trophy"></i> Level 32</span>
                                    <span><i class="fas fa-star"></i> 875 pts</span>
                                </div>
                            </div>
                        </li>
                        
                        <li class="top10-item">
                            <div class="top10-content">
                                <h4 class="top10-title">RetroGamer</h4>
                                <div class="top10-meta">
                                    <span><i class="fas fa-trophy"></i> Level 30</span>
                                    <span><i class="fas fa-star"></i> 760 pts</span>
                                </div>
                            </div>
                        </li>
                    </ol>
                    
                    <div class="text-center mt-6">
                        <a href="#" class="btn btn-primary">
                            <i class="fas fa-list-ol btn-icon"></i> Volledig Leaderboard
                        </a>
                    </div>
                </div>
                
                <!-- Gamification elementen -->
                <div class="grid grid-cols-2 gap-8 mt-12">
                    <div class="quest-log">
                        <h3 class="text-center mb-6">Actieve Quests</h3>
                        
                        <div class="quest">
                            <div class="quest-header">
                                <div class="quest-icon">
                                    <i class="fas fa-gamepad"></i>
                                </div>
                                <h4 class="quest-title">Review Schrijven</h4>
                                <span class="quest-reward">50 pts</span>
                            </div>
                            
                            <p class="quest-description">Schrijf een uitgebreide review voor een game en verdien punten.</p>
                            
                            <div class="quest-progress">
                                <div class="quest-progress-bar" style="width: 30%"></div>
                            </div>
                        </div>
                        
                        <div class="quest">
                            <div class="quest-header">
                                <div class="quest-icon">
                                    <i class="fas fa-comments"></i>
                                </div>
                                <h4 class="quest-title">Forum Discussie</h4>
                                <span class="quest-reward">30 pts</span>
                            </div>
                            
                            <p class="quest-description">Start of neem deel aan een discussie in het forum.</p>
                            
                            <div class="quest-progress">
                                <div class="quest-progress-bar" style="width: 70%"></div>
                            </div>
                        </div>
                        
                        <div class="quest">
                            <div class="quest-header">
                                <div class="quest-icon">
                                    <i class="fas fa-users"></i>
                                </div>
                                <h4 class="quest-title">Community Event</h4>
                                <span class="quest-reward">100 pts</span>
                            </div>
                            
                            <p class="quest-description">Doe mee aan een community gaming event.</p>
                            
                            <div class="quest-progress">
                                <div class="quest-progress-bar" style="width: 10%"></div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="achievements">
                        <h3 class="text-center mb-6">Behaalde Achievements</h3>
                        
                        <div class="achievement">
                            <div class="achievement-icon">
                                <i class="fas fa-star"></i>
                            </div>
                            
                            <div class="achievement-content">
                                <h4 class="achievement-title">Eerste Review</h4>
                                <p class="achievement-desc">Je hebt je eerste game review geschreven!</p>
                                
                                <div class="achievement-progress">
                                    <div class="achievement-progress-bar" style="width: 100%"></div>
                                </div>
                            </div>
                        </div>
                        
                        <div class="achievement">
                            <div class="achievement-icon">
                                <i class="fas fa-comment"></i>
                            </div>
                            
                            <div class="achievement-content">
                                <h4 class="achievement-title">Forum Deelnemer</h4>
                                <p class="achievement-desc">10 posts in het forum gemaakt</p>
                                
                                <div class="achievement-progress">
                                    <div class="achievement-progress-bar" style="width: 60%"></div>
                                </div>
                            </div>
                        </div>
                        
                        <div class="achievement">
                            <div class="achievement-icon">
                                <i class="fas fa-trophy"></i>
                            </div>
                            
                            <div class="achievement-content">
                                <h4 class="achievement-title">Game Expert</h4>
                                <p class="achievement-desc">5 games gereviewd</p>
                                
                                <div class="achievement-progress">
                                    <div class="achievement-progress-bar" style="width: 40%"></div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Live events sectie -->
        <section class="section">
            <div class="container">
                <div class="section-title">
                    <h2>Live Events & Streams</h2>
                    <p>Komende gaming evenementen en live streams</p>
                </div>
                
                <div class="live-event">
                    <span class="live-badge">LIVE</span>
                    <div>
                        <h3 class="event-title">Community Game Night: Galaxy Warriors Tournament</h3>
                        <p class="event-time">Vandaag om 20:00 | Prijzenpot: €500</p>
                    </div>
                    <a href="#" class="btn btn-danger ml-auto">Doe Mee</a>
                </div>
                
                <div class="live-event">
                    <span class="live-badge">Binnenkort</span>
                    <div>
                        <h3 class="event-title">Cyber Odyssey Speedrun Challenge</h3>
                        <p class="event-time">15 juni 2025 om 18:00 | Speciale gasten</p>
                    </div>
                    <a href="#" class="btn btn-secondary ml-auto">Meer Info</a>
                </div>
                
                <div class="live-event">
                    <span class="live-badge">Binnenkort</span>
                    <div>
                        <h3 class="event-title">Mythic Realms Raid Night</h3>
                        <p class="event-time">22 juni 2025 om 19:00 | Endgame content</p>
                    </div>
                    <a href="#" class="btn btn-secondary ml-auto">Meer Info</a>
                </div>
                
                <div class="text-center mt-8">
                    <a href="#" class="btn btn-primary">
                        <i class="fas fa-calendar-alt btn-icon"></i> Bekijk Alle Evenementen
                    </a>
                </div>
            </div>
        </section>

        <!-- Contact sectie -->
        <section class="section contact-section" id="contact">
            <div class="container">
                <div class="section-title">
                    <h2>Contacteer Ons</h2>
                    <p>Heb je vragen of suggesties? We horen graag van je!</p>
                </div>
                
                <div class="grid grid-cols-2 gap-12">
                    <div class="contact-info">
                        <h3 class="mb-6">Contactgegevens</h3>
                        
                        <div class="flex items-center gap-4 mb-6">
                            <div class="w-12 h-12 bg-primary rounded-full flex items-center justify-center text-white">
                                <i class="fas fa-envelope"></i>
                            </div>
                            <div>
                                <h4>Email</h4>
                                <a href="mailto:123456@gmail.com" class="text-secondary">123456@gmail.com</a>
                            </div>
                        </div>
                        
                        <div class="flex items-center gap-4 mb-6">
                            <div class="w-12 h-12 bg-primary rounded-full flex items-center justify-center text-white">
                                <i class="fas fa-phone"></i>
                            </div>
                            <div>
                                <h4>Telefoon</h4>
                                <a href="tel:0699876562" class="text-secondary">06 99876562</a>
                            </div>
                        </div>
                        
                        <div class="flex items-center gap-4 mb-6">
                            <div class="w-12 h-12 bg-primary rounded-full flex items-center justify-center text-white">
                                <i class="fas fa-clock"></i>
                            </div>
                            <div>
                                <h4>Support Tijden</h4>
                                <p>Ma-Vr: 10:00 - 18:00</p>
                                <p>Za-Zo: 12:00 - 16:00</p>
                            </div>
                        </div>
                        
                        <div class="social-links flex gap-4 mt-8">
                            <a href="#" class="social-link w-10 h-10 bg-dark rounded-full flex items-center justify-center text-white hover:bg-primary">
                                <i class="fab fa-twitter"></i>
                            </a>
                            <a href="#" class="social-link w-10 h-10 bg-dark rounded-full flex items-center justify-center text-white hover:bg-primary">
                                <i class="fab fa-instagram"></i>
                            </a>
                            <a href="#" class="social-link w-10 h-10 bg-dark rounded-full flex items-center justify-center text-white hover:bg-primary">
                                <i class="fab fa-twitch"></i>
                            </a>
                            <a href="#" class="social-link w-10 h-10 bg-dark rounded-full flex items-center justify-center text-white hover:bg-primary">
                                <i class="fab fa-discord"></i>
                            </a>
                        </div>
                    </div>
                    
                    <div class="contact-form">
                        <h3 class="mb-6">Stuur ons een bericht</h3>
                        
                        <form>
                            <div class="form-group">
                                <label for="name" class="form-label">Naam</label>
                                <input type="text" id="name" class="form-control" placeholder="Jouw naam" required>
                            </div>
                            
                            <div class="form-group">
                                <label for="email" class="form-label">Email</label>
                                <input type="email" id="email" class="form-control" placeholder="Jouw email" required>
                            </div>
                            
                            <div class="form-group">
                                <label for="subject" class="form-label">Onderwerp</label>
                                <input type="text" id="subject" class="form-control" placeholder="Onderwerp" required>
                            </div>
                            
                            <div class="form-group">
                                <label for="message" class="form-label">Bericht</label>
                                <textarea id="message" class="form-control" rows="5" placeholder="Jouw bericht" required></textarea>
                            </div>
                            
                            <button type="submit" class="btn btn-primary btn-lg w-full mt-4">
                                <i class="fas fa-paper-plane btn-icon"></i> Verstuur Bericht
                            </button>
                        </form>
                    </div>
                </div>
            </div>
        </section>

        <!-- Game muziek sectie -->
        <section class="section">
            <div class="container">
                <div class="section-title">
                    <h2>Game Soundtracks</h2>
                    <p>Beluister de beste muziek uit populaire games</p>
                </div>
                
                <div class="grid grid-cols-3 gap-8">
                    <div class="audio-player">
                        <div class="player-controls">
                            <button class="player-btn">
                                <i class="fas fa-play"></i>
                            </button>
                        </div>
                        
                        <div class="player-info">
                            <h4 class="player-title">Cyber Odyssey Main Theme</h4>
                            <p class="player-artist">Hans Zimmer</p>
                            
                            <div class="player-progress">
                                <div class="player-progress-bar"></div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="audio-player">
                        <div class="player-controls">
                            <button class="player-btn">
                                <i class="fas fa-play"></i>
                            </button>
                        </div>
                        
                        <div class="player-info">
                            <h4 class="player-title">Mythic Realms OST</h4>
                            <p class="player-artist">Sarah Schachner</p>
                            
                            <div class="player-progress">
                                <div class="player-progress-bar"></div>
                            </div>
                        </div>
                    </div>
                    
                    <div class="audio-player">
                        <div class="player-controls">
                            <button class="player-btn">
                                <i class="fas fa-play"></i>
                            </button>
                        </div>
                        
                        <div class="player-info">
                            <h4 class="player-title">Galaxy Warriors Battle Theme</h4>
                            <p class="player-artist">Mick Gordon</p>
                            
                            <div class="player-progress">
                                <div class="player-progress-bar"></div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="text-center mt-8">
                    <a href="#" class="btn btn-primary">
                        <i class="fas fa-music btn-icon"></i> Meer Soundtracks
                    </a>
                </div>
            </div>
        </section>
    </main>

    <!-- Footer -->
    <footer class="footer">
        <div class="container">
            <div class="footer-grid">
                <div class="footer-about">
                    <h3 class="footer-logo">MODAWIGAMES</h3>
                    <p>De ultieme bestemming voor gamers in 2025. Wij bieden de laatste nieuws, reviews en een levendige community voor gaming enthousiastelingen.</p>
                    
                    <div class="footer-social mt-6">
                        <a href="#" class="social-link">
                            <i class="fab fa-twitter"></i>
                        </a>
                        <a href="#" class="social-link">
                            <i class="fab fa-instagram"></i>
                        </a>
                        <a href="#" class="social-link">
                            <i class="fab fa-twitch"></i>
                        </a>
                        <a href="#" class="social-link">
                            <i class="fab fa-youtube"></i>
                        </a>
                        <a href="#" class="social-link">
                            <i class="fab fa-discord"></i>
                        </a>
                    </div>
                </div>
                
                <div class="footer-links">
                    <h3>Snelle Links</h3>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#news">Nieuws</a></li>
                        <li><a href="#reviews">Reviews</a></li>
                        <li><a href="#games">Games</a></li>
                        <li><a href="#community">Community</a></li>
                        <li><a href="#leaderboard">Leaderboard</a></li>
                    </ul>
                </div>
                
                <div class="footer-links">
                    <h3>Informatie</h3>
                    <ul>
                        <li><a href="#">Over Ons</a></li>
                        <li><a href="#">Contact</a></li>
                        <li><a href="#">Privacybeleid</a></li>
                        <li><a href="#">Voorwaarden</a></li>
                        <li><a href="#">Cookiebeleid</a></li>
                        <li><a href="#">FAQ</a></li>
                    </ul>
                </div>
                
                <div class="footer-links">
                    <h3>Community</h3>
                    <ul>
                        <li><a href="#">Forum</a></li>
                        <li><a href="#">Events</a></li>
                        <li><a href="#">Teams</a></li>
                        <li><a href="#">Guides</a></li>
                        <li><a href="#">Streams</a></li>
                        <li><a href="#">Shop</a></li>
                    </ul>
                </div>
            </div>
            
            <div class="footer-bottom">
                <p>&copy; 2025 MODAWIGAMES. Alle rechten voorbehouden. Alle game-afbeeldingen zijn eigendom van hun respectieve eigenaren.</p>
            </div>
        </div>
    </footer>

    <!-- Thema switcher -->
    <div class="theme-switcher">
        <div class="theme-btn default-theme active" onclick="changeTheme('default')" title="Standaard Thema"></div>
        <div class="theme-btn retro-theme" onclick="changeTheme('retro')" title="Retro Thema"></div>
        <div class="theme-btn fantasy-theme" onclick="changeTheme('fantasy')" title="Fantasy Thema"></div>
        <div class="theme-btn futuristic-theme" onclick="changeTheme('futuristic')" title="Futuristisch Thema"></div>
    </div>

    <!-- Scripts -->
    <script>
        // Verberg loading screen wanneer pagina geladen is
        window.addEventListener('load', function() {
            const loadingScreen = document.querySelector('.loading-screen');
            loadingScreen.style.opacity = '0';
            setTimeout(() => {
                loadingScreen.style.display = 'none';
            }, 500);
        });

        // Thema switcher functionaliteit
        function changeTheme(theme) {
            document.body.className = theme + '-theme';
            
            // Update active knop in thema switcher
            document.querySelectorAll('.theme-btn').forEach(btn => {
                btn.classList.remove('active');
            });
            document.querySelector(`.theme-btn.${theme}-theme`).classList.add('active');
            
            // Toon melding
            showToast(`Thema gewijzigd naar: ${theme.charAt(0).toUpperCase() + theme.slice(1)}`, 'success');
        }

        // Toast meldingen
        function showToast(message, type) {
            const toast = document.createElement('div');
            toast.className = `toast toast-${type}`;
            toast.innerHTML = `
                <div class="toast-icon">
                    <i class="fas fa-${type === 'success' ? 'check-circle' : type === 'error' ? 'times-circle' : type === 'warning' ? 'exclamation-triangle' : 'info-circle'}"></i>
                </div>
                <div class="toast-message">${message}</div>
                <button class="toast-close">
                    <i class="fas fa-times"></i>
                </button>
            `;
            
            document.body.appendChild(toast);
            
            setTimeout(() => {
                toast.classList.add('show');
            }, 100);
            
            // Verwijder toast na klik op sluiten
            toast.querySelector('.toast-close').addEventListener('click', () => {
                toast.classList.remove('show');
                setTimeout(() => {
                    toast.remove();
                }, 300);
            });
            
            // Verwijder toast automatisch na 5 seconden
            setTimeout(() => {
                toast.classList.remove('show');
                setTimeout(() => {
                    toast.remove();
                }, 300);
            }, 5000);
        }

        // Animaties voor elementen wanneer ze in beeld komen
        const animateOnScroll = function() {
            const elements = document.querySelectorAll('.news-card, .review-card, .game-card, .achievement, .quest, .audio-player');
            
            elements.forEach(element => {
                const elementPosition = element.getBoundingClientRect().top;
                const windowHeight = window.innerHeight;
                
                if (elementPosition < windowHeight - 100) {
                    element.classList.add('animate__animated', 'animate__fadeInUp');
                }
            });
        };

        // Voeg scroll event listener toe
        window.addEventListener('scroll', animateOnScroll);
        
        // Voer een keer uit bij laden
        animateOnScroll();

        // Progress bars animeren
        document.querySelectorAll('.progress-bar, .player-progress-bar, .quest-progress-bar, .achievement-progress-bar').forEach(bar => {
            const width = bar.style.width;
            bar.style.width = '0';
            setTimeout(() => {
                bar.style.width = width;
            }, 500);
        });

        // Audio player functionaliteit
        document.querySelectorAll('.player-btn').forEach(btn => {
            btn.addEventListener('click', function() {
                const icon = this.querySelector('i');
                if (icon.classList.contains('fa-play')) {
                    icon.classList.remove('fa-play');
                    icon.classList.add('fa-pause');
                } else {
                    icon.classList.remove('fa-pause');
                    icon.classList.add('fa-play');
                }
            });
        });

        // Tooltip initialisatie
        document.querySelectorAll('.platform-icon').forEach(icon => {
            const platform = icon.getAttribute('title');
            icon.setAttribute('data-tooltip', platform);
            icon.classList.add('tooltip');
            
            const tooltip = document.createElement('span');
            tooltip.className = 'tooltip-text';
            tooltip.textContent = platform;
            icon.appendChild(tooltip);
        });

        // Smooth scrolling voor anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                const targetElement = document.querySelector(targetId);
                
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });

        // Laad meer content bij scrollen (oneindig scrollen)
        let isLoading = false;
        window.addEventListener('scroll', function() {
            if ((window.innerHeight + window.scrollY) >= document.body.offsetHeight - 500 && !isLoading) {
                isLoading = true;
                
                // Simuleer laden van meer content
                setTimeout(() => {
                    // Hier zou je echte content kunnen laden via AJAX
                    console.log('Meer content laden...');
                    isLoading = false;
                }, 1000);
            }
        });
    </script>
</body>
</html>
