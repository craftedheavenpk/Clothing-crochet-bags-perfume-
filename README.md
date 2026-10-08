<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aura & Craft | Luxury Boutique, Crochet, Apparel, Bags & Perfumes</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        boutiqueDark: '#1c1917',
                        boutiqueRose: '#e11d48',
                        boutiqueGold: '#d97706',
                    }
                }
            }
        }
    </script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;600;700&family=Plus+Jakarta+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Plus Jakarta Sans', sans-serif; }
        .brand-font { font-family: 'Playfair Display', serif; }
    </style>
</head>
<body class="bg-stone-950 text-stone-100 min-h-screen flex flex-col">

    <!-- Top Announcement Bar -->
    <div class="bg-stone-900 text-amber-200 text-xs py-2 px-4 text-center border-b border-stone-800 tracking-wide font-medium">
        <i class="fa-solid fa-gem mr-2 text-rose-500"></i> Luxury Handmade & Branded Collection | Custom Orders Open | WhatsApp: 03034812714
    </div>

    <!-- Header / Navbar -->
    <header class="sticky top-0 z-40 bg-stone-950/90 backdrop-blur-md border-b border-stone-800 shadow-xl">
        <div class="max-w-7xl mx-auto px-4 py-3.5 flex items-center justify-between">
            
            <!-- Mobile Menu & Logo -->
            <div class="flex items-center space-x-3">
                <button onclick="toggleSideMenu()" class="text-amber-200 text-xl p-1 focus:outline-none md:hidden">
                    <i class="fa-solid fa-bars"></i>
                </button>
                <a href="#" class="flex items-center space-x-2.5">
                    <div class="w-10 h-10 rounded-full bg-gradient-to-tr from-amber-600 to-rose-600 flex items-center justify-center shadow-lg">
                        <i class="fa-solid fa-wand-magic-sparkles text-white text-sm"></i>
                    </div>
                    <div>
                        <span class="text-xl font-bold tracking-wider brand-font text-white block leading-none">Aura & Craft</span>
                        <span class="text-[10px] text-amber-400 tracking-widest uppercase font-semibold">Boutique & Studio</span>
                    </div>
                </a>
            </div>

            <!-- Desktop Nav Links -->
            <nav class="hidden md:flex items-center space-x-6 font-medium text-sm text-stone-300">
                <a href="#home" class="hover:text-amber-400 transition">Home</a>
                <a href="#products" class="hover:text-amber-400 transition">Collections</a>
                <a href="#custom-order" class="hover:text-amber-400 transition">Custom Crochet</a>
                <a href="#about" class="hover:text-amber-400 transition">About</a>
                <a href="#contact" class="hover:text-amber-400 transition">Contact</a>
            </nav>

            <!-- Cart / Bucket Button -->
            <div class="flex items-center space-x-3">
                <button onclick="toggleCart()" class="relative bg-amber-600 hover:bg-amber-500 text-stone-950 font-bold px-4 py-2 rounded-full text-xs sm:text-sm flex items-center shadow-lg transition">
                    <i class="fa-solid fa-bag-shopping mr-2"></i>
                    <span>Bag</span>
                    <span id="cart-count" class="absolute -top-1.5 -right-1.5 bg-rose-600 text-white text-xs w-5 h-5 rounded-full flex items-center justify-center font-bold shadow">0</span>
                </button>
            </div>
        </div>
    </header>

    <!-- Side Menu Drawer for Mobile -->
    <div id="sideMenu" class="fixed inset-0 z-50 bg-black/80 backdrop-blur-sm hidden transition-opacity">
        <div class="bg-stone-900 w-72 h-full p-6 flex flex-col justify-between shadow-2xl border-r border-stone-800 transform -translate-x-full transition-transform duration-300" id="sideMenuPanel">
            <div>
                <div class="flex items-center justify-between mb-8 pb-4 border-b border-stone-800">
                    <div class="flex items-center space-x-2">
                        <div class="w-8 h-8 rounded-full bg-amber-600 flex items-center justify-center">
                            <i class="fa-solid fa-wand-magic-sparkles text-stone-950 text-xs"></i>
                        </div>
                        <span class="font-bold text-lg brand-font text-white">Aura & Craft</span>
                    </div>
                    <button onclick="toggleSideMenu()" class="text-stone-400 hover:text-white text-xl">
                        <i class="fa-solid fa-xmark"></i>
                    </button>
                </div>
                <nav class="flex flex-col space-y-4 font-medium text-sm">
                    <a href="#home" onclick="toggleSideMenu()" class="flex items-center space-x-3 text-stone-300 hover:text-amber-400 py-2 border-b border-stone-800/60"><i class="fa-solid fa-house w-6 text-amber-500"></i> <span>Home</span></a>
                    <a href="#products" onclick="toggleSideMenu()" class="flex items-center space-x-3 text-stone-300 hover:text-amber-400 py-2 border-b border-stone-800/60"><i class="fa-solid fa-shirt w-6 text-amber-500"></i> <span>Collections</span></a>
                    <a href="#custom-order" onclick="toggleSideMenu()" class="flex items-center space-x-3 text-stone-300 hover:text-amber-400 py-2 border-b border-stone-800/60"><i class="fa-solid fa-scissors w-6 text-amber-500"></i> <span>Custom Crochet</span></a>
                    <a href="#about" onclick="toggleSideMenu()" class="flex items-center space-x-3 text-stone-300 hover:text-amber-400 py-2 border-b border-stone-800/60"><i class="fa-solid fa-circle-info w-6 text-amber-500"></i> <span>About Us</span></a>
                    <a href="#contact" onclick="toggleSideMenu()" class="flex items-center space-x-3 text-stone-300 hover:text-amber-400 py-2 border-b border-stone-800/60"><i class="fa-solid fa-phone w-6 text-amber-500"></i> <span>Contact & WhatsApp</span></a>
                </nav>
            </div>
            <div class="text-xs text-stone-500 text-center py-4 border-t border-stone-800">
                <p>© 2026 Aura & Craft Studio</p>
                <p class="mt-1">WhatsApp: 03034812714</p>
            </div>
        </div>
    </div>

    <!-- Hero Section -->
    <section id="home" class="relative bg-gradient-to-r from-stone-950 via-stone-900 to-stone-950 py-16 px-4 text-center border-b border-stone-800 overflow-hidden">
        <div class="max-w-4xl mx-auto relative z-10">
            <span class="inline-block bg-amber-950/60 text-amber-300 text-xs font-semibold px-4 py-1.5 rounded-full mb-4 border border-amber-800/50 tracking-wider">
                <i class="fa-solid fa-star text-amber-400 mr-1.5"></i> Premium Handmade Crochet, Designer Apparel & Luxury Fragrances
            </span>
            <h1 class="text-3xl sm:text-6xl font-extrabold tracking-tight text-white mb-6 brand-font leading-tight">
                Elevate Your Style With <span class="text-transparent bg-clip-text bg-gradient-to-r from-amber-400 via-rose-400 to-amber-200">Exquisite Craftsmanship</span>
            </h1>
            <p class="text-stone-300 text-sm sm:text-base max-w-2xl mx-auto mb-8 leading-relaxed font-light">
                Explore custom-made crochet masterpieces, trendy apparel branding collections, luxury designer handbags, and signature long-lasting perfumes crafted for elegance.
            </p>
            <div class="flex flex-wrap justify-center gap-4">
                <a href="#products" class="bg-amber-600 hover:bg-amber-500 text-stone-950 font-bold px-6 py-3.5 rounded-xl shadow-lg transition flex items-center text-sm">
                    <i class="fa-solid fa-bag-shopping mr-2"></i> Explore Collections
                </a>
                <a href="#custom-order" class="bg-stone-900 hover:bg-stone-800 text-amber-300 border border-amber-600/50 font-semibold px-6 py-3.5 rounded-xl transition flex items-center text-sm">
                    <i class="fa-solid fa-wand-magic mr-2 text-rose-500"></i> Request Custom Crochet
                </a>
            </div>
        </div>
    </section>

    <!-- Main Products & Catalog Section -->
    <section id="products" class="max-w-7xl mx-auto px-4 py-12 flex-grow w-full">
        
        <!-- Section Header & Controls -->
        <div class="flex flex-col md:flex-row md:items-center justify-between gap-4 mb-8 bg-stone-900/60 p-5 rounded-2xl border border-stone-800">
            <div>
                <h2 class="text-2xl font-bold text-white brand-font">Curated Collections</h2>
                <p class="text-xs text-stone-400 mt-1">Select items with live preview, add to bag, and order seamlessly via WhatsApp.</p>
            </div>

            <!-- Search & Sort -->
            <div class="flex flex-wrap items-center gap-3">
                <div class="relative flex-grow sm:flex-grow-0">
                    <input type="text" id="searchInput" oninput="filterProducts()" placeholder="Search collection..." class="bg-stone-950 border border-stone-800 text-sm text-stone-200 rounded-xl px-4 py-2.5 pl-9 focus:outline-none focus:border-amber-500 w-full sm:w-56">
                    <i class="fa-solid fa-magnifying-glass absolute left-3 top-3.5 text-stone-500 text-xs"></i>
                </div>
                <select id="sortSelect" onchange="filterProducts()" class="bg-stone-950 border border-stone-800 text-sm text-stone-200 rounded-xl px-4 py-2.5 focus:outline-none focus:border-amber-500">
                    <option value="default">Sort by: Featured</option>
                    <option value="low-high">Price: Low to High</option>
                    <option value="high-low">Price: High to Low</option>
                    <option value="name">Name: A to Z</option>
                </select>
            </div>
        </div>

        <!-- Category Filter Pills -->
        <div class="flex items-center gap-2.5 overflow-x-auto pb-4 mb-8 no-scrollbar">
            <button onclick="setCategory('All')" class="cat-btn active-cat bg-amber-600 text-stone-950 font-bold px-5 py-2.5 rounded-xl text-xs whitespace-nowrap transition shadow">All Collections</button>
            <button onclick="setCategory('Crochet')" class="cat-btn bg-stone-900 text-stone-300 hover:bg-stone-800 px-5 py-2.5 rounded-xl text-xs font-semibold whitespace-nowrap transition border border-stone-800">Crochet Art</button>
            <button onclick="setCategory('Apparel')" class="cat-btn bg-stone-900 text-stone-300 hover:bg-stone-800 px-5 py-2.5 rounded-xl text-xs font-semibold whitespace-nowrap transition border border-stone-800">Apparel & Branding</button>
            <button onclick="setCategory('Bags')" class="cat-btn bg-stone-900 text-stone-300 hover:bg-stone-800 px-5 py-2.5 rounded-xl text-xs font-semibold whitespace-nowrap transition border border-stone-800">Luxury Bags</button>
            <button onclick="setCategory('Perfumes')" class="cat-btn bg-stone-900 text-stone-300 hover:bg-stone-800 px-5 py-2.5 rounded-xl text-xs font-semibold whitespace-nowrap transition border border-stone-800">Signature Perfumes</button>
        </div>

        <!-- Products Grid: STRICTLY 2 per row on mobile, up to 4 on desktop -->
        <div id="products-grid" class="grid grid-cols-2 lg:grid-cols-4 gap-4 sm:gap-6">
            <!-- Dynamically populated via JS -->
        </div>
    </section>

    <!-- Custom Crochet Order Section -->
    <section id="custom-order" class="bg-gradient-to-br from-stone-900 via-stone-950 to-amber-950/30 border-t border-b border-stone-800 py-16 px-4 my-10">
        <div class="max-w-3xl mx-auto bg-stone-900/80 p-6 sm:p-10 rounded-3xl border border-stone-800 shadow-2xl">
            <div class="text-center mb-8">
                <span class="bg-rose-950 text-rose-300 text-xs font-semibold px-3.5 py-1 rounded-full border border-rose-800/50">Made Just For You</span>
                <h2 class="text-2xl sm:text-3xl font-bold text-white mt-3 brand-font">Custom Crochet Order Request</h2>
                <p class="text-xs sm:text-sm text-stone-400 mt-2">Have a specific design, plushie, shawl, or outfit in mind? Send us your customization details directly.</p>
            </div>
            
            <form onsubmit="submitCustomOrder(event)" class="space-y-4">
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                    <div>
                        <label class="block text-xs font-semibold text-stone-300 mb-1">Your Name</label>
                        <input type="text" id="custName" required placeholder="Ayesha Khan" class="w-full bg-stone-950 border border-stone-800 text-sm text-stone-200 rounded-xl px-4 py-3 focus:outline-none focus:border-amber-500">
                    </div>
                    <div>
                        <label class="block text-xs font-semibold text-stone-300 mb-1">Phone / WhatsApp Number</label>
                        <input type="text" id="custPhone" required placeholder="0300-1234567" class="w-full bg-stone-950 border border-stone-800 text-sm text-stone-200 rounded-xl px-4 py-3 focus:outline-none focus:border-amber-500">
                    </div>
                </div>
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                    <div>
                        <label class="block text-xs font-semibold text-stone-300 mb-1">Item Type</label>
                        <select id="custType" class="w-full bg-stone-950 border border-stone-800 text-sm text-stone-200 rounded-xl px-4 py-3 focus:outline-none focus:border-amber-500">
                            <option value="Crochet Top / Cardigan">Crochet Top / Cardigan</option>
                            <option value="Crochet Bag / Purse">Crochet Bag / Purse</option>
                            <option value="Crochet Plushie / Toy">Crochet Plushie / Toy</option>
                            <option value="Other Custom Design">Other Custom Design</option>
                        </select>
                    </div>
                    <div>
                        <label class="block text-xs font-semibold text-stone-300 mb-1">Preferred Colors / Size</label>
                        <input type="text" id="custDetails" required placeholder="e.g. Pastel Pink, Medium Size" class="w-full bg-stone-950 border border-stone-800 text-sm text-stone-200 rounded-xl px-4 py-3 focus:outline-none focus:border-amber-500">
                    </div>
                </div>
                <button type="submit" class="w-full bg-amber-600 hover:bg-amber-500 text-stone-950 font-bold py-3.5 rounded-xl shadow-lg transition flex items-center justify-center space-x-2 text-sm mt-4">
                    <i class="fa-brands fa-whatsapp text-lg"></i>
                    <span>Send Custom Request via WhatsApp</span>
                </button>
            </form>
        </div>
    </section>

    <!-- About & Contact Section -->
    <section id="about" class="max-w-5xl mx-auto px-4 py-12 text-center">
        <h2 class="text-3xl font-bold text-white mb-4 brand-font">About Aura & Craft</h2>
        <p class="text-stone-300 text-sm sm:text-base leading-relaxed max-w-3xl mx-auto mb-8 font-light">
            Aura & Craft is your ultimate multi-brand studio showcasing handcrafted artisanal crochet items, premium apparel branding solutions, luxury designer handbags, and mesmerizing signature perfumes. Whether you want ready-to-wear style or a personalized crochet creation, we bring perfection to your doorstep.
        </p>
    </section>

    <section id="contact" class="max-w-4xl mx-auto px-4 py-6 mb-12 w-full text-center">
        <div class="bg-stone-900 p-6 sm:p-8 rounded-3xl border border-stone-800 inline-block w-full max-w-xl text-left shadow-xl">
            <h3 class="font-bold text-lg text-white mb-4 brand-font text-center">Store & Contact Information</h3>
            <div class="space-y-3 text-sm text-stone-300">
                <p><i class="fa-solid fa-location-dot text-amber-500 w-6"></i> <strong>Location:</strong> Main Boulevard, Gulberg III, Lahore</p>
                <p><i class="fa-solid fa-phone text-amber-500 w-6"></i> <strong>WhatsApp Helpline:</strong> 03034812714</p>
                <p><i class="fa-solid fa-credit-card text-amber-500 w-6"></i> <strong>Payment Methods:</strong> JazzCash, EasyPaisa & COD</p>
                <p><i class="fa-solid fa-clock text-amber-500 w-6"></i> <strong>Timings:</strong> 11:00 AM – 9:00 PM (Monday to Saturday)</p>
            </div>
        </div>
    </section>

    <!-- Cart / Bag Drawer Overlay -->
    <div id="cartDrawer" class="fixed inset-0 z-50 bg-black/80 backdrop-blur-sm hidden flex justify-end transition-opacity">
        <div class="bg-stone-900 w-full max-w-md h-full p-5 flex flex-col justify-between shadow-2xl border-l border-stone-800 transform translate-x-full transition-transform duration-300" id="cartPanel">
            <div>
                <div class="flex items-center justify-between pb-4 border-b border-stone-800">
                    <div class="flex items-center space-x-2">
                        <i class="fa-solid fa-bag-shopping text-amber-500 text-lg"></i>
                        <h3 class="font-bold text-lg text-white brand-font">Your Shopping Bag</h3>
                    </div>
                    <button onclick="toggleCart()" class="text-stone-400 hover:text-white text-xl">
                        <i class="fa-solid fa-xmark"></i>
                    </button>
                </div>

                <!-- Cart Items List -->
                <div id="cart-items" class="py-4 space-y-3 overflow-y-auto max-h-[calc(100vh-280px)]">
                    <p class="text-stone-500 text-center py-8 text-sm">Your shopping bag is currently empty.</p>
                </div>
            </div>

            <!-- Cart Footer & Subtotal / WhatsApp Checkout -->
            <div class="pt-4 border-t border-stone-800">
                <div class="flex justify-between items-center mb-4 text-base font-bold text-white">
                    <span>Subtotal:</span>
                    <span id="cart-total" class="text-amber-400">Rs. 0</span>
                </div>
                <button onclick="checkoutWhatsApp()" class="w-full bg-amber-600 hover:bg-amber-500 text-stone-950 font-bold py-3.5 rounded-xl shadow-lg transition flex items-center justify-center space-x-2 text-sm">
                    <i class="fa-brands fa-whatsapp text-lg"></i>
                    <span>Checkout via WhatsApp</span>
                </button>
                <p class="text-[11px] text-stone-500 text-center mt-2">Secure checkout via WhatsApp. JazzCash / EasyPaisa / COD supported (03034812714).</p>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer class="bg-stone-950 border-t border-stone-800 py-8 px-4 text-center text-xs text-stone-500">
        <div class="max-w-7xl mx-auto flex flex-col sm:flex-row items-center justify-between gap-4">
            <div class="flex items-center space-x-2">
                <div class="w-7 h-7 rounded-full bg-amber-600 flex items-center justify-center">
                    <i class="fa-solid fa-wand-magic-sparkles text-stone-950 text-xs"></i>
                </div>
                <span class="font-bold text-white brand-font text-sm">Aura & Craft Studio</span>
            </div>
            <p>© 2026 Aura & Craft Lahore. All rights reserved.</p>
            <div class="flex space-x-4 text-stone-400 text-base">
                <a href="https://wa.me/923034812714" target="_blank" class="hover:text-amber-400"><i class="fa-brands fa-whatsapp"></i></a>
                <a href="#home" class="hover:text-amber-400"><i class="fa-solid fa-arrow-up"></i></a>
            </div>
        </div>
    </footer>

    <!-- JavaScript Application Logic -->
    <script>
        const products = [
            {
                id: 1,
                name: "Handmade Crochet Daisy Cardigan",
                category: "Crochet",
                price: 4500,
                image: "https://images.unsplash.com/photo-1620799140408-edc6dcb6d633?auto=format&fit=crop&w=500&q=80",
                desc: "Hand-stitched floral crochet cardigan worn with cozy aesthetic style. Soft wool yarn."
            },
            {
                id: 2,
                name: "Boho Crochet Summer Tote Bag",
                category: "Crochet",
                price: 2200,
                image: "https://images.unsplash.com/photo-1590874103328-eac38a683ce7?auto=format&fit=crop&w=500&q=80",
                desc: "Intricately woven cotton crochet shoulder bag held by model. Perfect for daily chic look."
            },
            {
                id: 3,
                name: "Designer Velvet Branded Suit",
                category: "Apparel",
                price: 6800,
                image: "https://images.unsplash.com/photo-1515886657613-9f3515b0c78f?auto=format&fit=crop&w=500&q=80",
                desc: "Premium embroidered formal wear apparel worn by model with elegant styling."
            },
            {
                id: 4,
                name: "Luxury Casual Linen Co-ord Set",
                category: "Apparel",
                price: 4999,
                image: "https://images.unsplash.com/photo-1496747611176-843222e1e57c?auto=format&fit=crop&w=500&q=80",
                desc: "Trendy branded clothing piece featuring modern cuts and breathable fabric."
            },
            {
                id: 5,
                name: "Classic Quilted Leather Handbag",
                category: "Bags",
                price: 5500,
                image: "https://images.unsplash.com/photo-1584917865442-de89df76afd3?auto=format&fit=crop&w=500&q=80",
                desc: "Sophisticated luxury leather shoulder bag held in hand, featuring gold chain strap."
            },
            {
                id: 6,
                name: "Minimalist Everyday Tote Bag",
                category: "Bags",
                price: 3400,
                image: "https://images.unsplash.com/photo-1544816155-12df9643f363?auto=format&fit=crop&w=500&q=80",
                desc: "Spacious premium leather bag designed for office and college styling."
            },
            {
                id: 7,
                name: "Royal Oud Signature Perfume (100ml)",
                category: "Perfumes",
                price: 4200,
                image: "https://images.unsplash.com/photo-1523293182086-7651a899d37f?auto=format&fit=crop&w=500&q=80",
                desc: "Long-lasting rich oriental fragrance with wood and amber notes. Spray bottle elegance."
            },
            {
                id: 8,
                name: "Velvet Rose Luxury Eau de Parfum",
                category: "Perfumes",
                price: 3800,
                image: "https://images.unsplash.com/photo-1594035910387-fea47794261f?auto=format&fit=crop&w=500&q=80",
                desc: "Enchanting floral and warm vanilla blend perfume bottle placed on display."
            }
        ];

        let cart = [];
        let currentCategory = 'All';

        function renderProducts() {
            const grid = document.getElementById('products-grid');
            const searchVal = document.getElementById('searchInput').value.toLowerCase();
            const sortVal = document.getElementById('sortSelect').value;

            let filtered = products.filter(p => {
                let matchesCat = currentCategory === 'All' || p.category === currentCategory;
                let matchesSearch = p.name.toLowerCase().includes(searchVal) || p.desc.toLowerCase().includes(searchVal);
                return matchesCat && matchesSearch;
            });

            if (sortVal === 'low-high') {
                filtered.sort((a, b) => a.price - b.price);
            } else if (sortVal === 'high-low') {
                filtered.sort((a, b) => b.price - a.price);
            } else if (sortVal === 'name') {
                filtered.sort((a, b) => a.name.localeCompare(b.name));
            }

            if (filtered.length === 0) {
                grid.innerHTML = `<div class="col-span-2 lg:col-span-4 text-center py-12 text-stone-500"><p>No items found matching your criteria.</p></div>`;
                return;
            }

            grid.innerHTML = filtered.map(p => `
                <div class="bg-stone-900 rounded-2xl border border-stone-800 overflow-hidden flex flex-col justify-between shadow-md hover:border-amber-500/50 transition">
                    <div>
                        <div class="relative h-44 sm:h-56 overflow-hidden bg-stone-950">
                            <img src="${p.image}" alt="${p.name}" class="w-full h-full object-cover hover:scale-105 transition duration-300">
                            <span class="absolute top-2 left-2 bg-stone-950/90 text-amber-300 text-[10px] font-semibold px-2.5 py-1 rounded-full border border-amber-800/60">${p.category}</span>
                        </div>
                        <div class="p-3 sm:p-4">
                            <h3 class="font-bold text-sm sm:text-base text-white mb-1 line-clamp-1">${p.name}</h3>
                            <p class="text-xs text-stone-300 line-clamp-2 mb-3 leading-relaxed font-light">${p.desc}</p>
                        </div>
                    </div>
                    <div class="p-3 sm:p-4 pt-0 flex items-center justify-between border-t border-stone-800/80 mt-auto">
                        <span class="font-bold text-amber-400 text-sm sm:text-base">Rs. ${p.price.toLocaleString()}</span>
                        <button onclick="addToCart(${p.id})" class="bg-amber-600 hover:bg-amber-500 text-stone-950 text-xs font-bold px-3.5 py-2 rounded-xl transition flex items-center shadow">
                            <i class="fa-solid fa-plus mr-1"></i> Add
                        </button>
                    </div>
                </div>
            `).join('');
        }

        function setCategory(cat) {
            currentCategory = cat;
            document.querySelectorAll('.cat-btn').forEach(btn => {
                if (btn.innerText.includes(cat) || (cat === 'All' && btn.innerText.includes('All'))) {
                    btn.className = "cat-btn active-cat bg-amber-600 text-stone-950 font-bold px-5 py-2.5 rounded-xl text-xs whitespace-nowrap transition shadow";
                } else {
                    btn.className = "cat-btn bg-stone-900 text-stone-300 hover:bg-stone-800 px-5 py-2.5 rounded-xl text-xs font-semibold whitespace-nowrap transition border border-stone-800";
                }
            });
            renderProducts();
        }

        function filterProducts() {
            renderProducts();
        }

        function toggleSideMenu() {
            const menu = document.getElementById('sideMenu');
            const panel = document.getElementById('sideMenuPanel');
            if (menu.classList.contains('hidden')) {
                menu.classList.remove('hidden');
                setTimeout(() => panel.classList.remove('-translate-x-full'), 10);
            } else {
                panel.classList.add('-translate-x-full');
                setTimeout(() => menu.classList.add('hidden'), 300);
            }
        }

        function toggleCart() {
            const drawer = document.getElementById('cartDrawer');
            const panel = document.getElementById('cartPanel');
            if (drawer.classList.contains('hidden')) {
                drawer.classList.remove('hidden');
                setTimeout(() => panel.classList.remove('translate-x-full'), 10);
            } else {
                panel.classList.add('translate-x-full');
                setTimeout(() => drawer.classList.add('hidden'), 300);
            }
        }

        function addToCart(id) {
            const product = products.find(p => p.id === id);
            const existing = cart.find(item => item.id === id);
            if (existing) {
                existing.qty++;
            } else {
                cart.push({ ...product, qty: 1 });
            }
            updateCartUI();
            toggleCart();
        }

        function changeQty(id, delta) {
            const item = cart.find(i => i.id === id);
            if (item) {
                item.qty += delta;
                if (item.qty <= 0) {
                    cart = cart.filter(i => i.id !== id);
                }
            }
            updateCartUI();
        }

        function updateCartUI() {
            const countEl = document.getElementById('cart-count');
            const itemsEl = document.getElementById('cart-items');
            const totalEl = document.getElementById('cart-total');

            const totalCount = cart.reduce((sum, item) => sum + item.qty, 0);
            countEl.innerText = totalCount;

            if (cart.length === 0) {
                itemsEl.innerHTML = `<p class="text-stone-500 text-center py-8 text-sm">Your shopping bag is currently empty.</p>`;
                totalEl.innerText = "Rs. 0";
                return;
            }

            let totalPrice = 0;
            itemsEl.innerHTML = cart.map(item => {
                totalPrice += item.price * item.qty;
                return `
                    <div class="flex items-center justify-between bg-stone-950 p-3 rounded-xl border border-stone-800 text-sm">
                        <div class="flex-grow pr-2">
                            <h4 class="font-semibold text-white text-xs line-clamp-1">${item.name}</h4>
                            <p class="text-amber-400 text-xs">Rs. ${item.price.toLocaleString()} x ${item.qty}</p>
                        </div>
                        <div class="flex items-center space-x-2">
                            <button onclick="changeQty(${item.id}, -1)" class="bg-stone-800 text-white w-6 h-6 rounded-lg flex items-center justify-center hover:bg-stone-700">-</button>
                            <span class="text-xs font-bold text-white">${item.qty}</span>
                            <button onclick="changeQty(${item.id}, 1)" class="bg-stone-800 text-white w-6 h-6 rounded-lg flex items-center justify-center hover:bg-stone-700">+</button>
                        </div>
                    </div>
                `;
            }).join('');

            totalEl.innerText = `Rs. ${totalPrice.toLocaleString()}`;
        }

        function checkoutWhatsApp() {
            if (cart.length === 0) {
                alert("Your shopping bag is empty!");
                return;
            }

            let message = "Hello Aura & Craft, I want to place an order:%0A%0A";
            let total = 0;

            cart.forEach((item, index) => {
                let sub = item.price * item.qty;
                total += sub;
                message += `${index + 1}. ${item.name} (Qty: ${item.qty}) - Rs. ${sub.toLocaleString()}%0A`;
            });

            message += `%0A*Subtotal: Rs. ${total.toLocaleString()}*%0A%0APayment Method: JazzCash / EasyPaisa / Cash on Delivery%0ADelivery Address: [Please provide your address here]`;

            const whatsappUrl = `https://wa.me/923034812714?text=${message}`;
            window.open(whatsappUrl, '_blank');
        }

        function submitCustomOrder(e) {
            e.preventDefault();
            const name = document.getElementById('custName').value;
            const phone = document.getElementById('custPhone').value;
            const type = document.getElementById('custType').value;
            const details = document.getElementById('custDetails').value;

            let message = `Hello Aura & Craft, I want to place a *Custom Crochet Order*:%0A%0A*Name:* ${name}%0A*Phone:* ${phone}%0A*Item Type:* ${type}%0A*Details / Colors:* ${details}%0A%0APlease confirm availability and pricing.`;

            const whatsappUrl = `https://wa.me/923034812714?text=${message}`;
            window.open(whatsappUrl, '_blank');
        }

        window.onload = renderProducts;
    </script>
</body>
</html>
