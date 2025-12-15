<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Perfil GitHub</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0d1117 0%, #161b22 100%);
            color: #c9d1d9;
            line-height: 1.6;
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
        }
        
        .container {
            background-color: #0d1117;
            border-radius: 15px;
            padding: 30px;
            margin-top: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            border: 1px solid #30363d;
        }
        
        header {
            text-align: center;
            padding: 30px 0;
            border-bottom: 2px solid #238636;
            margin-bottom: 30px;
        }
        
        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 5px solid #238636;
            margin-bottom: 20px;
            object-fit: cover;
        }
        
        h1 {
            color: #58a6ff;
            font-size: 2.5rem;
            margin-bottom: 10px;
        }
        
        .tagline {
            font-size: 1.2rem;
            color: #8b949e;
            margin-bottom: 20px;
        }
        
        h2 {
            color: #58a6ff;
            border-left: 4px solid #238636;
            padding-left: 15px;
            margin: 30px 0 20px 0;
        }
        
        h3 {
            color: #c9d1d9;
            margin: 25px 0 15px 0;
        }
        
        .section {
            margin-bottom: 40px;
            padding-bottom: 20px;
            border-bottom: 1px solid #30363d;
        }
        
        .skills-container {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
            margin-top: 20px;
        }
        
        .skill-item {
            background: #161b22;
            border-radius: 10px;
            padding: 15px;
            width: 120px;
            text-align: center;
            border: 1px solid #30363d;
            transition: transform 0.3s, border-color 0.3s;
        }
        
        .skill-item:hover {
            transform: translateY(-5px);
            border-color: #238636;
        }
        
        .skill-icon {
            font-size: 2.5rem;
            margin-bottom: 10px;
            color: #58a6ff;
        }
        
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .project-card {
            background: #161b22;
            border-radius: 10px;
            padding: 20px;
            border: 1px solid #30363d;
            transition: transform 0.3s;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
            border-color: #238636;
        }
        
        .project-title {
            color: #58a6ff;
            font-size: 1.3rem;
            margin-bottom: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-top: 15px;
        }
        
        .tech-tag {
            background: #0d1117;
            color: #8b949e;
            padding: 5px 10px;
            border-radius: 15px;
            font-size: 0.8rem;
            border: 1px solid #30363d;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
            flex-wrap: wrap;
        }
        
        .social-link {
            display: flex;
            align-items: center;
            gap: 8px;
            color: #c9d1d9;
            text-decoration: none;
            background: #161b22;
            padding: 12px 20px;
            border-radius: 8px;
            border: 1px solid #30363d;
            transition: all 0.3s;
        }
        
        .social-link:hover {
            background: #238636;
            color: white;
            transform: translateY(-3px);
        }
        
        .social-icon {
            font-size: 1.5rem;
        }
        
        .support-options {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
            flex-wrap: wrap;
        }
        
        .support-btn {
            background: #161b22;
            border: 2px solid #30363d;
            border-radius: 10px;
            padding: 15px 25px;
            color: #c9d1d9;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 10px;
            transition: all 0.3s;
            font-size: 1rem;
        }
        
        .support-btn:hover {
            background: #238636;
            color: white;
            border-color: #238636;
        }
        
        .checked {
            color: #238636;
        }
        
        .unchecked {
            color: #8b949e;
        }
        
        .stats-container {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
            flex-wrap: wrap;
        }
        
        .stat-card {
            background: #161b22;
            border-radius: 10px;
            padding: 20px;
            text-align: center;
            min-width: 150px;
            border: 1px solid #30363d;
        }
        
        .stat-number {
            font-size: 2rem;
            color: #58a6ff;
            font-weight: bold;
        }
        
        .stat-label {
            color: #8b949e;
            margin-top: 5px;
        }
        
        footer {
            text-align: center;
            margin-top: 40px;
            padding-top: 20px;
            border-top: 1px solid #30363d;
            color: #8b949e;
        }
        
        @media (max-width: 768px) {
            .projects-grid {
                grid-template-columns: 1fr;
            }
            
            .skills-container {
                justify-content: center;
            }
            
            .social-links, .support-options {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <!-- Reemplaza la URL con tu foto de perfil -->
            <img src="https://avatars.githubusercontent.com/u/12345678?v=4" alt="Foto de perfil" class="profile-img">
            <h1>[Tu Nombre]</h1>
            <p class="tagline">🚀 Desarrollador Full Stack apasionado por crear soluciones innovadoras</p>
            <p>Me especializo en desarrollo web, aplicaciones escalables y experiencias de usuario excepcionales.</p>
        </header>
        
        <div class="section">
            <h2>🛠️ Tecnologías y Herramientas</h2>
            <div class="skills-container">
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-html5"></i></div>
                    <div>HTML5</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-css3-alt"></i></div>
                    <div>CSS3</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-js"></i></div>
                    <div>JavaScript</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-react"></i></div>
                    <div>React</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-node-js"></i></div>
                    <div>Node.js</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-python"></i></div>
                    <div>Python</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fas fa-database"></i></div>
                    <div>MySQL</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-git-alt"></i></div>
                    <div>Git</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-docker"></i></div>
                    <div>Docker</div>
                </div>
                <div class="skill-item">
                    <div class="skill-icon"><i class="fab fa-figma"></i></div>
                    <div>Figma</div>
                </div>
            </div>
            
            <!-- También puedes usar el enfoque de skillicons.dev que mencionaste -->
            <div style="margin-top: 40px; text-align: center;">
                <h3>Más tecnologías que uso</h3>
                <a href="https://skillicons.dev">
                    <img src="https://skillicons.dev/icons?i=git,css,discord,docker,postgres,figma,github,html,java,js,mysql,postman,react,tailwind,ts,vscode" style="margin-top: 15px;" />
                </a>
            </div>
        </div>
        
        <div class="section">
            <h2>📂 Proyectos Destacados</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-title">
                        <i class="fas fa-shopping-cart"></i>
                        E-commerce Platform
                    </div>
                    <p>Plataforma de comercio electrónico con carrito de compras, autenticación y panel de administración.</p>
                    <div class="project-tech">
                        <span class="tech-tag">React</span>
                        <span class="tech-tag">Node.js</span>
                        <span class="tech-tag">MongoDB</span>
                        <span class="tech-tag">Stripe</span>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-title">
                        <i class="fas fa-tasks"></i>
                        Task Manager App
                    </div>
                    <p>Aplicación de gestión de tareas con arrastrar y soltar, categorías y recordatorios.</p>
                    <div class="project-tech">
                        <span class="tech-tag">Vue.js</span>
                        <span class="tech-tag">Express</span>
                        <span class="tech-tag">PostgreSQL</span>
                        <span class="tech-tag">Socket.io</span>
                    </div>
                </div>
                
                <div class="project-card">
                    <div class="project-title">
                        <i class="fas fa-chart-line"></i>
                        Analytics Dashboard
                    </div>
                    <p>Tablero de análisis de datos con gráficos interactivos, filtros y exportación de informes.</p>
                    <div class="project-tech">
                        <span class="tech-tag">React</span>
                        <span class="tech-tag">D3.js</span>
                        <span class="tech-tag">Python</span>
                        <span class="tech-tag">FastAPI</span>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="section">
            <h2>📊 Mis Estadísticas</h2>
            <div class="stats-container">
                <div class="stat-card">
                    <div class="stat-number">50+</div>
                    <div class="stat-label">Proyectos Completados</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">5+</div>
                    <div class="stat-label">Años de Experiencia</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">25+</div>
                    <div class="stat-label">Clientes Satisfechos</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number">1000+</div>
                    <div class="stat-label">Commits en GitHub</div>
                </div>
            </div>
        </div>
        
        <div class="section">
            <h2>🌐 Encuéntrame en</h2>
            <div class="social-links">
                <a href="https://github.com/tuusuario" class="social-link" target="_blank">
                    <i class="fab fa-github social-icon"></i>
                    GitHub
                </a>
                <a href="https://linkedin.com/in/tuusuario" class="social-link" target="_blank">
                    <i class="fab fa-linkedin social-icon"></i>
                    LinkedIn
                </a>
                <a href="https://twitter.com/tuusuario" class="social-link" target="_blank">
                    <i class="fab fa-twitter social-icon"></i>
                    Twitter
                </a>
                <a href="https://instagram.com/tuusuario" class="social-link" target="_blank">
                    <i class="fab fa-instagram social-icon"></i>
                    Instagram
                </a>
                <a href="https://tusitio.com" class="social-link" target="_blank">
                    <i class="fas fa-globe social-icon"></i>
                    Mi Portfolio
                </a>
            </div>
        </div>
        
        <div class="section">
            <h2>☕ ¿Quieres apoyarme?</h2>
            <p style="text-align: center; margin-bottom: 20px;">Si te gusta mi trabajo, puedes invitarme un café ☕</p>
            <div class="support-options">
                <button class="support-btn" onclick="selectOption('cafecito')">
                    <i class="fas fa-coffee"></i>
                    <span>Invitame un Cafecito</span>
                    <i class="far fa-square unchecked"></i>
                </button>
                <button class="support-btn" onclick="selectOption('matecito')">
                    <i class="fas fa-mug-hot"></i>
                    <span>Convidame un Matecito</span>
                    <i class="fas fa-check-square checked"></i>
                </button>
                <button class="support-btn" onclick="selectOption('coffee')">
                    <i class="fas fa-mug-saucer"></i>
                    <span>Buy Me a Coffee</span>
                    <i class="far fa-square unchecked"></i>
                </button>
            </div>
        </div>
        
        <footer>
            <p>© 2023 [Tu Nombre]. Todos los derechos reservados.</p>
            <p style="margin-top: 10px;">
                <i class="fas fa-code"></i> Con mucho <i class="fas fa-heart" style="color: #ff6b6b;"></i> y <i class="fas fa-coffee" style="color: #8b4513;"></i>
            </p>
        </footer>
    </div>
    
    <script>
        function selectOption(option) {
            // Reset all checkboxes
            document.querySelectorAll('.support-btn i.fa-check-square').forEach(icon => {
                icon.className = 'far fa-square unchecked';
            });
            
            // Mark the selected option
            let selectedBtn = event.currentTarget;
            let checkIcon = selectedBtn.querySelector('i:last-child');
            checkIcon.className = 'fas fa-check-square checked';
            
            // Show a thank you message
            let messages = {
                'cafecito': '¡Gracias por el cafecito! ☕',
                'matecito': '¡Gracias por el matecito! 🧉',
                'coffee': '¡Gracias por el café! 💖'
            };
            
            alert(messages[option]);
        }
        
        // Initialize with matecito selected (as in your example)
        document.addEventListener('DOMContentLoaded', function() {
            // Simulate matecito already selected
            let matecitoBtn = document.querySelector('.support-btn:nth-child(2)');
            let matecitoCheck = matecitoBtn.querySelector('i:last-child');
            matecitoCheck.className = 'fas fa-check-square checked';
        });
    </script>
</body>
</html>
