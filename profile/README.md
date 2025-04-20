 <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pregnancy & Health Calculators | Due Date, Ovulation & Fertility Tracking</title>
    <meta name="description" content="Free accurate pregnancy calculators for due date, ovulation tracking, trimester calculator, BMI, fertility window & 20+ health tools. Medically reviewed & secure.">
    <meta name="keywords" content="pregnancy calculator, due date calculator, ovulation tracker, pregnancy week calculator, trimester calculator, BMI calculator, pregnancy health, fertility window, baby kick counter, age calculator">
    <meta name="author" content="Health Calculators">
    
    <!-- Open Graph / Facebook -->
    <meta property="og:type" content="website">
    <meta property="og:url" content="https://healthcalculators.example.com/">
    <meta property="og:title" content="Pregnancy & Health Calculators | Due Date, Ovulation & Fertility Tracking">
    <meta property="og:description" content="Free accurate pregnancy calculators for due date, ovulation tracking, trimester calculator, BMI, fertility window & 20+ health tools. Medically reviewed & secure.">
    <meta property="og:image" content="https://healthcalculators.example.com/images/pregnancy-calculator-social.jpg">
    
    <!-- Twitter -->
    <meta property="twitter:card" content="summary_large_image">
    <meta property="twitter:url" content="https://healthcalculators.example.com/">
    <meta property="twitter:title" content="Pregnancy & Health Calculators | Due Date, Ovulation & Fertility Tracking">
    <meta property="twitter:description" content="Free accurate pregnancy calculators for due date, ovulation tracking, trimester calculator, BMI, fertility window & 20+ health tools. Medically reviewed & secure.">
    <meta property="twitter:image" content="https://healthcalculators.example.com/images/pregnancy-calculator-social.jpg">

    <!-- Canonical URL -->
    <link rel="canonical" href="https://healthcalculators.example.com/">
    
    <!-- Favicon -->
    <link rel="icon" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='80' font-size='80'>👶</text></svg>">

    <!-- Tailwind CSS -->
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/css/all.min.css">
    
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

    <!-- Schema.org markup for Google -->
    <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "WebApplication",
      "name": "Pregnancy & Health Calculators",
      "url": "https://healthcalculators.example.com/",
      "description": "All-in-one pregnancy and health calculator toolkit. Calculate your due date, track ovulation, monitor pregnancy progress, and maintain health metrics with professional tools.",
      "applicationCategory": "HealthApplication",
      "operatingSystem": "All",
      "offers": {
        "@type": "Offer",
        "price": "0",
        "priceCurrency": "USD"
      },
      "creator": {
        "@type": "Organization",
        "name": "Health Calculators",
        "url": "https://healthcalculators.example.com/"
      }
    }
    </script>
    
    <style>
        :root {
            --primary-color: #ff6b8b;
            --secondary-color: #7209b7;
            --accent-color: #4cc9f0;
            --light-bg: #f8f9fa;
            --dark-bg: #2b2d42;
        }

        body {
            font-family: 'Poppins', sans-serif;
            scroll-behavior: smooth;
        }

        .calculator-tab {
            display: none;
        }

        .calculator-tab.active {
            display: block;
        }

        .nav-link {
            transition: all 0.3s ease;
            border-bottom: 2px solid transparent;
        }

        .nav-link:hover, .nav-link.active {
            border-bottom: 2px solid var(--primary-color);
            color: var(--primary-color);
        }

        .custom-btn {
            background: linear-gradient(to right, var(--primary-color), var(--secondary-color));
            transition: all 0.3s ease;
        }

        .custom-btn:hover { 
            transform: translateY(-2px); 
            box-shadow: 0 4px 8px rgba(0,0,0,0.2); 
        }

        .card {
            transition: all 0.3s ease;
        }

        .card:hover { 
            transform: translateY(-5px); 
            box-shadow: 0 10px 20px rgba(0,0,0,0.1); 
        }

        .result-container {
            background-color: var(--light-bg);
            border-left: 4px solid var(--primary-color);
        }

        /* Modal styles */
        .modal {
            display: none;
            position: fixed;
            z-index: 100;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(0,0,0,0.5);
        }

        .modal-content {
            background-color: #fefefe;
            margin: 5% auto;
            padding: 20px;
            border-radius: 8px;
            width: 80%;
            max-width: 800px;
            max-height: 80vh;
            overflow-y: auto;
        }

        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
        }

        .close:hover,
        .close:focus {
            color: black;
            text-decoration: none;
            cursor: pointer;
        }

        /* Age calculator specific styles */
        .age-result-item {
            background-color: white;
            border-radius: 0.5rem;
            padding: 1rem;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }

        /* Responsive adjustments */
        @media (max-width: 768px) {
            .modal-content {
                width: 90%;
                margin: 10% auto;
            }
        }
    </style>
</head>
<body class="bg-gray-50">
    <!-- Header Section -->
    <header class="bg-white shadow-md">
        <div class="container mx-auto px-4 py-6">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="flex items-center mb-4 md:mb-0">
                    <a href="#" class="flex items-center">
                        <i class="fas fa-baby text-4xl text-pink-500 mr-3"></i>
                        <h1 class="text-2xl md:text-3xl font-bold text-gray-800">Pregnancy & Health <span class="text-pink-500">Calculators</span></h1>
                    </a>
                </div>
                <nav class="flex flex-wrap justify-center">
                    <a href="#calculators" class="bg-pink-500 hover:bg-pink-600 text-white font-medium py-2 px-4 rounded-full transition duration-300 ease-in-out transform hover:-translate-y-1 shadow-md mx-1 mb-2 md:mb-0 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                        <i class="fas fa-calculator mr-2"></i>View Calculators
                    </a>
                    <button onclick="openModal('about-modal')" class="mx-1 font-medium py-2 px-4 text-gray-700 hover:text-pink-500 transition duration-300">About</button>
                    <button onclick="openModal('privacy-modal')" class="mx-1 font-medium py-2 px-4 text-gray-700 hover:text-pink-500 transition duration-300">Privacy</button>
                    <button onclick="openModal('terms-modal')" class="mx-1 font-medium py-2 px-4 text-gray-700 hover:text-pink-500 transition duration-300">Terms</button>
                    <button onclick="openModal('disclaimer-modal')" class="mx-1 font-medium py-2 px-4 text-gray-700 hover:text-pink-500 transition duration-300">Disclaimer</button>
                </nav>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="bg-gradient-to-r from-pink-500 to-purple-600 text-white py-16">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 mb-8 md:mb-0">
                    <h2 class="text-3xl md:text-4xl font-bold mb-4">Your Complete Pregnancy & Health Journey</h2>
                    <p class="text-lg mb-6">Access 20+ professional calculators to track your pregnancy, fertility, and overall health metrics all in one place.</p>
                    <div class="flex flex-wrap">
                        <button class="bg-white text-pink-600 font-medium py-2 px-6 rounded-full mr-4 mb-2 transition duration-300 ease-in-out transform hover:scale-105 hover:shadow-lg" onclick="scrollToCalculatorSection('pregnancy-due-date')">
                            <i class="fas fa-calendar-alt mr-2"></i>Calculate Due Date
                        </button>
                        <button class="bg-transparent border-2 border-white text-white font-medium py-2 px-6 rounded-full mb-2 transition duration-300 ease-in-out transform hover:scale-105 hover:bg-white hover:text-pink-600" onclick="scrollToCalculatorSection('bmi-calculator')">
                            <i class="fas fa-weight mr-2"></i>Check BMI
                        </button>
                    </div>
                </div>
                <div class="md:w-1/2 flex justify-center">
                    <div class="relative w-64 h-64 md:w-80 md:h-80">
                        <div class="absolute inset-0 bg-white rounded-full opacity-20 animate-pulse"></div>
                        <div class="absolute inset-4 bg-white rounded-full opacity-30 animate-pulse" style="animation-delay: 0.3s"></div>
                        <div class="absolute inset-8 bg-white rounded-full opacity-40 animate-pulse" style="animation-delay: 0.6s"></div>
                        <div class="absolute inset-0 flex items-center justify-center">
                            <i class="fas fa-heartbeat text-white text-6xl animate-pulse"></i>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-12 text-gray-800">Why Use Our <span class="text-pink-500">Calculators</span></h2>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="bg-white rounded-lg shadow-lg p-6 text-center hover:shadow-xl transition-shadow duration-300">
                    <div class="text-pink-500 text-4xl mb-4">
                        <i class="fas fa-check-circle"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Accurate & Reliable</h3>
                    <p class="text-gray-600">All calculators use medically-reviewed formulas to ensure accurate results for your health planning.</p>
                </div>
                <div class="bg-white rounded-lg shadow-lg p-6 text-center hover:shadow-xl transition-shadow duration-300">
                    <div class="text-pink-500 text-4xl mb-4">
                        <i class="fas fa-lock"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Private & Secure</h3>
                    <p class="text-gray-600">Your data never leaves your device - all calculations happen locally in your browser.</p>
                </div>
                <div class="bg-white rounded-lg shadow-lg p-6 text-center hover:shadow-xl transition-shadow duration-300">
                    <div class="text-pink-500 text-4xl mb-4">
                        <i class="fas fa-mobile-alt"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-2">Mobile Friendly</h3>
                    <p class="text-gray-600">Access all calculators on any device - desktop, tablet, or mobile phone.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Calculators Navigation -->
    <section id="calculators" class="py-10 bg-gray-100">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-8 text-gray-800">Our <span class="text-pink-500">Calculators</span></h2>
            <div class="flex flex-wrap justify-center tab-navigation mb-8 overflow-x-auto whitespace-nowrap pb-2">
                <button class="nav-link active mx-2 px-4 py-2 text-gray-700 font-medium text-sm rounded-full hover:bg-pink-100 focus:outline-none" onclick="openCalculator('pregnancy-due-date')">Due Date</button>
                <button class="nav-link mx-2 px-4 py-2 text-gray-700 font-medium text-sm rounded-full hover:bg-pink-100 focus:outline-none" onclick="openCalculator('ovulation-calculator')">Ovulation</button>
                <button class="nav-link mx-2 px-4 py-2 text-gray-700 font-medium text-sm rounded-full hover:bg-pink-100 focus:outline-none" onclick="openCalculator('baby-kick-counter')">Kick Counter</button>
                <button class="nav-link mx-2 px-4 py-2 text-gray-700 font-medium text-sm rounded-full hover:bg-pink-100 focus:outline-none" onclick="openCalculator('trimester-calculator')">Trimesters</button>
                <button class="nav-link mx-2 px-4 py-2 text-gray-700 font-medium text-sm rounded-full hover:bg-pink-100 focus:outline-none" onclick="openCalculator('period-tracker')">Period Tracker</button>
                <button class="nav-link mx-2 px-4 py-2 text-gray-700 font-medium text-sm rounded-full hover:bg-pink-100 focus:outline-none" onclick="openCalculator('bmi-calculator')">BMI</button>
                <button class="nav-link mx-2 px-4 py-2 text-gray-700 font-medium text-sm rounded-full hover:bg-pink-100 focus:outline-none" onclick="openCalculator('age-calculator')">Age</button>
                <button class="nav-link mx-2 px-4 py-2 text-gray-700 font-medium text-sm rounded-full hover:bg-pink-100 focus:outline-none" onclick="openCalculator('weight-gain-calculator')">Weight Gain</button>
                <button class="nav-link mx-2 px-4 py-2 text-gray-700 font-medium text-sm rounded-full hover:bg-pink-100 focus:outline-none" onclick="openCalculator('nutrition-calculator')">Nutrition</button>
                <button class="nav-link mx-2 px-4 py-2 text-gray-700 font-medium text-sm rounded-full hover:bg-pink-100 focus:outline-none" onclick="openCalculator('blood-volume-calculator')">Blood Volume</button>
                <button class="nav-link mx-2 px-4 py-2 text-gray-700 font-medium text-sm rounded-full hover:bg-pink-100 focus:outline-none" onclick="openCalculator('labor-probability-calculator')">Labor Probability</button>
                <button class="nav-link mx-2 px-4 py-2 text-gray-700 font-medium text-sm rounded-full hover:bg-pink-100 focus:outline-none" onclick="openCalculator('breastfeeding-calculator')">Breastfeeding</button>
                <button class="nav-link mx-2 px-4 py-2 text-gray-700 font-medium text-sm rounded-full hover:bg-pink-100 focus:outline-none" onclick="openCalculator('fertility-age-calculator')">Fertility Age</button>
                <button class="nav-link mx-2 px-4 py-2 text-gray-700 font-medium text-sm rounded-full hover:bg-pink-100 focus:outline-none" onclick="openCalculator('conception-probability-calculator')">Conception Probability</button>
                <button class="nav-link mx-2 px-4 py-2 text-gray-700 font-medium text-sm rounded-full hover:bg-pink-100 focus:outline-none" onclick="openCalculator('ivf-success-calculator')">IVF Success</button>
                <button class="nav-link mx-2 px-4 py-2 text-gray-700 font-medium text-sm rounded-full hover:bg-pink-100 focus:outline-none" onclick="openCalculator('baby-growth-calculator')">Baby Growth</button>
                <button class="nav-link mx-2 px-4 py-2 text-gray-700 font-medium text-sm rounded-full hover:bg-pink-100 focus:outline-none" onclick="openCalculator('baby-feeding-calculator')">Baby Feeding</button>
                <button class="nav-link mx-2 px-4 py-2 text-gray-700 font-medium text-sm rounded-full hover:bg-pink-100 focus:outline-none" onclick="openCalculator('baby-sleep-calculator')">Baby Sleep</button>
                <button class="nav-link mx-2 px-4 py-2 text-gray-700 font-medium text-sm rounded-full hover:bg-pink-100 focus:outline-none" onclick="openCalculator('height-predictor')">Height Predictor</button>
                <button class="nav-link mx-2 px-4 py-2 text-gray-700 font-medium text-sm rounded-full hover:bg-pink-100 focus:outline-none" onclick="openCalculator('body-fat-calculator')">Body Fat</button>
                <button class="nav-link mx-2 px-4 py-2 text-gray-700 font-medium text-sm rounded-full hover:bg-pink-100 focus:outline-none" onclick="openCalculator('calorie-needs-calculator')">Calorie Needs</button>
                <button class="nav-link mx-2 px-4 py-2 text-gray-700 font-medium text-sm rounded-full hover:bg-pink-100 focus:outline-none" onclick="openCalculator('water-intake-calculator')">Water Intake</button>
                <button class="nav-link mx-2 px-4 py-2 text-gray-700 font-medium text-sm rounded-full hover:bg-pink-100 focus:outline-none" onclick="openCalculator('heart-rate-calculator')">Heart Rate</button>
                <button class="nav-link mx-2 px-4 py-2 text-gray-700 font-medium text-sm rounded-full hover:bg-pink-100 focus:outline-none" onclick="openCalculator('postpartum-calculator')">Postpartum</button>
            </div>

            <!-- Calculator Containers -->
            <div class="calculator-container bg-white rounded-xl shadow-lg p-6 md:p-8">
                <!-- Pregnancy Due Date Calculator -->
                <div id="pregnancy-due-date" class="calculator-tab active">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">Pregnancy Due Date Calculator</h3>
                    <p class="text-gray-600 mb-6">Calculate your estimated due date based on your last menstrual period or conception date.</p>

                    <div class="bg-pink-50 p-4 rounded-lg mb-6">
                        <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-pink-500 mr-2"></i> A typical pregnancy lasts about 40 weeks (280 days) from the first day of your last menstrual period to your due date.</p>
                    </div>

                    <form id="due-date-form" class="mb-6">
                        <div class="mb-4">
                            <label class="block text-gray-700 font-medium mb-2">Calculation Method</label>
                            <div class="flex flex-wrap">
                                <label class="inline-flex items-center mr-6 mb-2">
                                    <input type="radio" name="calculationMethod" value="lmp" checked class="form-radio text-pink-500 focus:ring-pink-500 h-4 w-4">
                                    <span class="ml-2">Last Menstrual Period</span>
                                </label>
                                <label class="inline-flex items-center mb-2">
                                    <input type="radio" name="calculationMethod" value="conception" class="form-radio text-pink-500 focus:ring-pink-500 h-4 w-4">
                                    <span class="ml-2">Conception Date</span>
                                </label>
                            </div>
                        </div>

                        <div id="lmp-input" class="mb-4">
                            <label for="lmpDate" class="block text-gray-700 font-medium mb-2">First day of last menstrual period</label>
                            <input type="date" id="lmpDate" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div id="conception-input" class="mb-4 hidden">
                            <label for="conceptionDate" class="block text-gray-700 font-medium mb-2">Conception Date</label>
                            <input type="date" id="conceptionDate" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="cycleLength" class="block text-gray-700 font-medium mb-2">Average Menstrual Cycle Length (days)</label>
                            <div class="flex items-center">
                                <input type="number" id="cycleLength" value="28" min="21" max="45" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                                <div class="tooltip ml-2">
                                    <i class="fas fa-question-circle text-gray-400"></i>
                                    <span class="tooltiptext">The average cycle is 28 days, but can range from 21 to 45 days.</span>
                                </div>
                            </div>
                        </div>

                        <button type="button" id="calculateDueDate" class="w-full bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-4 rounded-md transition duration-300 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                            Calculate Due Date
                        </button>
                    </form>

                    <div id="due-date-result" class="hidden bg-gray-50 rounded-lg p-6 border-l-4 border-pink-500">
                        <h4 class="text-xl font-semibold text-gray-800 mb-4">Your Pregnancy Timeline</h4>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-4">
                            <div>
                                <p class="text-gray-600 mb-1">Due Date:</p>
                                <p class="text-xl font-bold text-pink-600" id="dueDate">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Current Week:</p>
                                <p class="text-xl font-bold text-pink-600" id="currentWeek">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">First Trimester:</p>
                                <p class="font-medium" id="firstTrimester">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Second Trimester:</p>
                                <p class="font-medium" id="secondTrimester">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Third Trimester:</p>
                                <p class="font-medium" id="thirdTrimester">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Estimated Conception Date:</p>
                                <p class="font-medium" id="conceptionDateResult">-</p>
                            </div>
                        </div>
                        <div class="mt-6">
                            <p class="text-gray-600 mb-2">Pregnancy Progress:</p>
                            <div class="w-full bg-gray-200 rounded-full h-2.5">
                                <div class="bg-pink-500 h-2.5 rounded-full" id="pregnancyProgress" style="width: 0%"></div>
                            </div>
                            <p class="text-sm text-gray-500 mt-2 text-right"><span id="progressPercentage">0%</span> Complete</p>
                        </div>
                    </div>
                </div>

                <!-- Ovulation Calculator -->
                <div id="ovulation-calculator" class="calculator-tab">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">Ovulation Calculator</h3>
                    <p class="text-gray-600 mb-6">Track your fertile window and find the best days to conceive.</p>

                    <div class="bg-pink-50 p-4 rounded-lg mb-6">
                        <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-pink-500 mr-2"></i> Ovulation typically occurs 14 days before the start of your next period. The fertile window includes 5 days before ovulation and the day of ovulation.</p>
                    </div>

                    <form id="ovulation-form" class="mb-6">
                        <div class="mb-4">
                            <label for="lastPeriodDate" class="block text-gray-700 font-medium mb-2">First day of last period</label>
                            <input type="date" id="lastPeriodDate" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="ovulationCycleLength" class="block text-gray-700 font-medium mb-2">Average Cycle Length (days)</label>
                            <div class="flex items-center">
                                <input type="number" id="ovulationCycleLength" value="28" min="21" max="45" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                                <div class="tooltip ml-2">
                                    <i class="fas fa-question-circle text-gray-400"></i>
                                    <span class="tooltiptext">The average cycle is 28 days, but can range from 21 to 45 days.</span>
                                </div>
                            </div>
                        </div>

                        <div class="mb-4">
                            <label for="lutealPhaseLength" class="block text-gray-700 font-medium mb-2">Luteal Phase Length (days)</label>
                            <div class="flex items-center">
                                <input type="number" id="lutealPhaseLength" value="14" min="10" max="16" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                                <div class="tooltip ml-2">
                                    <i class="fas fa-question-circle text-gray-400"></i>
                                    <span class="tooltiptext">The luteal phase is typically 14 days, but can range from 10 to 16 days.</span>
                                </div>
                            </div>
                        </div>

                        <button type="button" id="calculateOvulation" class="w-full bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-4 rounded-md transition duration-300 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                            Calculate Ovulation
                        </button>
                    </form>

                    <div id="ovulation-result" class="hidden bg-gray-50 rounded-lg p-6 border-l-4 border-pink-500">
                        <h4 class="text-xl font-semibold text-gray-800 mb-4">Your Fertility Window</h4>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-4">
                            <div>
                                <p class="text-gray-600 mb-1">Most Fertile Day:</p>
                                <p class="text-xl font-bold text-pink-600" id="ovulationDate">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Fertile Window:</p>
                                <p class="text-xl font-bold text-pink-600" id="fertileWindow">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Next Period:</p>
                                <p class="font-medium" id="nextPeriod">-</p>
                            </div>
                        </div>
                        <div class="mt-6">
                            <h5 class="font-semibold mb-3">Monthly Fertility Calendar</h5>
                            <div id="fertilityCalendar" class="grid grid-cols-7 gap-1">
                                <!-- Calendar will be generated here -->
                            </div>
                            <div class="flex flex-wrap mt-4 text-sm">
                                <div class="flex items-center mr-4 mb-2">
                                    <div class="w-3 h-3 rounded-full bg-pink-500 mr-1"></div>
                                    <span>Ovulation Day</span>
                                </div>
                                <div class="flex items-center mr-4 mb-2">
                                    <div class="w-3 h-3 rounded-full bg-pink-200 mr-1"></div>
                                    <span>Fertile Window</span>
                                </div>
                                <div class="flex items-center mr-4 mb-2">
                                    <div class="w-3 h-3 rounded-full bg-red-200 mr-1"></div>
                                    <span>Period</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Baby Kick Counter -->
                <div id="baby-kick-counter" class="calculator-tab">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">Baby Kick Counter</h3>
                    <p class="text-gray-600 mb-6">Track your baby's movements to monitor their well-being during pregnancy.</p>

                    <div class="bg-pink-50 p-4 rounded-lg mb-6">
                        <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-pink-500 mr-2"></i> Healthcare providers recommend counting 10 movements within a 2-hour period. If you don't feel 10 movements in that time, contact your healthcare provider.</p>
                    </div>

                    <div class="text-center mb-8">
                        <div class="inline-block bg-white rounded-full shadow-lg p-6 mb-4">
                            <div id="kick-counter-display" class="text-5xl font-bold text-pink-600">0</div>
                            <p class="text-gray-500 mt-2">Kicks Counted</p>
                        </div>
                        <div class="mb-4">
                            <button id="record-kick" class="bg-pink-500 hover:bg-pink-600 text-white font-bold py-4 px-8 rounded-full text-lg transition duration-300 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                                <i class="fas fa-baby mr-2"></i> Record Kick
                            </button>
                        </div>
                        <div class="flex justify-center space-x-4 mb-4">
                            <button id="start-session" class="bg-green-500 hover:bg-green-600 text-white font-bold py-2 px-4 rounded-md transition duration-300">
                                <i class="fas fa-play mr-1"></i> Start
                            </button>
                            <button id="pause-session" class="bg-yellow-500 hover:bg-yellow-600 text-white font-bold py-2 px-4 rounded-md transition duration-300" disabled>
                                <i class="fas fa-pause mr-1"></i> Pause
                            </button>
                            <button id="reset-session" class="bg-red-500 hover:bg-red-600 text-white font-bold py-2 px-4 rounded-md transition duration-300" disabled>
                                <i class="fas fa-redo mr-1"></i> Reset
                            </button>
                        </div>
                        <div id="session-timer" class="text-2xl font-medium text-gray-700 mb-2">00:00:00</div>
                        <p id="session-status" class="text-sm text-gray-500 mb-4">Session not started</p>
                    </div>

                    <div id="kick-history" class="hidden bg-gray-50 rounded-lg p-6 border-l-4 border-pink-500">
                        <h4 class="text-xl font-semibold text-gray-800 mb-4">Kick Session Summary</h4>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                            <div>
                                <p class="text-gray-600 mb-1">Total Kicks:</p>
                                <p class="text-xl font-bold text-pink-600" id="total-kicks">0</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Session Duration:</p>
                                <p class="text-xl font-bold text-pink-600" id="session-duration">00:00:00</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Time to 10 Kicks:</p>
                                <p class="font-medium" id="time-to-ten">Not reached</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Session Date:</p>
                                <p class="font-medium" id="session-date"></p>
                            </div>
                        </div>
                        <div class="mt-6">
                            <h5 class="font-semibold mb-3">Kick Timeline</h5>
                            <div id="kick-timeline" class="text-sm text-gray-600">
                                <!-- Timeline will be generated here -->
                            </div>
                        </div>
                    </div>

                    <div class="mt-6">
                        <h5 class="font-semibold mb-3">Previous Sessions</h5>
                        <div id="previous-sessions" class="text-sm text-gray-600">
                            <p class="text-center text-gray-500 italic">No previous sessions recorded</p>
                        </div>
                    </div>
                </div>

                <!-- Trimester Calculator -->
                <div id="trimester-calculator" class="calculator-tab">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">Trimester Calculator</h3>
                    <p class="text-gray-600 mb-6">Track which trimester you're in and key milestones during your pregnancy.</p>

                    <div class="bg-pink-50 p-4 rounded-lg mb-6">
                        <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-pink-500 mr-2"></i> Pregnancy is divided into three trimesters: First (weeks 1-13), Second (weeks 14-27), and Third (week 28 to birth).</p>
                    </div>

                    <form id="trimester-form" class="mb-6">
                        <div class="mb-4">
                            <label class="block text-gray-700 font-medium mb-2">Enter Information</label>
                            <div class="flex flex-wrap">
                                <label class="inline-flex items-center mr-6 mb-2">
                                    <input type="radio" name="trimesterMethod" value="lmp" checked class="form-radio text-pink-500 focus:ring-pink-500 h-4 w-4">
                                    <span class="ml-2">Last Menstrual Period</span>
                                </label>
                                <label class="inline-flex items-center mb-2">
                                    <input type="radio" name="trimesterMethod" value="dueDate" class="form-radio text-pink-500 focus:ring-pink-500 h-4 w-4">
                                    <span class="ml-2">Due Date</span>
                                </label>
                            </div>
                        </div>

                        <div id="trimester-lmp-input" class="mb-4">
                            <label for="trimesterLmpDate" class="block text-gray-700 font-medium mb-2">First day of last menstrual period</label>
                            <input type="date" id="trimesterLmpDate" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div id="trimester-due-date-input" class="mb-4 hidden">
                            <label for="trimesterDueDate" class="block text-gray-700 font-medium mb-2">Expected Due Date</label>
                            <input type="date" id="trimesterDueDate" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <button type="button" id="calculateTrimester" class="w-full bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-4 rounded-md transition duration-300 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                            Calculate Trimesters
                        </button>
                    </form>

                    <div id="trimester-result" class="hidden bg-gray-50 rounded-lg p-6 border-l-4 border-pink-500">
                        <h4 class="text-xl font-semibold text-gray-800 mb-4">Your Pregnancy Timeline</h4>
                        <div class="mb-6">
                            <p class="text-gray-600 mb-1">You are currently in:</p>
                            <p class="text-2xl font-bold text-pink-600" id="current-trimester">-</p>
                            <p class="text-gray-600 mb-1 mt-2">Due Date:</p>
                            <p class="text-xl font-bold text-pink-600" id="trimester-due-date-result">-</p>
                        </div>
                        <div class="mb-4">
                            <div class="w-full bg-gray-200 rounded-full h-2.5 mb-2">
                                <div class="bg-pink-500 h-2.5 rounded-full" id="pregnancy-progress-bar" style="width: 0%"></div>
                            </div>
                            <p class="text-sm text-gray-500 text-right" id="pregnancy-progress-text">0% Complete</p>
                        </div>
                        <div class="grid grid-cols-1 md:grid-cols-3 gap-4 mb-4">
                            <div class="p-4 bg-white rounded-lg shadow border-t-4 border-blue-400">
                                <h5 class="font-semibold text-blue-500 mb-2">First Trimester</h5>
                                <p class="text-sm text-gray-600 mb-2" id="first-trimester-dates">-</p>
                                <ul class="text-sm text-gray-600 list-disc list-inside">
                                    <li>Major organ development</li>
                                    <li>Morning sickness common</li>
                                    <li>Fatigue and tiredness</li>
                                </ul>
                            </div>
                            <div class="p-4 bg-white rounded-lg shadow border-t-4 border-green-400">
                                <h5 class="font-semibold text-green-500 mb-2">Second Trimester</h5>
                                <p class="text-sm text-gray-600 mb-2" id="second-trimester-dates">-</p>
                                <ul class="text-sm text-gray-600 list-disc list-inside">
                                    <li>Baby movement begins</li>
                                    <li>Gender can be determined</li>
                                    <li>Energy levels improve</li>
                                </ul>
                            </div>
                            <div class="p-4 bg-white rounded-lg shadow border-t-4 border-purple-400">
                                <h5 class="font-semibold text-purple-500 mb-2">Third Trimester</h5>
                                <p class="text-sm text-gray-600 mb-2" id="third-trimester-dates">-</p>
                                <ul class="text-sm text-gray-600 list-disc list-inside">
                                    <li>Baby gains weight</li>
                                    <li>More frequent movements</li>
                                    <li>Preparation for birth</li>
                                </ul>
                            </div>
                        </div>
                        <div class="mt-6">
                            <h5 class="font-semibold mb-3">Key Milestones</h5>
                            <div id="pregnancy-milestones" class="space-y-3">
                                <!-- Milestones will be generated here -->
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Period Tracker -->
                <div id="period-tracker" class="calculator-tab">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">Period Tracker</h3>
                    <p class="text-gray-600 mb-6">Track your menstrual cycle, predict your next period, and monitor cycle regularity.</p>

                    <div class="bg-pink-50 p-4 rounded-lg mb-6">
                        <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-pink-500 mr-2"></i> Regular tracking of your period can help identify irregularities and provide insights about your reproductive health.</p>
                    </div>

                    <form id="period-tracker-form" class="mb-6">
                        <div class="mb-4">
                            <label for="lastPeriodStartDate" class="block text-gray-700 font-medium mb-2">First day of your last period</label>
                            <input type="date" id="lastPeriodStartDate" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="periodLength" class="block text-gray-700 font-medium mb-2">Average Period Length (days)</label>
                            <div class="flex items-center">
                                <input type="number" id="periodLength" value="5" min="1" max="10" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                                <div class="tooltip ml-2">
                                    <i class="fas fa-question-circle text-gray-400"></i>
                                    <span class="tooltiptext">Most periods last between 3-7 days.</span>
                                </div>
                            </div>
                        </div>

                        <div class="mb-4">
                            <label for="periodCycleLength" class="block text-gray-700 font-medium mb-2">Average Cycle Length (days)</label>
                            <div class="flex items-center">
                                <input type="number" id="periodCycleLength" value="28" min="21" max="45" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                                <div class="tooltip ml-2">
                                    <i class="fas fa-question-circle text-gray-400"></i>
                                    <span class="tooltiptext">The average cycle is 28 days, but can range from 21 to 45 days.</span>
                                </div>
                            </div>
                        </div>

                        <button type="button" id="calculatePeriodTracker" class="w-full bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-4 rounded-md transition duration-300 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                            Calculate Next Period
                        </button>
                    </form>

                    <div id="period-tracker-result" class="hidden bg-gray-50 rounded-lg p-6 border-l-4 border-pink-500">
                        <h4 class="text-xl font-semibold text-gray-800 mb-4">Your Menstrual Cycle</h4>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-6">
                            <div>
                                <p class="text-gray-600 mb-1">Next Period Expected:</p>
                                <p class="text-xl font-bold text-pink-600" id="next-period-date">-</p>
                                <p class="text-sm text-gray-500" id="days-until-period">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Fertile Window:</p>
                                <p class="text-xl font-bold text-pink-600" id="period-fertile-window">-</p>
                                <p class="text-sm text-gray-500" id="fertility-status">-</p>
                            </div>
                        </div>
                        <div class="mb-6">
                            <div class="w-full h-8 rounded-full bg-gray-200 overflow-hidden">
                                <div class="h-full bg-gradient-to-r from-pink-500 via-yellow-500 to-green-500 relative" id="period-cycle-indicator" style="width: 100%"></div>
                            </div>
                            <div class="flex justify-between text-xs text-gray-500 mt-1">
                                <span>Period</span>
                                <span>Follicular</span>
                                <span>Ovulation</span>
                                <span>Luteal</span>
                                <span>Next Period</span>
                            </div>
                        </div>
                        <div class="mt-6">
                            <h5 class="font-semibold mb-3">3-Month Period Calendar</h5>
                            <div id="period-calendar" class="space-y-4">
                                <!-- Calendar will be generated here -->
                            </div>
                        </div>
                    </div>
                </div>

                <!-- BMI Calculator -->
                <div id="bmi-calculator" class="calculator-tab">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">BMI Calculator</h3>
                    <p class="text-gray-600 mb-6">Calculate your Body Mass Index (BMI) to assess if your weight is healthy for your height.</p>

                    <div class="bg-pink-50 p-4 rounded-lg mb-6">
                        <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-pink-500 mr-2"></i> BMI is a measure of body fat based on height and weight. It's an important indicator for weight categories that may lead to health problems.</p>
                    </div>

                    <form id="bmi-form" class="mb-6">
                        <div class="mb-4">
                            <label class="block text-gray-700 font-medium mb-2">Unit System</label>
                            <div class="flex">
                                <label class="inline-flex items-center mr-6">
                                    <input type="radio" name="bmiUnitSystem" value="metric" checked class="form-radio text-pink-500 focus:ring-pink-500 h-4 w-4">
                                    <span class="ml-2">Metric (kg, cm)</span>
                                </label>
                                <label class="inline-flex items-center">
                                    <input type="radio" name="bmiUnitSystem" value="imperial" class="form-radio text-pink-500 focus:ring-pink-500 h-4 w-4">
                                    <span class="ml-2">Imperial (lb, in)</span>
                                </label>
                            </div>
                        </div>

                        <div id="bmi-metric-inputs">
                            <div class="mb-4">
                                <label for="weight-kg" class="block text-gray-700 font-medium mb-2">Weight (kg)</label>
                                <input type="number" id="weight-kg" placeholder="e.g. 70" min="30" max="300" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                            </div>

                            <div class="mb-4">
                                <label for="height-cm" class="block text-gray-700 font-medium mb-2">Height (cm)</label>
                                <input type="number" id="height-cm" placeholder="e.g. 170" min="100" max="250" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                            </div>
                        </div>

                        <div id="bmi-imperial-inputs" class="hidden">
                            <div class="mb-4">
                                <label for="weight-lb" class="block text-gray-700 font-medium mb-2">Weight (lb)</label>
                                <input type="number" id="weight-lb" placeholder="e.g. 154" min="66" max="660" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                            </div>

                            <div class="grid grid-cols-2 gap-4 mb-4">
                                <div>
                                    <label for="height-ft" class="block text-gray-700 font-medium mb-2">Height (ft)</label>
                                    <input type="number" id="height-ft" placeholder="e.g. 5" min="3" max="8" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                                </div>
                                <div>
                                    <label for="height-in" class="block text-gray-700 font-medium mb-2">Height (in)</label>
                                    <input type="number" id="height-in" placeholder="e.g. 7" min="0" max="11" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                                </div>
                            </div>
                        </div>

                        <button type="button" id="calculateBMI" class="w-full bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-4 rounded-md transition duration-300 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                            Calculate BMI
                        </button>
                    </form>

                    <div id="bmi-result" class="hidden bg-gray-50 rounded-lg p-6 border-l-4 border-pink-500">
                        <h4 class="text-xl font-semibold text-gray-800 mb-4">Your BMI Results</h4>
                        <div class="flex flex-col md:flex-row items-center mb-6">
                            <div class="w-32 h-32 rounded-full bg-gradient-to-r from-pink-400 to-pink-600 flex items-center justify-center text-white mb-4 md:mb-0 md:mr-6">
                                <div class="text-center">
                                    <div class="text-3xl font-bold" id="bmi-value">-</div>
                                    <div class="text-sm">BMI</div>
                                </div>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Weight Category:</p>
                                <p class="text-xl font-bold" id="bmi-category">-</p>
                                <p class="text-gray-600 text-sm mt-2" id="bmi-message">-</p>
                            </div>
                        </div>
                        <div class="mb-6">
                            <div class="relative pt-4">
                                <div class="flex mb-2">
                                    <div class="flex-1 text-center text-xs">
                                        <span class="bg-blue-500 block h-2 rounded-l-full"></span>
                                        Underweight
                                    </div>
                                    <div class="flex-1 text-center text-xs">
                                        <span class="bg-green-500 block h-2"></span>
                                        Normal
                                    </div>
                                    <div class="flex-1 text-center text-xs">
                                        <span class="bg-yellow-500 block h-2"></span>
                                        Overweight
                                    </div>
                                    <div class="flex-1 text-center text-xs">
                                        <span class="bg-red-500 block h-2 rounded-r-full"></span>
                                        Obese
                                    </div>
                                </div>
                                <div class="w-4 h-4 absolute top-0 transform -translate-x-1/2 -translate-y-1/2 bg-white border-2 border-gray-800 rounded-full" id="bmi-indicator" style="left: 0%"></div>
                            </div>
                            <div class="flex justify-between text-xs text-gray-500 mt-1">
                                <span>16</span>
                                <span>18.5</span>
                                <span>25</span>
                                <span>30</span>
                                <span>40</span>
                            </div>
                        </div>
                        <div class="grid grid-cols-1 md:grid-cs-2 gap-4 mb-4">
                            <div class="bg-white p-4 rounded-lg shadow">
                                <h5 class="font-semibold text-lg mb-3">Healthy Weight Range</h5>
                                <p class="text-gray-600" id="healthy-weight-range">-</p>
                            </div>
                            <div class="bg-white p-4 rounded-lg shadow">
                                <h5 class="font-semibold text-lg mb-3">Weight Change Needed</h5>
                                <p class="text-gray-600" id="weight-change-needed">-</p>
                            </div>
                        </div>
                        <div class="bg-blue-50 p-4 rounded-lg mt-4">
                            <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-blue-500 mr-2"></i> BMI is a screening tool, not a diagnostic of body fatness or health. Consult healthcare providers for a complete health assessment.</p>
                        </div>
                    </div>
                </div>

                <!-- Age Calculator -->
                <div id="age-calculator" class="calculator-tab">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">Age Calculator</h3>
                    <p class="text-gray-600 mb-6">Calculate your exact age in years, months, days, hours, minutes, and seconds based on your birth date.</p>

                    <div class="bg-pink-50 p-4 rounded-lg mb-6">
                        <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-pink-500 mr-2"></i> Did you know? The average human lives for approximately 2.2 billion heartbeats regardless of species. That's about 672,768,000 seconds or 77,870 days.</p>
                    </div>

                    <form id="age-form" class="mb-6">
                        <div class="mb-4">
                            <label for="birthday" class="block text-gray-700 font-medium mb-2">Birth Date</label>
                            <input type="date" id="birthday" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="birth-time" class="block text-gray-700 font-medium mb-2">Birth Time (optional)</label>
                            <input type="time" id="birth-time" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <button type="button" id="calculateAge" class="w-full bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-4 rounded-md transition duration-300 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                            Calculate My Age
                        </button>
                    </form>

                    <div id="age-result" class="hidden bg-gray-50 rounded-lg p-6 border-l-4 border-pink-500">
                        <h4 class="text-xl font-semibold text-gray-800 mb-4">Your Age Results</h4>
                        <div class="flex flex-col items-center mb-6">
                            <div class="w-32 h-32 rounded-full bg-gradient-to-r from-purple-400 to-purple-600 flex items-center justify-center text-white mb-4">
                                <div class="text-center">
                                    <div class="text-3xl font-bold" id="age-years">-</div>
                                    <div class="text-sm">years old</div>
                                </div>
                            </div>
                            <div class="text-center">
                                <p class="text-gray-600 mb-1">You were born on:</p>
                                <p class="text-xl font-bold text-purple-600" id="birth-date-display">-</p>
                            </div>
                        </div>
                        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4 mb-6">
                            <div class="age-result-item">
                                <p class="text-gray-600 text-sm">Years</p>
                                <p class="text-lg font-bold text-purple-600" id="total-years">-</p>
                            </div>
                            <div class="age-result-item">
                                <p class="text-gray-600 text-sm">Months</p>
                                <p class="text-lg font-bold text-purple-600" id="total-months">-</p>
                            </div>
                            <div class="age-result-item">
                                <p class="text-gray-600 text-sm">Weeks</p>
                                <p class="text-lg font-bold text-purple-600" id="total-weeks">-</p>
                            </div>
                            <div class="age-result-item">
                                <p class="text-gray-600 text-sm">Days</p>
                                <p class="text-lg font-bold text-purple-600" id="total-days">-</p>
                            </div>
                            <div class="age-result-item">
                                <p class="text-gray-600 text-sm">Hours</p>
                                <p class="text-lg font-bold text-purple-600" id="total-hours">-</p>
                            </div>
                            <div class="age-result-item">
                                <p class="text-gray-600 text-sm">Minutes</p>
                                <p class="text-lg font-bold text-purple-600" id="total-minutes">-</p>
                            </div>
                        </div>
                        <div class="bg-white p-4 rounded-lg shadow mb-4">
                            <h5 class="font-semibold text-lg mb-3">Age Breakdown</h5>
                            <p class="text-gray-600 mb-2" id="age-breakdown">-</p>
                        </div>
                        <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                            <div class="bg-white p-4 rounded-lg shadow">
                                <h5 class="font-semibold text-lg mb-3">Next Birthday</h5>
                                <p class="text-gray-600 mb-1">Your next birthday is in:</p>
                                <p class="text-lg font-bold text-purple-600" id="next-birthday">--</p>
                                <p class="text-sm text-gray-500" id="next-birthday-day">--</p>
                            </div>
                            <div class="bg-white p-4 rounded-lg shadow">
                                <h5 class="font-semibold text-lg mb-3">Fun Facts</h5>
                                <ul class="text-sm text-gray-600 space-y-2" id="age-fun-facts">
                                    <li id="heartbeats">Your heart has beaten approximately <span class="font-semibold">--</span> times.</li>
                                    <li id="breaths">You have taken about <span class="font-semibold">--</span> breaths.</li>
                                    <li id="sleep">You have spent around <span class="font-semibold">--</span> hours sleeping.</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Pregnancy Weight Gain Calculator -->
                <div id="weight-gain-calculator" class="calculator-tab">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">Pregnancy Weight Gain Calculator</h3>
                    <p class="text-gray-600 mb-6">Calculate recommended weight gain based on your pre-pregnancy BMI.</p>

                    <div class="bg-pink-50 p-4 rounded-lg mb-6">
                        <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-pink-500 mr-2"></i> Recommended weight gain varies based on your pre-pregnancy BMI.</p>
                    </div>

                    <form id="weight-gain-form" class="mb-6">
                        <div class="mb-4">
                            <label for="pre-pregnancy-weight" class="block text-gray-700 font-medium mb-2">Pre-pregnancy Weight (kg)</label>
                            <input type="number" id="pre-pregnancy-weight" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="height" class="block text-gray-700 font-medium mb-2">Height (cm)</label>
                            <input type="number" id="height" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <button type="button" id="calculate-weight-gain" class="w-full bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-4 rounded-md transition duration-300 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                            Calculate Recommended Weight Gain
                        </button>
                    </form>

                    <div id="weight-gain-result" class="hidden bg-gray-50 rounded-lg p-6 border-l-4 border-pink-500">
                        <h4 class="text-xl font-semibold text-gray-800 mb-4">Your Pregnancy Weight Gain Recommendations</h4>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-4">
                            <div>
                                <p class="text-gray-600 mb-1">Pre-pregnancy BMI:</p>
                                <p class="text-xl font-bold text-pink-600" id="bmi-result">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Weight Category:</p>
                                <p class="text-xl font-bold text-pink-600" id="weight-category">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Total Recommended Gain:</p>
                                <p class="text-xl font-bold text-pink-600" id="total-gain">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">2nd & 3rd Trimester (per week):</p>
                                <p class="text-xl font-bold text-pink-600" id="weekly-gain">-</p>
                            </div>
                        </div>
                        <div class="mt-4">
                            <p class="text-gray-600 mb-2">Weight Gain Timeline:</p>
                            <div class="bg-white p-4 rounded-lg shadow">
                                <div class="flex justify-between mb-2">
                                    <span class="text-sm font-medium">1st Trimester</span>
                                    <span class="text-sm font-medium" id="first-trimester-gain">1-1.5 kg</span>
                                </div>
                                <div class="flex justify-between mb-2">
                                    <span class="text-sm font-medium">2nd Trimester</span>
                                    <span class="text-sm font-medium" id="second-trimester-gain">~0.5 kg/week</span>
                                </div>
                                <div class="flex justify-between">
                                    <span class="text-sm font-medium">3rd Trimester</span>
                                    <span class="text-sm font-medium" id="third-trimester-gain">~0.5 kg/week</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Pregnancy Nutrition Calculator -->
                <div id="nutrition-calculator" class="calculator-tab">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">Pregnancy Nutrition Calculator</h3>
                    <p class="text-gray-600 mb-6">Calculate your daily calorie and nutrient needs during pregnancy.</p>

                    <div class="bg-pink-50 p-4 rounded-lg mb-6">
                        <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-pink-500 mr-2"></i> Nutritional needs increase during pregnancy to support your baby's growth and development.</p>
                    </div>

                    <form id="nutrition-form" class="mb-6">
                        <div class="mb-4">
                            <label for="nutrition-weight" class="block text-gray-700 font-medium mb-2">Current Weight (kg)</label>
                            <input type="number" id="nutrition-weight" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="nutrition-height" class="block text-gray-700 font-medium mb-2">Height (cm)</label>
                            <input type="number" id="nutrition-height" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="nutrition-trimester" class="block text-gray-700 font-medium mb-2">Current Trimester</label>
                            <select id="nutrition-trimester" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                                <option value="1">First Trimester</option>
                                <option value="2">Second Trimester</option>
                                <option value="3">Third Trimester</option>
                            </select>
                        </div>

                        <div class="mb-4">
                            <label for="nutrition-activity" class="block text-gray-700 font-medium mb-2">Activity Level</label>
                            <select id="nutrition-activity" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                                <option value="1.2">Sedentary (little or no exercise)</option>
                                <option value="1.375">Lightly active (light exercise 1-3 days/week)</option>
                                <option value="1.55">Moderately active (moderate exercise 3-5 days/week)</option>
                                <option value="1.725">Very active (hard exercise 6-7 days/week)</option>
                                <option value="1.9">Extra active (very hard exercise & physical job)</option>
                            </select>
                        </div>

                        <button type="button" id="calculate-nutrition" class="w-full bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-4 rounded-md transition duration-300 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                            Calculate Nutritional Needs
                        </button>
                    </form>

                    <div id="nutrition-result" class="hidden bg-gray-50 rounded-lg p-6 border-l-4 border-pink-500">
                        <h4 class="text-xl font-semibold text-gray-800 mb-4">Your Pregnancy Nutritional Needs</h4>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-6">
                            <div>
                                <p class="text-gray-600 mb-1">Daily Calorie Needs:</p>
                                <p class="text-xl font-bold text-pink-600" id="calorie-needs">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Protein Needs:</p>
                                <p class="text-xl font-bold text-pink-600" id="protein-needs">-</p>
                            </div>
                        </div>
                        <div class="mb-6">
                            <h5 class="font-semibold mb-3">Key Nutrients</h5>
                            <div class="bg-white p-4 rounded-lg shadow">
                                <div class="flex justify-between mb-2">
                                    <span class="text-sm font-medium">Folic Acid</span>
                                    <span class="text-sm font-medium" id="folic-acid">600 mcg</span>
                                </div>
                                <div class="flex justify-between mb-2">
                                    <span class="text-sm font-medium">Iron</span>
                                    <span class="text-sm font-medium" id="iron">27 mg</span>
                                </div>
                                <div class="flex justify-between mb-2">
                                    <span class="text-sm font-medium">Calcium</span>
                                    <span class="text-sm font-medium" id="calcium">1000 mg</span>
                                </div>
                                <div class="flex justify-between">
                                    <span class="text-sm font-medium">Omega-3 (DHA)</span>
                                    <span class="text-sm font-medium" id="omega3">200-300 mg</span>
                                </div>
                            </div>
                        </div>
                        <div class="bg-blue-50 p-4 rounded-lg">
                            <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-blue-500 mr-2"></i> These are general guidelines. Consult your healthcare provider for personalized recommendations.</p>
                        </div>
                    </div>
                </div>

                <!-- Pregnancy Blood Volume Calculator -->
                <div id="blood-volume-calculator" class="calculator-tab">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">Pregnancy Blood Volume Calculator</h3>
                    <p class="text-gray-600 mb-6">Estimate your blood volume increase during pregnancy and its effects.</p>

                    <div class="bg-pink-50 p-4 rounded-lg mb-6">
                        <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-pink-500 mr-2"></i> Blood volume increases significantly during pregnancy to support your growing baby.</p>
                    </div>

                    <form id="blood-volume-form" class="mb-6">
                        <div class="mb-4">
                            <label for="blood-volume-weight" class="block text-gray-700 font-medium mb-2">Pre-pregnancy Weight (kg)</label>
                            <input type="number" id="blood-volume-weight" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="blood-volume-trimester" class="block text-gray-700 font-medium mb-2">Current Trimester</label>
                            <select id="blood-volume-trimester" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                                <option value="1">First Trimester</option>
                                <option value="2">Second Trimester</option>
                                <option value="3">Third Trimester</option>
                            </select>
                        </div>

                        <div class="mb-4">
                            <label for="blood-volume-hemoglobin" class="block text-gray-700 font-medium mb-2">Pre-pregnancy Hemoglobin (g/dL)</label>
                            <input type="number" id="blood-volume-hemoglobin" value="14" min="10" max="18" step="0.1" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <button type="button" id="calculate-blood-volume" class="w-full bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-4 rounded-md transition duration-300 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                            Calculate Blood Volume Changes
                        </button>
                    </form>

                    <div id="blood-volume-result" class="hidden bg-gray-50 rounded-lg p-6 border-l-4 border-pink-500">
                        <h4 class="text-xl font-semibold text-gray-800 mb-4">Your Blood Volume Changes</h4>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-6">
                            <div>
                                <p class="text-gray-600 mb-1">Blood Volume Increase:</p>
                                <p class="text-xl font-bold text-pink-600" id="blood-volume-increase">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Estimated Hemoglobin:</p>
                                <p class="text-xl font-bold text-pink-600" id="current-hemoglobin">-</p>
                            </div>
                        </div>
                        <div class="mb-6">
                            <h5 class="font-semibold mb-3">Effects of Increased Blood Volume</h5>
                            <ul class="list-disc pl-6 space-y-2 text-gray-600">
                                <li>Supports placenta and growing baby</li>
                                <li>Helps compensate for blood loss during delivery</li>
                                <li>May cause mild anemia (normal in pregnancy)</li>
                                <li>Can lead to lower blood pressure</li>
                            </ul>
                        </div>
                        <div class="bg-blue-50 p-4 rounded-lg">
                            <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-blue-500 mr-2"></i> Consult your healthcare provider if you experience severe fatigue, dizziness, or other concerning symptoms.</p>
                        </div>
                    </div>
                </div>

                <!-- Labor Probability Calculator -->
                <div id="labor-probability-calculator" class="calculator-tab">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">Labor Probability Calculator</h3>
                    <p class="text-gray-600 mb-6">Estimate the probability of labor by day based on your due date.</p>

                    <div class="bg-pink-50 p-4 rounded-lg mb-6">
                        <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-pink-500 mr-2"></i> Only about 5% of babies are born on their exact due date. Most arrive within two weeks before or after.</p>
                    </div>

                    <form id="labor-probability-form" class="mb-6">
                        <div class="mb-4">
                            <label for="due-date" class="block text-gray-700 font-medium mb-2">Due Date</label>
                            <input type="date" id="due-date" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <button type="button" id="calculate-labor-probability" class="w-full bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-4 rounded-md transition duration-300 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                            Calculate Labor Probability
                        </button>
                    </form>

                    <div id="labor-probability-result" class="hidden bg-gray-50 rounded-lg p-6 border-l-4 border-pink-500">
                        <h4 class="text-xl font-semibold text-gray-800 mb-4">Labor Probability Timeline</h4>
                        <div class="mb-6">
                            <div class="w-full bg-gray-200 rounded-full h-4 mb-2">
                                <div class="bg-pink-500 h-4 rounded-full" id="labor-probability-bar" style="width: 0%"></div>
                            </div>
                            <p class="text-sm text-gray-500 text-right" id="current-probability">0% chance today</p>
                        </div>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-6">
                            <div>
                                <p class="text-gray-600 mb-1">Most Likely Delivery Window:</p>
                                <p class="text-xl font-bold text-pink-600" id="delivery-window">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Probability of Early Delivery:</p>
                                <p class="text-xl font-bold text-pink-600" id="early-delivery">-</p>
                            </div>
                        </div>
                        <div class="bg-white p-4 rounded-lg shadow">
                            <h5 class="font-semibold mb-3">Signs of Labor</h5>
                            <ul class="list-disc pl-6 space-y-2 text-gray-600">
                                <li>Regular contractions that increase in frequency and intensity</li>
                                <li>Rupture of membranes (water breaking)</li>
                                <li>Bloody show (mucus plug discharge)</li>
                                <li>Lower back pain and cramping</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <!-- Breastfeeding Calculator -->
                <div id="breastfeeding-calculator" class="calculator-tab">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">Breastfeeding Calculator</h3>
                    <p class="text-gray-600 mb-6">Calculate additional calorie needs while breastfeeding and track feeding patterns.</p>

                    <div class="bg-pink-50 p-4 rounded-lg mb-6">
                        <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-pink-500 mr-2"></i> Breastfeeding requires additional calories and nutrients to support milk production.</p>
                    </div>

                    <form id="breastfeeding-form" class="mb-6">
                        <div class="mb-4">
                            <label for="breastfeeding-weight" class="block text-gray-700 font-medium mb-2">Current Weight (kg)</label>
                            <input type="number" id="breastfeeding-weight" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="breastfeeding-activity" class="block text-gray-700 font-medium mb-2">Activity Level</label>
                            <select id="breastfeeding-activity" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                                <option value="1.2">Sedentary (little or no exercise)</option>
                                <option value="1.375">Lightly active (light exercise 1-3 days/week)</option>
                                <option value="1.55">Moderately active (moderate exercise 3-5 days/week)</option>
                                <option value="1.725">Very active (hard exercise 6-7 days/week)</option>
                            </select>
                        </div>

                        <div class="mb-4">
                            <label for="breastfeeding-months" class="block text-gray-700 font-medium mb-2">Months Postpartum</label>
                            <input type="number" id="breastfeeding-months" min="0" max="12" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="breastfeeding-exclusive" class="block text-gray-700 font-medium mb-2">Feeding Method</label>
                            <select id="breastfeeding-exclusive" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                                <option value="1">Exclusive breastfeeding</option>
                                <option value="0.5">Partial breastfeeding</option>
                            </select>
                        </div>

                        <button type="button" id="calculate-breastfeeding" class="w-full bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-4 rounded-md transition duration-300 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                            Calculate Needs
                        </button>
                    </form>

                    <div id="breastfeeding-result" class="hidden bg-gray-50 rounded-lg p-6 border-l-4 border-pink-500">
                        <h4 class="text-xl font-semibold text-gray-800 mb-4">Your Breastfeeding Needs</h4>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-6">
                            <div>
                                <p class="text-gray-600 mb-1">Daily Calorie Needs:</p>
                                <p class="text-xl font-bold text-pink-600" id="breastfeeding-calories">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Additional Calories Needed:</p>
                                <p class="text-xl font-bold text-pink-600" id="additional-calories">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Recommended Water Intake:</p>
                                <p class="text-xl font-bold text-pink-600" id="water-intake">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Protein Needs:</p>
                                <p class="text-xl font-bold text-pink-600" id="breastfeeding-protein">-</p>
                            </div>
                        </div>
                        <div class="bg-white p-4 rounded-lg shadow mb-4">
                            <h5 class="font-semibold mb-3">Feeding Schedule</h5>
                            <p class="text-gray-600">Newborns typically feed 8-12 times per day (every 2-3 hours). As your baby grows, feedings will become less frequent but more substantial.</p>
                        </div>
                        <div class="bg-blue-50 p-4 rounded-lg">
                            <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-blue-500 mr-2"></i> These are general guidelines. Your baby's needs may vary - follow their hunger cues.</p>
                        </div>
                    </div>
                </div>

                <!-- Fertility Age Calculator -->
                <div id="fertility-age-calculator" class="calculator-tab">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">Fertility Age Calculator</h3>
                    <p class="text-gray-600 mb-6">Estimate your remaining fertile years based on your current age.</p>

                    <div class="bg-pink-50 p-4 rounded-lg mb-6">
                        <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-pink-500 mr-2"></i> Female fertility declines with age, with the most significant drop occurring after age 35.</p>
                    </div>

                    <form id="fertility-age-form" class="mb-6">
                        <div class="mb-4">
                            <label for="current-age" class="block text-gray-700 font-medium mb-2">Current Age</label>
                            <input type="number" id="current-age" min="18" max="50" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="fertility-history" class="block text-gray-700 font-medium mb-2">Reproductive History</label>
                            <select id="fertility-history" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                                <option value="average">No known fertility issues</option>
                                <option value="good">No issues and family history of late fertility</option>
                                <option value="poor">Known fertility issues or family history of early menopause</option>
                            </select>
                        </div>

                        <button type="button" id="calculate-fertility-age" class="w-full bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-4 rounded-md transition duration-300 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                            Calculate Fertility Outlook
                        </button>
                    </form>

                    <div id="fertility-age-result" class="hidden bg-gray-50 rounded-lg p-6 border-l-4 border-pink-500">
                        <h4 class="text-xl font-semibold text-gray-800 mb-4">Your Fertility Outlook</h4>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-6">
                            <div>
                                <p class="text-gray-600 mb-1">Estimated Remaining Fertile Years:</p>
                                <p class="text-xl font-bold text-pink-600" id="fertile-years">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Peak Fertility Age:</p>
                                <p class="text-xl font-bold text-pink-600">20-24</p>
                            </div>
                        </div>
                        <div class="mb-6">
                            <h5 class="font-semibold mb-3">Age-Related Fertility Decline</h5>
                            <div class="w-full bg-gray-200 rounded-full h-2.5 mb-2">
                                <div class="bg-pink-500 h-2.5 rounded-full" id="fertility-decline-bar" style="width: 0%"></div>
                            </div>
                            <div class="flex justify-between text-xs text-gray-500">
                                <span>20</span>
                                <span>25</span>
                                <span>30</span>
                                <span>35</span>
                                <span>40</span>
                                <span>45</span>
                            </div>
                        </div>
                        <div class="bg-white p-4 rounded-lg shadow mb-4">
                            <h5 class="font-semibold mb-3">Recommendations</h5>
                            <ul class="list-disc pl-6 space-y-2 text-gray-600">
                                <li id="fertility-recommendation-1">Consider fertility testing if planning pregnancy after 35</li>
                                <li id="fertility-recommendation-2">Egg freezing may be an option if delaying pregnancy</li>
                                <li id="fertility-recommendation-3">Maintain healthy lifestyle to support fertility</li>
                            </ul>
                        </div>
                        <div class="bg-blue-50 p-4 rounded-lg">
                            <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-blue-500 mr-2"></i> These are statistical averages. Individual fertility varies widely.</p>
                        </div>
                    </div>
                </div>

                <!-- Conception Probability Calculator -->
                <div id="conception-probability-calculator" class="calculator-tab">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">Conception Probability Calculator</h3>
                    <p class="text-gray-600 mb-6">Estimate your chances of conception based on cycle day and age.</p>

                    <div class="bg-pink-50 p-4 rounded-lg mb-6">
                        <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-pink-500 mr-2"></i> The probability of conception varies throughout your cycle and decreases with age.</p>
                    </div>

                    <form id="conception-probability-form" class="mb-6">
                        <div class="mb-4">
                            <label for="conception-age" class="block text-gray-700 font-medium mb-2">Age</label>
                            <input type="number" id="conception-age" min="18" max="45" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="cycle-day" class="block text-gray-700 font-medium mb-2">Cycle Day</label>
                            <input type="number" id="cycle-day" min="1" max="35" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="cycle-length" class="block text-gray-700 font-medium mb-2">Average Cycle Length</label>
                            <input type="number" id="cycle-length" value="28" min="21" max="45" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <button type="button" id="calculate-conception-probability" class="w-full bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-4 rounded-md transition duration-300 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                            Calculate Conception Probability
                        </button>
                    </form>

                    <div id="conception-probability-result" class="hidden bg-gray-50 rounded-lg p-6 border-l-4 border-pink-500">
                        <h4 class="text-xl font-semibold text-gray-800 mb-4">Conception Probability</h4>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-6">
                            <div>
                                <p class="text-gray-600 mb-1">Probability This Cycle:</p>
                                <p class="text-xl font-bold text-pink-600" id="cycle-probability">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Probability Within 1 Year:</p>
                                <p class="text-xl font-bold text-pink-600" id="year-probability">-</p>
                            </div>
                        </div>
                        <div class="mb-6">
                            <h5 class="font-semibold mb-3">Probability by Cycle Day</h5>
                            <div class="w-full bg-gray-200 rounded-full h-2.5 mb-2">
                                <div class="bg-pink-500 h-2.5 rounded-full" id="conception-probability-bar" style="width: 0%"></div>
                            </div>
                            <div class="flex justify-between text-xs text-gray-500">
                                <span>Day 1</span>
                                <span>Day 7</span>
                                <span>Day 14</span>
                                <span>Day 21</span>
                                <span>Day 28</span>
                            </div>
                        </div>
                        <div class="bg-white p-4 rounded-lg shadow mb-4">
                            <h5 class="font-semibold mb-3">Tips to Improve Chances</h5>
                            <ul class="list-disc pl-6 space-y-2 text-gray-600">
                                <li>Have intercourse every 1-2 days during fertile window</li>
                                <li>Maintain healthy weight and lifestyle</li>
                                <li>Track ovulation for optimal timing</li>
                                <li>Consider preconception health checkup</li>
                            </ul>
                        </div>
                        <div class="bg-blue-50 p-4 rounded-lg">
                            <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-blue-500 mr-2"></i> Consult a fertility specialist if not pregnant after 1 year (or 6 months if over 35).</p>
                        </div>
                    </div>
                </div>

                <!-- IVF Success Calculator -->
                <div id="ivf-success-calculator" class="calculator-tab">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">IVF Success Calculator</h3>
                    <p class="text-gray-600 mb-6">Estimate IVF success rates based on age and other factors.</p>

                    <div class="bg-pink-50 p-4 rounded-lg mb-6">
                        <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-pink-500 mr-2"></i> IVF success rates vary significantly by age and individual fertility factors.</p>
                    </div>

                    <form id="ivf-success-form" class="mb-6">
                        <div class="mb-4">
                            <label for="ivf-age" class="block text-gray-700 font-medium mb-2">Age</label>
                            <input type="number" id="ivf-age" min="18" max="50" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="ivf-cycles" class="block text-gray-700 font-medium mb-2">Number of Previous IVF Cycles</label>
                            <input type="number" id="ivf-cycles" min="0" max="10" value="0" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="ivf-cause" class="block text-gray-700 font-medium mb-2">Primary Cause of Infertility</label>
                            <select id="ivf-cause" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                                <option value="tubal">Tubal factor</option>
                                <option value="male">Male factor</option>
                                <option value="ovulation">Ovulation disorders</option>
                                <option value="endometriosis">Endometriosis</option>
                                <option value="unexplained">Unexplained</option>
                                <option value="other">Other</option>
                            </select>
                        </div>

                        <button type="button" id="calculate-ivf-success" class="w-full bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-4 rounded-md transition duration-300 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                            Calculate Success Rates
                        </button>
                    </form>

                    <div id="ivf-success-result" class="hidden bg-gray-50 rounded-lg p-6 border-l-4 border-pink-500">
                        <h4 class="text-xl font-semibold text-gray-800 mb-4">IVF Success Estimates</h4>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-6">
                            <div>
                                <p class="text-gray-600 mb-1">Success Rate Per Cycle:</p>
                                <p class="text-xl font-bold text-pink-600" id="ivf-cycle-success">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Cumulative Success (3 cycles):</p>
                                <p class="text-xl font-bold text-pink-600" id="ivf-cumulative-success">-</p>
                            </div>
                        </div>
                        <div class="mb-6">
                            <h5 class="font-semibold mb-3">Success Rates by Age</h5>
                            <div class="w-full bg-gray-200 rounded-full h-2.5 mb-2">
                                <div class="bg-pink-500 h-2.5 rounded-full" id="ivf-age-bar" style="width: 0%"></div>
                            </div>
                            <div class="flex justify-between text-xs text-gray-500">
                                <span>Under 35</span>
                                <span>35-37</span>
                                <span>38-40</span>
                                <span>41-42</span>
                                <span>Over 42</span>
                            </div>
                        </div>
                        <div class="bg-white p-4 rounded-lg shadow mb-4">
                            <h5 class="font-semibold mb-3">Factors Affecting Success</h5>
                            <ul class="list-disc pl-6 space-y-2 text-gray-600">
                                <li>Egg quality and quantity (ovarian reserve)</li>
                                <li>Sperm quality</li>
                                <li>Uterine receptivity</li>
                                <li>Embryo quality</li>
                                <li>Clinic expertise and protocols</li>
                            </ul>
                        </div>
                        <div class="bg-blue-50 p-4 rounded-lg">
                            <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-blue-500 mr-2"></i> These are statistical averages. Consult with a fertility specialist for personalized assessment.</p>
                        </div>
                    </div>
                </div>

                <!-- Baby Growth Percentile Calculator -->
                <div id="baby-growth-calculator" class="calculator-tab">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">Baby Growth Percentile Calculator</h3>
                    <p class="text-gray-600 mb-6">Track your baby's growth percentile based on measurements.</p>

                    <div class="bg-pink-50 p-4 rounded-lg mb-6">
                        <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-pink-500 mr-2"></i> Percentiles compare your baby's growth to others of the same age and sex.</p>
                    </div>

                    <form id="baby-growth-form" class="mb-6">
                        <div class="mb-4">
                            <label class="block text-gray-700 font-medium mb-2">Baby's Sex</label>
                            <div class="flex">
                                <label class="inline-flex items-center mr-6">
                                    <input type="radio" name="baby-sex" value="male" checked class="form-radio text-pink-500 focus:ring-pink-500 h-4 w-4">
                                    <span class="ml-2">Male</span>
                                </label>
                                <label class="inline-flex items-center">
                                    <input type="radio" name="baby-sex" value="female" class="form-radio text-pink-500 focus:ring-pink-500 h-4 w-4">
                                    <span class="ml-2">Female</span>
                                </label>
                            </div>
                        </div>

                        <div class="mb-4">
                            <label for="baby-age" class="block text-gray-700 font-medium mb-2">Age (months)</label>
                            <input type="number" id="baby-age" min="0" max="36" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="baby-weight" class="block text-gray-700 font-medium mb-2">Weight (kg)</label>
                            <input type="number" id="baby-weight" step="0.1" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="baby-length" class="block text-gray-700 font-medium mb-2">Length/Height (cm)</label>
                            <input type="number" id="baby-length" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="baby-head" class="block text-gray-700 font-medium mb-2">Head Circumference (cm)</label>
                            <input type="number" id="baby-head" step="0.1" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <button type="button" id="calculate-baby-growth" class="w-full bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-4 rounded-md transition duration-300 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                            Calculate Percentiles
                        </button>
                    </form>

                    <div id="baby-growth-result" class="hidden bg-gray-50 rounded-lg p-6 border-l-4 border-pink-500">
                        <h4 class="text-xl font-semibold text-gray-800 mb-4">Growth Percentiles</h4>
                        <div class="grid grid-cols-1 md:grid-cols-3 gap-4 mb-6">
                            <div>
                                <p class="text-gray-600 mb-1">Weight Percentile:</p>
                                <p class="text-xl font-bold text-pink-600" id="weight-percentile">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Length Percentile:</p>
                                <p class="text-xl font-bold text-pink-600" id="length-percentile">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Head Circumference Percentile:</p>
                                <p class="text-xl font-bold text-pink-600" id="head-percentile">-</p>
                            </div>
                        </div>
                        <div class="mb-6">
                            <h5 class="font-semibold mb-3">Growth Chart</h5>
                            <div class="bg-white p-4 rounded-lg shadow">
                                <div class="flex justify-between mb-2">
                                    <span class="text-sm font-medium">3rd Percentile</span>
                                    <span class="text-sm font-medium">50th Percentile</span>
                                    <span class="text-sm font-medium">97th Percentile</span>
                                </div>
                                <div class="relative h-32 bg-gray-100 rounded">
                                    <div class="absolute bottom-0 left-0 right-0 flex justify-around">
                                        <div class="w-8 h-8 rounded-full bg-pink-500 transform -translate-y-1/2" id="weight-marker" style="bottom: 50%"></div>
                                        <div class="w-8 h-8 rounded-full bg-blue-500 transform -translate-y-1/2" id="length-marker" style="bottom: 50%"></div>
                                        <div class="w-8 h-8 rounded-full bg-green-500 transform -translate-y-1/2" id="head-marker" style="bottom: 50%"></div>
                                    </div>
                                </div>
                                <div class="flex justify-between mt-2">
                                    <span class="text-xs text-gray-500">Small</span>
                                    <span class="text-xs text-gray-500">Average</span>
                                    <span class="text-xs text-gray-500">Large</span>
                                </div>
                            </div>
                        </div>
                        <div class="bg-blue-50 p-4 rounded-lg">
                            <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-blue-500 mr-2"></i> Percentiles show how your baby compares to others. Healthy babies come in all sizes.</p>
                        </div>
                    </div>
                </div>

                <!-- Baby Feeding Calculator -->
                <div id="baby-feeding-calculator" class="calculator-tab">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">Baby Feeding Calculator</h3>
                    <p class="text-gray-600 mb-6">Calculate formula/breastmilk amounts by age and weight.</p>

                    <div class="bg-pink-50 p-4 rounded-lg mb-6">
                        <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-pink-500 mr-2"></i> Feeding needs vary by age, weight, and whether breastfed or formula-fed.</p>
                    </div>

                    <form id="baby-feeding-form" class="mb-6">
                        <div class="mb-4">
                            <label class="block text-gray-700 font-medium mb-2">Feeding Method</label>
                            <div class="flex">
                                <label class="inline-flex items-center mr-6">
                                    <input type="radio" name="feeding-method" value="breast" checked class="form-radio text-pink-500 focus:ring-pink-500 h-4 w-4">
                                    <span class="ml-2">Breastfed</span>
                                </label>
                                <label class="inline-flex items-center">
                                    <input type="radio" name="feeding-method" value="formula" class="form-radio text-pink-500 focus:ring-pink-500 h-4 w-4">
                                    <span class="ml-2">Formula-fed</span>
                                </label>
                            </div>
                        </div>

                        <div class="mb-4">
                            <label for="baby-age-feeding" class="block text-gray-700 font-medium mb-2">Age (months)</label>
                            <input type="number" id="baby-age-feeding" min="0" max="12" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="baby-weight-feeding" class="block text-gray-700 font-medium mb-2">Weight (kg)</label>
                            <input type="number" id="baby-weight-feeding" step="0.1" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <button type="button" id="calculate-baby-feeding" class="w-full bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-4 rounded-md transition duration-300 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                            Calculate Feeding Needs
                        </button>
                    </form>

                    <div id="baby-feeding-result" class="hidden bg-gray-50 rounded-lg p-6 border-l-4 border-pink-500">
                        <h4 class="text-xl font-semibold text-gray-800 mb-4">Feeding Recommendations</h4>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-6">
                            <div>
                                <p class="text-gray-600 mb-1">Daily Milk Intake:</p>
                                <p class="text-xl font-bold text-pink-600" id="daily-milk">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Feedings Per Day:</p>
                                <p class="text-xl font-bold text-pink-600" id="feedings-per-day">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Amount Per Feeding:</p>
                                <p class="text-xl font-bold text-pink-600" id="amount-per-feeding">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Time Between Feedings:</p>
                                <p class="text-xl font-bold text-pink-600" id="time-between-feedings">-</p>
                            </div>
                        </div>
                        <div class="mb-6">
                            <h5 class="font-semibold mb-3">Sample Feeding Schedule</h5>
                            <div id="feeding-schedule" class="bg-white p-4 rounded-lg shadow">
                                <!-- Schedule will be generated here -->
                            </div>
                        </div>
                        <div class="bg-blue-50 p-4 rounded-lg">
                            <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-blue-500 mr-2"></i> Follow your baby's hunger cues. These are general guidelines - individual needs may vary.</p>
                        </div>
                    </div>
                </div>

                <!-- Baby Sleep Calculator -->
                <div id="baby-sleep-calculator" class="calculator-tab">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">Baby Sleep Calculator</h3>
                    <p class="text-gray-600 mb-6">Calculate recommended sleep needs by age and track sleep patterns.</p>

                    <div class="bg-pink-50 p-4 rounded-lg mb-6">
                        <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-pink-500 mr-2"></i> Sleep needs change rapidly during the first year of life.</p>
                    </div>

                    <form id="baby-sleep-form" class="mb-6">
                        <div class="mb-4">
                            <label for="baby-age-sleep" class="block text-gray-700 font-medium mb-2">Age (months)</label>
                            <input type="number" id="baby-age-sleep" min="0" max="36" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <button type="button" id="calculate-baby-sleep" class="w-full bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-4 rounded-md transition duration-300 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                            Calculate Sleep Needs
                        </button>
                    </form>

                    <div id="baby-sleep-result" class="hidden bg-gray-50 rounded-lg p-6 border-l-4 border-pink-500">
                        <h4 class="text-xl font-semibold text-gray-800 mb-4">Sleep Recommendations</h4>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-6">
                            <div>
                                <p class="text-gray-600 mb-1">Total Sleep Needed:</p>
                                <p class="text-xl font-bold text-pink-600" id="total-sleep">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Nighttime Sleep:</p>
                                <p class="text-xl font-bold text-pink-600" id="night-sleep">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Daytime Naps:</p>
                                <p class="text-xl font-bold text-pink-600" id="day-naps">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Awake Windows:</p>
                                <p class="text-xl font-bold text-pink-600" id="awake-windows">-</p>
                            </div>
                        </div>
                        <div class="mb-6">
                            <h5 class="font-semibold mb-3">Sample Sleep Schedule</h5>
                            <div id="sleep-schedule" class="bg-white p-4 rounded-lg shadow">
                                <!-- Schedule will be generated here -->
                            </div>
                        </div>
                        <div class="bg-blue-50 p-4 rounded-lg">
                            <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-blue-500 mr-2"></i> Every baby is different. These are averages - follow your baby's sleep cues.</p>
                        </div>
                    </div>
                </div>

                <!-- Child Height Predictor -->
                <div id="height-predictor" class="calculator-tab">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">Child Height Predictor</h3>
                    <p class="text-gray-600 mb-6">Estimate your child's adult height based on parents' heights.</p>

                    <div class="bg-pink-50 p-4 rounded-lg mb-6">
                        <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-pink-500 mr-2"></i> Height is influenced by genetics (60-80%) and environmental factors (20-40%).</p>
                    </div>

                    <form id="height-predictor-form" class="mb-6">
                        <div class="mb-4">
                            <label class="block text-gray-700 font-medium mb-2">Child's Sex</label>
                            <div class="flex">
                                <label class="inline-flex items-center mr-6">
                                    <input type="radio" name="child-sex" value="male" checked class="form-radio text-pink-500 focus:ring-pink-500 h-4 w-4">
                                    <span class="ml-2">Male</span>
                                </label>
                                <label class="inline-flex items-center">
                                    <input type="radio" name="child-sex" value="female" class="form-radio text-pink-500 focus:ring-pink-500 h-4 w-4">
                                    <span class="ml-2">Female</span>
                                </label>
                            </div>
                        </div>

                        <div class="mb-4">
                            <label for="mother-height" class="block text-gray-700 font-medium mb-2">Mother's Height (cm)</label>
                            <input type="number" id="mother-height" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="father-height" class="block text-gray-700 font-medium mb-2">Father's Height (cm)</label>
                            <input type="number" id="father-height" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="child-current-age" class="block text-gray-700 font-medium mb-2">Child's Current Age (years, optional)</label>
                            <input type="number" id="child-current-age" min="0" max="18" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="child-current-height" class="block text-gray-700 font-medium mb-2">Child's Current Height (cm, optional)</label>
                            <input type="number" id="child-current-height" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <button type="button" id="calculate-height-prediction" class="w-full bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-4 rounded-md transition duration-300 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                            Predict Adult Height
                        </button>
                    </form>

                    <div id="height-prediction-result" class="hidden bg-gray-50 rounded-lg p-6 border-l-4 border-pink-500">
                        <h4 class="text-xl font-semibold text-gray-800 mb-4">Height Prediction</h4>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-6">
                            <div>
                                <p class="text-gray-600 mb-1">Predicted Adult Height:</p>
                                <p class="text-xl font-bold text-pink-600" id="predicted-height">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Height Percentile:</p>
                                <p class="text-xl font-bold text-pink-600" id="height-percentile">-</p>
                            </div>
                        </div>
                        <div class="mb-6">
                            <h5 class="font-semibold mb-3">Growth Potential</h5>
                            <div class="w-full bg-gray-200 rounded-full h-2.5 mb-2">
                                <div class="bg-pink-500 h-2.5 rounded-full" id="growth-potential-bar" style="width: 0%"></div>
                            </div>
                            <div class="flex justify-between text-xs text-gray-500">
                                <span>Short</span>
                                <span>Average</span>
                                <span>Tall</span>
                            </div>
                        </div>
                        <div class="bg-white p-4 rounded-lg shadow mb-4">
                            <h5 class="font-semibold mb-3">Factors Affecting Height</h5>
                            <ul class="list-disc pl-6 space-y-2 text-gray-600">
                                <li>Genetics (parents' heights)</li>
                                <li>Nutrition during childhood</li>
                                <li>Hormonal factors</li>
                                <li>Chronic illness</li>
                                <li>Physical activity</li>
                            </ul>
                        </div>
                        <div class="bg-blue-50 p-4 rounded-lg">
                            <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-blue-500 mr-2"></i> This is an estimate. Actual adult height may vary by ±10 cm.</p>
                        </div>
                    </div>
                </div>

                <!-- Body Fat Percentage Calculator -->
                <div id="body-fat-calculator" class="calculator-tab">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">Body Fat Percentage Calculator</h3>
                    <p class="text-gray-600 mb-6">Estimate your body fat percentage using skinfold or measurement methods.</p>

                    <div class="bg-pink-50 p-4 rounded-lg mb-6">
                        <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-pink-500 mr-2"></i> Body fat percentage is a better indicator of health than BMI alone.</p>
                    </div>

                    <form id="body-fat-form" class="mb-6">
                        <div class="mb-4">
                            <label class="block text-gray-700 font-medium mb-2">Gender</label>
                            <div class="flex">
                                <label class="inline-flex items-center mr-6">
                                    <input type="radio" name="body-fat-gender" value="male" checked class="form-radio text-pink-500 focus:ring-pink-500 h-4 w-4">
                                    <span class="ml-2">Male</span>
                                </label>
                                <label class="inline-flex items-center">
                                    <input type="radio" name="body-fat-gender" value="female" class="form-radio text-pink-500 focus:ring-pink-500 h-4 w-4">
                                    <span class="ml-2">Female</span>
                                </label>
                            </div>
                        </div>

                        <div class="mb-4">
                            <label for="body-fat-age" class="block text-gray-700 font-medium mb-2">Age</label>
                            <input type="number" id="body-fat-age" min="18" max="80" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="body-fat-method" class="block text-gray-700 font-medium mb-2">Calculation Method</label>
                            <select id="body-fat-method" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                                <option value="navy">Navy Tape Measure Method</option>
                                <option value="skinfold">Skinfold Caliper Method</option>
                            </select>
                        </div>

                        <div id="navy-method-inputs">
                            <div class="mb-4">
                                <label for="neck" class="block text-gray-700 font-medium mb-2">Neck Circumference (cm)</label>
                                <input type="number" id="neck" step="0.1" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                            </div>
                            <div class="mb-4">
                                <label for="waist" class="block text-gray-700 font-medium mb-2">Waist Circumference (cm)</label>
                                <input type="number" id="waist" step="0.1" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                            </div>
                            <div id="female-navy-inputs" class="hidden">
                                <div class="mb-4">
                                    <label for="hip" class="block text-gray-700 font-medium mb-2">Hip Circumference (cm)</label>
                                    <input type="number" id="hip" step="0.1" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                                </div>
                            </div>
                        </div>

                        <div id="skinfold-method-inputs" class="hidden">
                            <div class="mb-4">
                                <label for="chest-skinfold" class="block text-gray-700 font-medium mb-2">Chest Skinfold (mm)</label>
                                <input type="number" id="chest-skinfold" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                            </div>
                            <div class="mb-4">
                                <label for="abdominal-skinfold" class="block text-gray-700 font-medium mb-2">Abdominal Skinfold (mm)</label>
                                <input type="number" id="abdominal-skinfold" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                            </div>
                            <div class="mb-4">
                                <label for="thigh-skinfold" class="block text-gray-700 font-medium mb-2">Thigh Skinfold (mm)</label>
                                <input type="number" id="thigh-skinfold" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                            </div>
                            <div id="female-skinfold-inputs" class="hidden">
                                <div class="mb-4">
                                    <label for="tricep-skinfold" class="block text-gray-700 font-medium mb-2">Tricep Skinfold (mm)</label>
                                    <input type="number" id="tricep-skinfold" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                                </div>
                                <div class="mb-4">
                                    <label for="suprailiac-skinfold" class="block text-gray-700 font-medium mb-2">Suprailiac Skinfold (mm)</label>
                                    <input type="number" id="suprailiac-skinfold" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                                </div>
                            </div>
                        </div>

                        <button type="button" id="calculate-body-fat" class="w-full bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-4 rounded-md transition duration-300 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                            Calculate Body Fat Percentage
                        </button>
                    </form>

                    <div id="body-fat-result" class="hidden bg-gray-50 rounded-lg p-6 border-l-4 border-pink-500">
                        <h4 class="text-xl font-semibold text-gray-800 mb-4">Body Fat Results</h4>
                        <div class="flex flex-col md:flex-row items-center mb-6">
                            <div class="w-32 h-32 rounded-full bg-gradient-to-r from-blue-400 to-blue-600 flex items-center justify-center text-white mb-4 md:mb-0 md:mr-6">
                                <div class="text-center">
                                    <div class="text-3xl font-bold" id="body-fat-percentage">-</div>
                                    <div class="text-sm">% body fat</div>
                                </div>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Category:</p>
                                <p class="text-xl font-bold" id="body-fat-category">-</p>
                                <p class="text-gray-600 text-sm mt-2" id="body-fat-message">-</p>
                            </div>
                        </div>
                        <div class="mb-6">
                            <div class="relative pt-4">
                                <div class="flex mb-2">
                                    <div class="flex-1 text-center text-xs">
                                        <span class="bg-blue-500 block h-2 rounded-l-full"></span>
                                        Essential
                                    </div>
                                    <div class="flex-1 text-center text-xs">
                                        <span class="bg-green-500 block h-2"></span>
                                        Athletic
                                    </div>
                                    <div class="flex-1 text-center text-xs">
                                        <span class="bg-yellow-500 block h-2"></span>
                                        Fitness
                                    </div>
                                    <div class="flex-1 text-center text-xs">
                                        <span class="bg-orange-500 block h-2"></span>
                                        Average
                                    </div>
                                    <div class="flex-1 text-center text-xs">
                                        <span class="bg-red-500 block h-2 rounded-r-full"></span>
                                        Obese
                                    </div>
                                </div>
                                <div class="w-4 h-4 absolute top-0 transform -translate-x-1/2 -translate-y-1/2 bg-white border-2 border-gray-800 rounded-full" id="body-fat-indicator" style="left: 0%"></div>
                            </div>
                            <div class="flex justify-between text-xs text-gray-500 mt-1">
                                <span>3-5%</span>
                                <span>6-13%</span>
                                <span>14-17%</span>
                                <span>18-24%</span>
                                <span>25%+</span>
                            </div>
                        </div>
                        <div class="bg-blue-50 p-4 rounded-lg">
                            <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-blue-500 mr-2"></i> For women, add 8-10% to these ranges. Body fat percentages are estimates.</p>
                        </div>
                    </div>
                </div>

                <!-- Calorie Needs Calculator -->
                <div id="calorie-needs-calculator" class="calculator-tab">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">Calorie Needs Calculator</h3>
                    <p class="text-gray-600 mb-6">Calculate your daily calorie requirements based on activity level and goals.</p>

                    <div class="bg-pink-50 p-4 rounded-lg mb-6">
                        <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-pink-500 mr-2"></i> Calorie needs vary based on age, gender, weight, height, and activity level.</p>
                    </div>

                    <form id="calorie-needs-form" class="mb-6">
                        <div class="mb-4">
                            <label class="block text-gray-700 font-medium mb-2">Gender</label>
                            <div class="flex">
                                <label class="inline-flex items-center mr-6">
                                    <input type="radio" name="calorie-gender" value="male" checked class="form-radio text-pink-500 focus:ring-pink-500 h-4 w-4">
                                    <span class="ml-2">Male</span>
                                </label>
                                <label class="inline-flex items-center">
                                    <input type="radio" name="calorie-gender" value="female" class="form-radio text-pink-500 focus:ring-pink-500 h-4 w-4">
                                    <span class="ml-2">Female</span>
                                </label>
                            </div>
                        </div>

                        <div class="mb-4">
                            <label for="calorie-age" class="block text-gray-700 font-medium mb-2">Age</label>
                            <input type="number" id="calorie-age" min="18" max="80" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="calorie-weight" class="block text-gray-700 font-medium mb-2">Weight (kg)</label>
                            <input type="number" id="calorie-weight" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="calorie-height" class="block text-gray-700 font-medium mb-2">Height (cm)</label>
                            <input type="number" id="calorie-height" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="calorie-activity" class="block text-gray-700 font-medium mb-2">Activity Level</label>
                            <select id="calorie-activity" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                                <option value="1.2">Sedentary (little or no exercise)</option>
                                <option value="1.375">Lightly active (light exercise 1-3 days/week)</option>
                                <option value="1.55">Moderately active (moderate exercise 3-5 days/week)</option>
                                <option value="1.725">Very active (hard exercise 6-7 days/week)</option>
                                <option value="1.9">Extra active (very hard exercise & physical job)</option>
                            </select>
                        </div>

                        <div class="mb-4">
                            <label for="calorie-goal" class="block text-gray-700 font-medium mb-2">Goal</label>
                            <select id="calorie-goal" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                                <option value="maintain">Maintain weight</option>
                                <option value="lose">Lose weight</option>
                                <option value="gain">Gain weight</option>
                            </select>
                        </div>

                        <button type="button" id="calculate-calorie-needs" class="w-full bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-4 rounded-md transition duration-300 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                            Calculate Calorie Needs
                        </button>
                    </form>

                    <div id="calorie-needs-result" class="hidden bg-gray-50 rounded-lg p-6 border-l-4 border-pink-500">
                        <h4 class="text-xl font-semibold text-gray-800 mb-4">Your Calorie Needs</h4>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-6">
                            <div>
                                <p class="text-gray-600 mb-1">Basal Metabolic Rate (BMR):</p>
                                <p class="text-xl font-bold text-pink-600" id="bmr">-</p>
                                <p class="text-sm text-gray-500">Calories burned at complete rest</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Total Daily Energy Expenditure (TDEE):</p>
                                <p class="text-xl font-bold text-pink-600" id="tdee">-</p>
                                <p class="text-sm text-gray-500">Calories burned with activity</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Recommended Daily Intake:</p>
                                <p class="text-xl font-bold text-pink-600" id="recommended-calories">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Macronutrient Distribution:</p>
                                <p class="text-xl font-bold text-pink-600" id="macronutrients">-</p>
                            </div>
                        </div>
                        <div class="bg-white p-4 rounded-lg shadow mb-4">
                            <h5 class="font-semibold mb-3">Weight Change Projection</h5>
                            <p class="text-gray-600" id="weight-change-projection">-</p>
                        </div>
                        <div class="bg-blue-50 p-4 rounded-lg">
                            <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-blue-500 mr-2"></i> These are estimates. Individual needs may vary by ±15%.</p>
                        </div>
                    </div>
                </div>

                <!-- Water Intake Calculator -->
                <div id="water-intake-calculator" class="calculator-tab">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">Water Intake Calculator</h3>
                    <p class="text-gray-600 mb-6">Calculate your daily water needs based on weight, activity, and climate.</p>

                    <div class="bg-pink-50 p-4 rounded-lg mb-6">
                        <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-pink-500 mr-2"></i> Proper hydration is essential for health, especially during pregnancy.</p>
                    </div>

                    <form id="water-intake-form" class="mb-6">
                        <div class="mb-4">
                            <label for="water-weight" class="block text-gray-700 font-medium mb-2">Weight (kg)</label>
                            <input type="number" id="water-weight" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="water-activity" class="block text-gray-700 font-medium mb-2">Activity Level</label>
                            <select id="water-activity" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                                <option value="1">Sedentary (little or no exercise)</option>
                                <option value="1.2">Lightly active (light exercise 1-3 days/week)</option>
                                <option value="1.4">Moderately active (moderate exercise 3-5 days/week)</option>
                                <option value="1.6">Very active (hard exercise 6-7 days/week)</option>
                            </select>
                        </div>

                        <div class="mb-4">
                            <label for="water-climate" class="block text-gray-700 font-medium mb-2">Climate</label>
                            <select id="water-climate" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                                <option value="1">Temperate</option>
                                <option value="1.2">Hot/Humid</option>
                                <option value="1.1">Dry/High Altitude</option>
                            </select>
                        </div>

                        <div class="mb-4">
                            <label for="water-pregnant" class="block text-gray-700 font-medium mb-2">Pregnancy Status</label>
                            <select id="water-pregnant" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                                <option value="0">Not pregnant</option>
                                <option value="300">Pregnant</option>
                                <option value="700">Breastfeeding</option>
                            </select>
                        </div>

                        <button type="button" id="calculate-water-intake" class="w-full bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-4 rounded-md transition duration-300 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                            Calculate Water Needs
                        </button>
                    </form>

                    <div id="water-intake-result" class="hidden bg-gray-50 rounded-lg p-6 border-l-4 border-pink-500">
                        <h4 class="text-xl font-semibold text-gray-800 mb-4">Your Hydration Needs</h4>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-6">
                            <div>
                                <p class="text-gray-600 mb-1">Daily Water Intake:</p>
                                <p class="text-xl font-bold text-pink-600" id="total-water">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Equivalent Glasses (250ml):</p>
                                <p class="text-xl font-bold text-pink-600" id="water-glasses">-</p>
                            </div>
                        </div>
                        <div class="mb-6">
                            <h5 class="font-semibold mb-3">Hydration Schedule</h5>
                            <div id="hydration-schedule" class="bg-white p-4 rounded-lg shadow">
                                <!-- Schedule will be generated here -->
                            </div>
                        </div>
                        <div class="bg-blue-50 p-4 rounded-lg">
                            <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-blue-500 mr-2"></i> Includes water from all beverages and foods. Increase intake during exercise or hot weather.</p>
                        </div>
                    </div>
                </div>

                <!-- Heart Rate Zone Calculator -->
                <div id="heart-rate-calculator" class="calculator-tab">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">Heart Rate Zone Calculator</h3>
                    <p class="text-gray-600 mb-6">Calculate your target heart rate zones for exercise intensity.</p>

                    <div class="bg-pink-50 p-4 rounded-lg mb-6">
                        <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-pink-500 mr-2"></i> Training in different heart rate zones provides different fitness benefits.</p>
                    </div>

                    <form id="heart-rate-form" class="mb-6">
                        <div class="mb-4">
                            <label for="heart-rate-age" class="block text-gray-700 font-medium mb-2">Age</label>
                            <input type="number" id="heart-rate-age" min="18" max="100" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="resting-heart-rate" class="block text-gray-700 font-medium mb-2">Resting Heart Rate (bpm)</label>
                            <input type="number" id="resting-heart-rate" min="40" max="100" value="70" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <button type="button" id="calculate-heart-rate-zones" class="w-full bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-4 rounded-md transition duration-300 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                            Calculate Heart Rate Zones
                        </button>
                    </form>

                    <div id="heart-rate-result" class="hidden bg-gray-50 rounded-lg p-6 border-l-4 border-pink-500">
                        <h4 class="text-xl font-semibold text-gray-800 mb-4">Your Heart Rate Zones</h4>
                        <div class="mb-6">
                            <p class="text-gray-600 mb-2">Maximum Heart Rate (MHR):</p>
                            <p class="text-xl font-bold text-pink-600" id="max-heart-rate">-</p>
                        </div>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-6">
                            <div class="bg-blue-50 p-4 rounded-lg">
                                <h5 class="font-semibold text-blue-600 mb-2">Zone 1: Very Light (50-60% MHR)</h5>
                                <p class="text-gray-600 mb-1">Heart Rate Range:</p>
                                <p class="font-bold" id="zone-1-range">-</p>
                                <p class="text-sm text-gray-600 mt-2">Recovery, improves basic endurance</p>
                            </div>
                            <div class="bg-green-50 p-4 rounded-lg">
                                <h5 class="font-semibold text-green-600 mb-2">Zone 2: Light (60-70% MHR)</h5>
                                <p class="text-gray-600 mb-1">Heart Rate Range:</p>
                                <p class="font-bold" id="zone-2-range">-</p>
                                <p class="text-sm text-gray-600 mt-2">Fat burning, aerobic base building</p>
                            </div>
                            <div class="bg-yellow-50 p-4 rounded-lg">
                                <h5 class="font-semibold text-yellow-600 mb-2">Zone 3: Moderate (70-80% MHR)</h5>
                                <p class="text-gray-600 mb-1">Heart Rate Range:</p>
                                <p class="font-bold" id="zone-3-range">-</p>
                                <p class="text-sm text-gray-600 mt-2">Aerobic fitness, improves endurance</p>
                            </div>
                            <div class="bg-orange-50 p-4 rounded-lg">
                                <h5 class="font-semibold text-orange-600 mb-2">Zone 4: Hard (80-90% MHR)</h5>
                                <p class="text-gray-600 mb-1">Heart Rate Range:</p>
                                <p class="font-bold" id="zone-4-range">-</p>
                                <p class="text-sm text-gray-600 mt-2">Anaerobic threshold, improves speed</p>
                            </div>
                            <div class="bg-red-50 p-4 rounded-lg">
                                <h5 class="font-semibold text-red-600 mb-2">Zone 5: Maximum (90-100% MHR)</h5>
                                <p class="text-gray-600 mb-1">Heart Rate Range:</p>
                                <p class="font-bold" id="zone-5-range">-</p>
                                <p class="text-sm text-gray-600 mt-2">Peak performance, short bursts</p>
                            </div>
                        </div>
                        <div class="bg-white p-4 rounded-lg shadow mb-4">
                            <h5 class="font-semibold mb-3">Training Recommendations</h5>
                            <ul class="list-disc pl-6 space-y-2 text-gray-600">
                                <li>Beginners: Focus on Zones 1-2 (70% of training)</li>
                                <li>Intermediate: Add Zone 3 (20% of training)</li>
                                <li>Advanced: Include Zones 4-5 (10% of training)</li>
                                <li>Pregnant women: Stay in Zones 1-2 unless cleared by doctor</li>
                            </ul>
                        </div>
                        <div class="bg-blue-50 p-4 rounded-lg">
                            <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-blue-500 mr-2"></i> Consult your doctor before starting any intense exercise program, especially during pregnancy.</p>
                        </div>
                    </div>
                </div>

                <!-- Postpartum Recovery Calculator -->
                <div id="postpartum-calculator" class="calculator-tab">
                    <h3 class="text-2xl font-bold text-gray-800 mb-6">Postpartum Recovery Calculator</h3>
                    <p class="text-gray-600 mb-6">Track your postpartum recovery milestones and health indicators.</p>

                    <div class="bg-pink-50 p-4 rounded-lg mb-6">
                        <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-pink-500 mr-2"></i> Postpartum recovery typically takes 6-8 weeks, but full recovery can take up to a year.</p>
                    </div>

                    <form id="postpartum-form" class="mb-6">
                        <div class="mb-4">
                            <label for="delivery-date" class="block text-gray-700 font-medium mb-2">Delivery Date</label>
                            <input type="date" id="delivery-date" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                        </div>

                        <div class="mb-4">
                            <label for="delivery-method" class="block text-gray-700 font-medium mb-2">Delivery Method</label>
                            <select id="delivery-method" class="w-full rounded-md border-gray-300 shadow-sm focus:border-pink-500 focus:ring focus:ring-pink-200 focus:ring-opacity-50 p-2 border">
                                <option value="vaginal">Vaginal Delivery</option>
                                <option value="c-section">Cesarean Section</option>
                                <option value="assisted">Assisted Vaginal Delivery</option>
                            </select>
                        </div>

                        <button type="button" id="calculate-postpartum" class="w-full bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-4 rounded-md transition duration-300 focus:outline-none focus:ring-2 focus:ring-pink-500 focus:ring-opacity-50">
                            Calculate Recovery Timeline
                        </button>
                    </form>

                    <div id="postpartum-result" class="hidden bg-gray-50 rounded-lg p-6 border-l-4 border-pink-500">
                        <h4 class="text-xl font-semibold text-gray-800 mb-4">Your Postpartum Recovery</h4>
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-6">
                            <div>
                                <p class="text-gray-600 mb-1">Days Postpartum:</p>
                                <p class="text-xl font-bold text-pink-600" id="postpartum-days">-</p>
                            </div>
                            <div>
                                <p class="text-gray-600 mb-1">Recovery Stage:</p>
                                <p class="text-xl font-bold text-pink-600" id="recovery-stage">-</p>
                            </div>
                        </div>
                        <div class="mb-6">
                            <h5 class="font-semibold mb-3">Recovery Milestones</h5>
                            <div class="relative pt-1">
                                <div class="flex mb-2 items-center justify-between">
                                    <div>
                                        <span class="text-xs font-semibold inline-block py-1 px-2 uppercase rounded-full text-pink-600 bg-pink-200">
                                            Immediate
                                        </span>
                                    </div>
                                    <div class="text-right">
                                        <span class="text-xs font-semibold inline-block text-pink-600">
                                            6 Weeks
                                        </span>
                                    </div>
                                </div>
                                <div class="overflow-hidden h-2 mb-4 text-xs flex rounded bg-pink-200">
                                    <div id="recovery-progress" style="width: 0%" class="shadow-none flex flex-col text-center whitespace-nowrap text-white justify-center bg-pink-500"></div>
                                </div>
                            </div>
                            <div id="milestones-list" class="space-y-3">
                                <!-- Milestones will be generated here -->
                            </div>
                        </div>
                        <div class="bg-white p-4 rounded-lg shadow mb-4">
                            <h5 class="font-semibold mb-3">Postpartum Warning Signs</h5>
                            <ul class="list-disc pl-6 space-y-2 text-gray-600">
                                <li>Heavy bleeding (soaking a pad in 1 hour)</li>
                                <li>Fever over 100.4°F (38°C)</li>
                                <li>Severe headache or vision changes</li>
                                <li>Painful, red, or swollen legs</li>
                                <li>Chest pain or difficulty breathing</li>
                            </ul>
                        </div>
                        <div class="bg-blue-50 p-4 rounded-lg">
                            <p class="text-sm text-gray-700"><i class="fas fa-info-circle text-blue-500 mr-2"></i> Contact your healthcare provider immediately if you experience any warning signs.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Testimonials Section -->
    <section class="py-16 bg-gradient-to-r from-purple-50 to-pink-50">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-12 text-gray-800">What Our <span class="text-pink-500">Users Say</span></h2>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="bg-white rounded-lg shadow-lg p-6">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 rounded-full bg-pink-100 flex items-center justify-center text-pink-500 text-xl font-bold mr-4">S</div>
                        <div>
                            <h4 class="font-semibold">Sarah J.</h4>
                            <p class="text-gray-500 text-sm">First-time mom</p>
                        </div>
                    </div>
                    <p class="text-gray-600">"The due date calculator was spot on! My baby arrived just one day after the predicted date. All the pregnancy calculators helped me feel more prepared."</p>
                    <div class="flex mt-4 text-yellow-400">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                </div>
                <div class="bg-white rounded-lg shadow-lg p-6">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 rounded-full bg-blue-100 flex items-center justify-center text-blue-500 text-xl font-bold mr-4">M</div>
                        <div>
                            <h4 class="font-semibold">Michael T.</h4>
                            <p class="text-gray-500 text-sm">Expecting father</p>
                        </div>
                    </div>
                    <p class="text-gray-600">"As an expecting dad, these calculators helped me understand my partner's pregnancy journey better. The trimester calculator was especially helpful for tracking progress."</p>
                    <div class="flex mt-4 text-yellow-400">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star-half-alt"></i>
                    </div>
                </div>
                <div class="bg-white rounded-lg shadow-lg p-6">
                    <div class="flex items-center mb-4">
                        <div class="w-12 h-12 rounded-full bg-green-100 flex items-center justify-center text-green-500 text-xl font-bold mr-4">A</div>
                        <div>
                            <h4 class="font-semibold">Amanda L.</h4>
                            <p class="text-gray-500 text-sm">Trying to conceive</p>
                        </div>
                    </div>
                    <p class="text-gray-600">"The ovulation calculator helped me identify my fertile window accurately. After 6 months of trying, we finally got pregnant thanks to tracking with this tool!"</p>
                    <div class="flex mt-4 text-yellow-400">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- FAQ Section -->
    <section class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-12 text-gray-800">Frequently Asked <span class="text-pink-500">Questions</span></h2>
            <div class="max-w-3xl mx-auto">
                <div class="border-b border-gray-200 pb-4 mb-6">
                    <button class="flex justify-between items-center w-full text-left font-medium text-gray-700 focus:outline-none" onclick="toggleFAQ(1)">
                        <span>How accurate are these pregnancy calculators?</span>
                        <i class="fas fa-chevron-down text-pink-500 transition-transform duration-300" id="faq-icon-1"></i>
                    </button>
                    <div id="faq-content-1" class="hidden mt-2 text-gray-600">
                        <p>Our calculators use medically-reviewed formulas and algorithms to provide estimates based on the data you input. The due date calculator, for example, is accurate to within ±5 days for most pregnancies when the last menstrual period date is known. However, individual variations can occur, so always consult with your healthcare provider for medical advice.</p>
                    </div>
                </div>
                <div class="border-b border-gray-200 pb-4 mb-6">
                    <button class="flex justify-between items-center w-full text-left font-medium text-gray-700 focus:outline-none" onclick="toggleFAQ(2)">
                        <span>Is my personal data stored when I use these calculators?</span>
                        <i class="fas fa-chevron-down text-pink-500 transition-transform duration-300" id="faq-icon-2"></i>
                    </button>
                    <div id="faq-content-2" class="hidden mt-2 text-gray-600">
                        <p>No, we do not store any of your personal health data. All calculations are performed locally in your browser, and no information is sent to our servers. This ensures complete privacy and security for your sensitive health information.</p>
                    </div>
                </div>
                <div class="border-b border-gray-200 pb-4 mb-6">
                    <button class="flex justify-between items-center w-full text-left font-medium text-gray-700 focus:outline-none" onclick="toggleFAQ(3)">
                        <span>Can I use these calculators on my mobile phone?</span>
                        <i class="fas fa-chevron-down text-pink-500 transition-transform duration-300" id="faq-icon-3"></i>
                    </button>
                    <div id="faq-content-3" class="hidden mt-2 text-gray-600">
                        <p>Yes! All our calculators are fully responsive and work on any device including smartphones and tablets. The interface automatically adjusts to provide the best user experience regardless of screen size.</p>
                    </div>
                </div>
                <div class="border-b border-gray-200 pb-4 mb-6">
                    <button class="flex justify-between items-center w-full text-left font-medium text-gray-700 focus:outline-none" onclick="toggleFAQ(4)">
                        <span>How often should I use the baby kick counter?</span>
                        <i class="fas fa-chevron-down text-pink-500 transition-transform duration-300" id="faq-icon-4"></i>
                    </button>
                    <div id="faq-content-4" class="hidden mt-2 text-gray-600">
                        <p>Most healthcare providers recommend doing kick counts once or twice daily starting around 28 weeks of pregnancy. Choose a time when your baby is typically active, and count how long it takes to feel 10 movements. If you don't feel 10 movements in 2 hours, contact your healthcare provider.</p>
                    </div>
                </div>
                <div class="border-b border-gray-200 pb-4 mb-6">
                    <button class="flex justify-between items-center w-full text-left font-medium text-gray-700 focus:outline-none" onclick="toggleFAQ(5)">
                        <span>Are these calculators suitable for twins or multiple pregnancies?</span>
                        <i class="fas fa-chevron-down text-pink-500 transition-transform duration-300" id="faq-icon-5"></i>
                    </button>
                    <div id="faq-content-5" class="hidden mt-2 text-gray-600">
                        <p>Some calculators like the due date calculator can be used for twin pregnancies, but results may be less accurate as twins often arrive earlier. The weight gain and nutrition calculators should be adjusted for multiples - consult your healthcare provider for personalized recommendations for twin or multiple pregnancies.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA Section -->
    <section class="py-16 bg-gradient-to-r from-pink-500 to-purple-600 text-white">
        <div class="container mx-auto px-4 text-center">
            <h2 class="text-3xl md:text-4xl font-bold mb-6">Ready to Track Your Pregnancy Journey?</h2>
            <p class="text-xl mb-8 max-w-2xl mx-auto">Join thousands of parents who use our calculators to stay informed and prepared.</p>
            <div class="flex flex-col sm:flex-row justify-center space-y-4 sm:space-y-0 sm:space-x-4">
                <button onclick="scrollToCalculatorSection('pregnancy-due-date')" class="bg-white text-pink-600 hover:bg-gray-100 font-bold py-3 px-8 rounded-full text-lg transition duration-300 transform hover:scale-105">
                    <i class="fas fa-calculator mr-2"></i> Try Our Calculators
                </button>
                <button onclick="openModal('about-modal')" class="border-2 border-white text-white hover:bg-white hover:text-pink-600 font-bold py-3 px-8 rounded-full text-lg transition duration-300 transform hover:scale-105">
                    <i class="fas fa-info-circle mr-2"></i> Learn More
                </button>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white py-12">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <div>
                    <h3 class="text-xl font-bold mb-4 flex items-center">
                        <i class="fas fa-baby text-pink-400 mr-2"></i> Pregnancy Calculators
                    </h3>
                    <p class="text-gray-400">Your complete toolkit for pregnancy, fertility, and parenting calculations.</p>
                    <div class="flex space-x-4 mt-4">
                        <a href="#" class="text-gray-400 hover:text-pink-400 transition duration-300">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-pink-400 transition duration-300">
                            <i class="fab fa-twitter"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-pink-400 transition duration-300">
                            <i class="fab fa-instagram"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-pink-400 transition duration-300">
                            <i class="fab fa-pinterest-p"></i>
                        </a>
                    </div>
                </div>
                <div>
                    <h4 class="font-semibold text-lg mb-4">Calculators</h4>
                    <ul class="space-y-2">
                        <li><a href="#" onclick="openCalculator('pregnancy-due-date')" class="text-gray-400 hover:text-pink-400 transition duration-300">Due Date Calculator</a></li>
                        <li><a href="#" onclick="openCalculator('ovulation-calculator')" class="text-gray-400 hover:text-pink-400 transition duration-300">Ovulation Calculator</a></li>
                        <li><a href="#" onclick="openCalculator('bmi-calculator')" class="text-gray-400 hover:text-pink-400 transition duration-300">BMI Calculator</a></li>
                        <li><a href="#" onclick="openCalculator('baby-kick-counter')" class="text-gray-400 hover:text-pink-400 transition duration-300">Kick Counter</a></li>
                        <li><a href="#" onclick="openCalculator('trimester-calculator')" class="text-gray-400 hover:text-pink-400 transition duration-300">Trimester Calculator</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="font-semibold text-lg mb-4">Resources</h4>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-400 hover:text-pink-400 transition duration-300">Pregnancy Articles</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-pink-400 transition duration-300">Week-by-Week Guide</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-pink-400 transition duration-300">Nutrition Tips</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-pink-400 transition duration-300">Exercise During Pregnancy</a></li>
                        <li><a href="#" class="text-gray-400 hover:text-pink-400 transition duration-300">Baby Development</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="font-semibold text-lg mb-4">Company</h4>
                    <ul class="space-y-2">
                        <li><button onclick="openModal('about-modal')" class="text-gray-400 hover:text-pink-400 transition duration-300 text-left">About Us</button></li>
                        <li><button onclick="openModal('privacy-modal')" class="text-gray-400 hover:text-pink-400 transition duration-300 text-left">Privacy Policy</button></li>
                        <li><button onclick="openModal('terms-modal')" class="text-gray-400 hover:text-pink-400 transition duration-300 text-left">Terms of Service</button></li>
                        <li><button onclick="openModal('disclaimer-modal')" class="text-gray-400 hover:text-pink-400 transition duration-300 text-left">Medical Disclaimer</button></li>
                        <li><a href="mailto:contact@healthcalculators.example.com" class="text-gray-400 hover:text-pink-400 transition duration-300">Contact Us</a></li>
                    </ul>
                </div>
            </div>
            <div class="border-t border-gray-700 mt-8 pt-8 text-center text-gray-400">
                <p>&copy; 2023 Health Calculators. All rights reserved.</p>
                <p class="mt-2 text-sm">This tool does not provide medical advice. It is intended for informational purposes only.</p>
            </div>
        </div>
    </footer>

    <!-- Modals -->
    <div id="about-modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('about-modal')">&times;</span>
            <h3 class="text-2xl font-bold text-gray-800 mb-4">About Pregnancy & Health Calculators</h3>
            <div class="prose max-w-none">
                <p>Welcome to Pregnancy & Health Calculators, your comprehensive resource for accurate, easy-to-use health calculators related to pregnancy, fertility, and parenting.</p>
                
                <h4 class="text-xl font-semibold mt-6 mb-3">Our Mission</h4>
                <p>Our mission is to empower expecting parents and those planning pregnancy with reliable, medically-reviewed tools to track their health journey. We believe knowledge reduces anxiety and helps parents make informed decisions.</p>
                
                <h4 class="text-xl font-semibold mt-6 mb-3">Our Team</h4>
                <p>Our calculators are developed in consultation with healthcare professionals including OB-GYNs, midwives, and pediatricians. While we're not a medical provider, we strive to ensure our tools reflect current medical guidelines.</p>
                
                <h4 class="text-xl font-semibold mt-6 mb-3">Data Privacy</h4>
                <p>We take your privacy seriously. All calculations happen locally in your browser - we don't store your personal health data. You can use our tools with complete confidence that your information remains private.</p>
            </div>
        </div>
    </div>

    <div id="privacy-modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('privacy-modal')">&times;</span>
            <h3 class="text-2xl font-bold text-gray-800 mb-4">Privacy Policy</h3>
            <div class="prose max-w-none">
                <p><strong>Last Updated:</strong> January 1, 2023</p>
                
                <h4 class="text-xl font-semibold mt-6 mb-3">Information We Collect</h4>
                <p>We do not collect personal health information through our calculators. All calculations are performed locally in your web browser and no data is transmitted to our servers.</p>
                <p>We may collect anonymous usage statistics to improve our services, but this data cannot be linked to individual users.</p>
                
                <h4 class="text-xl font-semibold mt-6 mb-3">Cookies</h4>
                <p>Our website may use cookies to enhance user experience. You may choose to set your web browser to refuse cookies, but some features may not function properly.</p>
                
                <h4 class="text-xl font-semibold mt-6 mb-3">Third-Party Services</h4>
                <p>We may use third-party services (like Google Analytics) that collect, monitor and analyze this information to improve our website's functionality.</p>
                
                <h4 class="text-xl font-semibold mt-6 mb-3">Changes To This Privacy Policy</h4>
                <p>This Privacy Policy is effective as of the date above and will remain in effect except with respect to any changes in its provisions in the future.</p>
            </div>
        </div>
    </div>

    <div id="terms-modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('terms-modal')">&times;</span>
            <h3 class="text-2xl font-bold text-gray-800 mb-4">Terms of Service</h3>
            <div class="prose max-w-none">
                <h4 class="text-xl font-semibold mt-6 mb-3">1. Terms</h4>
                <p>By accessing this website, you are agreeing to be bound by these Terms of Service, all applicable laws and regulations, and agree that you are responsible for compliance with any applicable local laws.</p>
                
                <h4 class="text-xl font-semibold mt-6 mb-3">2. Use License</h4>
                <p>Permission is granted to temporarily use the tools on this website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title.</p>
                
                <h4 class="text-xl font-semibold mt-6 mb-3">3. Disclaimer</h4>
                <p>The materials on this website are provided "as is". We make no warranties, expressed or implied, and hereby disclaim all other warranties including, without limitation, implied warranties of merchantability or fitness for a particular purpose.</p>
                
                <h4 class="text-xl font-semibold mt-6 mb-3">4. Limitations</h4>
                <p>In no event shall we be liable for any damages arising out of the use or inability to use the materials on this website.</p>
            </div>
        </div>
    </div>

    <div id="disclaimer-modal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal('disclaimer-modal')">&times;</span>
            <h3 class="text-2xl font-bold text-gray-800 mb-4">Medical Disclaimer</h3>
            <div class="prose max-w-none">
                <p>The content and tools provided on this website are for informational purposes only and are not intended to be a substitute for professional medical advice, diagnosis, or treatment.</p>
                
                <h4 class="text-xl font-semibold mt-6 mb-3">Not Medical Advice</h4>
                <p>Always seek the advice of your physician or other qualified health provider with any questions you may have regarding a medical condition or pregnancy. Never disregard professional medical advice or delay in seeking it because of something you have read on this website.</p>
                
                <h4 class="text-xl font-semibold mt-6 mb-3">Accuracy of Information</h4>
                <p>While we strive to provide accurate information, the field of medicine is constantly evolving. We make no representation or warranty as to the accuracy, completeness, or usefulness of any information provided.</p>
                
                <h4 class="text-xl font-semibold mt-6 mb-3">Emergency Situations</h4>
                <p>If you think you may have a medical emergency, call your doctor or emergency services immediately. Do not rely on electronic communications or this website for assistance in urgent situations.</p>
            </div>
        </div>
    </div>

    <!-- JavaScript -->
    <script>
        // Calculator tab functionality
        function openCalculator(calculatorId) {
            // Hide all calculator tabs
            document.querySelectorAll('.calculator-tab').forEach(tab => {
                tab.classList.remove('active');
            });
            
            // Show selected calculator tab
            document.getElementById(calculatorId).classList.add('active');
            
            // Update active nav link
            document.querySelectorAll('.nav-link').forEach(link => {
                link.classList.remove('active');
            });
            
            // Scroll to calculator section
            document.getElementById('calculators').scrollIntoView({ behavior: 'smooth' });
        }
        
        function scrollToCalculatorSection(calculatorId) {
            openCalculator(calculatorId);
        }
        
        // Modal functionality
        function openModal(modalId) {
            document.getElementById(modalId).style.display = 'block';
            document.body.style.overflow = 'hidden';
        }
        
        function closeModal(modalId) {
            document.getElementById(modalId).style.display = 'none';
            document.body.style.overflow = 'auto';
        }
        
        // Close modal when clicking outside
        window.onclick = function(event) {
            document.querySelectorAll('.modal').forEach(modal => {
                if (event.target == modal) {
                    modal.style.display = 'none';
                    document.body.style.overflow = 'auto';
                }
            });
        }
        
        // FAQ toggle functionality
        function toggleFAQ(index) {
            const content = document.getElementById(`faq-content-${index}`);
            const icon = document.getElementById(`faq-icon-${index}`);
            
            if (content.classList.contains('hidden')) {
                content.classList.remove('hidden');
                icon.classList.add('transform', 'rotate-180');
            } else {
                content.classList.add('hidden');
                icon.classList.remove('transform', 'rotate-180');
            }
        }
        
        // Due Date Calculator functionality
        document.addEventListener('DOMContentLoaded', function() {
            // Toggle between LMP and conception date inputs
            const methodRadios = document.querySelectorAll('input[name="calculationMethod"]');
            const lmpInput = document.getElementById('lmp-input');
            const conceptionInput = document.getElementById('conception-input');
            
            methodRadios.forEach(radio => {
                radio.addEventListener('change', function() {
                    if (this.value === 'lmp') {
                        lmpInput.classList.remove('hidden');
                        conceptionInput.classList.add('hidden');
                    } else {
                        lmpInput.classList.add('hidden');
                        conceptionInput.classList.remove('hidden');
                    }
                });
            });
            
            // Calculate due date
            document.getElementById('calculateDueDate').addEventListener('click', function() {
                const method = document.querySelector('input[name="calculationMethod"]:checked').value;
                const cycleLength = parseInt(document.getElementById('cycleLength').value) || 28;
                let dueDate;
                
                if (method === 'lmp') {
                    const lmpDate = new Date(document.getElementById('lmpDate').value);
                    if (isNaN(lmpDate.getTime())) {
                        alert('Please enter a valid last menstrual period date');
                        return;
                    }
                    // Naegele's rule: LMP + 1 year - 3 months + 7 days + (cycle length - 28 days)
                    dueDate = new Date(lmpDate);
                    dueDate.setFullYear(dueDate.getFullYear() + 1);
                    dueDate.setMonth(dueDate.getMonth() - 3);
                    dueDate.setDate(dueDate.getDate() + 7 + (cycleLength - 28));
                } else {
                    const conceptionDate = new Date(document.getElementById('conceptionDate').value);
                    if (isNaN(conceptionDate.getTime())) {
                        alert('Please enter a valid conception date');
                        return;
                    }
                    // Conception date + 266 days (38 weeks)
                    dueDate = new Date(conceptionDate);
                    dueDate.setDate(dueDate.getDate() + 266);
                }
                
                // Calculate current week of pregnancy
                const today = new Date();
                let startDate;
                
                if (method === 'lmp') {
                    startDate = new Date(document.getElementById('lmpDate').value);
                } else {
                    startDate = new Date(conceptionDate);
                    startDate.setDate(startDate.getDate() - 14); // Approximate LMP from conception
                }
                
                const daysPassed = Math.floor((today - startDate) / (1000 * 60 * 60 * 24));
                const currentWeek = Math.floor(daysPassed / 7);
                const progressPercentage = Math.min(Math.floor((daysPassed / 280) * 100), 100);
                
                // Update results
                document.getElementById('dueDate').textContent = formatDate(dueDate);
                document.getElementById('currentWeek').textContent = currentWeek > 0 ? `${currentWeek} weeks` : 'Not pregnant yet';
                
                // Calculate trimester dates
                const firstTriStart = formatDate(startDate);
                const firstTriEnd = new Date(startDate);
                firstTriEnd.setDate(firstTriEnd.getDate() + 13 * 7);
                
                const secondTriStart = new Date(firstTriEnd);
                secondTriStart.setDate(secondTriStart.getDate() + 1);
                const secondTriEnd = new Date(secondTriStart);
                secondTriEnd.setDate(secondTriEnd.getDate() + 13 * 7);
                
                const thirdTriStart = new Date(secondTriEnd);
                thirdTriStart.setDate(thirdTriStart.getDate() + 1);
                
                document.getElementById('firstTrimester').textContent = `${firstTriStart} to ${formatDate(firstTriEnd)}`;
                document.getElementById('secondTrimester').textContent = `${formatDate(secondTriStart)} to ${formatDate(secondTriEnd)}`;
                document.getElementById('thirdTrimester').textContent = `${formatDate(thirdTriStart)} to ${formatDate(dueDate)}`;
                
                // Estimated conception date (ovulation typically occurs 14 days before next period)
                const estimatedConception = new Date(startDate);
                estimatedConception.setDate(estimatedConception.getDate() + (cycleLength - 14));
                document.getElementById('conceptionDateResult').textContent = formatDate(estimatedConception);
                
                // Update progress bar
                document.getElementById('pregnancyProgress').style.width = `${progressPercentage}%`;
                document.getElementById('progressPercentage').textContent = `${progressPercentage}%`;
                
                // Show results
                document.getElementById('due-date-result').classList.remove('hidden');
            });
            
            // Helper function to format dates
            function formatDate(date) {
                return date.toLocaleDateString('en-US', { 
                    year: 'numeric', 
                    month: 'long', 
                    day: 'numeric' 
                });
            }
            
            // Set default dates
            const today = new Date();
            document.getElementById('lmpDate').valueAsDate = new Date(today.setDate(today.getDate() - 14));
            document.getElementById('conceptionDate').valueAsDate = new Date();
            
            // Initialize other calculator functionalities would go here...
            // (Ovulation calculator, BMI calculator, etc.)
        });
    </script>
</body>
</html>

