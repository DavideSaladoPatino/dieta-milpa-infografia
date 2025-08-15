<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Infografía: La Dieta de la Milpa</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f0f4f8;
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            height: 300px;
            max-height: 400px;
        }
        @media (min-width: 768px) {
            .chart-container {
                height: 350px;
            }
        }
        .stat-card {
            background-color: white;
            border-radius: 0.75rem;
            padding: 2rem;
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
            text-align: center;
            border-left: 5px solid #118AB2;
        }
        .stat-number {
            font-size: 3.5rem;
            font-weight: 700;
            color: #073B4C;
        }
        .stat-label {
            font-size: 1.1rem;
            color: #555;
            margin-top: 0.5rem;
        }
        .flow-arrow {
            font-size: 2.5rem;
            color: #FFD166;
            margin: 1rem 0;
        }
        .icon-circle {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            color: white;
            margin: 0 auto 1rem auto;
        }
        .recipe-section {
            background-color: white;
            border-radius: 0.75rem;
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
            padding: 2rem;
        }
    </style>
</head>
<body class="text-gray-800">

    <div class="container mx-auto p-4 md:p-8">

        <header class="text-center mb-12">
            <h1 class="text-4xl md:text-5xl font-bold text-[#073B4C] mb-4">La Dieta de la Milpa: Un Camino Hacia la Salud</h1>
            <p class="text-lg text-gray-600 max-w-3xl mx-auto">Una guía visual para entender la crisis de salud en México y cómo la sabiduría ancestral de la milpa ofrece una solución sostenible y nutritiva.</p>
        </header>

        <section id="crisis" class="mb-16">
            <h2 class="text-3xl font-bold text-center text-[#073B4C] mb-8">La Encrucijada de la Salud en México</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="stat-card">
                    <div class="stat-number">40.2%</div>
                    <p class="stat-label">Prevalencia de obesidad en localidades rurales e indígenas, superando a las urbanas (38.6%).</p>
                </div>
                <div class="stat-card border-left-color-[#FF6B6B]">
                    <div class="stat-number">8.5 kg</div>
                    <p class="stat-label">Aumento de peso promedio en mexicanos durante la pandemia de COVID-19, el más alto a nivel mundial.</p>
                </div>
                <div class="stat-card border-left-color-[#FFD166] md:col-span-2 lg:col-span-1">
                    <div class="stat-number">>85 mil</div>
                    <p class="stat-label">Millones de pesos anuales es el costo de la diabetes asociada al sobrepeso y la obesidad en México.</p>
                </div>
            </div>
             <div class="bg-white rounded-lg shadow-md p-6 mt-8">
                <h3 class="text-xl font-semibold text-center mb-4 text-[#073B4C]">Obesidad Rural vs. Urbana (2023)</h3>
                <p class="text-center text-gray-600 mb-4">Contrario a la creencia popular, la prevalencia de la obesidad es ahora mayor en las zonas rurales e indígenas. Esto indica una profunda alteración de los sistemas alimentarios tradicionales por la penetración de alimentos ultraprocesados.</p>
                <div class="chart-container h-64 md:h-80">
                    <canvas id="obesidadChart"></canvas>
                </div>
            </div>
        </section>

        <section id="comparacion" class="mb-16">
            <h2 class="text-3xl font-bold text-center text-[#073B4C] mb-8">Dos Dietas, Dos Destinos</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <div class="bg-white rounded-lg shadow-md p-6 border-t-8 border-[#FF6B6B]">
                    <h3 class="text-2xl font-bold text-center mb-4 text-[#FF6B6B]">Dieta Occidental</h3>
                    <ul class="list-none space-y-3 text-center">
                        <li><span class="font-semibold">Base:</span> Alimentos ultraprocesados</li>
                        <li><span class="font-semibold">Características:</span> Exceso de azúcar, sal, grasas saturadas, aditivos químicos.</li>
                        <li><span class="font-semibold">Deficiencias:</span> Baja en fibra, vitaminas y minerales.</li>
                    </ul>
                    <div class="text-center flow-arrow">⬇️</div>
                    <div class="bg-red-100 text-red-800 p-4 rounded-lg text-center">
                        <p class="font-bold">Resultado:</p>
                        <p>Estrés oxidativo, inflamación, y mayor riesgo de enfermedades crónicas como diabetes y obesidad.</p>
                    </div>
                </div>
                <div class="bg-white rounded-lg shadow-md p-6 border-t-8 border-[#06D6A0]">
                    <h3 class="text-2xl font-bold text-center mb-4 text-[#06D6A0]">Dieta de la Milpa</h3>
                    <ul class="list-none space-y-3 text-center">
                        <li><span class="font-semibold">Base:</span> Alimentos integrales y frescos</li>
                        <li><span class="font-semibold">Características:</span> Rica en fibra, antioxidantes, vitaminas y minerales.</li>
                        <li><span class="font-semibold">Equilibrio:</span> Proteínas vegetales, grasas saludables.</li>
                    </ul>
                    <div class="text-center flow-arrow">⬇️</div>
                    <div class="bg-green-100 text-green-800 p-4 rounded-lg text-center">
                        <p class="font-bold">Resultado:</p>
                        <p>Protección celular, salud intestinal, menor inflamación y prevención de enfermedades crónicas.</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="pilares" class="mb-16">
            <h2 class="text-3xl font-bold text-center text-[#073B4C] mb-8">Los Pilares del Plato de la Milpa</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="bg-white rounded-lg shadow-md p-6 lg:col-span-2">
                    <h3 class="text-xl font-semibold text-center mb-4 text-[#073B4C]">Grasas Cardioprotectoras del Aguacate</h3>
                     <p class="text-center text-gray-600 mb-4">El aguacate es una fuente primordial de grasas saludables. Más del 70% de sus grasas son insaturadas, las cuales ayudan a reducir el colesterol "malo" (LDL), protegiendo la salud del corazón.</p>
                    <div class="chart-container h-80">
                        <canvas id="aguacateChart"></canvas>
                    </div>
                </div>

                <div class="bg-white rounded-lg shadow-md p-6">
                    <h3 class="text-xl font-semibold text-center mb-4 text-[#073B4C]">Come el Arcoíris de Antioxidantes</h3>
                    <p class="text-center text-gray-600 mb-6">Cada color en las verduras y frutas de la milpa aporta diferentes fitoquímicos que protegen tus células del daño oxidativo.</p>
                    <div class="space-y-4">
                        <div class="flex items-center"><div class="w-8 h-8 rounded-full bg-[#FF6B6B] mr-4"></div><div><span class="font-bold">Rojos:</span> Licopeno y antocianinas</div></div>
                        <div class="flex items-center"><div class="w-8 h-8 rounded-full bg-[#FFD166] mr-4"></div><div><span class="font-bold">Naranjas/Amarillos:</span> Carotenos</div></div>
                        <div class="flex items-center"><div class="w-8 h-8 rounded-full bg-[#06D6A0] mr-4"></div><div><span class="font-bold">Verdes:</span> Luteína y betacaroteno</div></div>
                        <div class="flex items-center"><div class="w-8 h-8 rounded-full bg-[#118AB2] mr-4"></div><div><span class="font-bold">Azules/Violetas:</span> Antocianinas</div></div>
                        <div class="flex items-center"><div class="w-8 h-8 rounded-full bg-gray-200 mr-4"></div><div><span class="font-bold">Blancos:</span> Flavonoides</div></div>
                    </div>
                </div>
                
                <div class="bg-white rounded-lg shadow-md p-6 md:col-span-2 lg:col-span-3">
                    <h3 class="text-xl font-semibold text-center mb-4 text-[#073B4C]">Ranking de Omega-3 en Pescados</h3>
                    <p class="text-center text-gray-600 mb-4">Priorizar pescados grasos es clave para obtener ácidos grasos omega-3, esenciales para la salud cerebral y cardiovascular. La Dieta de la Milpa favorece estas fuentes de proteína sobre las carnes rojas.</p>
                    <div class="chart-container h-96">
                        <canvas id="omega3Chart"></canvas>
                    </div>
                </div>
            </div>
        </section>
        
        <section id="evitar" class="mb-16">
            <h2 class="text-3xl font-bold text-center text-[#073B4C] mb-8">Prácticas a Reconsiderar para una Salud Óptima</h2>
            <div class="max-w-4xl mx-auto grid grid-cols-1 md:grid-cols-2 gap-6">
                <div class="bg-red-100 p-6 rounded-lg flex items-start space-x-4">
                    <div class="text-3xl text-red-600">🚫</div>
                    <div>
                        <h4 class="font-bold text-lg text-red-800">Alimentos Ultraprocesados</h4>
                        <p class="text-red-700">Evítalos por completo. Son la principal causa de estrés oxidativo y enfermedades crónicas.</p>
                    </div>
                </div>
                 <div class="bg-red-100 p-6 rounded-lg flex items-start space-x-4">
                    <div class="text-3xl text-red-600">🚫</div>
                    <div>
                        <h4 class="font-bold text-lg text-red-800">Carnes Rojas y Procesadas</h4>
                        <p class="text-red-700">Limita la carne roja a 2 veces por mes y elimina los embutidos, asociados a un mayor riesgo de cáncer.</p>
                    </div>
                </div>
                 <div class="bg-yellow-100 p-6 rounded-lg flex items-start space-x-4">
                    <div class="text-3xl text-yellow-600">⚠️</div>
                    <div>
                        <h4 class="font-bold text-lg text-yellow-800">Azúcares Añadidos</h4>
                        <p class="text-yellow-700">Consume bebidas tradicionales como atole o chocolate sin azúcar, como se hacía ancestralmente.</p>
                    </div>
                </div>
                 <div class="bg-yellow-100 p-6 rounded-lg flex items-start space-x-4">
                    <div class="text-3xl text-yellow-600">⚠️</div>
                    <div>
                        <h4 class="font-bold text-lg text-yellow-800">Cerámica con Plomo</h4>
                        <p class="text-yellow-700">Usa utensilios de barro certificados libres de plomo para evitar la contaminación de tus alimentos.</p>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- SECCIÓN DE RECETAS CON GEMINI API -->
        <section id="recetas-gemini" class="mb-16">
            <h2 class="text-3xl font-bold text-center text-[#073B4C] mb-8">✨ Genera una Receta de la Milpa ✨</h2>
            <div class="recipe-section max-w-2xl mx-auto">
                <p class="text-center text-gray-600 mb-6">Ingresa un ingrediente de la milpa (por ejemplo: maíz, frijol, calabaza) y te sugeriré una receta tradicional.</p>
                <div class="flex flex-col md:flex-row items-center justify-center space-y-4 md:space-y-0 md:space-x-4 mb-8">
                    <input type="text" id="recipeIngredientInput" placeholder="Ej: maíz, calabaza" class="w-full md:w-auto p-3 rounded-lg border-2 border-gray-300 focus:outline-none focus:border-[#FFD166] transition-colors">
                    <button id="generateRecipeBtn" class="w-full md:w-auto p-3 rounded-lg bg-[#06D6A0] text-white font-bold hover:bg-[#04C994] transition-colors">
                        Generar Receta
                    </button>
                </div>
                <div id="recipeOutput" class="min-h-[200px] text-gray-800">
                    <div id="loadingIndicator" class="hidden text-center text-lg text-[#118AB2] animate-pulse">
                        Cargando receta...
                    </div>
                    <div id="recipeContent" class="hidden">
                        <h3 id="recipeTitle" class="text-2xl font-bold text-[#073B4C] mb-4"></h3>
                        <div class="mb-4">
                            <h4 class="text-xl font-semibold text-[#118AB2] mb-2">Ingredientes:</h4>
                            <ul id="recipeIngredients" class="list-disc list-inside space-y-1 text-gray-700"></ul>
                        </div>
                        <div>
                            <h4 class="text-xl font-semibold text-[#118AB2] mb-2">Instrucciones:</h4>
                            <ol id="recipeInstructions" class="list-decimal list-inside space-y-1 text-gray-700"></ol>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <footer class="text-center pt-8 border-t border-gray-300">
            <p class="text-gray-600">Esta infografía se basa en el documento "La Dieta de la Milpa: Modelo de alimentación saludable, culturalmente pertinente" de la Secretaría de Salud de México.</p>
            <p class="text-sm text-gray-500 mt-2">Adopta un estilo de vida que nutre tu cuerpo y tu alma.</p>
        </footer>

    </div>

<script>
function wrapLabels(label, maxWidth) {
    if (typeof label !== 'string' || label.length <= maxWidth) {
        return label;
    }
    const words = label.split(' ');
    const lines = [];
    let currentLine = '';
    for (const word of words) {
        if ((currentLine + word).length > maxWidth && currentLine.length > 0) {
            lines.push(currentLine.trim());
            currentLine = '';
        }
        currentLine += word + ' ';
    }
    lines.push(currentLine.trim());
    return lines;
}

const tooltipTitleCallback = function(tooltipItems) {
    const item = tooltipItems[0];
    let label = item.chart.data.labels[item.dataIndex];
    if (Array.isArray(label)) {
        return label.join(' ');
    } else {
        return label;
    }
};

const commonChartOptions = {
    responsive: true,
    maintainAspectRatio: false,
    plugins: {
        legend: {
            position: 'top',
            labels: {
                font: {
                    size: 14,
                    family: 'Inter'
                }
            }
        },
        tooltip: {
            callbacks: {
                title: tooltipTitleCallback
            },
            bodyFont: {
                size: 14,
                family: 'Inter'
            },
            titleFont: {
                 size: 16,
                 family: 'Inter'
            }
        }
    }
};

const colors = {
    red: '#FF6B6B',
    yellow: '#FFD166',
    green: '#06D6A0',
    blue: '#118AB2',
    darkBlue: '#073B4C'
};

document.addEventListener('DOMContentLoaded', function () {
    const obesidadCtx = document.getElementById('obesidadChart').getContext('2d');
    new Chart(obesidadCtx, {
        type: 'bar',
        data: {
            labels: ['Localidades Rurales e Indígenas', 'Localidades Urbanas'],
            datasets: [{
                label: 'Prevalencia de Obesidad (%)',
                data: [40.2, 38.6],
                backgroundColor: [colors.blue, colors.green],
                borderColor: [colors.blue, colors.green],
                borderWidth: 1
            }]
        },
        options: {
            ...commonChartOptions,
            scales: {
                y: {
                    beginAtZero: true,
                    title: {
                        display: true,
                        text: 'Porcentaje (%)'
                    }
                }
            }
        }
    });

    const aguacateCtx = document.getElementById('aguacateChart').getContext('2d');
    new Chart(aguacateCtx, {
        type: 'doughnut',
        data: {
            labels: ['Grasas Insaturadas (Buenas)', 'Grasas Saturadas'],
            datasets: [{
                label: 'Composición de Grasas',
                data: [70, 15],
                backgroundColor: [colors.green, colors.red],
                hoverOffset: 4
            }]
        },
        options: {
            ...commonChartOptions,
            plugins: {
                ...commonChartOptions.plugins,
                legend: {
                    position: 'bottom'
                }
            }
        }
    });

    const omega3Ctx = document.getElementById('omega3Chart').getContext('2d');
    const omega3Data = {
        labels: ['Atún Fresco', 'Sardinas', 'Salmón', 'Caballa', 'Arenque'].map(label => wrapLabels(label, 16)),
        datasets: [{
            label: 'Contenido de Omega-3 (mg por 100g)',
            data: [3200, 2350, 2260, 2100, 1700],
            backgroundColor: [colors.blue, colors.green, colors.yellow, colors.red, '#6C757D'],
            borderColor: '#ffffff',
            borderWidth: 2
        }]
    };
    new Chart(omega3Ctx, {
        type: 'bar',
        data: omega3Data,
        options: {
            ...commonChartOptions,
            indexAxis: 'y',
            scales: {
                x: {
                    beginAtZero: true,
                    title: {
                        display: true,
                        text: 'Miligramos (mg)'
                    }
                }
            },
             plugins: {
                ...commonChartOptions.plugins,
                legend: {
                    display: false
                }
            }
        }
    });

    const generateRecipeBtn = document.getElementById('generateRecipeBtn');
    const recipeIngredientInput = document.getElementById('recipeIngredientInput');
    const recipeOutput = document.getElementById('recipeOutput');
    const loadingIndicator = document.getElementById('loadingIndicator');
    const recipeContent = document.getElementById('recipeContent');
    const recipeTitle = document.getElementById('recipeTitle');
    const recipeIngredients = document.getElementById('recipeIngredients');
    const recipeInstructions = document.getElementById('recipeInstructions');

    const getRecipe = async (ingredient) => {
        let chatHistory = [];
        const prompt = `Genera una receta tradicional mexicana usando ${ingredient} como ingrediente principal, siguiendo los principios de la Dieta de la Milpa. La receta debe incluir un nombre, una lista de ingredientes y las instrucciones paso a paso.`;
        chatHistory.push({ role: "user", parts: [{ text: prompt }] });
        const payload = {
            contents: chatHistory,
            generationConfig: {
                responseMimeType: "application/json",
                responseSchema: {
                    type: "OBJECT",
                    properties: {
                        "nombre": { "type": "STRING" },
                        "ingredientes": {
                            "type": "ARRAY",
                            "items": { "type": "STRING" }
                        },
                        "instrucciones": {
                            "type": "ARRAY",
                            "items": { "type": "STRING" }
                        }
                    },
                    "propertyOrdering": ["nombre", "ingredientes", "instrucciones"]
                }
            }
        };

        const apiKey = "";
        const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-05-20:generateContent?key=${apiKey}`;

        let retries = 0;
        const maxRetries = 5;
        const baseDelay = 1000;

        while (retries < maxRetries) {
            try {
                const response = await fetch(apiUrl, {
                    method: 'POST',
                    headers: { 'Content-Type': 'application/json' },
                    body: JSON.stringify(payload)
                });

                if (response.ok) {
                    const result = await response.json();
                    if (result.candidates && result.candidates.length > 0 &&
                        result.candidates[0].content && result.candidates[0].content.parts &&
                        result.candidates[0].content.parts.length > 0) {
                        const json = result.candidates[0].content.parts[0].text;
                        return JSON.parse(json);
                    } else {
                        throw new Error('Respuesta de la API incompleta o mal formada.');
                    }
                } else if (response.status === 429) {
                    const delay = baseDelay * Math.pow(2, retries);
                    retries++;
                    await new Promise(res => setTimeout(res, delay));
                } else {
                    throw new Error(`Error de la API: ${response.status} ${response.statusText}`);
                }
            } catch (error) {
                if (retries === maxRetries - 1) {
                    console.error("Error al obtener la receta:", error);
                    throw error;
                }
                const delay = baseDelay * Math.pow(2, retries);
                retries++;
                await new Promise(res => setTimeout(res, delay));
            }
        }
    };

    const renderRecipe = (recipe) => {
        recipeTitle.textContent = recipe.nombre;

        recipeIngredients.innerHTML = '';
        recipe.ingredientes.forEach(item => {
            const li = document.createElement('li');
            li.textContent = item;
            recipeIngredients.appendChild(li);
        });

        recipeInstructions.innerHTML = '';
        recipe.instrucciones.forEach(step => {
            const li = document.createElement('li');
            li.textContent = step;
            recipeInstructions.appendChild(li);
        });

        loadingIndicator.classList.add('hidden');
        recipeContent.classList.remove('hidden');
    };

    generateRecipeBtn.addEventListener('click', async () => {
        const ingredient = recipeIngredientInput.value.trim();
        if (ingredient) {
            loadingIndicator.classList.remove('hidden');
            recipeContent.classList.add('hidden');
            recipeOutput.innerHTML = '';
            
            try {
                const recipe = await getRecipe(ingredient);
                if (recipe && recipe.nombre && recipe.ingredientes && recipe.instrucciones) {
                     renderRecipe(recipe);
                } else {
                    recipeOutput.innerHTML = `<div class="p-4 bg-red-100 text-red-700 rounded-lg text-center">No se pudo generar una receta válida. Intenta con otro ingrediente.</div>`;
                    loadingIndicator.classList.add('hidden');
                }
            } catch (error) {
                console.error("Error al generar la receta:", error);
                recipeOutput.innerHTML = `<div class="p-4 bg-red-100 text-red-700 rounded-lg text-center">Ocurrió un error. Por favor, inténtalo de nuevo.</div>`;
                loadingIndicator.classList.add('hidden');
            }
        }
    });
});
</script>

</body>
</html>
