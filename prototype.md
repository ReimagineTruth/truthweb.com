<html lang="en">
<head>
    <meta charset="utf-8"/>
    <meta content="width=device-width, initial-scale=1.0" name="viewport"/>
    <title>Reimagine Truth</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css" rel="stylesheet"/>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet"/>
    <style>
        body {
            font-family: 'Roboto', sans-serif;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        .fade-in {
            animation: fadeIn 2s ease-in-out;
        }
        @keyframes slideIn {
            from { transform: translateY(20px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
        .slide-in {
            animation: slideIn 1s ease-in-out;
        }
        .sidebar {
            transition: transform 0.3s ease-in-out;
        }
        .sidebar:hover {
            transform: translateX(0);
        }
        .sidebar-item {
            transition: background-color 0.3s ease-in-out, color 0.3s ease-in-out;
        }
        .sidebar-item:hover {
            background-color: #4A5568;
            color: #E2E8F0;
        }
        .sticky-sidebar {
            position: -webkit-sticky;
            position: sticky;
            top: 0;
        }
        .button-click {
            animation: buttonClick 0.2s ease-in-out;
        }
        @keyframes buttonClick {
            0% { transform: scale(1); }
            50% { transform: scale(0.9); }
            100% { transform: scale(1); }
        }
    </style>
</head>
<body class="bg-gray-900 text-gray-200">
    <div class="flex flex-col md:flex-row">
        <aside class="w-full md:w-64 bg-gray-800 h-auto md:h-screen p-4 hidden md:block sticky-sidebar sidebar" id="sidebar">
            <div class="flex items-center mb-6">
                <img alt="A sharply dressed, intense-looking male character" class="w-16 h-16 rounded-full" height="64" src="https://i.ibb.co/p30Q5fs/Leonardo-Kino-XL-A-sharplydressed-intenselooking-male-characte-3.jpg" width="64"/>
                <h2 class="ml-4 text-xl font-bold">Reimagine Truth</h2>
            </div>
            <nav>
                <ul>
                    <li class="mb-4">
                        <a class="text-lg text-gray-200 hover:text-gray-100 sidebar-item" href="https://reimaginetruth.github.io/">Home</a>
                    </li>
                    <li class="mb-4">
                        <a class="text-lg text-gray-200 hover:text-gray-100 sidebar-item" href="#">My Assets</a>
                    </li>
                    <li class="mb-4">
                        <a class="text-lg text-gray-200 hover:text-gray-100 sidebar-item" href=https://reimaginetruth.github.io/aboutpage/">About</a>
                    </li>
                    <li class="mb-4">
                        <a class="text-lg text-gray-200 hover:text-gray-100 sidebar-item" href="https://linktr.ee/reimagine_truth" target="_blank">Community</a>
                    </li>
                    <li class="mb-4">
                        <a class="text-lg text-gray-200 hover:text-gray-100 sidebar-item" href="#">Settings</a>
                    </li>
                </ul>
            </nav>
        </aside>
        <div class="flex-1">
            <header class="bg-gray-800 text-gray-200 p-4 flex justify-between items-center relative shadow-md">
                <button class="md:hidden text-gray-200 absolute top-4 left-4" id="menu-button">
                    <i class="fas fa-bars"></i>
                </button>
                <div class="flex flex-col items-center w-full">
                    <img alt="A sharply dressed, intense-looking male character" class="w-24 mb-2 fade-in" height="50" src="https://i.ibb.co/p30Q5fs/Leonardo-Kino-XL-A-sharplydressed-intenselooking-male-characte-3.jpg" width="100"/>
                    <h1 class="text-2xl font-bold text-center fade-in">Welcome to Reimagine Truth</h1>
                    <p class="text-lg text-center fade-in">Explore the unique stories of our NFT characters.</p>
                </div>
            </header>
            <main class="p-4">
                <div class="flex justify-center mb-6">
                    <input type="text" id="search-bar" placeholder="Search your NFT serial number #" class="w-full max-w-md p-2 rounded bg-gray-700 text-gray-200 placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-blue-500">
                    <button class="ml-2 p-2 bg-blue-500 text-white rounded hover:bg-blue-600 focus:outline-none focus:ring-2 focus:ring-blue-500" onclick="searchNFT()">Search</button>
                </div>
                <div class="flex justify-center mb-6" id="view-all-container" style="display: none;">
                    <button class="p-2 bg-blue-500 text-white rounded hover:bg-blue-600 focus:outline-none focus:ring-2 focus:ring-blue-500" onclick="showAllNFTs()">View All</button>
                </div>
                <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4 p-4" id="nft-grid">
                    <!-- Card 1 -->
                    <div class="border border-gray-700 p-4 bg-gray-800 nft-card slide-in" data-serial="#1" style="display: none;">
                        <img alt="NFT character with a futuristic look" class="w-full mb-2" src="https://i.ibb.co/1mJM8ns/Image-7.png">
                        <h3 class="text-xl font-bold">Truth Seeker #1</h3>
                        <p>Rarity: Common</p>
                        <a href="#" class="text-blue-500">View Details</a>
                    </div>

                    <!-- Card 2 -->
                    <div class="border border-gray-700 p-4 bg-gray-800 nft-card slide-in" data-serial="#2" style="display: none;">
                        <img alt="NFT character with a mystical aura" class="w-full mb-2" src="https://i.ibb.co/zbjm89d/Image-4.png">
                        <h3 class="text-xl font-bold">Truth Seeker #2</h3>
                        <p>Rarity: Rare</p>
                        <a href="#" class="text-blue-500">View Details</a>
                    </div>

                    <!-- Card 3 -->
                    <div class="border border-gray-700 p-4 bg-gray-800 nft-card slide-in" data-serial="#3" style="display: none;">
                        <img alt="NFT character with a cyberpunk style" class="w-full mb-2" src="https://i.ibb.co/z8F7HW5/Image-3.png">
                        <h3 class="text-xl font-bold">Truth Seeker #3</h3>
                        <p>Rarity: Ultra Rare</p>
                        <a href="#" class="text-blue-500">View Details</a>
                    </div>

                    <!-- Card 4 -->
                    <div class="border border-gray-700 p-4 bg-gray-800 nft-card slide-in" data-serial="#4" style="display: none;">
                        <img alt="NFT character with a mystical aura" class="w-full mb-2" src="https://i.ibb.co/XXWGTy4/Image-5.png">
                        <h3 class="text-xl font-bold">Truth Seeker #4</h3>
                        <p>Rarity: Rare</p>
                        <a href="#" class="text-blue-500">View Details</a>
                    </div>
                </div>
            </main>
            <footer class="bg-gray-800 text-gray-200 p-4 text-center shadow-md hidden" id="footer">
                <p>© 2024 Reimagine Truth. All rights reserved.</p>
                <div id="view-all-container" style="display: none;" class="mt-4">
                    <button class="p-2 bg-blue-500 text-white rounded hover:bg-blue-600 focus:outline-none focus:ring-2 focus:ring-blue-500" onclick="showAllNFTs()">View All</button>
                </div>
            </footer>
        </div>
    </div>
    <audio id="click-sound" src="https://www.soundjay.com/button/sounds/button-16.mp3" preload="auto"></audio>
    <script>
        document.getElementById('menu-button').addEventListener('click', function() {
            const sidebar = document.getElementById('sidebar');
            const footer = document.getElementById('footer');
            if (sidebar.classList.contains('hidden')) {
                sidebar.classList.remove('hidden');
                footer.classList.remove('hidden');
            } else {
                sidebar.classList.add('hidden');
                footer.classList.add('hidden');
            }
            playClickSound();
        });

        function searchNFT() {
            const searchValue = document.getElementById('search-bar').value.trim();
            const nftCards = document.querySelectorAll('.nft-card');
            let found = false;

            nftCards.forEach(card => {
                if (card.getAttribute('data-serial') === searchValue) {
                    card.style.display = 'block';
                    found = true;
                } else {
                    card.style.display = 'none';
                }
            });

            if (found) {
                document.getElementById('view-all-container').style.display = 'flex';
            } else {
                document.getElementById('view-all-container').style.display = 'none';
            }
            playClickSound();
        }

        function showAllNFTs() {
            const nftCards = document.querySelectorAll('.nft-card');
            nftCards.forEach(card => {
                card.style.display = 'block';
            });
            document.getElementById('view-all-container').style.display = 'none';
            playClickSound();
        }

        function scrollToStart() {
            window.scrollTo({ top: 0, behavior: 'smooth' });
            playClickSound();
        }

        function playClickSound() {
            const clickSound = document.getElementById('click-sound');
            clickSound.play();
        }

        function redirectToAbout() {
            window.location.href = "https://reimaginetruth.github.io/aboutpages/";
        }

        document.querySelectorAll('button').forEach(button => {
            button.addEventListener('click', () => {
                button.classList.add('button-click');
                setTimeout(() => {
                    button.classList.remove('button-click');
                }, 200);
            });
        });
    </script>
</body>
</html>
