# Victor-
Currículum vitae

<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Certificaciones de Ciberseguridad - Ing. Victor Eduardo Resendiz Villegas</title>
    <style>
        :root {
            --primary-color: #00ff00;
            --secondary-color: #004d4d;
            --text-color: #fff;
            --card-bg: rgba(0, 26, 26, 0.9);
            --gradient-dark: rgba(0, 10, 20, 0.95);
        }

        body {
            font-family: 'Segoe UI', Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            color: var(--text-color);
            background-color: #001a1a;
            min-height: 100vh;
        }

        .hero-section {
            position: relative;
            height: 100vh;
            background: linear-gradient(var(--gradient-dark), var(--gradient-dark)),
                        url('/api/placeholder/1920/1080') center/cover no-repeat;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 0 20px;
        }

        .profile-container {
            background: rgba(0, 26, 26, 0.8);
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 0 30px rgba(0, 255, 255, 0.1);
            max-width: 800px;
            width: 100%;
        }

        .profile-image {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            margin: 0 auto 20px;
            border: 4px solid var(--primary-color);
            box-shadow: 0 0 20px rgba(0, 255, 0, 0.3);
        }

        .welcome-text {
            font-size: 2.5em;
            color: var(--primary-color);
            margin: 20px 0;
            text-shadow: 0 0 10px rgba(0, 255, 0, 0.5);
        }

        .scroll-indicator {
            position: absolute;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%);
            animation: bounce 2s infinite;
            cursor: pointer;
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {
                transform: translateY(0);
            }
            40% {
                transform: translateY(-30px);
            }
            60% {
                transform: translateY(-15px);
            }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
        }

        .certifications-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
            padding: 40px 0;
        }

        .certification-card {
            background: var(--card-bg);
            border-radius: 15px;
            padding: 25px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border: 1px solid rgba(0, 255, 255, 0.1);
        }

        .certification-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 30px rgba(0, 255, 255, 0.2);
        }

        .certification-icon {
            font-size: 40px;
            margin-bottom: 15px;
            color: var(--primary-color);
        }

        .certification-title {
            color: var(--primary-color);
            font-size: 1.2em;
            margin-bottom: 10px;
            font-weight: bold;
        }

        .certification-date {
            color: #888;
            font-size: 0.9em;
        }

        .certification-issuer {
            color: #666;
            font-size: 0.9em;
            margin-top: 5px;
        }

        .view-button {
            display: inline-block;
            margin-top: 15px;
            padding: 8px 20px;
            background: var(--secondary-color);
            color: white;
            text-decoration: none;
            border-radius: 5px;
            transition: background 0.3s ease;
        }

        .view-button:hover {
            background: var(--primary-color);
            color: black;
        }

        @media (max-width: 768px) {
            .welcome-text {
                font-size: 2em;
            }
            
            .profile-image {
                width: 150px;
                height: 150px;
            }
        }
    </style>
</head>
<body>
    <!-- Sección de Bienvenida -->
    <section class="hero-section">
        <div class="profile-container">
            <img src="/api/placeholder/200/200" alt="Victor Eduardo Resendiz Villegas" class="profile-image">
            <h1 class="welcome-text">¡Bienvenido a mi Portafolio de Certificaciones!</h1>
            <p>Especialista en Ciberseguridad y Tecnologías de la Información</p>
            <div id="typing-text" style="min-height: 60px; margin-top: 20px; color: var(--primary-color)"></div>
        </div>
        <div class="scroll-indicator" onclick="scrollToContent()">
            ▼
        </div>
    </section>

    <!-- Sección de Certificaciones -->
    <div class="container">
        <div class="certifications-grid" id="certifications">
            <!-- Las certificaciones se cargarán aquí dinámicamente -->
        </div>
    </div>

    <script>
        // Datos de certificaciones
        const certificaciones = [
            {
                titulo: "Certified Information Systems Security Professional (CISSP)",
                fecha: "2024-01-15",
                emisor: "ISC²",
                archivo: "cissp.pdf",
                descripcion: "Certificación líder en seguridad de la información"
            },
            {
                titulo: "Certified Ethical Hacker (CEH)",
                fecha: "2023-12-01",
                emisor: "EC-Council",
                archivo: "ceh.pdf",
                descripcion: "Especialización en técnicas de hacking ético"
            },
            {
                titulo: "CompTIA Security+",
                fecha: "2023-10-15",
                emisor: "CompTIA",
                archivo: "security_plus.pdf",
                descripcion: "Fundamentos de seguridad informática"
            },
            {
                titulo: "AWS Certified Security - Specialty",
                fecha: "2023-09-01",
                emisor: "Amazon Web Services",
                archivo: "aws_security.pdf",
                descripcion: "Especialización en seguridad cloud"
            },
            {
                titulo: "Certified Information Systems Auditor (CISA)",
                fecha: "2023-08-15",
                emisor: "ISACA",
                archivo: "cisa.pdf",
                descripcion: "Auditoría de sistemas de información"
            }
        ];

        // Efecto de escritura para el mensaje de bienvenida
        const messages = [
            "Descubre mi trayectoria en ciberseguridad...",
            "Explora mis certificaciones profesionales...",
            "Conoce mi expertise en seguridad informática..."
        ];
        let messageIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        const typingSpeed = 100;
        const deletingSpeed = 50;
        const pauseTime = 2000;

        function typeWriter() {
            const typingElement = document.getElementById('typing-text');
            const currentMessage = messages[messageIndex];

            if (isDeleting) {
                typingElement.textContent = currentMessage.substring(0, charIndex - 1);
                charIndex--;
            } else {
                typingElement.textContent = currentMessage.substring(0, charIndex + 1);
                charIndex++;
            }

            if (!isDeleting && charIndex === currentMessage.length) {
                setTimeout(() => isDeleting = true, pauseTime);
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                messageIndex = (messageIndex + 1) % messages.length;
            }

            setTimeout(typeWriter, isDeleting ? deletingSpeed : typingSpeed);
        }

        // Función para renderizar certificaciones
        function renderCertificaciones() {
            const container = document.getElementById('certifications');
            container.innerHTML = certificaciones.map(cert => `
                <div class="certification-card">
                    <div class="certification-icon">🏆</div>
                    <div class="certification-title">${cert.titulo}</div>
                    <div class="certification-date">
                        ${new Date(cert.fecha).toLocaleDateString('es-ES', {
                            year: 'numeric',
                            month: 'long'
                        })}
                    </div>
                    <div class="certification-issuer">
                        Emitido por: ${cert.emisor}
                    </div>
                    <p>${cert.descripcion}</p>
                    <a href="${cert.archivo}" class="view-button" target="_blank">
                        Ver Certificación
                    </a>
                </div>
            `).join('');
        }

        // Función para scroll suave
        function scrollToContent() {
            document.getElementById('certifications').scrollIntoView({
                behavior: 'smooth'
            });
        }

        // Inicializar la página
        document.addEventListener('DOMContentLoaded', () => {
            renderCertificaciones();
            typeWriter();
        });
    </script>
</body>
</html>
