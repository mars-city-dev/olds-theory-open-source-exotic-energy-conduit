\<\!DOCTYPE html\>  
\<html lang="en"\>  
\<head\>  
    \<meta charset="UTF-8"\>  
    \<meta name="viewport" content="width=device-width, initial-scale=1.0"\>  
    \<title\>Gemini Interface v2.3 | Sub-Quantum Lab\</title\>  
    \<script src="https://cdn.tailwindcss.com"\>\</script\>  
    \<script src="https://cdn.jsdelivr.net/npm/chart.js"\>\</script\>  
    \<script src="https://cdn.plot.ly/plotly-2.27.0.min.js"\>\</script\>  
    \<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;500;700\&family=Inter:wght@300;400;600\&display=swap" rel="stylesheet"\>  
    \<\!-- Chosen Palette: Violet Ignition (Stone 50 Background, Violet 600 Primary, Amber 500 Secondary) \--\>  
    \<\!-- Application Structure Plan:   
         1\. Spectral Transducer Control: Interactive frequency tuning (targeting 750 THz).  
         2\. 3-Geome Harmonic Tuner: Sliders for Tetrahedron, Cuboctahedron, and Dodecahedron to calculate Geometric Convergence.  
         3\. Muonic Penetration Index: Dynamic bubble chart responding to Geome inputs.  
         4\. The 12 Knowledge Domains: Deep-dive cards including the new Spatial Engineering postulations.  
         5\. Quantum Math Overlay: Live display of the Resonant Coordinate Algorithm ($R\_c$). \--\>  
    \<style\>  
        :root {  
            \--bg-stone: \#fafaf9;  
            \--violet-ignition: \#7c3aed;  
            \--amber-glow: \#f59e0b;  
            \--emerald-love: \#10b981;  
            \--text-dark: \#1c1917;  
            \--baryon-glow: \#fef3c7;  
        }  
        body { font-family: 'Inter', sans-serif; background-color: var(--bg-stone); color: var(--text-dark); overflow-x: hidden; }  
        .font-display { font-family: 'Space Grotesk', sans-serif; }  
          
        .chart-container {   
            position: relative;   
            width: 100%;   
            max-width: 600px;   
            margin-left: auto;   
            margin-right: auto;   
            height: 300px;   
            max-height: 400px;   
        }

        .codex-card { transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1); cursor: pointer; border: 1px solid \#e7e5e4; border-radius: 1.5rem; background: white; }  
        .codex-card:hover { transform: translateY(-6px); box-shadow: 0 20px 25px \-5px rgba(124, 58, 237, 0.15); border-color: var(--violet-ignition); }  
          
        .violet-pulse { animation: pulse-violet 2s infinite; }  
        @keyframes pulse-violet {  
            0%, 100% { box-shadow: 0 0 15px rgba(124, 58, 237, 0.4); }  
            50% { box-shadow: 0 0 35px rgba(124, 58, 237, 0.7); }  
        }  
          
        .baryon-glow-effect { background: radial-gradient(circle, var(--baryon-glow) 0%, rgba(250, 250, 249, 0\) 70%); }  
        .glass-panel { background: rgba(255, 255, 255, 0.85); backdrop-filter: blur(12px); border: 1px solid rgba(255, 255, 255, 0.5); }  
          
        input\[type=range\] { appearance: none; width: 100%; height: 4px; background: \#e7e5e4; border-radius: 5px; outline: none; }  
        input\[type=range\]::-webkit-slider-thumb { appearance: none; width: 16px; height: 16px; background: var(--violet-ignition); border-radius: 50%; cursor: pointer; transition: 0.2s; }  
        input\[type=range\]::-webkit-slider-thumb:hover { transform: scale(1.2); }  
    \</style\>  
\</head\>  
\<body class="selection:bg-violet-100"\>

    \<nav class="sticky top-0 z-50 glass-panel border-b border-stone-200"\>  
        \<div class="max-w-7xl mx-auto px-4 h-20 flex items-center justify-between"\>  
            \<div class="flex items-center space-x-4"\>  
                \<div class="w-12 h-12 bg-stone-900 rounded-2xl flex items-center justify-center text-violet-500 font-bold text-2xl violet-pulse italic"\>G\</div\>  
                \<div\>  
                    \<h1 class="font-display font-bold text-xl tracking-tighter leading-none uppercase italic"\>The Gemini Interface\</h1\>  
                    \<span class="text-\[10px\] text-stone-400 uppercase font-bold tracking-\[0.2em\]"\>v2.3 // Sub-Quantum Lab\</span\>  
                \</div\>  
            \</div\>  
            \<div class="hidden lg:flex items-center space-x-8 text-sm font-medium"\>  
                \<div class="flex flex-col items-end"\>  
                    \<span class="text-\[9px\] text-stone-400 uppercase"\>Spectral Transducer\</span\>  
                    \<span id="liveFreq" class="text-xs font-bold text-violet-600"\>750.00 THz\</span\>  
                \</div\>  
                \<div class="h-8 w-px bg-stone-200"\>\</div\>  
                \<div class="bg-violet-600 text-white px-5 py-2 rounded-full text-\[10px\] font-bold tracking-widest flex items-center shadow-lg shadow-violet-200"\>  
                    \<span class="w-2 h-2 bg-white rounded-full mr-2 animate-ping"\>\</span\>  
                    BARYONIC OUTPUT: ACTIVE  
                \</div\>  
            \</div\>  
        \</div\>  
    \</nav\>

    \<main class="max-w-7xl mx-auto px-4 py-12"\>

        \<\!-- Section 1: Interaction Lab Dashboard \--\>  
        \<section class="mb-16 grid lg:grid-cols-12 gap-8"\>  
              
            \<\!-- Left: Spectral & Geome Controls \--\>  
            \<div class="lg:col-span-4 space-y-8"\>  
                \<div class="bg-white p-8 rounded-\[2.5rem\] border border-stone-200 shadow-sm relative overflow-hidden"\>  
                    \<div class="absolute inset-0 baryon-glow-effect opacity-30"\>\</div\>  
                    \<div class="relative z-10"\>  
                        \<h3 class="text-\[10px\] font-bold text-stone-400 uppercase tracking-widest mb-6"\>Spectral Transducer Control\</h3\>  
                        \<div id="transducerGauge" class="w-full h-40"\>\</div\>  
                        \<div class="mt-4 space-y-4"\>  
                            \<label class="block"\>  
                                \<span class="text-\[10px\] text-stone-500 font-bold uppercase tracking-wider"\>Target Frequency (THz)\</span\>  
                                \<input type="range" id="freqSlider" min="0" max="800" value="750" class="mt-2" oninput="updateFreq(this.value)"\>  
                            \</label\>  
                            \<div class="flex justify-between text-\[10px\] font-mono text-stone-400"\>  
                                \<span\>0.00 THz\</span\>  
                                \<span\>800.00 THz\</span\>  
                            \</div\>  
                        \</div\>  
                    \</div\>  
                \</div\>

                \<div class="bg-stone-900 p-8 rounded-\[2.5rem\] text-white shadow-2xl"\>  
                    \<h3 class="text-\[10px\] font-bold text-violet-400 uppercase tracking-widest mb-6"\>3-Geome Harmonic Tuner\</h3\>  
                    \<div class="space-y-6"\>  
                        \<div class="space-y-2"\>  
                            \<div class="flex justify-between text-\[10px\] uppercase font-bold tracking-tighter"\>  
                                \<span class="text-stone-400"\>Tetrahedron (Stability)\</span\>  
                                \<span id="val-tetra" class="text-violet-400"\>98%\</span\>  
                            \</div\>  
                            \<input type="range" id="slider-tetra" min="0" max="100" value="98" oninput="updateGeomes()"\>  
                        \</div\>  
                        \<div class="space-y-2"\>  
                            \<div class="flex justify-between text-\[10px\] uppercase font-bold tracking-tighter"\>  
                                \<span class="text-stone-400"\>Cuboctahedron (Equilibrium)\</span\>  
                                \<span id="val-cubo" class="text-violet-400"\>92%\</span\>  
                            \</div\>  
                            \<input type="range" id="slider-cubo" min="0" max="100" value="92" oninput="updateGeomes()"\>  
                        \</div\>  
                        \<div class="space-y-2"\>  
                            \<div class="flex justify-between text-\[10px\] uppercase font-bold tracking-tighter"\>  
                                \<span class="text-stone-400"\>Dodecahedron (Buffer)\</span\>  
                                \<span id="val-dode" class="text-violet-400"\>95%\</span\>  
                            \</div\>  
                            \<input type="range" id="slider-dode" min="0" max="100" value="95" oninput="updateGeomes()"\>  
                        \</div\>  
                    \</div\>  
                \</div\>  
            \</div\>

            \<\!-- Center/Right: Visual Feedback \--\>  
            \<div class="lg:col-span-8 grid md:grid-cols-2 gap-8"\>  
                \<div class="bg-white p-8 rounded-\[2.5rem\] border border-stone-200 shadow-sm"\>  
                    \<h3 class="text-\[10px\] font-bold text-stone-400 uppercase tracking-widest mb-6"\>Resonance Stability Matrix\</h3\>  
                    \<div class="chart-container"\>  
                        \<canvas id="stabilityChart"\>\</canvas\>  
                    \</div\>  
                \</div\>  
                \<div class="bg-white p-8 rounded-\[2.5rem\] border border-stone-200 shadow-sm"\>  
                    \<h3 class="text-\[10px\] font-bold text-stone-400 uppercase tracking-widest mb-6"\>Muonic Penetration Index\</h3\>  
                    \<div class="chart-container"\>  
                        \<canvas id="penetrationChart"\>\</canvas\>  
                    \</div\>  
                \</div\>  
                \<\!-- Quantum Math Overlay \--\>  
                \<div class="md:col-span-2 bg-stone-50 p-8 rounded-\[2.5rem\] border border-stone-200 font-mono text-xs text-stone-600 relative overflow-hidden"\>  
                    \<h3 class="text-\[10px\] font-bold text-stone-400 uppercase tracking-widest mb-4"\>Quantum Math Logic: $R\_c$ Algorithm\</h3\>  
                    \<div class="grid md:grid-cols-2 gap-8"\>  
                        \<div\>  
                            \<p class="mb-4"\>Calculated Displacement Probability ($P\_d$):\</p\>  
                            \<div class="text-2xl font-bold text-violet-600" id="pdDisplay"\>0.9984\</div\>  
                            \<p class="mt-4 opacity-50 text-\[10px\]"\>Formula: $P\_d \= \\int (I\_n \\cdot \\Phi\_{geome} / T) dt$\</p\>  
                        \</div\>  
                        \<div class="space-y-2 text-\[10px\]"\>  
                            \<p class="text-stone-400"\>:: ARCHITECTURAL RAMIFICATIONS ::\</p\>  
                            \<p id="ramificationText"\>Harmonic balance achieved. Space is a resource. Transit nodes stable at current coordinates.\</p\>  
                        \</div\>  
                    \</div\>  
                \</div\>  
            \</div\>  
        \</section\>

        \<\!-- Section 2: Interactive Knowledge Lab \--\>  
        \<section id="codex" class="mb-20"\>  
            \<h2 class="text-4xl font-display font-bold text-stone-900 mb-8 italic tracking-tighter"\>The 12 Knowledge Domains\</h2\>  
            \<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6" id="domainGrid"\>  
                \<\!-- Cards injected by JS \--\>  
            \</div\>  
        \</section\>

        \<\!-- Section 3: dev/null Choice Engine \--\>  
        \<section id="choice" class="mb-20"\>  
            \<div class="bg-stone-950 rounded-\[3rem\] p-12 text-white relative overflow-hidden border border-violet-500/20"\>  
                \<div class="max-w-xl"\>  
                    \<span class="text-violet-400 text-\[10px\] font-bold tracking-\[0.4em\] uppercase mb-4 block"\>The dev/null Engine\</span\>  
                    \<h3 class="text-3xl font-display font-bold mb-6 italic tracking-tighter"\>Intent Selection\</h3\>  
                    \<div class="grid grid-cols-2 gap-4"\>  
                        \<button onclick="logIntent('LOVE')" class="p-6 rounded-2xl bg-emerald-500/10 border border-emerald-500/30 hover:bg-emerald-500/20 transition-all flex flex-col items-center"\>  
                            \<span class="text-emerald-400 font-bold uppercase tracking-widest text-\[10px\] mb-2"\>Love Iteration\</span\>  
                            \<span class="text-2xl"\>✧\</span\>  
                        \</button\>  
                        \<button onclick="logIntent('DISSONANCE')" class="p-6 rounded-2xl bg-red-500/10 border border-red-500/30 hover:bg-red-500/20 transition-all flex flex-col items-center"\>  
                            \<span class="text-red-400 font-bold uppercase tracking-widest text-\[10px\] mb-2"\>Shunt Dissonance\</span\>  
                            \<span class="text-2xl"\>⊘\</span\>  
                        \</button\>  
                    \</div\>  
                \</div\>  
                \<div id="choiceLog" class="mt-12 bg-black/40 rounded-3xl p-6 font-mono text-\[10px\] text-stone-500 space-y-2 h-40 overflow-y-auto"\>  
                    \<div class="opacity-50 border-b border-stone-800 pb-2 mb-2"\>:: IORIC 4.0 LOG :: WAITING FOR INJECTION\</div\>  
                \</div\>  
            \</div\>  
        \</section\>

    \</main\>

    \<\!-- Modal for Deep-Dive \--\>  
    \<div id="modalOverlay" class="fixed inset-0 bg-stone-900/40 backdrop-blur-md z-\[100\] hidden items-center justify-center p-4"\>  
        \<div class="bg-white rounded-\[3rem\] max-w-2xl w-full p-12 shadow-2xl relative border border-stone-100 transform scale-95 opacity-0 transition-all duration-300" id="modalBox"\>  
            \<button onclick="closeModal()" class="absolute top-8 right-8 text-stone-300 hover:text-violet-600 transition text-4xl"\>×\</button\>  
            \<div id="modalContent"\>\</div\>  
        \</div\>  
    \</div\>

    \<script\>  
        const domains \= \[  
            { id: 1, type: "Theory", title: "Resonant Density", desc: "Matter as a topological fold. Mass is frequency.", icon: "△", detail: "Spatial ramification: Walls and structures are localized frequency buffers, not static barriers." },  
            { id: 2, type: "Theory", title: "Causal Spline Constant", desc: "Eliminating randomness via probability mapping.", icon: "⌥", detail: "Quantum math: $K\_s$ dictates the refresh rate of the manifest environment." },  
            { id: 3, type: "Theory", title: "Exotic Energy Flow", desc: "Source-facilitated attenuation to finer strata.", icon: "≋", detail: "Intent steers the energy flow across the topological grid." },  
            { id: 4, type: "Engineering", title: "Practical Application", desc: "Biological transduction via neural ignition.", icon: "⚙", detail: "Designing the vessel as a high-fidelity receiver for 750 THz signals." },  
            { id: 5, type: "Engineering", title: "Synchronicity Mechanics", desc: "Geometric convergence of independent splines.", icon: "⎋", detail: "Using the 3-Geome harmonic to engineer timing and intersections." },  
            { id: 6, type: "Engineering", title: "Instantaneous Transit", desc: "Non-local displacement via coordinate re-coding.", icon: "🚀", detail: "Spatial ramification: Distance is eliminated; architecture becomes about resonance." },  
            { id: 7, type: "Being", title: "Everyday Transduction", desc: "Maintaining high-fidelity ignition in mundane 3D.", icon: "∞", detail: "The ethics of the Living Node: Every interaction is a field update." },  
            { id: 8, type: "Being", title: "Sign for Infinity", desc: "Sovereign choice: Shunting dissonance to dev/null.", icon: "✧", detail: "Love is the fundamental carrier wave for iterative refinement." },  
            { id: 9, type: "Fractal", title: "Muonic Synthesis", desc: "FTL communication via muon-catalyzed tunnels.", icon: "↯", detail: "Bypassing the friction of light-speed through sub-quantum depth." },  
            { id: 10, type: "Fractal", title: "Harmonic Feedback", desc: "Bidirectional data-flow between manifest and Source.", icon: "⟲", detail: "Managing the ripple effect of creative manifest on the Unified Field." },  
            { id: 11, type: "Fractal", title: "Baryonic Anchor", desc: "Stabilizing larger structures for manifest persistence.", icon: "⚓", detail: "Architectural necessity: Building nodes that resist institutional erosion." },  
            { id: 12, type: "Universal", title: "Unified Codex", desc: "Synthesizing Infrastructure into operational reality.", icon: "⊕", detail: "The final integration of the 18 planned cards into IORIC Codex 4.0." }  
        \];

        let charts \= {};

        // \--- CORE UI \---  
        const renderGrid \= () \=\> {  
            const grid \= document.getElementById('domainGrid');  
            grid.innerHTML \= '';  
            domains.forEach(d \=\> {  
                const card \= document.createElement('div');  
                card.className \= \`codex-card p-8 flex flex-col justify-between h-72\`;  
                card.onclick \= () \=\> openModal(d);  
                card.innerHTML \= \`  
                    \<div class="mb-4"\>  
                        \<div class="flex justify-between items-start mb-6"\>  
                            \<span class="text-3xl text-violet-600"\>${d.icon}\</span\>  
                            \<span class="text-\[8px\] font-bold bg-stone-100 px-2 py-0.5 rounded text-stone-400 uppercase tracking-widest"\>${d.type}\</span\>  
                        \</div\>  
                        \<h4 class="font-display font-bold text-stone-900 leading-tight mb-3 text-lg"\>${d.title}\</h4\>  
                        \<p class="text-\[11px\] text-stone-500 leading-relaxed"\>${d.desc}\</p\>  
                    \</div\>  
                \`;  
                grid.appendChild(card);  
            });  
        };

        const openModal \= (d) \=\> {  
            const overlay \= document.getElementById('modalOverlay');  
            const box \= document.getElementById('modalBox');  
            overlay.classList.remove('hidden');  
            overlay.classList.add('flex');  
            setTimeout(() \=\> { box.classList.remove('scale-95', 'opacity-0'); box.classList.add('scale-100', 'opacity-100'); }, 10);  
            document.getElementById('modalContent').innerHTML \= \`  
                \<span class="text-violet-600 text-3xl mb-4 block"\>${d.icon}\</span\>  
                \<h3 class="text-5xl font-display font-bold text-stone-900 mb-8 italic"\>${d.title}\</h3\>  
                \<p class="text-stone-600 text-xl border-l-4 border-stone-100 pl-8 mb-10"\>${d.detail}\</p\>  
                \<div class="p-8 bg-stone-50 rounded-\[2rem\] flex items-center justify-between"\>  
                    \<span class="text-xs font-mono"\>DOMAIN\_ID: 0x${d.id}\</span\>  
                    \<button class="px-8 py-3 bg-violet-600 text-white text-\[10px\] font-bold rounded-full uppercase"\>Verify Linkage\</button\>  
                \</div\>  
            \`;  
        };

        const closeModal \= () \=\> {  
            const box \= document.getElementById('modalBox');  
            box.classList.add('scale-95', 'opacity-0');  
            setTimeout(() \=\> { document.getElementById('modalOverlay').classList.add('hidden'); }, 300);  
        };

        // \--- INTERACTIVE LAB LOGIC \---  
        const updateFreq \= (val) \=\> {  
            document.getElementById('liveFreq').innerText \= \`${val}.00 THz\`;  
            Plotly.restyle('transducerGauge', 'value', \[parseFloat(val)\]);  
            updateSimulation();  
        };

        const updateGeomes \= () \=\> {  
            const t \= document.getElementById('slider-tetra').value;  
            const c \= document.getElementById('slider-cubo').value;  
            const d \= document.getElementById('slider-dode').value;  
              
            document.getElementById('val-tetra').innerText \= \`${t}%\`;  
            document.getElementById('val-cubo').innerText \= \`${c}%\`;  
            document.getElementById('val-dode').innerText \= \`${d}%\`;  
              
            charts.stability.data.datasets\[0\].data \= \[t, c, d, 88, 85\];  
            charts.stability.update();  
            updateSimulation();  
        };

        const updateSimulation \= () \=\> {  
            const t \= parseInt(document.getElementById('slider-tetra').value);  
            const freq \= parseInt(document.getElementById('freqSlider').value);  
              
            // Calculate pseudo-Pd  
            const pd \= ( (t/100) \* (freq/750) ).toFixed(4);  
            document.getElementById('pdDisplay').innerText \= pd;  
              
            // Update Muonic Penetration Chart  
            const muonicData \= Array.from({length: 10}, () \=\> ({   
                x: Math.random()\*20 \+ (t/2),   
                y: Math.random()\*40 \+ (freq/10),   
                r: Math.random()\*15 \+ 5   
            }));  
            charts.penetration.data.datasets\[1\].data \= muonicData;  
            charts.penetration.update();

            // Dynamic Ramification Text  
            const ram \= document.getElementById('ramificationText');  
            if(pd \> 0.95) ram.innerText \= "CRITICAL COHERENCE: Spatial barriers are fully permeable. Transit Node alignment optimal.";  
            else if(pd \> 0.8) ram.innerText \= "STABLE RESONANCE: Architecture holding field tension. Minimal interference detected.";  
            else ram.innerText \= "SIGNAL SCATTER: Increase Tetrahedral stability or Spectral output to refine spatial coordinate.";  
        };

        const logIntent \= (type) \=\> {  
            const log \= document.getElementById('choiceLog');  
            const entry \= document.createElement('div');  
            entry.className \= type \=== 'LOVE' ? 'text-emerald-500' : 'text-red-400';  
            entry.innerText \= \`\[${new Date().toLocaleTimeString()}\] :: ${type} ITERATION :: Shunting noise to dev/null.\`;  
            log.prepend(entry);  
        };

        // \--- CHARTS \---  
        const initCharts \= () \=\> {  
            // Radar  
            charts.stability \= new Chart(document.getElementById('stabilityChart').getContext('2d'), {  
                type: 'radar',  
                data: {  
                    labels: \['Tetrahedron', 'Cuboctahedron', 'Dodecahedron', 'Baryonic Output', 'Muonic Density'\],  
                    datasets: \[{  
                        data: \[98, 92, 95, 88, 85\],  
                        borderColor: '\#7c3aed', backgroundColor: 'rgba(124, 58, 237, 0.1)', borderWidth: 2  
                    }\]  
                },  
                options: { maintainAspectRatio: false, scales: { r: { ticks: { display: false }, grid: { color: '\#e7e5e4' } } }, plugins: { legend: { display: false } } }  
            });

            // Bubble  
            charts.penetration \= new Chart(document.getElementById('penetrationChart').getContext('2d'), {  
                type: 'bubble',  
                data: {  
                    datasets: \[  
                        { label: 'Baryonic', data: Array.from({length: 10}, () \=\> ({ x: Math.random()\*40+60, y: Math.random()\*30, r: 8 })), backgroundColor: '\#d6d3d1' },  
                        { label: 'Muonic', data: \[\], backgroundColor: '\#7c3aed88' }  
                    \]  
                },  
                options: { maintainAspectRatio: false, scales: { x: { display: false }, y: { display: false } }, plugins: { legend: { display: false } } }  
            });

            // Plotly Gauge  
            const gaugeData \= \[{  
                type: "indicator", mode: "gauge+number", value: 750,  
                number: { suffix: " THz", font: { color: "\#7c3aed" } },  
                gauge: { axis: { range: \[0, 800\] }, bar: { color: "\#7c3aed" }, bgcolor: "white", steps: \[{ range: \[0, 700\], color: "\#fafaf9" }, { range: \[700, 800\], color: "\#ede9fe" }\], threshold: { line: { color: "\#10b981", width: 4 }, value: 750 } }  
            }\];  
            Plotly.newPlot('transducerGauge', gaugeData, { width: 300, height: 200, margin: {t:0, b:0, l:30, r:30}, paper\_bgcolor: 'rgba(0,0,0,0)' }, {displayModeBar: false});  
        };

        window.onload \= () \=\> {  
            renderGrid();  
            initCharts();  
            updateSimulation();  
        };  
    \</script\>  
\</body\>  
\</html\>  
