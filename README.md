<!DOCTYPE html>
<html lang="fr" dir="ltr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Librairie Multilingue</title>
    <link rel="icon" href="https://via.placeholder.com/32" type="image/x-icon">
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/feather-icons/dist/feather.min.js"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&family=Playfair+Display:wght@400;700&family=Roboto:wght@400;500&display=swap');
        
        :root {
            --primary: #4F46E5;
            --secondary: #10B981;
            --dark: #1F2937;
            --light: #F3F4F6;
        }
        
        body {
            font-family: 'Roboto', sans-serif;
        }
        
        .font-arabic {
            font-family: 'Cairo', sans-serif;
        }
        
        .font-french {
            font-family: 'Playfair Display', serif;
        }
        
        .hero-gradient {
            background: linear-gradient(135deg, #4F46E5 0%, #10B981 100%);
        }
        
        .language-selector:hover .language-dropdown {
            display: block;
        }
        
        .book-card {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .book-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }
        
        .nav-link::after {
            content: '';
            display: block;
            width: 0;
            height: 2px;
            background: var(--primary);
            transition: width .3s;
        }
        
        .nav-link:hover::after {
            width: 100%;
        }
    </style>
</head>
<body class="bg-gray-50">
    <!-- Language Switcher -->
    <div class="bg-gray-100 py-2 px-4 flex justify-end">
        <div class="language-selector relative">
            <button class="flex items-center text-gray-700">
                <i data-feather="globe" class="w-4 h-4 mr-1"></i>
                Français
                <i data-feather="chevron-down" class="w-4 h-4 ml-1"></i>
            </button>
            <div class="language-dropdown hidden absolute right-0 mt-2 w-32 bg-white rounded-md shadow-lg z-10">
                <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-100 font-french">Français</a>
                <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-100 font-arabic text-right">العربية</a>
                <a href="#" class="block px-4 py-2 text-gray-800 hover:bg-gray-100">English</a>
            </div>
        </div>
    </div>

    <!-- Navigation -->
    <nav class="bg-white shadow-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-16">
                <div class="flex items-center">
                    <a href="#" class="flex-shrink-0 flex items-center">
                        <i data-feather="book-open" class="h-8 w-8 text-indigo-600"></i>
                        <span class="ml-2 text-xl font-bold text-gray-900">Librairie Multilingue</span>
                    </a>
                </div>
                <div class="hidden md:ml-6 md:flex md:items-center md:space-x-8">
                    <a href="#" class="nav-link text-gray-900 inline-flex items-center px-1 pt-1 border-b-2 border-indigo-500 text-sm font-medium">Accueil</a>
                    <a href="#" class="nav-link text-gray-500 hover:text-gray-700 inline-flex items-center px-1 pt-1 text-sm font-medium">Catalogue</a>
                    <a href="#" class="nav-link text-gray-500 hover:text-gray-700 inline-flex items-center px-1 pt-1 text-sm font-medium">Promotions</a>
                    <a href="#" class="nav-link text-gray-500 hover:text-gray-700 inline-flex items-center px-1 pt-1 text-sm font-medium">FAQ</a>
                    <a href="#" class="nav-link text-gray-500 hover:text-gray-700 inline-flex items-center px-1 pt-1 text-sm font-medium">Contact</a>
                    <a href="#" class="flex items-center text-gray-500 hover:text-gray-700 p-2">
                        <i data-feather="shopping-cart" class="w-5 h-5"></i>
                        <span class="ml-1">Panier (0)</span>
                    </a>
                </div>
                <div class="-mr-2 flex items-center md:hidden">
                    <button type="button" class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none" aria-label="Ouvrir le menu">
                        <i data-feather="menu" class="block h-6 w-6"></i>
                    </button>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <main>
        <div class="hero-gradient text-white">
            <div class="max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:px-8">
                <div class="lg:grid lg:grid-cols-2 lg:gap-8 items-center">
                    <div class="mb-8 lg:mb-0" data-aos="fade-right">
                        <h1 class="text-4xl font-extrabold tracking-tight sm:text-5xl lg:text-6xl mb-4">
                            Explorez des livres dans votre langue
                        </h1>
                        <p class="text-xl mb-8">
                            Découvrez notre collection de livres numériques en français, arabe et anglais. Téléchargez instantanément après paiement.
                        </p>
                        <div class="flex space-x-4">
                            <a href="#" class="bg-white text-indigo-600 hover:bg-gray-100 px-6 py-3 rounded-md font-medium">
                                Explorer les livres
                            </a>
                            <a href="#" class="border-2 border-white text-white hover:bg-white hover:text-indigo-600 px-6 py-3 rounded-md font-medium">
                                Voir les promotions
                            </a>
                        </div>
                    </div>
                    <div data-aos="fade-left">
                        <img src="https://via.placeholder.com/1024x576" alt="Books" class="rounded-lg shadow-xl">
                    </div>
                </div>
            </div>
        </div>

        <!-- Featured Books -->
        <div class="max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-extrabold text-gray-900 sm:text-4xl" data-aos="fade-up">
                    Nos nouveautés
                </h2>
                <p class="mt-3 max-w-2xl mx-auto text-xl text-gray-500 sm:mt-4" data-aos="fade-up" data-aos-delay="100">
                    Découvrez nos dernières parutions
                </p>
            </div>
            
            <div class="grid grid-cols-1 gap-y-10 sm:grid-cols-2 gap-x-6 lg:grid-cols-3 xl:grid-cols-4 xl:gap-x-8">
                <!-- Book 1 -->
                <div class="group book-card" data-aos="fade-up" data-aos-delay="200">
                    <div class="w-full aspect-w-1 aspect-h-1 bg-gray-200 rounded-lg overflow-hidden xl:aspect-w-7 xl:aspect-h-8">
                        <img src="https://via.placeholder.com/320x240" alt="Book cover" class="w-full h-full object-center object-cover group-hover:opacity-75">
                    </div>
                    <div class="mt-4">
                        <div class="flex justify-between">
                            <h3 class="text-lg font-medium text-gray-900">Le Petit Prince</h3>
                            <span class="px-2 py-1 text-xs font-semibold text-green-800 bg-green-100 rounded-full">FR</span>
                        </div>
                        <p class="mt-1 text-sm text-gray-500">Antoine de Saint-Exupéry</p>
                        <div class="mt-2 flex justify-between items-center">
                            <span class="text-lg font-bold text-indigo-600">9.99 €</span>
                            <button class="text-indigo-600 hover:text-indigo-800 p-2">
                                <i data-feather="shopping-cart" class="w-5 h-5"></i>
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Book 2 -->
                <div class="group book-card" data-aos="fade-up" data-aos-delay="300">
                    <div class="w-full aspect-w-1 aspect-h-1 bg-gray-200 rounded-lg overflow-hidden xl:aspect-w-7 xl:aspect-h-8">
                        <img src="https://via.placeholder.com/320x240" alt="Book cover" class="w-full h-full object-center object-cover group-hover:opacity-75">
                    </div>
                    <div class="mt-4">
                        <div class="flex justify-between">
                            <h3 class="text-lg font-medium text-gray-900">ألف ليلة وليلة</h3>
                            <span class="px-2 py-1 text-xs font-semibold text-green-800 bg-green-100 rounded-full">AR</span>
                        </div>
                        <p class="mt-1 text-sm text-gray-500">تراث عربي</p>
                        <div class="mt-2 flex justify-between items-center">
                            <span class="text-lg font-bold text-indigo-600">12.99 €</span>
                            <button class="text-indigo-600 hover:text-indigo-800 p-2">
                                <i data-feather="shopping-cart" class="w-5 h-5"></i>
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Book 3 -->
                <div class="group book-card" data-aos="fade-up" data-aos-delay="400">
                    <div class="w-full aspect-w-1 aspect-h-1 bg-gray-200 rounded-lg overflow-hidden xl:aspect-w-7 xl:aspect-h-8">
                        <img src="https://via.placeholder.com/320x240" alt="Book cover" class="w-full h-full object-center object-cover group-hover:opacity-75">
                    </div>
                    <div class="mt-4">
                        <div class="flex justify-between">
                            <h3 class="text-lg font-medium text-gray-900">1984</h3>
                            <span class="px-2 py-1 text-xs font-semibold text-green-800 bg-green-100 rounded-full">EN</span>
                        </div>
                        <p class="mt-1 text-sm text-gray-500">George Orwell</p>
                        <div class="mt-2 flex justify-between items-center">
                            <span class="text-lg font-bold text-indigo-600">8.99 €</span>
                            <button class="text-indigo-600 hover:text-indigo-800 p-2">
                                <i data-feather="shopping-cart" class="w-5 h-5"></i>
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Book 4 -->
                <div class="group book-card" data-aos="fade-up" data-aos-delay="500">
                    <div class="w-full aspect-w-1 aspect-h-1 bg-gray-200 rounded-lg overflow-hidden xl:aspect-w-7 xl:aspect-h-8">
                        <img src="https://via.placeholder.com/320x240" alt="Book cover" class="w-full h-full object-center object-cover group-hover:opacity-75">
                    </div>
                    <div class="mt-4">
                        <div class="flex justify-between">
                            <h3 class="text-lg font-medium text-gray-900">L'Étranger</h3>
                            <span class="px-2 py-1 text-xs font-semibold text-green-800 bg-green-100 rounded-full">FR</span>
                        </div>
                        <p class="mt-1 text-sm text-gray-500">Albert Camus</p>
                        <div class="mt-2 flex justify-between items-center">
                            <span class="text-lg font-bold text-indigo-600">7.99 €</span>
                            <button class="text-indigo-600 hover:text-indigo-800 p-2">
                                <i data-feather="shopping-cart" class="w-5 h-5"></i>
                            </button>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="mt-12 text-center">
                <a href="#" class="inline-flex items-center px-6 py-3 border border-transparent text-base font-medium rounded-md shadow-sm text-white bg-indigo-600 hover:bg-indigo-700">
                    Voir tout le catalogue
                    <i data-feather="arrow-right" class="ml-2 w-5 h-5"></i>
                </a>
            </div>
        </div>

        <!-- Features -->
        <div class="bg-gray-100 py-12">
            <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
                <div class="lg:text-center">
                    <h2 class="text-3xl font-extrabold text-gray-900 sm:text-4xl" data-aos="fade-up">
                        Pourquoi choisir notre librairie ?
                    </h2>
                    <p class="mt-4 max-w-2xl text-xl text-gray-500 lg:mx-auto" data-aos="fade-up" data-aos-delay="100">
                        Une expérience de lecture multilingue simplifiée
                    </p>
                </div>

                <div class="mt-10">
                    <div class="grid grid-cols-1 gap-10 sm:grid-cols-2 lg:grid-cols-4">
                        <!-- Feature 1 -->
                        <div class="bg-white p-6 rounded-lg shadow-md" data-aos="fade-up" data-aos-delay="200">
                            <div class="flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white">
                                <i data-feather="globe" class="w-6 h-6"></i>
                            </div>
                            <div class="mt-6">
                                <h3 class="text-lg font-medium text-gray-900">Multilingue</h3>
                                <p class="mt-2 text-base text-gray-500">
                                    Livres disponibles en français, arabe et anglais pour répondre à tous vos besoins.
                                </p>
                            </div>
                        </div>
                        
                        <!-- Feature 2 -->
                        <div class="bg-white p-6 rounded-lg shadow-md" data-aos="fade-up" data-aos-delay="300">
                            <div class="flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white">
                                <i data-feather="download" class="w-6 h-6"></i>
                            </div>
                            <div class="mt-6">
                                <h3 class="text-lg font-medium text-gray-900">Téléchargement instantané</h3>
                                <p class="mt-2 text-base text-gray-500">
                                    Recevez vos livres immédiatement après paiement, sans attente.
                                </p>
                            </div>
                        </div>
                        
                        <!-- Feature 3 -->
                        <div class="bg-white p-6 rounded-lg shadow-md" data-aos="fade-up" data-aos-delay="400">
                            <div class="flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white">
                                <i data-feather="credit-card" class="w-6 h-6"></i>
                            </div>
                            <div class="mt-6">
                                <h3 class="text-lg font-medium text-gray-900">Paiement sécurisé</h3>
                                <p class="mt-2 text-base text-gray-500">
                                    Paiement via CCP Postal ou RIB avec confirmation sécurisée.
                                </p>
                            </div>
                        </div>
                        
                        <!-- Feature 4 -->
                        <div class="bg-white p-6 rounded-lg shadow-md" data-aos="fade-up" data-aos-delay="500">
                            <div class="flex items-center justify-center h-12 w-12 rounded-md bg-indigo-500 text-white">
                                <i data-feather="smartphone" class="w-6 h-<headphone" class="w-6 h-6"></i>
                            </div>
                            <div class="mt-6">
                                <h3 class="text-lg font-medium text-gray-900">Lecture mobile</h3>
                                <p class="mt-2 text-base text-gray-500">
                                    Compatible avec tous les appareils : lisez sur smartphone, tablette ou ordinateur.
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Testimonials -->
        <div class="max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-12">
                <h2 class="text-3xl font-extrabold text-gray-900 sm:text-4xl" data-aos="fade-up">
                    Témoignages
                </h2>
                <p class="mt-3 max-w-2xl mx-auto text-xl text-gray-500 sm:mt-4" data-aos="fade-up" data-aos-delay="100">
                    Ce que nos clients disent de nous
                </p>
            </div>

            <div class="grid grid-cols-1 gap-8 sm:grid-cols-2 lg:grid-cols-3">
                <!-- Testimonial 1 -->
                <div class="bg-white p-6 rounded-lg shadow-md" data-aos="fade-up" data-aos-delay="200">
                    <div class="flex items-center">
                        <div class="flex-shrink-0">
                            <img class="h-10 w-10 rounded-full" src="https://via.placeholder.com/40" alt="Client">
                        </div>
                        <div class="ml-4">
                            <h4 class="text-lg font-medium text-gray-900">Jean Dupont</h4>
                            <p class="text-gray-500">Paris, France</p>
                        </div>
                    </div>
                    <div class="mt-4">
                        <p class="text-gray-600">
                            "J'ai trouvé tous les livres que je cherchais en français et arabe. Le téléchargement est instantané et la qualité est excellente."
                        </p>
                    </div>
                </div>

                <!-- Testimonial 2 -->
                <div class="bg-white p-6 rounded-lg shadow-md" data-aos="fade-up" data-aos-delay="300">
                    <div class="flex items-center">
                        <div class="flex-shrink-0">
                            <img class="h-10 w-10 rounded-full" src="https://via.placeholder.com/40" alt="Client">
                        </div>
                        <div class="ml-4">
                            <h4 class="text-lg font-medium text-gray-900">Layla Ahmed</h4>
                            <p class="text-gray-500">Casablanca, Maroc</p>
                        </div>
                    </div>
                    <div class="mt-4">
                        <p class="text-gray-600">
                            "Enfin une librairie qui comprend les besoins des lecteurs multilingues. J'adore leur sélection de livres en arabe."
                        </p>
                    </div>
                </div>

                <!-- Testimonial 3 -->
                <div class="bg-white p-6 rounded-lg shadow-md" data-aos="fade-up" data-aos-delay="400">
                    <div class="flex items-center">
                        <div class="flex-shrink-0">
                            <img class="h-10 w-10 rounded-full" src="https://via.placeholder.com/40" alt="Client">
                        </div>
                        <div class="ml-4">
                            <h4 class="text-lg font-medium text-gray-900">Emma Johnson</h4>
                            <p class="text-gray-500">London, UK</p>
                        </div>
                    </div>
                    <div class="mt-4">
                        <p class="text-gray-600">
                            "Great selection of French books for language learners. The payment process was smooth and secure."
                        </p>
                    </div>
                </div>
            </div>
        </div>

        <!-- CTA Section -->
        <div class="bg-indigo-700">
            <div class="max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:px-8">
                <div class="lg:grid lg:grid-cols-2 lg:gap-8 items-center">
                    <div class="mb-8 lg:mb-0" data-aos="fade-right">
                        <h2 class="text-3xl font-extrabold tracking-tight text-white sm:text-4xl">
                            Abonnez-vous à notre newsletter
                        </h2>
                        <p class="mt-4 text-lg text-indigo-200">
                            Recevez les dernières nouveautés et promotions directement dans votre boîte email.
                        </p>
                    </div>
                    <div data-aos="fade-left">
                        <form class="sm:flex">
                            <label for="email" class="sr-only">Email</label>
                            <input type="email" id="email" name="email" placeholder="Votre email" required class="w-full px-5 py-3 placeholder-gray-500 focus:ring-indigo-500 focus:border-indigo-500 sm:max-w-xs rounded-md">
                            <button type="submit" class="mt-3 w-full flex items-center justify-center px-5 py-3 border border-transparent text-base font-medium rounded-md text-white bg-indigo-500 hover:bg-indigo-600 sm:mt-0 sm:ml-3 sm:w-auto sm:flex-shrink-0">
                                S'abonner
                            </button>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-800">
        <div class="max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-2 gap-8 md:grid-cols-4">
                <div>
                    <h3 class="text-sm font-semibold text-gray-400 tracking-wider uppercase">Navigation</h3>
                    <ul class="mt-4 space-y-4">
                        <li><a href="#" class="text-base text-gray-300 hover:text-white">Accueil</a></li>
                        <li><a href="#" class="text-base text-gray-300 hover:text-white">Catalogue</a></li>
                        <li><a href="#" class="text-base text-gray-300 hover:text-white">Promotions</a></li>
                        <li><a href="#" class="text-base text-gray-300 hover:text-white">FAQ</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-sm font-semibold text-gray-400 tracking-wider uppercase">Support</h3>
                    <ul class="mt-4 space-y-4">
                        <li><a href="#" class="text-base text-gray-300 hover:text-white">Centre d'aide</a></li>
                        <li><a href="#" class="text-base text-gray-300 hover:text-white">Modes de paiement</a></li>
                        <li><a href="#" class="text-base text-gray-300 hover:text-white">Confidentialité</a></li>
                        <li><a href="#" class="text-base text-gray-300 hover:text-white">Conditions</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-sm font-semibold text-gray-400 tracking-wider uppercase">Entreprise</h3>
                    <ul class="mt-4 space-y-4">
                        <li><a href="#" class="text-base text-gray-300 hover:text-white">À propos</a></li>
                        <li><a href="#" class="text-base text-gray-300 hover:text-white">Blog</a></li>
                        <li><a href="#" class="text-base text-gray-300 hover:text-white">Carrières</a></li>
                        <li><a href="#" class="text-base text-gray-300 hover:text-white">Contact</a></li>
                    </ul>
                </div>
                <div>
                    <h3 class="text-sm font-semibold text-gray-400 tracking-wider uppercase">Suivez-nous</h3>
                    <div class="mt-4 flex space-x-6">
                        <a href="#" class="text-gray-400 hover:text-white">
                            <i data-feather="facebook" class="w-6 h-6"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white">
                            <i data-feather="twitter" class="w-6 h-6"></i>
                        </a>
                        <a href="#" class="text-gray-400 hover:text-white">
                            <i data-feather="instagram" class="w-6 h-6"></i>
                        </a>
                    </div>
                </div>
            </div>
            <div class="mt-8 border-t border-gray-700 pt-8 md:flex md:items-center md:justify-between">
                <div class="flex space-x-6 md:order-2">
                    <a href="#" class="text-gray-400 hover:text-white">
                        <i data-feather="globe" class="w-6 h-6"></i>
                    </a>
                </div>
                <p class="mt-8 text-base text-gray-400 md:mt-0 md:order-1">
                    &copy; 2025 Librairie Multilingue. Tous droits réservés.
                </p>
            </div>
        </div>
    </footer>

    <script>
        // Initialize AOS
        AOS.init({
            duration: 800,
            easing: 'ease-in-out',
            once: true,
            disable: window.innerWidth < 768
        });

        // Initialize Feather Icons
        feather.replace();
    </script>
</body>
</html>
