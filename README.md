# personal-digital-file.
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Personal Digital File</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a1a2e 0%, #16213e 50%, #0f3460 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            color: #fff;
            overflow: hidden;
            position: relative;
        }
        
        body::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 10% 20%, rgba(255, 200, 124, 0.15) 0%, transparent 20%),
                        radial-gradient(circle at 90% 80%, rgba(108, 92, 231, 0.15) 0%, transparent 20%);
            z-index: -1;
        }
        
        .container {
            text-align: center;
            max-width: 800px;
            padding: 40px;
            z-index: 2;
        }
        
        .logo {
            font-size: 4rem;
            margin-bottom: 20px;
            background: linear-gradient(45deg, #ff7e5f, #feb47b);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .title {
            font-size: 3.5rem;
            margin-bottom: 10px;
            background: linear-gradient(45deg, #12c2e9, #c471ed, #f64f59);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            letter-spacing: 1px;
        }
        
        .subtitle {
            font-size: 1.8rem;
            margin-bottom: 40px;
            color: #e0e0e0;
            font-weight: 300;
            letter-spacing: 2px;
        }
        
        .coming-soon {
            font-size: 1.8rem;
            margin-bottom: 50px;
            padding: 15px 30px;
            display: inline-block;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.2);
            position: relative;
            overflow: hidden;
        }
        
        .coming-soon::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            animation: shine 3s infinite;
        }
        
        .instagram-btn {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            padding: 15px 35px;
            font-size: 1.4rem;
            font-weight: 600;
            color: white;
            background: linear-gradient(45deg, #833ab4, #fd1d1d, #fcb045);
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 6px 20px rgba(253, 29, 29, 0.3);
            position: relative;
            overflow: hidden;
            text-decoration: none;
            margin-bottom: 40px;
        }
        
        .instagram-btn i {
            margin-right: 12px;
            font-size: 1.8rem;
        }
        
        .instagram-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(253, 29, 29, 0.4);
        }
        
        .instagram-btn:active {
            transform: translateY(0);
        }
        
        .instagram-btn::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, #833ab4, #fd1d1d, #fcb045);
            z-index: -1;
            border-radius: 50px;
        }
        
        .instagram-btn::before {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(45deg, #833ab4, #fd1d1d, #fcb045);
            z-index: -2;
            filter: blur(10px);
            opacity: 0.6;
            border-radius: 50px;
        }
        
        .features {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-top: 30px;
            flex-wrap: wrap;
        }
        
        .feature {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 25px;
            width: 180px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: transform 0.3s ease;
        }
        
        .feature:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.1);
        }
        
        .feature i {
            font-size: 2.5rem;
            margin-bottom: 15px;
            color: #4cc9f0;
        }
        
        .feature h3 {
            font-size: 1.1rem;
            margin-bottom: 10px;
            color: #f1f1f1;
        }
        
        .feature p {
            font-size: 0.9rem;
            color: #b0b0b0;
        }
        
        .footer {
            position: absolute;
            bottom: 20px;
            width: 100%;
            text-align: center;
            color: rgba(255, 255, 255, 0.5);
            font-size: 0.9rem;
        }
        
        @keyframes shine {
            0% { left: -100%; }
            100% { left: 100%; }
        }
        
        @media (max-width: 768px) {
            .container {
                padding: 20px;
            }
            
            .logo {
                font-size: 3rem;
            }
            
            .title {
                font-size: 2.5rem;
            }
            
            .subtitle {
                font-size: 1.3rem;
            }
            
            .coming-soon {
                font-size: 1.4rem;
            }
            
            .features {
                gap: 15px;
            }
            
            .feature {
                width: 150px;
                padding: 15px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="logo">
            <i class="fas fa-folder-open"></i>
        </div>
        <h1 class="title">PERSONAL DIGITAL FILE</h1>
        <p class="subtitle">Tu solución integral de gestión digital</p>
        
        <div class="coming-soon">
            PRÓXIMAMENTE DISPONIBLE...
        </div>
        
        <a href="https://www.instagram.com/7alex.07/" target="_blank" class="instagram-btn">
            <i class="fab fa-instagram"></i> SÍGUEME EN INSTAGRAM
        </a>
        
        <div class="features">
            <div class="feature">
                <i class="fas fa-lock"></i>
                <h3>Seguridad</h3>
                <p>Protección avanzada de tus archivos</p>
            </div>
            <div class="feature">
                <i class="fas fa-sync-alt"></i>
                <h3>Sincronización</h3>
                <p>Accede desde cualquier dispositivo</p>
            </div>
            <div class="feature">
                <i class="fas fa-bolt"></i>
                <h3>Rápido</h3>
                <p>Velocidad y rendimiento óptimo</p>
            </div>
        </div>
    </div>
    
    <div class="footer">
        &copy; 2023 Personal Digital File. Todos los derechos reservados.
    </div>

    <script>
        // Efecto de brillo para "Próximamente disponible"
        document.addEventListener('DOMContentLoaded', function() {
            const comingSoon = document.querySelector('.coming-soon');
            
            setInterval(() => {
                comingSoon.style.boxShadow = '0 0 15px rgba(255, 255, 255, 0.5)';
                setTimeout(() => {
                    comingSoon.style.boxShadow = '0 8px 32px rgba(0, 0, 0, 0.2)';
                }, 500);
            }, 2000);
        });
    </script>
</body>
</html>
