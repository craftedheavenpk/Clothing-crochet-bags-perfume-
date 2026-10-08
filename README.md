<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aura & Craft | Luxury Boutique Studio</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        body { font-family: 'Plus Jakarta Sans', sans-serif; }
        .no-scrollbar::-webkit-scrollbar { display: none; }
        .no-scrollbar { -ms-overflow-style: none; scrollbar-width: none; }
    </style>
</head>
<body class="bg-stone-950 text-stone-100 min-h-screen flex flex-col">

    <!-- Top Bar -->
    <div class="bg-stone-900 text-amber-200 text-xs py-2 px-3 text-center border-b border-stone-800 font-medium">
        <i class="fa-solid fa-gem text-rose-500 mr-1"></i> Custom Crochet & Luxury Boutique | WhatsApp: 03034812714
    </div>

    <!-- Header -->
    <header class="sticky top-0 z-40 bg-stone-950/95 backdrop-blur border-b border-stone-800">
        <div class="max-w-md mx-auto px-4 py-3 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <button onclick="toggleSideMenu()" class="text-amber-300 text-lg p-1">
                    <i class="fa-solid fa-bars"></i>
                </button>
                <span class="font-bold text-base text-white tracking-wide">Aura & Craft</span>
            </div>
            <button onclick="toggleCart()" class="relative bg-amber-600 text-stone-950 px-3.5 py-1.5 rounded-full text-xs font-bold flex items-center shadow">
                <i class="fa-solid fa-bag-shopping mr-1"></i> Bag
                <span id="cart-count" class="absolute -top-1 -right-1 bg-rose-600 text-white text-[10px] w-4 h-4 rounded-full flex items-center justify-center font-bold">0</span>
            </button>
        </div>
    </header>

    <!-- Side Menu -->
    <div id="sideMenu" class="fixed inset-0 z-50 bg-black/80 hidden">
        <div class="bg-stone-900 w-72 h-full p-5 flex flex-col justify-between border-r border-stone-800">
            <div>
                <div class="flex justify-between items-center mb-6 pb-3 border-b border-stone-800">
                    <span class="font-bold text-white text-base">Menu</span>
                    <button onclick="toggleSideMenu()" class="text-stone-400 text-lg"><i class="fa-solid fa-xmark"></i></button>
                </div>
                <nav class="space-y-4 text-sm font-medium">
                    <a href="#products" onclick="toggleSideMenu()" class="block text-stone-300 hover:text-amber-400">Collections</a>
                    <a href="#custom-order" onclick="toggleSideMenu()" class="block text-stone-300 hover:text-amber-400">Custom Crochet Order</a>
                    <a href="#contact" onclick="toggleSideMenu()" class="block text-stone-300 hover:text-amber-400">Store Info & WhatsApp</a>
                </nav>
            </div>
            <div class="text-xs text-stone-500 text-center py-3 border-t border-stone-800">
                WhatsApp: 03034812714
            </div>
        </div>
    </div>

    <!-- Main Content -->
    <main class="max-w-md mx-auto px-3 py-4 flex-grow w-full space-y-6">

        <!-- Hero Banner -->
        <div class="bg-gradient-to-r from-stone-900 to-stone-950 p-5 rounded-2xl border border-stone-800 text-center">
            <h1 class="text-xl font-bold text-white mb-2">Handmade Luxury & Apparel</h1>
            <p class="text-xs text-stone-300 mb-4">Explore custom crochet, branded clothing, luxury bags & perfumes.</p>
            <a href="#custom-order" class="inline-block bg-amber-600 text-stone-950 text-xs font-bold px-4 py-2 rounded-xl shadow">
                Request Custom Crochet
            </a>
        </div>

        <!-- Filter Categories -->
        <div class="flex items-center gap-2 overflow-x-auto pb-2 no-scrollbar">
            <button onclick="setCategory('All')" class="cat-btn bg-amber-600 text-stone-950 px-3 py-1.5 rounded-xl text-xs font-bold whitespace-nowrap">All</button>
            <button onclick="setCategory('Crochet')" class="cat-btn bg-stone-900 text-stone-300 border border-stone-800 px-3 py-1.5 rounded-xl text-xs font-medium whitespace-nowrap">Crochet</button>
            <button onclick="setCategory('Apparel')" class="cat-btn bg-stone-900 text-stone-300 border border-stone-800 px-3 py-1.5 rounded-xl text-xs font-medium whitespace-nowrap">Apparel</button>
            <button onclick="setCategory('Bags')" class="cat-btn bg-stone-900 text-stone-300 border border-stone-800 px-3 py-1.5 rounded-xl text-xs font-medium whitespace-nowrap">Bags</button>
            <button onclick="setCategory('Perfumes')" class="cat-btn bg-stone-900 text-stone-300 border border-stone-800 px-3 py-1.5 rounded-xl text-xs font-medium whitespace-nowrap">Perfumes</button>
        </div>

        <!-- Products Grid -->
        <div id="products-grid" class="grid grid-cols-2 gap-3">
            <!-- JS Populated -->
        </div>

        <!-- Custom Crochet Order Section -->
        <section id="custom-order" class="bg-stone-900 p-4 rounded-2xl border border-stone-800">
            <h2 class="text-base font-bold text-white mb-1">Custom Crochet Order</h2>
            <p class="text-[11px] text-stone-400 mb-3">Specify your custom design, color, and sizing.</p>
            <form onsubmit="submitCustomOrder(event)" class="space-y-3">
                <input type="text" id="custName" required placeholder="Your Name" class="w-full bg-stone-950 border border-stone-800 text-xs text-stone-200 rounded-xl px-3 py-2.5 focus:outline-none focus:border-amber-500">
                <input type="text" id="custPhone" required placeholder="WhatsApp Number (e.g. 03001234567)" class="w-full bg-stone-950 border border-stone-800 text-xs text-stone-200 rounded-xl px-3 py-2.5 focus:outline-none focus:border-amber-500">
                <select id="custType" class="w-full bg-stone-950 border border-stone-800 text-xs text-stone-200 rounded-xl px-3 py-2.5 focus:outline-none focus:border-amber-500">
                    <option value="Crochet Top / Wear">Crochet Top / Wear</option>
                    <option value="Crochet Bag">Crochet Bag</option>
                    <option value="Crochet Plushie">Crochet Plushie</option>
                </select>
                <input type="text" id="custDetails" required placeholder="Colors & Size details..." class="w-full bg-stone-950 border border-stone-800 text-xs text-stone-200 rounded-xl px-3 py-2.5 focus:outline-none focus:border-amber-500">
                <button type="submit" class="w-full bg-amber-600 text-stone-950 text-xs font-bold py-2.5 rounded-xl shadow">
                    Send Custom Request via WhatsApp
                </button>
            </form>
        </section>

        <!-- Store & Contact Info -->
        <section id="contact" class="bg-stone-900 p-4 rounded-2xl border border-stone-800 text-xs space-y-2 text-stone-300">
            <p><i class="fa-solid fa-location-dot text-amber-500 mr-2"></i> Gulberg III, Lahore</p>
            <p><i class="fa-solid fa-phone text-amber-500 mr-2"></i> WhatsApp: 03034812714</p>
            <p><i class="fa-solid fa-credit-card text-amber-500 mr-2"></i> JazzCash / EasyPaisa / COD</p>
        </section>

    </main>

    <!-- Cart Drawer -->
    <div id="cartDrawer" class="fixed inset-0 z-50 bg-black/80 hidden flex justify-end">
        <div class="bg-stone-900 w-full max-w-xs h-full p-4 flex flex-col justify-between border-l border-stone-800">
            <div>
                <div class="flex justify-between items-center pb-3 border-b border-stone-800">
                    <span class="font-bold text-white text-sm">Shopping Bag</span>
                    <button onclick="toggleCart()" class="text-stone-400 text-lg"><i class="fa-solid fa-xmark"></i></button>
                </div>
                <!-- Cart Items Container -->
                <div id="cart-items" class="py-3 space-y-2.5 overflow-y-auto max-h-[60vh]">
                    <p class="text-stone-500 text-center text-xs py-4">Your bag is empty.</p>
                </div>
            </div>
            <div class="pt-3 border-t border-stone-800">
                <div class="flex justify-between items-center mb-3 text-sm font-bold text-white">
                    <span>Subtotal:</span>
                    <span id="cart-total" class="text-amber-400">Rs. 0</span>
                </div>
                <button onclick="checkoutWhatsApp()" class="w-full bg-amber-600 text-stone-950 text-xs font-bold py-3 rounded-xl shadow">
                    Checkout via WhatsApp
                </button>
            </div>
        </div>
    </div>

    <!-- Footer -->
    <footer class="bg-stone-950 border-t border-stone-800 py-4 px-3 text-center text-[10px] text-stone-500">
        <p>© 2026 Aura & Craft Studio, Lahore</p>
    </footer>

    <!-- Script -->
    <script>
        const products = [
            { id: 1, name: "Daisy Crochet Cardigan", category: "Crochet", price: 4500, image: "https://images.unsplash.com/photo-1620799140408-edc6dcb6d633?auto=format&fit=crop&w=400&q=80", desc: "Hand-stitched floral crochet top." },
            { id: 2, name: "Boho Crochet Tote Bag", category: "Crochet", price: 2200, image: "https://images.unsplash.com/photo-1590874103328-eac38a683ce7?auto=format&fit=crop&w=400&q=80", desc: "Woven cotton shoulder bag." },
            { id: 3, name: "Designer Velvet Suit", category: "Apparel", price: 6800, image: "https://images.unsplash.com/photo-1515886657613-9f3515b0c78f?auto=format&fit=crop&w=400&q=80", desc: "Embroidered formal wear apparel." },
            { id: 4, name: "Casual Linen Co-ord", category: "Apparel", price: 4999, image: "https://images.unsplash.com/photo-1496747611176-843222e1e57c?auto=format&fit=crop&w=400&q=80", desc: "Trendy branded clothing." },
            { id: 5, name: "Quilted Leather Bag", category: "Bags", price: 5500, image: "https://images.unsplash.com/photo-1584917865442-de89df76afd3?auto=format&fit=crop&w=400&q=80", desc: "Luxury shoulder bag." },
            { id: 6, name: "Minimalist Tote Bag", category: "Bags", price: 3400, image: "https://images.unsplash.com/photo-1544816155-12df9643f363?auto=format&fit=crop&w=400&q=80", desc: "Spacious everyday bag." },
            { id: 7, name: "Royal Oud Perfume", category: "Perfumes", price: 4200, image: "https://images.unsplash.com/photo-1523293182086-7651a899d37f?auto=format&fit=crop&w=400&q=80", desc: "Long-lasting oriental fragrance." },
            { id: 8, name: "Velvet Rose Parfum", category: "Perfumes", price: 3800, image: "https://images.unsplash.com/photo-1594035910387-fea47794261f?auto=format&fit=crop&w=400&q=80", desc: "Floral and warm vanilla blend." }
        ];

        let cart = [];
        let currentCategory = 'All';

        function renderProducts() {
            const grid = document.getElementById('products-grid');
            let filtered = currentCategory === 'All' ? products : products.filter(p => p.category === currentCategory);

            grid.innerHTML = filtered.map(p => `
                <div class="bg-stone-900 rounded-xl border border-stone-800 overflow-hidden flex flex-col justify-between">
                    <div>
                        <div class="h-32 bg-stone-950 relative overflow-hidden">
                            <img src="${p.image}" alt="${p.name}" class="w-full h-full object-cover">
                        </div>
                        <div class="p-2.5">
                            <h3 class="font-bold text-xs text-white line-clamp-1 mb-1">${p.name}</h3>
                            <p class="text-[10px] text-stone-400 line-clamp-1 mb-2">${p.desc}</p>
                        </div>
                    </div>
                    <div class="p-2.5 pt-0 flex items-center justify-between border-t border-stone-800">
                        <span class="font-bold text-amber-400 text-xs">Rs. ${p.price.toLocaleString()}</span>
                        <button onclick="addToCart(${p.id})" class="bg-amber-600 text-stone-950 text-[10px] font-bold px-2.5 py-1.5 rounded-lg shadow">
                            + Add
                        </button>
                    </div>
                </div>
            `).join('');
        }

        function setCategory(cat) {
            currentCategory = cat;
            document.querySelectorAll('.cat-btn').forEach(btn => {
                if (btn.innerText.toLowerCase() === cat.toLowerCase()) {
                    btn.className = "cat-btn bg-amber-600 text-stone-950 px-3 py-1.5 rounded-xl text-xs font-bold whitespace-nowrap";
                } else {
                    btn.className = "cat-btn bg-stone-900 text-stone-300 border border-stone-800 px-3 py-1.5 rounded-xl text-xs font-medium whitespace-nowrap";
                }
            });
            renderProducts();
        }

        function toggleSideMenu() {
            document.getElementById('sideMenu').classList.toggle('hidden');
        }

        function toggleCart() {
            document.getElementById('cartDrawer').classList.toggle('hidden');
        }

        function addToCart(id) {
            const prod = products.find(p => p.id === id);
            const exist = cart.find(item => item.id === id);
            if (exist) { 
                exist.qty++; 
            } else { 
                cart.push({ ...prod, qty: 1 }); 
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
            const totalCount = cart.reduce((s, i) => s + i.qty, 0);
            document.getElementById('cart-count').innerText = totalCount;
            const container = document.getElementById('cart-items');
            
            if (cart.length === 0) {
                container.innerHTML = `<p class="text-stone-500 text-center text-xs py-4">Your bag is empty.</p>`;
                document.getElementById('cart-total').innerText = "Rs. 0";
                return;
            }

            let total = 0;
            container.innerHTML = cart.map(item => {
                let sub = item.price * item.qty;
                total += sub;
                return `
                    <div class="flex items-center justify-between bg-stone-950 p-2 rounded-xl border border-stone-800 text-xs">
                        <div class="flex items-center space-x-2.5 overflow-hidden">
                            <img src="${item.image}" alt="${item.name}" class="w-10 h-10 object-cover rounded-lg flex-shrink-0">
                            <div class="overflow-hidden">
                                <h4 class="font-bold text-white text-[11px] truncate">${item.name}</h4>
                                <p class="text-amber-400 text-[10px]">Rs. ${item.price} × ${item.qty}</p>
                            </div>
                        </div>
                        <div class="flex items-center space-x-1 flex-shrink-0">
                            <button onclick="changeQty(${item.id}, -1)" class="bg-stone-800 w-5 h-5 rounded text-white font-bold flex items-center justify-center">-</button>
                            <span class="text-white font-bold text-xs px-1">${item.qty}</span>
                            <button onclick="changeQty(${item.id}, 1)" class="bg-stone-800 w-5 h-5 rounded text-white font-bold flex items-center justify-center">+</button>
                        </div>
                    </div>
                `;
            }).join('');

            document.getElementById('cart-total').innerText = `Rs. ${total.toLocaleString()}`;
        }

        function checkoutWhatsApp() {
            if (cart.length === 0) { 
                alert("Your bag is empty!"); 
                return; 
            }
            
            let msg = "Hello Aura & Craft, I want to place an order:\n\n";
            let total = 0;
            
            cart.forEach((item, idx) => {
                let sub = item.price * item.qty;
                total += sub;
                msg += `${idx + 1}. ${item.name} (Qty: ${item.qty}) - Rs. ${sub}\n`;
            });
            
            msg += `\nTotal Bill: Rs. ${total.toLocaleString()}\nPayment: JazzCash / EasyPaisa / COD`;
            
            const encodedMsg = encodeURIComponent(msg);
            window.open(`https://wa.me/923034812714?text=${encodedMsg}`, '_blank');
        }

        function submitCustomOrder(e) {
            e.preventDefault();
            let name = document.getElementById('custName').value;
            let phone = document.getElementById('custPhone').value;
            let type = document.getElementById('custType').value;
            let details = document.getElementById('custDetails').value;
            
            let msg = `Hello Aura & Craft, Custom Crochet Order:\n\nName: ${name}\nPhone: ${phone}\nType: ${type}\nDetails: ${details}`;
            
            const encodedMsg = encodeURIComponent(msg);
            window.open(`https://wa.me/923034812714?text=${encodedMsg}`, '_blank');
        }

        window.onload = renderProducts;
    </script>
</body>
</html>
