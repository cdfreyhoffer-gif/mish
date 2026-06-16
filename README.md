<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Resultados: Encuesta de Sustentabilidad Escolar</title>
    
    <!-- Fuentes de Google -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Chart.js -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

    <!-- Configuración personalizada de Tailwind -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                    colors: {
                        brand: {
                            light: '#d1fae5',
                            DEFAULT: '#10b981',
                            dark: '#047857',
                        }
                    }
                }
            }
        }
    </script>
    
    <style>
        body {
            background-color: #f3f4f6;
            color: #1f2937;
        }
        .chart-container {
            position: relative;
            height: 250px;
            width: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
        }
    </style>
</head>
<body class="antialiased min-h-screen pb-12">

    <header class="bg-gradient-to-r from-brand-dark to-brand text-white py-12 shadow-md">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <div class="inline-block p-3 bg-white/20 rounded-full mb-4 backdrop-blur-sm">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-10 w-10 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3.055 11H5a2 2 0 012 2v1a2 2 0 002 2 2 2 0 012 2v2.945M8 3.935V5.5A2.5 2.5 0 0010.5 8h.5a2 2 0 012 2 2 2 0 104 0 2 2 0 012-2h1.064M15 20.488V18a2 2 0 012-2h3.064M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
                </svg>
            </div>
            <h1 class="text-3xl md:text-5xl font-bold mb-4 tracking-tight">Encuesta de Sustentabilidad y Ahorro Energético</h1>
            <p class="text-lg md:text-xl text-brand-light max-w-3xl mx-auto">
                Diagnóstico del compromiso de la comunidad escolar con el cuidado del medio ambiente y el uso eficiente de la energía.
            </p>
        </div>
    </header>

    <main class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 mt-10">
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 xl:grid-cols-2 gap-8">
            
            <!-- Gráfico 1 -->
            <div class="bg-white rounded-2xl shadow-sm border border-gray-100 p-6 hover:shadow-lg transition-shadow duration-300">
                <h3 class="text-lg font-semibold text-gray-800 mb-4 h-14 line-clamp-2">1. ¿Qué medio de transporte utilizas habitualmente para llegar al colegio?</h3>
                <div class="chart-container">
                    <canvas id="chart1"></canvas>
                </div>
            </div>

            <!-- Gráfico 2 -->
            <div class="bg-white rounded-2xl shadow-sm border border-gray-100 p-6 hover:shadow-lg transition-shadow duration-300">
                <h3 class="text-lg font-semibold text-gray-800 mb-4 h-14 line-clamp-2">2. ¿Apagas las luces de la sala de clases cuando eres la última persona en salir?</h3>
                <div class="chart-container">
                    <canvas id="chart2"></canvas>
                </div>
            </div>

            <!-- Gráfico 3 -->
            <div class="bg-white rounded-2xl shadow-sm border border-gray-100 p-6 hover:shadow-lg transition-shadow duration-300">
                <h3 class="text-lg font-semibold text-gray-800 mb-4 h-14 line-clamp-2">3. Nivel de información sobre el impacto ambiental del consumo de energía</h3>
                <div class="chart-container">
                    <canvas id="chart3"></canvas>
                </div>
            </div>

            <!-- Gráfico 4 -->
            <div class="bg-white rounded-2xl shadow-sm border border-gray-100 p-6 hover:shadow-lg transition-shadow duration-300">
                <h3 class="text-lg font-semibold text-gray-800 mb-4 h-14 line-clamp-2">4. ¿Cómo calificarías los esfuerzos actuales del colegio para ahorrar energía?</h3>
                <div class="chart-container">
                    <canvas id="chart4"></canvas>
                </div>
            </div>

            <!-- Gráfico 5 -->
            <div class="bg-white rounded-2xl shadow-sm border border-gray-100 p-6 hover:shadow-lg transition-shadow duration-300">
                <h3 class="text-lg font-semibold text-gray-800 mb-4 h-14 line-clamp-2">5. ¿Cuál es la principal fuente de desperdicio de energía en el colegio?</h3>
                <div class="chart-container">
                    <canvas id="chart5"></canvas>
                </div>
            </div>

            <!-- Gráfico 6 -->
            <div class="bg-white rounded-2xl shadow-sm border border-gray-100 p-6 hover:shadow-lg transition-shadow duration-300">
                <h3 class="text-lg font-semibold text-gray-800 mb-4 h-14 line-clamp-2">6. ¿Te desconectas de tus dispositivos electrónicos durante los recreos?</h3>
                <div class="chart-container">
                    <canvas id="chart6"></canvas>
                </div>
            </div>

            <!-- Gráfico 7 -->
            <div class="bg-white rounded-2xl shadow-sm border border-gray-100 p-6 hover:shadow-lg transition-shadow duration-300">
                <h3 class="text-lg font-semibold text-gray-800 mb-4 h-14 line-clamp-2">7. Disposición a participar en una brigada de ahorro de energía</h3>
                <div class="chart-container">
                    <canvas id="chart7"></canvas>
                </div>
            </div>

            <!-- Gráfico 8 -->
            <div class="bg-white rounded-2xl shadow-sm border border-gray-100 p-6 hover:shadow-lg transition-shadow duration-300">
                <h3 class="text-lg font-semibold text-gray-800 mb-4 h-14 line-clamp-2">8. ¿La infraestructura del colegio aprovecha bien la luz natural y el calor?</h3>
                <div class="chart-container">
                    <canvas id="chart8"></canvas>
                </div>
            </div>

            <!-- Gráfico 9 -->
            <div class="bg-white rounded-2xl shadow-sm border border-gray-100 p-6 hover:shadow-lg transition-shadow duration-300">
                <h3 class="text-lg font-semibold text-gray-800 mb-4 h-14 line-clamp-2">9. ¿Crees que el colegio debería invertir en energías renovables (paneles solares)?</h3>
                <div class="chart-container">
                    <canvas id="chart9"></canvas>
                </div>
            </div>

            <!-- Gráfico 10 -->
            <div class="bg-white rounded-2xl shadow-sm border border-gray-100 p-6 hover:shadow-lg transition-shadow duration-300">
                <h3 class="text-lg font-semibold text-gray-800 mb-4 h-14 line-clamp-2">10. Propuestas sustentables (Tendencias en respuestas abiertas)</h3>
                <div class="chart-container">
                    <canvas id="chart10"></canvas>
                </div>
            </div>
        </div>

        <div class="mt-12 bg-white rounded-3xl shadow-lg border-l-8 border-brand overflow-hidden">
            <div class="p-8 md:p-10">
                <div class="flex items-center mb-6">
                    <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-brand mr-3" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
                    </svg>
                    <h2 class="text-2xl md:text-3xl font-bold text-gray-900">Principales Conclusiones</h2>
                </div>
                <div class="space-y-4 text-gray-600 text-lg leading-relaxed">
                    <p>
                        Los estudiantes tienen un nivel de información <strong>intermedio-alto</strong> sobre el problema ambiental, pero sienten que el colegio se queda corto en sus esfuerzos de gestión.
                    </p>
                    <p>
                        La propuesta más popular y con mayor urgencia visual es solucionar el tema de las <strong>luces encendidas en salas vacías</strong>.
                    </p>
                    <div class="bg-brand-light/40 p-4 rounded-xl mt-4 border border-brand-light">
                        <p class="text-brand-dark font-medium flex items-center">
                            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 mr-2" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
                            </svg>
                            Existe un apoyo masivo (casi el 90%) para modernizar el colegio con energías limpias como los paneles solares.
                        </p>
                    </div>
                </div>
            </div>
        </div>
    </main>

    <script>
        // Opciones globales para todos los gráficos
        Chart.defaults.font.family = "'Inter', sans-serif";
        Chart.defaults.color = '#4b5563'; // text-gray-600
        
        const commonOptions = {
            responsive: true,
            maintainAspectRatio: false,
            plugins: {
                legend: {
                    position: 'bottom',
                    labels: {
                        padding: 20,
                        usePointStyle: true,
                    }
                },
                tooltip: {
                    callbacks: {
                        label: function(context) {
                            let label = context.dataset.label || '';
                            if (label) {
                                label += ': ';
                            }
                            if (context.parsed.y !== null && context.chart.config.type !== 'pie' && context.chart.config.type !== 'doughnut' && context.chart.config.type !== 'polarArea') {
                                label += context.parsed.y + '%';
                            } else {
                                label += context.parsed + '%';
                            }
                            return label;
                        }
                    }
                }
            }
        };

        const barOptions = {
            ...commonOptions,
            plugins: {
                ...commonOptions.plugins,
                legend: { display: false } // Ocultar leyenda en gráficos de barras simples
            },
            scales: {
                y: {
                    beginAtZero: true,
                    max: 100,
                    ticks: {
                        callback: function(value) {
                            return value + '%';
                        }
                    }
                }
            }
        };

        const horizontalBarOptions = {
            ...commonOptions,
            indexAxis: 'y',
            plugins: {
                ...commonOptions.plugins,
                legend: { display: false }
            },
            scales: {
                x: {
                    beginAtZero: true,
                    max: 100,
                    ticks: {
                        callback: function(value) {
                            return value + '%';
                        }
                    }
                }
            }
        };

        // Paletas de colores
        const colors = {
            transport: ['#3b82f6', '#8b5cf6', '#10b981', '#f59e0b'],
            yesNo: ['#10b981', '#ef4444'], // Verde para Sí, Rojo para No
            likert: ['#ef4444', '#f97316', '#eab308', '#84cc16', '#22c55e'], // 1 al 5 (Rojo a Verde)
            waste: ['#f59e0b', '#3b82f6', '#ec4899', '#9ca3af'],
            infra: ['#eab308', '#ef4444', '#10b981'],
            proposals: ['#0ea5e9', '#8b5cf6', '#14b8a6']
        };

        
        // 1. Transporte (Pie)
        new Chart(document.getElementById('chart1'), {
            type: 'pie',
            data: {
                labels: ['Transporte público', 'Automóvil particular', 'Caminando', 'Bicicleta / Scooter'],
                datasets: [{
                    data: [42, 35, 15, 8],
                    backgroundColor: colors.transport,
                    borderWidth: 2,
                    borderColor: '#ffffff'
                }]
            },
            options: commonOptions
        });

        // 2. Apagar Luces (Doughnut)
        new Chart(document.getElementById('chart2'), {
            type: 'doughnut',
            data: {
                labels: ['Sí', 'No'],
                datasets: [{
                    data: [68, 32],
                    backgroundColor: colors.yesNo,
                    borderWidth: 2,
                    borderColor: '#ffffff'
                }]
            },
            options: commonOptions
        });

        // 3. Nivel de información (Bar)
        new Chart(document.getElementById('chart3'), {
            type: 'bar',
            data: {
                labels: ['1 (Nada)', '2', '3', '4', '5 (Muy inf.)'],
                datasets: [{
                    label: 'Porcentaje',
                    data: [5, 12, 28, 37, 18],
                    backgroundColor: colors.likert,
                    borderRadius: 6
                }]
            },
            options: barOptions
        });

        // 4. Esfuerzos del colegio (Bar)
        new Chart(document.getElementById('chart4'), {
            type: 'bar',
            data: {
                labels: ['1 (Deficiente)', '2', '3 (Regular)', '4', '5 (Excelente)'],
                datasets: [{
                    label: 'Porcentaje',
                    data: [14, 25, 38, 18, 5],
                    backgroundColor: colors.likert,
                    borderRadius: 6
                }]
            },
            options: barOptions
        });

        // 5. Fuente de desperdicio (Doughnut)
        new Chart(document.getElementById('chart5'), {
            type: 'doughnut',
            data: {
                labels: ['Luces en salas vacías', 'Equipos sin uso', 'Climatización ineficiente', 'Otro / No sé'],
                datasets: [{
                    data: [53, 26, 16, 5],
                    backgroundColor: colors.waste,
                    borderWidth: 2,
                    borderColor: '#ffffff'
                }]
            },
            options: commonOptions
        });

        // 6. Desconexión en recreos (Pie)
        new Chart(document.getElementById('chart6'), {
            type: 'pie',
            data: {
                labels: ['No', 'Sí'],
                datasets: [{
                    data: [74, 26],
                    backgroundColor: [colors.yesNo[1], colors.yesNo[0]], // Invertido porque "No" es rojo, "Sí" es verde
                    borderWidth: 2,
                    borderColor: '#ffffff'
                }]
            },
            options: commonOptions
        });

        // 7. Disposición a participar (Bar)
        new Chart(document.getElementById('chart7'), {
            type: 'bar',
            data: {
                labels: ['1 (Nada)', '2', '3', '4', '5 (Muy disp.)'],
                datasets: [{
                    label: 'Porcentaje',
                    data: [18, 22, 31, 19, 10],
                    backgroundColor: colors.likert,
                    borderRadius: 6
                }]
            },
            options: barOptions
        });

        // 8. Infraestructura (Pie)
        new Chart(document.getElementById('chart8'), {
            type: 'pie',
            data: {
                labels: ['Podría mejorar', 'No, depende de artificial', 'Sí, excelente'],
                datasets: [{
                    data: [58, 27, 15],
                    backgroundColor: colors.infra,
                    borderWidth: 2,
                    borderColor: '#ffffff'
                }]
            },
            options: commonOptions
        });

        // 9. Inversión renovables (Doughnut)
        new Chart(document.getElementById('chart9'), {
            type: 'doughnut',
            data: {
                labels: ['Sí, es necesaria', 'No, hay otras prioridades'],
                datasets: [{
                    data: [89, 11],
                    backgroundColor: colors.yesNo,
                    borderWidth: 2,
                    borderColor: '#ffffff'
                }]
            },
            options: commonOptions
        });

        // 10. Propuestas sustentables (Horizontal Bar)
        new Chart(document.getElementById('chart10'), {
            type: 'bar', // Modificado a horizontal con indexAxis: 'y'
            data: {
                labels: ['Sensores de mov.', 'Delegados ambientales', 'Afiches informativos'],
                datasets: [{
                    label: 'Menciones',
                    data: [45, 30, 25],
                    backgroundColor: colors.proposals,
                    borderRadius: 6
                }]
            },
            options: horizontalBarOptions
        });
    </script>
</body>
</html>
