<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>William Choi - Interactive Portfolio</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&family=Playfair+Display:wght@700&display=swap');

        :root {
            --bg-warm: #fdfbf7;
            --text-main: #2d2a26;
            --accent-gold: #c29b40;
            --accent-soft: #e6dfd1;
            --gaming-color: #4f46e5; /* Indigo */
            --venture-color: #059669; /* Emerald */
        }

        body {
            background-color: var(--bg-warm);
            color: var(--text-main);
            font-family: 'Inter', sans-serif;
        }

        h1, h2, h3 {
            font-family: 'Playfair Display', serif;
        }

        .chart-container {
            position: relative;
            width: 100%;
            max-width: 500px;
            margin: 0 auto;
            height: 300px;
        }

        .timeline-line {
            position: absolute;
            left: 50%;
            top: 0;
            bottom: 0;
            width: 2px;
            background-color: #d1d5db;
            transform: translateX(-50%);
        }

        .skill-card {
            transition: all 0.3s ease;
        }
        .skill-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
        }

        /* Hide scrollbar for clean horizontal scroll */
        .no-scrollbar::-webkit-scrollbar {
            display: none;
        }
        .no-scrollbar {
            -ms-overflow-style: none;
            scrollbar-width: none;
        }
    </style>
    <!-- Chosen Palette: Warm Neutrals (Background: #fdfbf7, Text: #2d2a26, Accent: #c29b40) -->
    <!-- Application Structure Plan: 
         1. Hero Section: Introduces William as a dual-track strategist (Gaming + Ventures). 
         2. Competency Radar: Visualizes the balance between Ops, Strategy, and Leadership.
         3. Interactive Timeline: The core experience section. Users can toggle between "Core Gaming Ops" and "Market Ventures" to see the parallel career tracks. Experience cards expand for details.
         4. The Innovation Bridge: A specific interactive section to demonstrate "Cross-Industry Innovation", linking gaming skills to real-world business applications (as requested in the resume analysis).
         5. Technical Toolkit: Categorized skills display.
    -->
    <!-- Visualization & Content Choices:
         - Radar Chart: Perfect for showing multi-faceted competencies (Ops, Tech, Leadership, Strategy).
         - Custom HTML Timeline: Used for the Experience section to allow complex content (text, titles, tags) which is hard to render well inside a Canvas chart.
         - Interaction: Filtering on the timeline allows the user to focus on specific career narratives (Gaming expert vs. Entrepreneur).
         - Color Coding: Indigo for Gaming, Emerald for Ventures to visually distinguish the dual tracks.
         - CONFIRMATION: NO SVG graphics used. NO Mermaid JS used.
    -->
</head>
<body class="antialiased min-h-screen flex flex-col">

    <!-- Header / Contact -->
    <header class="w-full max-w-6xl mx-auto p-6 flex flex-col md:flex-row justify-between items-center border-b border-gray-200">
        <div class="text-center md:text-left">
            <h1 class="text-4xl font-bold text-gray-900">William Choi</h1>
            <p class="text-lg text-gray-600 mt-1">Live Operations Strategist & Entrepreneur</p>
        </div>
        <div class="mt-4 md:mt-0 flex flex-col items-center md:items-end text-sm text-gray-500 space-y-1">
            <span>Coquitlam, BC</span>
            <a href="mailto:william@geniusorc.ca" class="hover:text-amber-600 transition">william@geniusorc.ca</a>
            <span>604-809-0582</span>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="w-full max-w-4xl mx-auto px-6 py-12 text-center">
        <h2 class="text-2xl md:text-3xl font-semibold mb-6 text-gray-800 leading-tight">
            Bridging <span class="text-indigo-600">Technical Operations</span> and <span class="text-emerald-600">Market Strategy</span>
        </h2>
        <p class="text-gray-700 leading-relaxed text-lg max-w-2xl mx-auto">
            Over 10 years of experience evolving from a hands-on manager to a Founder. 
            I architect full-service infrastructures for online games and apply those high-engagement strategies 
            to innovate in real estate and e-commerce. An adaptable leader transforming operational expertise into business viability.
        </p>
    </section>

    <!-- Core Competencies Visualization -->
    <section class="w-full bg-stone-50 py-12 border-y border-gray-200">
        <div class="max-w-6xl mx-auto px-6 grid grid-cols-1 md:grid-cols-2 gap-12 items-center">
            
            <!-- Chart Side -->
            <div class="flex flex-col items-center">
                <h3 class="text-xl font-bold mb-4 text-gray-800">Competency Profile</h3>
                <div class="chart-container">
                    <canvas id="competencyChart"></canvas>
                </div>
                <p class="text-sm text-gray-500 mt-4 text-center">
                    Visualizing the balance between operational rigor and strategic growth.
                </p>
            </div>

            <!-- Text Side -->
            <div>
                <h3 class="text-xl font-bold mb-6 text-gray-800">Core Areas of Expertise</h3>
                <div class="grid grid-cols-1 gap-4">
                    <div class="bg-white p-4 rounded-lg shadow-sm border-l-4 border-indigo-500">
                        <h4 class="font-bold text-gray-900">Live Operations & Infrastructure</h4>
                        <p class="text-sm text-gray-600 mt-1">Lifecycle Management, Server/Payment Setup, Workflow Automation (AI).</p>
                    </div>
                    <div class="bg-white p-4 rounded-lg shadow-sm border-l-4 border-emerald-500">
                        <h4 class="font-bold text-gray-900">Community & Growth Strategy</h4>
                        <p class="text-sm text-gray-600 mt-1">Influencer Marketing, Community Building, User Funnel Optimization.</p>
                    </div>
                    <div class="bg-white p-4 rounded-lg shadow-sm border-l-4 border-amber-500">
                        <h4 class="font-bold text-gray-900">Cross-Functional Leadership</h4>
                        <p class="text-sm text-gray-600 mt-1">Managing Multi-regional Teams (Vancouver/Singapore/Seoul).</p>
                    </div>
                    <div class="bg-white p-4 rounded-lg shadow-sm border-l-4 border-gray-500">
                        <h4 class="font-bold text-gray-900">Business Versatility</h4>
                        <p class="text-sm text-gray-600 mt-1">Transferring digital operation skills to physical goods and real estate.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Timeline -->
    <section class="w-full max-w-5xl mx-auto px-6 py-16">
        <div class="flex flex-col md:flex-row justify-between items-end mb-10">
            <div class="max-w-xl">
                <h2 class="text-3xl font-bold text-gray-900 mb-2">Professional Journey</h2>
                <p class="text-gray-600">
                    A dual track record. Use the filters to explore my core gaming career or my market expansion ventures.
                </p>
            </div>
            
            <!-- Filters -->
            <div class="flex space-x-2 mt-4 md:mt-0">
                <button onclick="filterTimeline('all')" id="btn-all" class="px-4 py-2 rounded-full text-sm font-semibold bg-gray-800 text-white shadow hover:bg-gray-700 transition">All</button>
                <button onclick="filterTimeline('gaming')" id="btn-gaming" class="px-4 py-2 rounded-full text-sm font-semibold bg-white text-indigo-600 border border-indigo-200 hover:bg-indigo-50 transition">Gaming Ops</button>
                <button onclick="filterTimeline('venture')" id="btn-venture" class="px-4 py-2 rounded-full text-sm font-semibold bg-white text-emerald-600 border border-emerald-200 hover:bg-emerald-50 transition">Ventures</button>
            </div>
        </div>

        <div class="relative min-h-[800px]">
            <!-- Center Line -->
            <div class="timeline-line hidden md:block"></div>

            <!-- Timeline Items Container -->
            <div id="timeline-container" class="space-y-8">
                <!-- JS will populate this -->
            </div>
        </div>
    </section>

    <!-- The Innovation Bridge (Skill Transfer) -->
    <section class="w-full bg-gray-900 text-white py-16">
        <div class="max-w-6xl mx-auto px-6">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-bold mb-4 text-white">Cross-Industry Innovation</h2>
                <p class="text-gray-400 max-w-2xl mx-auto">
                    How I translate high-engagement gaming methodologies into tangible business results for other sectors.
                    <br><span class="text-sm text-amber-500 uppercase tracking-widest mt-2 block">Click cards to reveal the connection</span>
                </p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-6" id="innovation-grid">
                <!-- Logic Card 1 -->
                <div class="bg-gray-800 rounded-xl p-6 cursor-pointer hover:bg-gray-750 transition border border-gray-700 group" onclick="toggleInnovation(1)">
                    <div class="text-indigo-400 font-bold mb-2 text-sm uppercase">Gaming Skill</div>
                    <h4 class="text-xl font-semibold mb-4">Community Management</h4>
                    <div class="h-px w-full bg-gray-600 my-4 group-hover:bg-amber-500 transition duration-500"></div>
                    <div class="text-emerald-400 font-bold mb-2 text-sm uppercase">Real Estate Application</div>
                    <h4 class="text-xl font-semibold">Vertical Platform Strategy</h4>
                    
                    <div id="innov-detail-1" class="hidden mt-4 pt-4 border-t border-gray-700 text-gray-300 text-sm">
                        <p class="mb-2"><strong class="text-white">Context:</strong> Zipjoe.com</p>
                        <p>Applied gaming community principles to build a dedicated user base for a specialized real estate platform, treating property seekers as a 'player base' to be nurtured.</p>
                    </div>
                    <p class="text-xs text-center mt-4 text-gray-500 group-hover:text-amber-500 transition">Click to Expand</p>
                </div>

                <!-- Logic Card 2 -->
                <div class="bg-gray-800 rounded-xl p-6 cursor-pointer hover:bg-gray-750 transition border border-gray-700 group" onclick="toggleInnovation(2)">
                    <div class="text-indigo-400 font-bold mb-2 text-sm uppercase">Gaming Skill</div>
                    <h4 class="text-xl font-semibold mb-4">User Acquisition Funnels</h4>
                    <div class="h-px w-full bg-gray-600 my-4 group-hover:bg-amber-500 transition duration-500"></div>
                    <div class="text-emerald-400 font-bold mb-2 text-sm uppercase">Digital Marketing</div>
                    <h4 class="text-xl font-semibold">SEO & Content Ops</h4>
                    
                    <div id="innov-detail-2" class="hidden mt-4 pt-4 border-t border-gray-700 text-gray-300 text-sm">
                        <p class="mb-2"><strong class="text-white">Context:</strong> Zipjoe.com</p>
                        <p>Optimized content strategies mirroring game UA techniques. Achieved first-page Google rankings within 3 months.</p>
                    </div>
                    <p class="text-xs text-center mt-4 text-gray-500 group-hover:text-amber-500 transition">Click to Expand</p>
                </div>

                <!-- Logic Card 3 -->
                <div class="bg-gray-800 rounded-xl p-6 cursor-pointer hover:bg-gray-750 transition border border-gray-700 group" onclick="toggleInnovation(3)">
                    <div class="text-indigo-400 font-bold mb-2 text-sm uppercase">Gaming Skill</div>
                    <h4 class="text-xl font-semibold mb-4">Whale (VIP) Management</h4>
                    <div class="h-px w-full bg-gray-600 my-4 group-hover:bg-amber-500 transition duration-500"></div>
                    <div class="text-emerald-400 font-bold mb-2 text-sm uppercase">E-Commerce</div>
                    <h4 class="text-xl font-semibold">High-Touch Customer Exp</h4>
                    
                    <div id="innov-detail-3" class="hidden mt-4 pt-4 border-t border-gray-700 text-gray-300 text-sm">
                        <p class="mb-2"><strong class="text-white">Context:</strong> Cellion.ca</p>
                        <p>Managed the full lifecycle for luxury heating products. Treated high-value customers with the same "VIP" care systems used for top-tier gamers.</p>
                    </div>
                    <p class="text-xs text-center mt-4 text-gray-500 group-hover:text-amber-500 transition">Click to Expand</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Technical & Creative Toolkit -->
    <section class="w-full max-w-6xl mx-auto px-6 py-16">
        <h2 class="text-3xl font-bold text-gray-900 mb-8 text-center">Technical & Creative Toolkit</h2>
        
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
            <!-- Col 1 -->
            <div class="bg-white p-5 rounded-lg shadow-sm border border-gray-100">
                <div class="flex items-center mb-4">
                    <span class="text-2xl mr-2">🤖</span>
                    <h4 class="font-bold text-gray-800">AI & Automation</h4>
                </div>
                <ul class="space-y-2 text-sm text-gray-600">
                    <li class="flex items-center"><span class="w-2 h-2 bg-indigo-500 rounded-full mr-2"></span>LLM Integration</li>
                    <li class="flex items-center"><span class="w-2 h-2 bg-indigo-500 rounded-full mr-2"></span>Workflow Auto.</li>
                    <li class="text-xs text-gray-400 ml-4">(ChatGPT, Claude, Gemini)</li>
                </ul>
            </div>

            <!-- Col 2 -->
            <div class="bg-white p-5 rounded-lg shadow-sm border border-gray-100">
                <div class="flex items-center mb-4">
                    <span class="text-2xl mr-2">🎨</span>
                    <h4 class="font-bold text-gray-800">Creative Tools</h4>
                </div>
                <ul class="space-y-2 text-sm text-gray-600">
                    <li class="flex items-center"><span class="w-2 h-2 bg-pink-500 rounded-full mr-2"></span>Midjourney</li>
                    <li class="flex items-center"><span class="w-2 h-2 bg-pink-500 rounded-full mr-2"></span>Canva (Gen/Edit)</li>
                    <li class="flex items-center"><span class="w-2 h-2 bg-pink-500 rounded-full mr-2"></span>Clipchamp (Video)</li>
                    <li class="flex items-center"><span class="w-2 h-2 bg-pink-500 rounded-full mr-2"></span>Pixlr / Nano Banana</li>
                </ul>
            </div>

            <!-- Col 3 -->
            <div class="bg-white p-5 rounded-lg shadow-sm border border-gray-100">
                <div class="flex items-center mb-4">
                    <span class="text-2xl mr-2">📊</span>
                    <h4 class="font-bold text-gray-800">Analysis & Ops</h4>
                </div>
                <ul class="space-y-2 text-sm text-gray-600">
                    <li class="flex items-center"><span class="w-2 h-2 bg-blue-500 rounded-full mr-2"></span>Google Analytics</li>
                    <li class="flex items-center"><span class="w-2 h-2 bg-blue-500 rounded-full mr-2"></span>Excel (Advanced)</li>
                    <li class="flex items-center"><span class="w-2 h-2 bg-blue-500 rounded-full mr-2"></span>Jira / Confluence</li>
                </ul>
            </div>

            <!-- Col 4 -->
            <div class="bg-white p-5 rounded-lg shadow-sm border border-gray-100">
                <div class="flex items-center mb-4">
                    <span class="text-2xl mr-2">🗣️</span>
                    <h4 class="font-bold text-gray-800">Languages</h4>
                </div>
                <ul class="space-y-2 text-sm text-gray-600">
                    <li class="font-semibold text-gray-800">Korean</li>
                    <li class="text-xs text-gray-500 mb-2">Native Speaker</li>
                    <li class="font-semibold text-gray-800">English</li>
                    <li class="text-xs text-gray-500">Full Professional Proficiency<br>(Strong Written Comm.)</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Footer / Education -->
    <footer class="bg-gray-100 border-t border-gray-200 mt-auto">
        <div class="max-w-6xl mx-auto px-6 py-12 flex flex-col md:flex-row justify-between items-center">
            <div class="mb-6 md:mb-0 text-center md:text-left">
                <h4 class="font-bold text-gray-800 text-lg">Education</h4>
                <p class="text-gray-600 font-semibold">Simon Fraser University, Burnaby BC</p>
                <p class="text-gray-500 text-sm">B.A. Economics (Major) / Mathematics (Minor)</p>
                <p class="text-gray-400 text-xs mt-1">Dean’s Honor Roll | Sep 2007 – Dec 2011</p>
            </div>
            
            <div class="flex flex-col items-center md:items-end">
                 <button onclick="window.print()" class="mb-4 px-6 py-2 bg-gray-800 text-white rounded hover:bg-gray-700 transition shadow-lg text-sm font-semibold">
                    Print / Save PDF
                </button>
                <p class="text-gray-400 text-sm">© 2025 William Choi Portfolio</p>
            </div>
        </div>
    </footer>

    <script>
        // --- Data ---
        const experienceData = [
            {
                id: 1,
                role: "Strategic Partner",
                company: "Zipjoe.com / Zipjoe.ca",
                period: "2024 – Present",
                location: "Vancouver, BC",
                type: "venture",
                context: "Applying platform building strategies to the Real Estate sector as a key stakeholder.",
                details: [
                    "<strong>Platform Development Strategy:</strong> Disrupting local real estate market by setting up a specialized platform. Focused on structural setup to gather user interest.",
                    "<strong>Digital Marketing:</strong> Achieved first-page Google rankings within 3 months through strategic SEO optimization and targeted content planning."
                ]
            },
            {
                id: 2,
                role: "Founder & Strategic Consultant",
                company: "Genius Orc Entertainment Ltd.",
                period: "2021 – 2024",
                location: "Vancouver, BC",
                type: "gaming",
                context: "The materialization of Live Ops expertise: building a publishing entity from scratch.",
                details: [
                    "<strong>Infrastructure Orchestration:</strong> Directed realization of complete operational ecosystem (servers, payments, patching) by recruiting specialized talent. Led QA testing.",
                    "<strong>Operational Optimization:</strong> Established cost-effective structure using remote specialists, delivering stable service quality optimizing expenses.",
                    "<strong>Business Sustainability:</strong> Active sourcing of diverse operational ideas and gathering feedback to adapt strategies."
                ]
            },
            {
                id: 3,
                role: "Exclusive Distribution Partner",
                company: "Cellion.ca",
                period: "2023 – 2024",
                location: "Vancouver, BC",
                type: "venture",
                context: "Leveraging Influencer & Community Marketing for E-commerce sales.",
                details: [
                    "<strong>Influencer & Group-Buy Strategy:</strong> Overcame low brand awareness/high price barriers by leveraging influencer credibility. Accelerated decision-making.",
                    "<strong>Customer Experience:</strong> Managed full lifecycle from logistics to CS, ensuring high post-sales satisfaction."
                ]
            },
            {
                id: 4,
                role: "Product Manager (Global Ops Lead)",
                company: "Vertigo Games / Papaya Play",
                period: "Oct 2015 – Sep 2023",
                location: "Vancouver / Singapore / Seoul",
                type: "gaming",
                context: "Scaling operations from a single region to a global multi-hub structure.",
                details: [
                    "<strong>Multi-Regional Team Setup:</strong> Led establishment of hubs in Vancouver and Singapore. Recruited talent and standardized protocols.",
                    "<strong>Cross-Border Orchestration:</strong> Bridged Korean developers and global teams, aligning conflicting interests and managing time zones.",
                    "<strong>Revenue Growth:</strong> Led publishing for 10+ titles. Utilized user feedback to execute sales strategies resulting in substantial growth."
                ]
            },
            {
                id: 5,
                role: "Project Manager (Game Ops)",
                company: "OGPlanet",
                period: "2012 – 2015",
                location: "New Westminster, BC",
                type: "gaming",
                context: "Building the foundation through direct player engagement.",
                details: [
                    "<strong>Community & Support Management:</strong> Managed channels to gather user feedback. Executed data analysis for game balance decisions.",
                    "<strong>Live Service Management:</strong> Mastered fundamentals of daily live service, event planning, and crisis management."
                ]
            },
            {
                id: 6,
                role: "Operating Partner",
                company: "Gold Spot Lansdown / Gold Buyers Canada",
                period: "2011 – 2014",
                location: "Richmond, BC",
                type: "venture",
                context: "Gaining foundational Local Business and retail experience.",
                details: [
                    "<strong>Local Market Operations:</strong> Managed retail kiosk for precious metals, handling daily pricing strategies and face-to-face negotiations.",
                    "<strong>Business Fundamentals:</strong> Built lasting trust with local clientele through direct service standards."
                ]
            }
        ];

        // --- Chart.js ---
        document.addEventListener('DOMContentLoaded', function() {
            const ctx = document.getElementById('competencyChart').getContext('2d');
            
            // Warm/Professional Colors
            const colorGaming = 'rgba(79, 70, 229, 0.6)'; // Indigo
            const colorVenture = 'rgba(16, 185, 129, 0.6)'; // Emerald
            
            new Chart(ctx, {
                type: 'radar',
                data: {
                    labels: [
                        'Live Ops Strategy', 
                        'Infrastructure Setup', 
                        'Cross-Functional Leadership', 
                        'Community Building', 
                        'Business Versatility', 
                        'Data Analysis'
                    ],
                    datasets: [{
                        label: 'Proficiency Level',
                        // Updated based on user feedback:
                        // Tier 1 (95): Live Ops Strategy, Cross-Functional Leadership, Business Versatility
                        // Tier 2 (85): Infrastructure Setup, Community Building, Data Analysis
                        data: [95, 85, 95, 85, 95, 85],
                        fill: true,
                        backgroundColor: 'rgba(194, 155, 64, 0.2)', // Gold/Amber tint
                        borderColor: '#c29b40',
                        pointBackgroundColor: '#c29b40',
                        pointBorderColor: '#fff',
                        pointHoverBackgroundColor: '#fff',
                        pointHoverBorderColor: '#c29b40'
                    }]
                },
                options: {
                    maintainAspectRatio: false,
                    responsive: true,
                    scales: {
                        r: {
                            angleLines: { color: '#e5e7eb' },
                            grid: { color: '#e5e7eb' },
                            pointLabels: {
                                font: { size: 12, family: 'Inter' },
                                color: '#4b5563'
                            },
                            ticks: { display: false, max: 100 },
                            min: 60 // Set minimum to make the differences more visible visually
                        }
                    },
                    plugins: {
                        legend: { display: false },
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    return context.label + ': ' + (context.raw >= 90 ? 'Expert' : 'Advanced');
                                }
                            }
                        }
                    }
                }
            });

            // Initial Timeline Render
            renderTimeline('all');
        });

        // --- Timeline Logic ---
        function renderTimeline(filter) {
            const container = document.getElementById('timeline-container');
            container.innerHTML = ''; // Clear

            const filteredData = filter === 'all' 
                ? experienceData 
                : experienceData.filter(item => item.type === filter);

            // Update button styles
            updateFilterButtons(filter);

            filteredData.forEach((item, index) => {
                const isEven = index % 2 === 0;
                // For mobile, always left aligned. For desktop, alternate if 'all', else single column
                const alignClass = (window.innerWidth >= 768 && filter === 'all') 
                    ? (isEven ? 'md:flex-row-reverse' : 'md:flex-row') 
                    : 'flex-row'; // Simplified layout logic for robustness
                
                // Color coding
                const typeColor = item.type === 'gaming' ? 'indigo' : 'emerald';
                const typeLabel = item.type === 'gaming' ? 'Gaming Ops' : 'Venture';
                
                // Create Card HTML
                const cardHTML = `
                    <div class="relative flex flex-col md:flex-row items-center md:justify-between w-full group">
                        <!-- Dot on line (Hidden on mobile) -->
                        <div class="absolute left-1/2 w-4 h-4 bg-${typeColor}-500 rounded-full border-4 border-white shadow transform -translate-x-1/2 z-10 hidden md:block"></div>

                        <!-- Spacer for alternating layout -->
                        <div class="hidden md:block w-5/12"></div>

                        <!-- Content Card -->
                        <div class="w-full md:w-5/12 mb-8 md:mb-0 relative ${isEven && filter === 'all' ? 'md:mr-auto md:text-right' : 'md:ml-auto md:text-left'}">
                            <div class="bg-white p-6 rounded-lg shadow-sm border-t-4 border-${typeColor}-500 hover:shadow-md transition cursor-pointer" onclick="toggleDetails(${item.id})">
                                <div class="flex items-center justify-between mb-2 ${isEven && filter === 'all' ? 'md:flex-row-reverse' : ''}">
                                    <span class="text-xs font-bold uppercase tracking-wider text-${typeColor}-600 bg-${typeColor}-50 px-2 py-1 rounded">${typeLabel}</span>
                                    <span class="text-sm text-gray-400">${item.period}</span>
                                </div>
                                <h3 class="text-lg font-bold text-gray-900">${item.role}</h3>
                                <div class="text-md font-medium text-gray-700 mb-2">${item.company}</div>
                                <div class="text-sm text-gray-500 italic mb-3 context-text">"${item.context}"</div>
                                
                                <div id="details-${item.id}" class="hidden mt-4 pt-4 border-t border-gray-100 text-sm text-gray-600 space-y-2 ${isEven && filter === 'all' ? 'md:text-right' : 'md:text-left'} text-left">
                                    ${item.details.map(d => `<p>${d}</p>`).join('')}
                                </div>
                                <div class="text-xs text-center text-gray-400 mt-2 group-hover:text-${typeColor}-500 transition">Click for details</div>
                            </div>
                        </div>
                    </div>
                `;
                
                // If filter is specific, use a simpler stacked layout
                if (filter !== 'all') {
                    const simpleHTML = `
                        <div class="relative w-full max-w-2xl mx-auto">
                             <div class="bg-white p-6 rounded-lg shadow-sm border-l-4 border-${typeColor}-500 hover:shadow-md transition cursor-pointer mb-6" onclick="toggleDetails(${item.id})">
                                <div class="flex flex-col sm:flex-row justify-between sm:items-center mb-2">
                                    <h3 class="text-lg font-bold text-gray-900">${item.role}</h3>
                                    <span class="text-sm text-gray-400">${item.period}</span>
                                </div>
                                <div class="text-md font-medium text-gray-700 mb-1">${item.company}</div>
                                <div class="text-sm text-gray-500 italic mb-3">"${item.context}"</div>
                                
                                <div id="details-${item.id}" class="hidden mt-4 pt-4 border-t border-gray-100 text-sm text-gray-600 space-y-2">
                                    ${item.details.map(d => `<p>${d}</p>`).join('')}
                                </div>
                                <div class="text-xs text-right text-gray-400 mt-1">Tap to expand</div>
                            </div>
                        </div>
                    `;
                    container.innerHTML += simpleHTML;
                } else {
                    container.innerHTML += cardHTML;
                }
            });
        }

        function updateFilterButtons(active) {
            const btns = ['all', 'gaming', 'venture'];
            btns.forEach(type => {
                const btn = document.getElementById(`btn-${type}`);
                if (type === active) {
                    btn.classList.add('bg-gray-800', 'text-white', 'border-transparent');
                    btn.classList.remove('bg-white', 'text-gray-600', 'text-indigo-600', 'text-emerald-600');
                } else {
                    btn.classList.remove('bg-gray-800', 'text-white');
                    btn.classList.add('bg-white');
                    // Reset specific colors
                    if(type === 'gaming') btn.classList.add('text-indigo-600', 'border-indigo-200');
                    else if(type === 'venture') btn.classList.add('text-emerald-600', 'border-emerald-200');
                    else btn.classList.add('text-gray-600', 'border-gray-200');
                }
            });
            
            // Toggle centerline visibility
            const line = document.querySelector('.timeline-line');
            if (active === 'all') line.classList.remove('hidden');
            else line.classList.add('hidden');
        }

        function filterTimeline(type) {
            renderTimeline(type);
        }

        function toggleDetails(id) {
            const el = document.getElementById(`details-${id}`);
            if (el.classList.contains('hidden')) {
                el.classList.remove('hidden');
                el.classList.add('block');
            } else {
                el.classList.add('hidden');
                el.classList.remove('block');
            }
        }

        function toggleInnovation(id) {
            const el = document.getElementById(`innov-detail-${id}`);
            if (el.classList.contains('hidden')) {
                el.classList.remove('hidden');
                el.classList.add('block');
            } else {
                el.classList.add('hidden');
                el.classList.remove('block');
            }
        }
    </script>
</body>
</html>
