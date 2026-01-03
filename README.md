<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CYBER SECURITY GAME OPTIMIZER - Hacker An Ninh Mạng</title>
    <meta name="description" content="Công cụ tối ưu game an ninh mạng chuyên nghiệp - Tăng FPS 120, giảm lag 90%, hack hiệu suất thiết bị.">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        :root {
            --hacker-green: #00ff00;
            --cyber-blue: #0088ff;
            --matrix-purple: #aa00ff;
            --neon-pink: #ff00aa;
            --dark-bg: #050510;
            --darker-bg: #030308;
            --terminal-bg: #0a0a15;
        }
        
        body {
            font-family: 'Courier New', 'Consolas', 'Monaco', monospace;
            background-color: var(--dark-bg);
            color: var(--hacker-green);
            min-height: 100vh;
            overflow-x: hidden;
            position: relative;
            background-image: 
                radial-gradient(circle at 20% 30%, rgba(0, 136, 255, 0.05) 0%, transparent 20%),
                radial-gradient(circle at 80% 70%, rgba(170, 0, 255, 0.05) 0%, transparent 20%);
        }
        
        /* Cyber Grid Background */
        .cyber-grid {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: 
                linear-gradient(rgba(0, 136, 255, 0.1) 1px, transparent 1px),
                linear-gradient(90deg, rgba(0, 136, 255, 0.1) 1px, transparent 1px);
            background-size: 50px 50px;
            z-index: -3;
            opacity: 0.3;
        }
        
        /* Binary Rain */
        .binary-rain {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -2;
            opacity: 0.15;
            pointer-events: none;
        }
        
        /* Scanlines */
        .scanlines {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(
                to bottom,
                transparent 50%,
                rgba(0, 255, 0, 0.03) 50%
            );
            background-size: 100% 4px;
            z-index: -1;
            pointer-events: none;
            opacity: 0.3;
        }
        
        /* Container */
        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 25px;
            position: relative;
            z-index: 1;
        }
        
        /* Main Header */
        .cyber-header {
            background: linear-gradient(135deg, rgba(5, 10, 20, 0.95), rgba(3, 8, 18, 0.98));
            border: 2px solid var(--cyber-blue);
            border-radius: 0;
            padding: 30px;
            margin-bottom: 40px;
            position: relative;
            overflow: hidden;
            box-shadow: 
                0 0 40px rgba(0, 136, 255, 0.3),
                inset 0 0 20px rgba(0, 255, 0, 0.1);
        }
        
        .cyber-header::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 2px;
            background: linear-gradient(90deg, 
                transparent, 
                var(--neon-pink), 
                var(--cyber-blue), 
                var(--hacker-green),
                transparent);
            animation: scanline 3s linear infinite;
        }
        
        .cyber-header::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 2px;
            background: linear-gradient(90deg, 
                transparent, 
                var(--hacker-green), 
                var(--cyber-blue), 
                var(--neon-pink),
                transparent);
            animation: scanline-reverse 4s linear infinite;
        }
        
        @keyframes scanline {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }
        
        @keyframes scanline-reverse {
            0% { transform: translateX(100%); }
            100% { transform: translateX(-100%); }
        }
        
        .main-title {
            font-size: 3.5rem;
            text-align: center;
            background: linear-gradient(90deg, var(--hacker-green), var(--cyber-blue), var(--matrix-purple));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            margin-bottom: 20px;
            letter-spacing: 3px;
            font-weight: 900;
            text-transform: uppercase;
            text-shadow: 0 0 30px rgba(0, 136, 255, 0.5);
            position: relative;
            padding-bottom: 15px;
        }
        
        .main-title::after {
            content: "";
            position: absolute;
            bottom: 0;
            left: 25%;
            width: 50%;
            height: 3px;
            background: linear-gradient(90deg, transparent, var(--hacker-green), transparent);
        }
        
        .tagline {
            text-align: center;
            font-size: 1.3rem;
            color: var(--cyber-blue);
            margin-bottom: 25px;
            letter-spacing: 2px;
            text-shadow: 0 0 15px rgba(0, 136, 255, 0.5);
        }
        
        /* Status Badges */
        .badge-container {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            margin-top: 30px;
        }
        
        .cyber-badge {
            display: flex;
            align-items: center;
            background: rgba(0, 20, 40, 0.7);
            border: 1px solid var(--cyber-blue);
            padding: 12px 25px;
            border-radius: 0;
            font-size: 1.1rem;
            position: relative;
            overflow: hidden;
            transition: all 0.3s;
            min-width: 200px;
            justify-content: center;
        }
        
        .cyber-badge:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 136, 255, 0.4);
            border-color: var(--hacker-green);
        }
        
        .cyber-badge::before {
            content: "";
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(0, 255, 0, 0.1), transparent);
            transition: left 0.5s;
        }
        
        .cyber-badge:hover::before {
            left: 100%;
        }
        
        /* Dashboard Cards */
        .dashboard {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin: 40px 0;
        }
        
        .stat-card {
            background: linear-gradient(135deg, rgba(5, 15, 25, 0.9), rgba(3, 10, 20, 0.95));
            border: 1px solid var(--cyber-blue);
            border-radius: 0;
            padding: 30px;
            position: relative;
            overflow: hidden;
            transition: all 0.4s;
            min-height: 200px;
        }
        
        .stat-card:hover {
            transform: translateY(-10px) scale(1.02);
            border-color: var(--hacker-green);
            box-shadow: 
                0 15px 35px rgba(0, 136, 255, 0.3),
                inset 0 0 30px rgba(0, 255, 0, 0.05);
        }
        
        .stat-card::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: linear-gradient(to bottom, var(--hacker-green), var(--cyber-blue));
        }
        
        .stat-value {
            font-size: 4.5rem;
            font-weight: 900;
            color: transparent;
            background: linear-gradient(135deg, var(--hacker-green), var(--cyber-blue));
            -webkit-background-clip: text;
            background-clip: text;
            text-align: center;
            margin: 20px 0;
            font-family: 'Orbitron', 'Courier New', monospace;
            text-shadow: 0 0 20px rgba(0, 255, 0, 0.3);
        }
        
        .stat-label {
            text-align: center;
            color: var(--cyber-blue);
            font-size: 1.2rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            margin-top: 15px;
        }
        
        /* Feature Toggles */
        .feature-panel {
            background: linear-gradient(135deg, rgba(8, 15, 30, 0.95), rgba(5, 10, 25, 0.98));
            border: 2px solid var(--cyber-blue);
            padding: 35px;
            margin: 40px 0;
            position: relative;
            overflow: hidden;
        }
        
        .panel-title {
            color: var(--hacker-green);
            font-size: 2rem;
            margin-bottom: 30px;
            display: flex;
            align-items: center;
            border-bottom: 1px solid rgba(0, 136, 255, 0.3);
            padding-bottom: 15px;
        }
        
        .panel-title i {
            margin-right: 15px;
            color: var(--cyber-blue);
            font-size: 2.2rem;
        }
        
        .toggle-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }
        
        .cyber-toggle {
            background: rgba(10, 20, 40, 0.7);
            border: 1px solid var(--cyber-blue);
            padding: 25px;
            display: flex;
            align-items: center;
            cursor: pointer;
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
        }
        
        .cyber-toggle:hover {
            background: rgba(15, 30, 60, 0.9);
            transform: translateX(10px);
            border-color: var(--hacker-green);
        }
        
        .cyber-toggle.active {
            background: rgba(20, 40, 80, 0.9);
            border-color: var(--hacker-green);
            box-shadow: 
                0 0 20px rgba(0, 255, 0, 0.3),
                inset 0 0 20px rgba(0, 136, 255, 0.1);
        }
        
        .toggle-checkbox {
            position: relative;
            width: 50px;
            height: 25px;
            margin-right: 20px;
            -webkit-appearance: none;
            background: rgba(0, 20, 40, 0.8);
            border: 2px solid var(--cyber-blue);
            border-radius: 25px;
            outline: none;
            cursor: pointer;
            transition: all 0.3s;
        }
        
        .toggle-checkbox:checked {
            background: var(--hacker-green);
            border-color: var(--hacker-green);
        }
        
        .toggle-checkbox::before {
            content: "";
            position: absolute;
            width: 21px;
            height: 21px;
            border-radius: 50%;
            top: 1px;
            left: 1px;
            background: var(--cyber-blue);
            transition: all 0.3s;
        }
        
        .toggle-checkbox:checked::before {
            left: 26px;
            background: #000;
            box-shadow: 0 0 10px var(--hacker-green);
        }
        
        .toggle-label {
            flex-grow: 1;
        }
        
        .toggle-name {
            color: var(--hacker-green);
            font-size: 1.4rem;
            font-weight: bold;
            margin-bottom: 8px;
        }
        
        .toggle-desc {
            color: var(--cyber-blue);
            font-size: 0.95rem;
        }
        
        /* Slider Controls */
        .slider-panel {
            background: rgba(5, 15, 25, 0.9);
            border: 1px solid var(--cyber-blue);
            padding: 30px;
            margin: 30px 0;
        }
        
        .slider-container {
            margin: 25px 0;
        }
        
        .slider-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
        }
        
        .slider-title {
            color: var(--hacker-green);
            font-size: 1.5rem;
        }
        
        .slider-value {
            color: var(--cyber-blue);
            font-size: 1.8rem;
            font-weight: bold;
            font-family: 'Orbitron', monospace;
        }
        
        .cyber-slider {
            width: 100%;
            height: 15px;
            -webkit-appearance: none;
            background: linear-gradient(90deg, 
                #003300, 
                #00aa00, 
                #00ff00,
                #0088ff,
                #aa00ff);
            border-radius: 0;
            outline: none;
            border: 1px solid var(--cyber-blue);
            position: relative;
            overflow: hidden;
        }
        
        .cyber-slider::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 35px;
            height: 35px;
            background: #000;
            border: 3px solid var(--hacker-green);
            cursor: pointer;
            box-shadow: 
                0 0 20px var(--hacker-green),
                0 0 40px var(--hacker-green);
            border-radius: 50%;
            transition: all 0.2s;
        }
        
        .cyber-slider::-webkit-slider-thumb:hover {
            transform: scale(1.2);
            box-shadow: 
                0 0 30px var(--hacker-green),
                0 0 60px var(--hacker-green);
        }
        
        /* Action Buttons - ĐẶC BIỆT */
        .action-panel {
            margin: 50px 0;
        }
        
        .button-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }
        
        .cyber-button {
            position: relative;
            background: linear-gradient(135deg, 
                rgba(0, 40, 80, 0.8), 
                rgba(0, 20, 40, 0.9));
            color: var(--hacker-green);
            border: none;
            padding: 25px 35px;
            font-family: 'Orbitron', 'Courier New', monospace;
            font-size: 1.5rem;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 3px;
            cursor: pointer;
            overflow: hidden;
            transition: all 0.4s;
            text-align: center;
            border: 2px solid var(--cyber-blue);
            box-shadow: 
                0 0 20px rgba(0, 136, 255, 0.3),
                inset 0 0 20px rgba(0, 255, 0, 0.05);
        }
        
        .cyber-button::before,
        .cyber-button::after {
            content: "";
            position: absolute;
            width: 0;
            height: 0;
            background: var(--hacker-green);
            transition: all 0.3s;
            z-index: 1;
        }
        
        .cyber-button::before {
            top: 0;
            left: 0;
        }
        
        .cyber-button::after {
            bottom: 0;
            right: 0;
        }
        
        .cyber-button:hover {
            transform: translateY(-8px) scale(1.05);
            color: #000;
            background: linear-gradient(135deg, 
                var(--hacker-green), 
                var(--cyber-blue));
            box-shadow: 
                0 15px 35px rgba(0, 255, 0, 0.5),
                0 0 50px rgba(0, 136, 255, 0.4),
                inset 0 0 30px rgba(255, 255, 255, 0.1);
            border-color: var(--hacker-green);
        }
        
        .cyber-button:hover::before,
        .cyber-button:hover::after {
            width: 100%;
            height: 100%;
        }
        
        .cyber-button span {
            position: relative;
            z-index: 2;
            transition: color 0.3s;
        }
        
        .cyber-button:hover span {
            color: #000;
        }
        
        .cyber-button.primary {
            grid-column: span 2;
            background: linear-gradient(135deg, 
                rgba(0, 60, 120, 0.9), 
                rgba(0, 30, 60, 0.95));
            font-size: 1.8rem;
            padding: 30px;
            border: 3px solid var(--hacker-green);
        }
        
        .cyber-button.primary:hover {
            background: linear-gradient(135deg, 
                var(--hacker-green), 
                var(--cyber-blue),
                var(--matrix-purple));
            animation: pulse-primary 2s infinite;
        }
        
        @keyframes pulse-primary {
            0%, 100% { box-shadow: 0 0 30px rgba(0, 255, 0, 0.6), 0 0 60px rgba(0, 136, 255, 0.4); }
            50% { box-shadow: 0 0 50px rgba(0, 255, 0, 0.8), 0 0 100px rgba(0, 136, 255, 0.6); }
        }
        
        /* Terminal Window */
        .terminal-window {
            background: rgba(5, 10, 20, 0.95);
            border: 2px solid var(--cyber-blue);
            padding: 25px;
            margin: 40px 0;
            position: relative;
            font-family: 'Courier New', monospace;
            font-size: 1.1rem;
            line-height: 1.6;
            max-height: 500px;
            overflow-y: auto;
        }
        
        .terminal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid var(--cyber-blue);
            padding-bottom: 15px;
            margin-bottom: 20px;
        }
        
        .terminal-title {
            color: var(--hacker-green);
            font-size: 1.5rem;
            font-weight: bold;
        }
        
        .terminal-controls {
            display: flex;
            gap: 10px;
        }
        
        .terminal-btn {
            width: 15px;
            height: 15px;
            border-radius: 50%;
            cursor: pointer;
        }
        
        .terminal-btn.close { background: #ff5f56; }
        .terminal-btn.minimize { background: #ffbd2e; }
        .terminal-btn.maximize { background: #27ca3f; }
        
        .terminal-line {
            margin-bottom: 10px;
            color: var(--cyber-blue);
            padding-left: 20px;
            position: relative;
            animation: typing 0.5s steps(40, end);
        }
        
        .terminal-line::before {
            content: "> ";
            position: absolute;
            left: 0;
            color: var(--hacker-green);
            font-weight: bold;
        }
        
        .terminal-line.success { color: var(--hacker-green); }
        .terminal-line.warning { color: #ffaa00; }
        .terminal-line.error { color: #ff5555; }
        .terminal-line.info { color: var(--cyber-blue); }
        
        /* Progress Bars */
        .progress-panel {
            margin: 40px 0;
        }
        
        .progress-container {
            margin: 25px 0;
        }
        
        .progress-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
            color: var(--hacker-green);
            font-size: 1.2rem;
        }
        
        .cyber-progress {
            width: 100%;
            height: 25px;
            background: rgba(0, 20, 40, 0.8);
            border: 1px solid var(--cyber-blue);
            border-radius: 0;
            position: relative;
            overflow: hidden;
        }
        
        .cyber-progress::after {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            height: 100%;
            background: linear-gradient(90deg, 
                var(--hacker-green), 
                var(--cyber-blue));
            width: 0;
            transition: width 1s ease-in-out;
            animation: progress-glow 2s infinite;
        }
        
        @keyframes progress-glow {
            0%, 100% { box-shadow: 0 0 10px var(--hacker-green); }
            50% { box-shadow: 0 0 20px var(--hacker-green); }
        }
        
        /* Footer */
        .cyber-footer {
            text-align: center;
            margin-top: 60px;
            padding-top: 30px;
            border-top: 2px solid var(--cyber-blue);
            color: var(--cyber-blue);
            font-size: 0.9rem;
            position: relative;
        }
        
        .cyber-footer::before {
            content: "";
            position: absolute;
            top: -2px;
            left: 50%;
            transform: translateX(-50%);
            width: 50%;
            height: 2px;
            background: linear-gradient(90deg, transparent, var(--hacker-green), transparent);
        }
        
        /* Particle Effect */
        .particle {
            position: fixed;
            width: 4px;
            height: 4px;
            background: var(--hacker-green);
            border-radius: 50%;
            pointer-events: none;
            z-index: -1;
            opacity: 0.7;
        }
        
        /* Mobile Responsive */
        @media (max-width: 768px) {
            .container { padding: 15px; }
            .main-title { font-size: 2.2rem; }
            .dashboard, .toggle-grid, .button-grid { grid-template-columns: 1fr; }
            .cyber-button.primary { grid-column: span 1; }
            .stat-value { font-size: 3.5rem; }
            .feature-panel, .slider-panel { padding: 20px; }
        }
    </style>
</head>
<body>
    <!-- Background Elements -->
    <div class="cyber-grid"></div>
    <div class="binary-rain" id="binaryRain"></div>
    <div class="scanlines"></div>
    
    <div class="container">
        <!-- Main Header -->
        <div class="cyber-header">
            <h1 class="main-title">
                <i class="fas fa-shield-alt"></i> CYBER GAME OPTIMIZER
            </h1>
            <p class="tagline">ADVANCED SECURITY OPTIMIZATION TOOL | PENETRATION TESTING ACTIVE</p>
            
            <div class="badge-container">
                <div class="cyber-badge">
                    <i class="fas fa-bolt" style="margin-right: 10px; color: var(--hacker-green);"></i>
                    <span>FPS BOOST 120%</span>
                </div>
                <div class="cyber-badge">
                    <i class="fas fa-network-wired" style="margin-right: 10px; color: var(--cyber-blue);"></i>
                    <span>LATENCY REDUCTION 90%</span>
                </div>
                <div class="cyber-badge">
                    <i class="fas fa-memory" style="margin-right: 10px; color: var(--matrix-purple);"></i>
                    <span>RAM OPTIMIZATION 200%</span>
                </div>
                <div class="cyber-badge">
                    <i class="fas fa-user-secret" style="margin-right: 10px; color: var(--neon-pink);"></i>
                    <span>SECURITY MODE ACTIVE</span>
                </div>
            </div>
        </div>
        
        <!-- Dashboard Stats -->
        <div class="dashboard">
            <div class="stat-card">
                <div class="stat-label">CURRENT FPS</div>
                <div class="stat-value" id="currentFPS">60</div>
                <div class="stat-label">TARGET: 120 FPS</div>
            </div>
            
            <div class="stat-card">
                <div class="stat-label">RESPONSE TIME</div>
                <div class="stat-value" id="responseTime">16ms</div>
                <div class="stat-label">TARGET: &lt;8ms</div>
            </div>
            
            <div class="stat-card">
                <div class="stat-label">CPU LOAD</div>
                <div class="stat-value" id="cpuLoad">42%</div>
                <div class="stat-label">OPTIMIZED: 28%</div>
            </div>
            
            <div class="stat-card">
                <div class="stat-label">MEMORY FREE</div>
                <div class="stat-value" id="memoryFree">3.2GB</div>
                <div class="stat-label">TOTAL: 8GB</div>
            </div>
        </div>
        
        <!-- Optimization Features -->
        <div class="feature-panel">
            <div class="panel-title">
                <i class="fas fa-user-secret"></i> CYBER OPTIMIZATION MODULES
            </div>
            
            <div class="toggle-grid">
                <label class="cyber-toggle active" id="toggle1">
                    <input type="checkbox" class="toggle-checkbox" checked>
                    <div class="toggle-label">
                        <div class="toggle-name">⚡ ANIMATION REDUCTION</div>
                        <div class="toggle-desc">Increase FPS by 30% - Reduce visual effects</div>
                    </div>
                    <i class="fas fa-check-circle" style="color: var(--hacker-green); font-size: 1.5rem;"></i>
                </label>
                
                <label class="cyber-toggle active" id="toggle2">
                    <input type="checkbox" class="toggle-checkbox" checked>
                    <div class="toggle-label">
                        <div class="toggle-name">🎯 SENSITIVITY BOOST</div>
                        <div class="toggle-desc">Increase touch response by 150%</div>
                    </div>
                    <i class="fas fa-check-circle" style="color: var(--hacker-green); font-size: 1.5rem;"></i>
                </label>
                
                <label class="cyber-toggle active" id="toggle3">
                    <input type="checkbox" class="toggle-checkbox" checked>
                    <div class="toggle-label">
                        <div class="toggle-name">🚀 FPS OVERCLOCK</div>
                        <div class="toggle-desc">Push FPS to maximum 120+</div>
                    </div>
                    <i class="fas fa-check-circle" style="color: var(--hacker-green); font-size: 1.5rem;"></i>
                </label>
                
                <label class="cyber-toggle active" id="toggle4">
                    <input type="checkbox" class="toggle-checkbox" checked>
                    <div class="toggle-label">
                        <div class="toggle-name">🛡️ HEAVY GAME LAG FIX</div>
                        <div class="toggle-desc">Reduce lag by 90% in heavy games</div>
                    </div>
                    <i class="fas fa-check-circle" style="color: var(--hacker-green); font-size: 1.5rem;"></i>
                </label>
                
                <label class="cyber-toggle active" id="toggle5">
                    <input type="checkbox" class="toggle-checkbox" checked>
                    <div class="toggle-label">
                        <div class="toggle-name">💾 RAM MEMORY BOOST</div>
                        <div class="toggle-desc">Free up to 3GB+ of RAM</div>
                    </div>
                    <i class="fas fa-check-circle" style="color: var(--hacker-green); font-size: 1.5rem;"></i>
                </label>
                
                <label class="cyber-toggle active" id="toggle6">
                    <input type="checkbox" class="toggle-checkbox" checked>
                    <div class="toggle-label">
                        <div class="toggle-name">👆 TOUCH DELAY FIX</div>
                        <div class="toggle-desc">Reduce touch delay by 80%</div>
                    </div>
                    <i class="fas fa-check-circle" style="color: var(--hacker-green); font-size: 1.5rem;"></i>
                </label>
                
                <label class="cyber-toggle active" id="toggle7">
                    <input type="checkbox" class="toggle-checkbox" checked>
                    <div class="toggle-label">
                        <div class="toggle-name">🔋 BATTERY SAVER</div>
                        <div class="toggle-desc">Increase battery life by 60+ minutes</div>
                    </div>
                    <i class="fas fa-check-circle" style="color: var(--hacker-green); font-size: 1.5rem;"></i>
                </label>
                
                <label class="cyber-toggle active" id="toggle8">
                    <input type="checkbox" class="toggle-checkbox" checked>
                    <div class="toggle-label">
                        <div class="toggle-name">🌐 INTERNET OPTIMIZATION</div>
                        <div class="toggle-desc">Reduce ping by 70%</div>
                    </div>
                    <i class="fas fa-check-circle" style="color: var(--hacker-green); font-size: 1.5rem;"></i>
                </label>
            </div>
        </div>
        
        <!-- Slider Controls -->
        <div class="slider-panel">
            <div class="slider-container">
                <div class="slider-header">
                    <div class="slider-title">
                        <i class="fas fa-sliders-h"></i> OPTIMIZATION INTENSITY
                    </div>
                    <div class="slider-value" id="intensityValue">85%</div>
                </div>
                <input type="range" min="1" max="100" value="85" class="cyber-slider" id="intensitySlider">
            </div>
            
            <div class="slider-container">
                <div class="slider-header">
                    <div class="slider-title">
                        <i class="fas fa-tachometer-alt"></i> FPS TARGET
                    </div>
                    <div class="slider-value" id="fpsTargetValue">120</div>
                </div>
                <input type="range" min="30" max="120" value="120" class="cyber-slider" id="fpsTargetSlider">
            </div>
            
            <div class="slider-container">
                <div class="slider-header">
                    <div class="slider-title">
                        <i class="fas fa-wifi"></i> NETWORK PRIORITY
                    </div>
                    <div class="slider-value" id="networkValue">EXTREME</div>
                </div>
                <input type="range" min="1" max="100" value="95" class="cyber-slider" id="networkSlider">
            </div>
        </div>
        
        <!-- Action Buttons -->
        <div class="action-panel">
            <div class="button-grid">
                <button class="cyber-button" id="scanBtn">
                    <span><i class="fas fa-search"></i> SYSTEM SCAN</span>
                </button>
                
                <button class="cyber-button" id="analyzeBtn">
                    <span><i class="fas fa-chart-line"></i> PERFORMANCE ANALYZE</span>
                </button>
                
                <button class="cyber-button primary" id="optimizeBtn">
                    <span><i class="fas fa-rocket"></i> LAUNCH FULL OPTIMIZATION</span>
                </button>
                
                <button class="cyber-button" id="securityBtn">
                    <span><i class="fas fa-shield-alt"></i> ACTIVATE SECURITY MODE</span>
                </button>
                
                <button class="cyber-button" id="resetBtn">
                    <span><i class="fas fa-redo"></i> SYSTEM RESET</span>
                </button>
            </div>
        </div>
        
        <!-- Progress Bars -->
        <div class="progress-panel">
            <div class="panel-title">
                <i class="fas fa-chart-bar"></i> OPTIMIZATION PROGRESS
            </div>
            
            <div class="progress-container">
                <div class="progress-label">
                    <span>FPS IMPROVEMENT</span>
                    <span id="fpsProgress">0%</span>
                </div>
                <div class="cyber-progress" id="fpsProgressBar"></div>
            </div>
            
            <div class="progress-container">
                <div class="progress-label">
                    <span>LATENCY REDUCTION</span>
                    <span id="latencyProgress">0%</span>
                </div>
                <div class="cyber-progress" id="latencyProgressBar"></div>
            </div>
            
            <div class="progress-container">
                <div class="progress-label">
                    <span>MEMORY OPTIMIZATION</span>
                    <span id="memoryProgress">0%</span>
                </div>
                <div class="cyber-progress" id="memoryProgressBar"></div>
            </div>
        </div>
        
        <!-- Terminal Output -->
        <div class="terminal-window">
            <div class="terminal-header">
                <div class="terminal-title">
                    <i class="fas fa-terminal"></i> SYSTEM TERMINAL
                </div>
                <div class="terminal-controls">
                    <div class="terminal-btn close" id="termClose"></div>
                    <div class="terminal-btn minimize" id="termMinimize"></div>
                    <div class="terminal-btn maximize" id="termMaximize"></div>
                </div>
            </div>
            
            <div id="terminalOutput">
                <div class="terminal-line success">Cyber Game Optimizer v5.0 initialized</div>
                <div class="terminal-line">Loading security protocols...</div>
                <div class="terminal-line success">Security mode: ACTIVE</div>
                <div class="terminal-line">Detected device: Qualcomm Snapdragon 888 | Adreno 660 GPU</div>
                <div class="terminal-line">RAM: 8GB LPDDR5 | Storage: 256GB UFS 3.1</div>
                <div class="terminal-line">Current FPS: 60 | Target FPS: 120+</div>
                <div class="terminal-line">Network latency: 45ms | Target: &lt;20ms</div>
                <div class="terminal-line warning">Optimization required for maximum performance</div>
                <div class="terminal-line info">All optimization modules ready for activation</div>
                <div class="terminal-line">Terminal ready. Awaiting commands...</div>
            </div>
        </div>
        
        <!-- Footer -->
        <div class="cyber-footer">
            <p style="margin-bottom: 15px; font-size: 1.1rem;">
                <span class="blink">⚠️</span> CYBER SECURITY OPTIMIZATION TOOL v5.0 <span class="blink">⚠️</span>
            </p>
            <p style="color: var(--hacker-green); margin-bottom: 10px;">
                <i class="fas fa-lock"></i> ENCRYPTION: AES-256 | <i class="fas fa-shield-alt"></i> SECURITY: MAXIMUM
            </p>
            <p style="color: var(--cyber-blue); font-size: 0.8rem;">
                © 2024 Cyber Security Labs | This tool simulates optimization processes for educational purposes
            </p>
        </div>
    </div>

    <script>
        // Khởi tạo biến
        let intensity = 85;
        let fpsTarget = 120;
        let networkPriority = 95;
        let currentFPS = 60;
        let responseTime = 16;
        let cpuLoad = 42;
        let memoryFree = 3.2;
        let isOptimizing = false;
        let securityMode = false;
        
        // DOM Elements
        const currentFpsElement = document.getElementById('currentFPS');
        const responseTimeElement = document.getElementById('responseTime');
        const cpuLoadElement = document.getElementById('cpuLoad');
        const memoryFreeElement = document.getElementById('memoryFree');
        const intensitySlider = document.getElementById('intensitySlider');
        const intensityValue = document.getElementById('intensityValue');
        const fpsTargetSlider = document.getElementById('fpsTargetSlider');
        const fpsTargetValue = document.getElementById('fpsTargetValue');
        const networkSlider = document.getElementById('networkSlider');
        const networkValue = document.getElementById('networkValue');
        const scanBtn = document.getElementById('scanBtn');
        const analyzeBtn = document.getElementById('analyzeBtn');
        const optimizeBtn = document.getElementById('optimizeBtn');
        const securityBtn = document.getElementById('securityBtn');
        const resetBtn = document.getElementById('resetBtn');
        const terminalOutput = document.getElementById('terminalOutput');
        const fpsProgress = document.getElementById('fpsProgress');
        const latencyProgress = document.getElementById('latencyProgress');
        const memoryProgress = document.getElementById('memoryProgress');
        const fpsProgressBar = document.getElementById('fpsProgressBar');
        const latencyProgressBar = document.getElementById('latencyProgressBar');
        const memoryProgressBar = document.getElementById('memoryProgressBar');
        
        // Toggles
        const toggle1 = document.getElementById('toggle1');
        const toggle2 = document.getElementById('toggle2');
        const toggle3 = document.getElementById('toggle3');
        const toggle4 = document.getElementById('toggle4');
        const toggle5 = document.getElementById('toggle5');
        const toggle6 = document.getElementById('toggle6');
        const toggle7 = document.getElementById('toggle7');
        const toggle8 = document.getElementById('toggle8');
        
        // Terminal controls
        const termClose = document.getElementById('termClose');
        const termMinimize = document.getElementById('termMinimize');
        const termMaximize = document.getElementById('termMaximize');
        
        // Khởi tạo Binary Rain
        function initBinaryRain() {
            const chars = "01";
            const container = document.getElementById('binaryRain');
            
            for (let i = 0; i < 150; i++) {
                const char = document.createElement('div');
                char.textContent = chars.charAt(Math.floor(Math.random() * chars.length));
                char.style.position = 'absolute';
                char.style.color = Math.random() > 0.5 ? 'var(--hacker-green)' : 'var(--cyber-blue)';
                char.style.fontSize = Math.random() * 20 + 10 + 'px';
                char.style.fontWeight = 'bold';
                char.style.left = Math.random() * 100 + 'vw';
                char.style.top = '-50px';
                char.style.opacity = Math.random() * 0.7 + 0.1;
                char.style.animation = `binary-fall ${Math.random() * 10 + 5}s linear infinite`;
                char.style.animationDelay = Math.random() * 5 + 's';
                container.appendChild(char);
            }
            
            // Thêm CSS animation
            const style = document.createElement('style');
            style.textContent = `
                @keyframes binary-fall {
                    0% {
                        transform: translateY(0) rotate(0deg);
                        opacity: 1;
                    }
                    100% {
                        transform: translateY(100vh) rotate(360deg);
                        opacity: 0;
                    }
                }
            `;
            document.head.appendChild(style);
        }
        
        // Tạo particle effect
        function createParticles(x, y, color) {
            for (let i = 0; i < 15; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                particle.style.left = x + 'px';
                particle.style.top = y + 'px';
                particle.style.background = color;
                particle.style.transform = `translate(${Math.random() * 20 - 10}px, ${Math.random() * 20 - 10}px)`;
                
                document.body.appendChild(particle);
                
                // Animation
                const animation = particle.animate([
                    { transform: `translate(0, 0) scale(1)`, opacity: 1 },
                    { transform: `translate(${Math.random() * 100 - 50}px, ${Math.random() * 100 - 50}px) scale(0)`, opacity: 0 }
                ], {
                    duration: Math.random() * 1000 + 500,
                    easing: 'cubic-bezier(0.2, 0, 0.8, 1)'
                });
                
                animation.onfinish = () => particle.remove();
            }
        }
        
        // Thêm dòng vào terminal
        function addTerminalLine(text, type = '') {
            const line = document.createElement('div');
            line.className = `terminal-line ${type}`;
            line.textContent = text;
            terminalOutput.appendChild(line);
            terminalOutput.scrollTop = terminalOutput.scrollHeight;
        }
        
        // Cập nhật progress bars
        function updateProgressBars(fpsPercent, latencyPercent, memoryPercent) {
            fpsProgress.textContent = fpsPercent + '%';
            latencyProgress.textContent = latencyPercent + '%';
            memoryProgress.textContent = memoryPercent + '%';
            
            fpsProgressBar.style.setProperty('--width', fpsPercent + '%');
            latencyProgressBar.style.setProperty('--width', latencyPercent + '%');
            memoryProgressBar.style.setProperty('--width', memoryPercent + '%');
            
            // CSS variable cho width
            fpsProgressBar.style.width = fpsPercent + '%';
            latencyProgressBar.style.width = latencyPercent + '%';
            memoryProgressBar.style.width = memoryPercent + '%';
        }
        
        // Xử lý slider
        intensitySlider.addEventListener('input', function() {
            intensity = parseInt(this.value);
            intensityValue.textContent = intensity + '%';
            addTerminalLine(`Optimization intensity set to ${intensity}%`, 'info');
            
            // Hiệu ứng particle
            const rect = this.getBoundingClientRect();
            createParticles(rect.left + rect.width * (intensity/100), rect.top + rect.height/2, 'var(--hacker-green)');
        });
        
        fpsTargetSlider.addEventListener('input', function() {
            fpsTarget = parseInt(this.value);
            fpsTargetValue.textContent = fpsTarget;
            addTerminalLine(`FPS target set to ${fpsTarget}`, 'info');
        });
        
        networkSlider.addEventListener('input', function() {
            networkPriority = parseInt(this.value);
            let level = '';
            if (networkPriority < 33) level = 'LOW';
            else if (networkPriority < 66) level = 'MEDIUM';
            else if (networkPriority < 90) level = 'HIGH';
            else level = 'EXTREME';
            
            networkValue.textContent = level;
            addTerminalLine(`Network priority set to ${level}`, 'info');
        });
        
        // Xử lý toggle buttons
        [toggle1, toggle2, toggle3, toggle4, toggle5, toggle6, toggle7, toggle8].forEach((toggle, index) => {
            toggle.addEventListener('click', function(e) {
                const checkbox = this.querySelector('input');
                checkbox.checked = !checkbox.checked;
                
                if (checkbox.checked) {
                    this.classList.add('active');
                    this.querySelector('i.fa-check-circle').style.color = 'var(--hacker-green)';
                    addTerminalLine(`Module ${index+1}: ACTIVATED`, 'success');
                    
                    // Hiệu ứng particle
                    const rect = this.getBoundingClientRect();
                    createParticles(rect.left + rect.width/2, rect.top + rect.height/2, 'var(--hacker-green)');
                } else {
                    this.classList.remove('active');
                    this.querySelector('i.fa-check-circle').style.color = 'var(--cyber-blue)';
                    addTerminalLine(`Module ${index+1}: DEACTIVATED`, 'warning');
                }
            });
        });
        
        // System Scan Button
        scanBtn.addEventListener('click', function() {
            if (isOptimizing) return;
            
            addTerminalLine('Initiating deep system scan...', 'warning');
            
            // Hiệu ứng button
            const originalHtml = this.innerHTML;
            this.innerHTML = '<span><i class="fas fa-spinner fa-spin"></i> SCANNING...</span>';
            
            // Mô phỏng quét
            setTimeout(() => {
                addTerminalLine('Scanning hardware components...', 'info');
                setTimeout(() => {
                    addTerminalLine('Analyzing GPU performance...', 'info');
                    setTimeout(() => {
                        addTerminalLine('Checking memory allocation...', 'info');
                        setTimeout(() => {
                            addTerminalLine('Scan complete. System ready for optimization.', 'success');
                            this.innerHTML = originalHtml;
                            
                            // Cập nhật giá trị ngẫu nhiên
                            currentFPS = Math.floor(Math.random() * 20) + 40;
                            responseTime = Math.floor(Math.random() * 20) + 20;
                            cpuLoad = Math.floor(Math.random() * 30) + 40;
                            memoryFree = Math.random() * 2 + 2.5;
                            
                            currentFpsElement.textContent = currentFPS;
                            responseTimeElement.textContent = responseTime + 'ms';
                            cpuLoadElement.textContent = cpuLoad + '%';
                            memoryFreeElement.textContent = memoryFree.toFixed(1) + 'GB';
                            
                            // Hiệu ứng particle
                            const rect = this.getBoundingClientRect();
                            createParticles(rect.left + rect.width/2, rect.top + rect.height/2, 'var(--cyber-blue)');
                        }, 800);
                    }, 800);
                }, 800);
            }, 800);
        });
        
        // Analyze Button
        analyzeBtn.addEventListener('click', function() {
            if (isOptimizing) return;
            
            addTerminalLine('Analyzing performance metrics...', 'warning');
            
            // Hiệu ứng button
            const originalHtml = this.innerHTML;
            this.innerHTML = '<span><i class="fas fa-chart-line"></i> ANALYZING...</span>';
            
            // Tính toán hiệu suất
            setTimeout(() => {
                const improvement = Math.floor(intensity / 100 * 70);
                const latencyImprovement = Math.floor(intensity / 100 * 60);
                const memoryImprovement = Math.floor(intensity / 100 * 50);
                
                updateProgressBars(improvement, latencyImprovement, memoryImprovement);
                
                addTerminalLine(`FPS improvement potential: ${improvement}%`, 'info');
                addTerminalLine(`Latency reduction potential: ${latencyImprovement}%`, 'info');
                addTerminalLine(`Memory optimization potential: ${memoryImprovement}%`, 'info');
                addTerminalLine('Analysis complete. Ready for optimization.', 'success');
                
                this.innerHTML = originalHtml;
                
                // Hiệu ứng particle
                const rect = this.getBoundingClientRect();
                createParticles(rect.left + rect.width/2, rect.top + rect.height/2, 'var(--matrix-purple)');
            }, 1500);
        });
        
        // Optimize Button - NÚT CHÍNH ĐẶC BIỆT
        optimizeBtn.addEventListener('click', function() {
            if (isOptimizing) return;
            isOptimizing = true;
            
            addTerminalLine('INITIATING FULL SYSTEM OPTIMIZATION...', 'warning');
            addTerminalLine('This may take a few moments...', 'info');
            
            // Hiệu ứng button đặc biệt
            const originalHtml = this.innerHTML;
            this.innerHTML = '<span><i class="fas fa-cog fa-spin"></i> OPTIMIZING...</span>';
            this.style.animation = 'pulse-primary 0.5s infinite';
            
            // Mô phỏng tối ưu hóa từng bước
            let step = 0;
            const steps = [
                {text: 'Reducing system animations...', type: 'info'},
                {text: 'Overclocking GPU for maximum FPS...', type: 'info'},
                {text: 'Optimizing touch response algorithms...', type: 'info'},
                {text: 'Fixing heavy game lag issues...', type: 'info'},
                {text: 'Freeing up RAM memory...', type: 'info'},
                {text: 'Reducing touch delay...', type: 'info'},
                {text: 'Optimizing battery usage...', type: 'info'},
                {text: 'Improving network connection...', type: 'info'},
                {text: 'Applying security protocols...', type: 'info'},
                {text: 'Finalizing optimizations...', type: 'info'}
            ];
            
            const optimizeInterval = setInterval(() => {
                if (step < steps.length) {
                    addTerminalLine(steps[step].text, steps[step].type);
                    step++;
                    
                    // Cập nhật progress bars
                    const progress = Math.floor((step / steps.length) * 100);
                    updateProgressBars(progress, progress, progress);
                    
                    // Hiệu ứng particle ngẫu nhiên
                    const colors = ['var(--hacker-green)', 'var(--cyber-blue)', 'var(--matrix-purple)', 'var(--neon-pink)'];
                    const rect = this.getBoundingClientRect();
                    createParticles(
                        rect.left + Math.random() * rect.width,
                        rect.top + Math.random() * rect.height,
                        colors[Math.floor(Math.random() * colors.length)]
                    );
                } else {
                    clearInterval(optimizeInterval);
                    
                    // Tính toán kết quả cuối cùng
                    const finalFPS = Math.min(fpsTarget, Math.floor(currentFPS + (intensity / 100 * 60)));
                    const finalResponse = Math.max(4, Math.floor(responseTime - (intensity / 100 * 15)));
                    const finalCPU = Math.max(10, Math.floor(cpuLoad - (intensity / 100 * 30)));
                    const finalMemory = Math.min(8, memoryFree + (intensity / 100 * 3));
                    
                    // Cập nhật giá trị
                    currentFpsElement.textContent = finalFPS;
                    responseTimeElement.textContent = finalResponse + 'ms';
                    cpuLoadElement.textContent = finalCPU + '%';
                    memoryFreeElement.textContent = finalMemory.toFixed(1) + 'GB';
                    
                    // Cập nhật progress bars hoàn thành
                    updateProgressBars(100, 100, 100);
                    
                    addTerminalLine('OPTIMIZATION COMPLETE!', 'success');
                    addTerminalLine(`FPS: ${finalFPS} | Response: ${finalResponse}ms | CPU: ${finalCPU}% | RAM: ${finalMemory.toFixed(1)}GB`, 'success');
                    
                    // Khôi phục button
                    setTimeout(() => {
                        this.innerHTML = '<span><i class="fas fa-check-circle"></i> OPTIMIZATION SUCCESSFUL</span>';
                        this.style.animation = '';
                        
                        setTimeout(() => {
                            this.innerHTML = originalHtml;
                            isOptimizing = false;
                        }, 3000);
                    }, 1000);
                    
                    // Hiệu ứng particle mạnh
                    for (let i = 0; i < 50; i++) {
                        setTimeout(() => {
                            const rect = this.getBoundingClientRect();
                            createParticles(
                                rect.left + rect.width/2,
                                rect.top + rect.height/2,
                                Math.random() > 0.5 ? 'var(--hacker-green)' : 'var(--cyber-blue)'
                            );
                        }, i * 30);
                    }
                }
            }, 600);
        });
        
        // Security Mode Button
        securityBtn.addEventListener('click', function() {
            securityMode = !securityMode;
            
            if (securityMode) {
                addTerminalLine('ACTIVATING SECURITY MODE...', 'warning');
                addTerminalLine('Encrypting all connections...', 'info');
                addTerminalLine('Enabling firewall protection...', 'info');
                addTerminalLine('SECURITY MODE ACTIVATED', 'success');
                
                this.innerHTML = '<span><i class="fas fa-shield-alt"></i> SECURITY ACTIVE</span>';
                this.style.borderColor = 'var(--hacker-green)';
                this.style.background = 'linear-gradient(135deg, rgba(0, 40, 0, 0.9), rgba(0, 20, 0, 0.95))';
                
                // Thêm badge bảo mật
                const badge = document.createElement('div');
                badge.style.cssText = `
                    position: absolute;
                    top: -10px;
                    right: -10px;
                    background: var(--hacker-green);
                    color: #000;
                    padding: 5px 10px;
                    font-size: 0.8rem;
                    font-weight: bold;
                    border-radius: 0;
                    z-index: 10;
                `;
                badge.textContent = 'SECURE';
                this.appendChild(badge);
            } else {
                addTerminalLine('Security mode deactivated', 'warning');
                this.innerHTML = '<span><i class="fas fa-shield-alt"></i> ACTIVATE SECURITY MODE</span>';
                this.style.borderColor = '';
                this.style.background = '';
                
                const badge = this.querySelector('div[style*="position: absolute"]');
                if (badge) badge.remove();
            }
            
            // Hiệu ứng particle
            const rect = this.getBoundingClientRect();
            createParticles(rect.left + rect.width/2, rect.top + rect.height/2, 
                securityMode ? 'var(--hacker-green)' : 'var(--cyber-blue)');
        });
        
        // Reset Button
        resetBtn.addEventListener('click', function() {
            addTerminalLine('Resetting system to default settings...', 'warning');
            
            // Reset sliders
            intensitySlider.value = 85;
            fpsTargetSlider.value = 120;
            networkSlider.value = 95;
            
            intensity = 85;
            fpsTarget = 120;
            networkPriority = 95;
            
            intensityValue.textContent = '85%';
            fpsTargetValue.textContent = '120';
            networkValue.textContent = 'EXTREME';
            
            // Reset toggles
            [toggle1, toggle2, toggle3, toggle4, toggle5, toggle6, toggle7, toggle8].forEach(toggle => {
                toggle.classList.add('active');
                toggle.querySelector('input').checked = true;
                toggle.querySelector('i.fa-check-circle').style.color = 'var(--hacker-green)';
            });
            
            // Reset values
            currentFPS = 60;
            responseTime = 16;
            cpuLoad = 42;
            memoryFree = 3.2;
            
            currentFpsElement.textContent = currentFPS;
            responseTimeElement.textContent = responseTime + 'ms';
            cpuLoadElement.textContent = cpuLoad + '%';
            memoryFreeElement.textContent = memoryFree.toFixed(1) + 'GB';
            
            // Reset progress bars
            updateProgressBars(0, 0, 0);
            
            addTerminalLine('System reset complete. All settings restored to default.', 'success');
            
            // Hiệu ứng particle
            const rect = this.getBoundingClientRect();
            for (let i = 0; i < 20; i++) {
                setTimeout(() => {
                    createParticles(
                        rect.left + rect.width/2,
                        rect.top + rect.height/2,
                        'var(--neon-pink)'
                    );
                }, i * 50);
            }
        });
        
        // Terminal controls
        termClose.addEventListener('click', function() {
            terminalOutput.innerHTML = '';
            addTerminalLine('Terminal cleared. Type "help" for commands.', 'info');
        });
        
        termMinimize.addEventListener('click', function() {
            const terminal = document.querySelector('.terminal-window');
            terminal.style.maxHeight = terminal.style.maxHeight === '60px' ? '500px' : '60px';
        });
        
        termMaximize.addEventListener('click', function() {
            const terminal = document.querySelector('.terminal-window');
            terminal.style.maxHeight = terminal.style.maxHeight === '800px' ? '500px' : '800px';
        });
        
        // Khởi tạo
        window.addEventListener('load', function() {
            initBinaryRain();
            updateProgressBars(0, 0, 0);
            
            // Thêm CSS cho progress bars
            const style = document.createElement('style');
            style.textContent = `
                .cyber-progress::after {
                    width: var(--width, 0%);
                }
            `;
            document.head.appendChild(style);
            
            // Hiệu ứng khởi động
            setTimeout(() => {
                addTerminalLine('System initialization complete.', 'success');
                addTerminalLine('All modules loaded successfully.', 'success');
                addTerminalLine('Ready for optimization commands.', 'info');
            }, 1000);
        });
        
        // Hiệu ứng click cho tất cả button
        document.querySelectorAll('.cyber-button').forEach(button => {
            button.addEventListener('click', function(e) {
                // Hiệu ứng âm thanh giả (chỉ visual)
                const rect = this.getBoundingClientRect();
                createParticles(
                    e.clientX - rect.left,
                    e.clientY - rect.top,
                    'var(--hacker-green)'
                );
                
                // Hiệu ứng nhấn
                this.style.transform = 'translateY(-2px) scale(0.98)';
                setTimeout(() => {
                    this.style.transform = '';
                }, 150);
            });
        });
    </script>
</body>
</html>
