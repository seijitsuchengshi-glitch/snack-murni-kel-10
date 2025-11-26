<html lang="id" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Snack Murni - Group 10 (XII-H)</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Nunito:wght@400;600;700;800&family=Playfair+Display:wght@700;800&display=swap" rel="stylesheet">
    
    <!-- Ionicons -->
    <script type="module" src="https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.esm.js"></script>
    <script nomodule src="https://unpkg.com/ionicons@7.1.0/dist/ionicons/ionicons.js"></script>

    <!-- Config -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        'brand-cream': '#F8F4E3', 
                        'brand-brown': '#A0522D', 
                        'brand-dark': '#3C2A21', 
                        'brand-gray': '#D3D3D3', 
                        'brand-white': '#FFFFFF',
                    },
                    fontFamily: {
                        sans: ['Nunito', 'sans-serif'],
                        display: ['"Playfair Display"', 'serif'],
                    },
                    animation: {
                        'bounce-slow': 'bounce 3s infinite',
                    }
                }
            }
        }
    </script>
    
    <style>
        /* Custom Scrollbar */
        ::-webkit-scrollbar { width: 10px; }
        ::-webkit-scrollbar-track { background: #F8F4E3; }
        ::-webkit-scrollbar-thumb { background: #A0522D; border-radius: 5px; }
        ::-webkit-scrollbar-thumb:hover { background: #3C2A21; }
        
        body {
            background-image: radial-gradient(circle, rgba(60, 42, 33, 0.05) 1px, transparent 1px);
            background-size: 20px 20px;
        }
        .font-display { font-family: 'Playfair Display', serif; }
        
        /* Cart Badge Animation */
        @keyframes pop {
            0% { transform: scale(1); }
            50% { transform: scale(1.5); }
            100% { transform: scale(1); }
        }
        .animate-pop { animation: pop 0.3s ease-in-out; }
    </style>
</head>
<body class="bg-brand-cream text-brand-dark antialiased relative">

    <!-- ===== HEADER & NAVIGASI ===== -->
    <header class="sticky top-0 z-50 bg-brand-white/95 backdrop-blur-sm shadow-md transition-all duration-300">
        <nav class="container mx-auto px-6 py-4 flex justify-between items-center">
            <!-- Logo -->
            <a href="#beranda" class="text-2xl md:text-3xl font-bold font-display text-brand-brown hover:text-brand-dark transition flex flex-col">
                <span>Snack Murni</span>
                <span class="text-xs font-sans text-gray-500 -mt-1">Group 10 (XII-H)</span>
            </a>
            
            <!-- Menu Desktop -->
            <div class="hidden md:flex space-x-8 items-center font-semibold">
                <a href="#beranda" class="hover:text-brand-brown transition">Beranda</a>
                <a href="#tentang" class="hover:text-brand-brown transition">Tentang</a>
                <a href="#produk" class="hover:text-brand-brown transition">Produk</a>
                <a href="#pesan" class="hover:text-brand-brown transition">Pesan</a>
                
                <!-- Cart Icon Desktop -->
                <button onclick="toggleCart()" class="relative p-2 text-2xl hover:text-brand-brown transition">
                    <ion-icon name="cart-outline"></ion-icon>
                    <span id="cart-badge-desktop" class="absolute top-0 right-0 bg-red-500 text-white text-[10px] font-bold px-1.5 py-0.5 rounded-full hidden">0</span>
                </button>
            </div>
            
            <!-- Mobile Controls -->
            <div class="flex items-center space-x-4 md:hidden">
                <!-- Cart Icon Mobile -->
                <button onclick="toggleCart()" class="relative text-2xl text-brand-dark focus:outline-none">
                    <ion-icon name="cart-outline"></ion-icon>
                    <span id="cart-badge-mobile" class="absolute -top-1 -right-1 bg-red-500 text-white text-[10px] font-bold px-1.5 py-0.5 rounded-full hidden">0</span>
                </button>
                <!-- Menu Button -->
                <button id="menu-button" class="text-3xl text-brand-dark focus:outline-none">
                    <ion-icon name="menu-outline"></ion-icon>
                </button>
            </div>
        </nav>
        
        <!-- Menu Mobile -->
        <div id="mobile-menu" class="hidden md:hidden bg-brand-white shadow-lg absolute w-full border-t border-gray-100">
            <a href="#beranda" class="mobile-link block px-6 py-3 hover:bg-brand-cream font-medium">Beranda</a>
            <a href="#tentang" class="mobile-link block px-6 py-3 hover:bg-brand-cream font-medium">Tentang Kami</a>
            <a href="#produk" class="mobile-link block px-6 py-3 hover:bg-brand-cream font-medium">Produk</a>
            <a href="#pesan" class="mobile-link block px-6 py-3 hover:bg-brand-cream font-medium">Pesan</a>
        </div>
    </header>

    <!-- ===== 1. BERANDA ===== -->
    <section id="beranda" class="min-h-screen flex items-center justify-center bg-cover bg-center relative -mt-20 pt-20" style="background-image: url('https://images.unsplash.com/photo-1599490659213-e2b9527bd087?q=80&w=2070&auto=format&fit=crop')">
        <div class="absolute inset-0 bg-gradient-to-b from-brand-black/70 to-brand-brown/60"></div>
        
        <div class="container mx-auto px-6 text-center text-brand-white relative z-10">
            <span class="inline-block py-1 px-3 rounded-full bg-brand-brown/80 text-xs font-bold tracking-wider mb-4 border border-white/20">SMAN 1 DRAMAGA</span>
            <h1 class="text-5xl md:text-7xl font-bold font-display leading-tight mb-4 drop-shadow-lg">
                SNACK MURNI
            </h1>
            <p class="text-xl md:text-2xl mb-8 max-w-2xl mx-auto font-light italic">
                "Renyahnya Asli, Harganya Bikin Hepi!"
            </p>
            <div class="flex flex-col sm:flex-row justify-center gap-4">
                <a href="#produk" class="bg-brand-brown text-brand-white font-bold text-lg px-8 py-4 rounded-full shadow-xl hover:bg-brand-dark hover:scale-105 transition duration-300">
                    Lihat Menu
                </a>
                <a href="#tentang" class="bg-transparent border-2 border-brand-white text-brand-white font-bold text-lg px-8 py-4 rounded-full hover:bg-brand-white hover:text-brand-brown transition duration-300">
                    Tim Kami
                </a>
            </div>
        </div>
    </section>

    <!-- ===== 2. TENTANG KAMI & TIM (UPDATED) ===== -->
    <section id="tentang" class="py-20 bg-brand-white">
        <div class="container mx-auto px-6">
            <!-- Bagian Cerita -->
            <div class="grid md:grid-cols-2 gap-12 items-center mb-16">
                <div class="relative order-2 md:order-1">
                    <div class="absolute -inset-4 bg-brand-brown/20 rounded-3xl transform -rotate-2"></div>
                    <img src="https://images.unsplash.com/photo-1529333166437-7750a6dd5a70?ixlib=rb-1.2.1&auto=format&fit=crop&w=800&q=80" alt="Tim Snack Murni" class="relative w-full h-64 md:h-80 object-cover rounded-3xl shadow-2xl">
                </div>
                <div class="order-1 md:order-2">
                    <h2 class="text-4xl font-display text-brand-dark mb-4">Tentang Kami</h2>
                    <div class="w-16 h-1 bg-brand-brown mb-6"></div>
                    <p class="text-gray-600 leading-relaxed mb-4">
                        <strong>Snack Murni</strong> lahir dari tugas kewirausahaan kelas XII-H SMAN 1 Dramaga. Kami berdedikasi untuk menyediakan camilan yang tidak hanya enak, tapi juga bersih dan terjangkau untuk kantong pelajar.
                    </p>
                </div>
            </div>

            <!-- Bagian Tim (Group 10 - XII H) -->
            <div class="text-center mb-12">
                <h3 class="text-3xl font-display text-brand-dark mb-2">Meet The Team</h3>
                <p class="text-brand-brown font-bold">Group 10 — Kelas XII-H</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-5xl mx-auto">
                <!-- Anggota 1: Abidah -->
                <div class="bg-brand-cream rounded-2xl p-6 text-center hover:shadow-lg transition transform hover:-translate-y-2 border border-brand-brown/10">
                    <div class="w-24 h-24 mx-auto bg-brand-white rounded-full flex items-center justify-center text-4xl text-brand-brown mb-4 shadow-md overflow-hidden">
                        <!-- Placeholder Avatar -->
                        <img src="https://ui-avatars.com/api/?name=Abidah&background=A0522D&color=fff" alt="Abidah">
                    </div>
                    <h4 class="text-xl font-bold text-brand-dark">Abidah</h4>
                    <p class="text-sm text-gray-500">XII-H</p>
                    <p class="text-xs text-brand-brown mt-2 font-semibold">Finance & Admin</p>
                </div>

                <!-- Anggota 2: Aura -->
                <div class="bg-brand-cream rounded-2xl p-6 text-center hover:shadow-lg transition transform hover:-translate-y-2 border border-brand-brown/10">
                    <div class="w-24 h-24 mx-auto bg-brand-white rounded-full flex items-center justify-center text-4xl text-brand-brown mb-4 shadow-md overflow-hidden">
                        <img src="https://ui-avatars.com/api/?name=Aura&background=A0522D&color=fff" alt="Aura">
                    </div>
                    <h4 class="text-xl font-bold text-brand-dark">Aura</h4>
                    <p class="text-sm text-gray-500">XII-H</p>
                    <p class="text-xs text-brand-brown mt-2 font-semibold">Marketing & Promotion</p>
                </div>

                <!-- Anggota 3: Fardhan -->
                <div class="bg-brand-cream rounded-2xl p-6 text-center hover:shadow-lg transition transform hover:-translate-y-2 border border-brand-brown/10">
                    <div class="w-24 h-24 mx-auto bg-brand-white rounded-full flex items-center justify-center text-4xl text-brand-brown mb-4 shadow-md overflow-hidden">
                        <img src="https://ui-avatars.com/api/?name=Fardhan&background=A0522D&color=fff" alt="Fardhan">
                    </div>
                    <h4 class="text-xl font-bold text-brand-dark">Fardhan</h4>
                    <p class="text-sm text-gray-500">XII-H</p>
                    <p class="text-xs text-brand-brown mt-2 font-semibold">Production & Logistics</p>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== 3. PRODUK (UPDATED WITH ADD TO CART) ===== -->
    <section id="produk" class="py-24 bg-brand-cream relative">
        <div class="container mx-auto px-6 relative z-10">
            <div class="text-center mb-16">
                <span class="text-brand-brown font-bold uppercase tracking-widest">Katalog</span>
                <h2 class="text-4xl font-display text-brand-dark mt-2">Pilih Snack Kamu</h2>
            </div>
            
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Produk 1 -->
                <div class="group bg-brand-white rounded-3xl shadow-md hover:shadow-xl transition duration-300 overflow-hidden flex flex-col">
                    <div class="relative h-56 overflow-hidden">
                        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSlB1TFahL_Yj9w70rctpvW0sHmvw5INLUXnA&s" 
                             onerror="this.src='https://placehold.co/600x400/F8F4E3/A0522D?text=Kripik+Singkong'"
                             class="w-full h-full object-cover group-hover:scale-110 transition duration-500">
                    </div>
                    <div class="p-6 flex-1 flex flex-col">
                        <h3 class="text-xl font-bold text-brand-dark mb-2">Kripik Singkong Balado</h3>
                        <p class="text-gray-500 text-sm mb-4 flex-1">Renyah, pedas, manis. Bikin nagih!</p>
                        <div class="flex items-center justify-between mt-auto pt-4 border-t border-gray-100">
                            <span class="text-xl font-bold text-brand-brown">Rp 3.000</span>
                            <button onclick="addToCart(1, 'Kripik Singkong Balado', 3000, 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSlB1TFahL_Yj9w70rctpvW0sHmvw5INLUXnA&s')" 
                                    class="bg-brand-dark text-brand-white py-2 px-4 rounded-full hover:bg-brand-brown transition text-sm flex items-center">
                                <ion-icon name="add-circle" class="mr-1 text-lg"></ion-icon> Tambah
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Produk 2 -->
                <div class="group bg-brand-white rounded-3xl shadow-md hover:shadow-xl transition duration-300 overflow-hidden flex flex-col">
                    <div class="relative h-56 overflow-hidden">
                        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTdIo9cl5mvK1GHWFCP5R-Z0w1UakeTi17ZEg&s" 
                             onerror="this.src='https://placehold.co/600x400/F8F4E3/A0522D?text=Kue+Gabus'"
                             class="w-full h-full object-cover group-hover:scale-110 transition duration-500">
                    </div>
                    <div class="p-6 flex-1 flex flex-col">
                        <h3 class="text-xl font-bold text-brand-dark mb-2">Kue Gabus Keju</h3>
                        <p class="text-gray-500 text-sm mb-4 flex-1">Gurih keju asli, lumer di mulut.</p>
                        <div class="flex items-center justify-between mt-auto pt-4 border-t border-gray-100">
                            <span class="text-xl font-bold text-brand-brown">Rp 3.000</span>
                            <button onclick="addToCart(2, 'Kue Gabus Keju', 3000, 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTdIo9cl5mvK1GHWFCP5R-Z0w1UakeTi17ZEg&s')" 
                                    class="bg-brand-dark text-brand-white py-2 px-4 rounded-full hover:bg-brand-brown transition text-sm flex items-center">
                                <ion-icon name="add-circle" class="mr-1 text-lg"></ion-icon> Tambah
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Produk 3 -->
                <div class="group bg-brand-white rounded-3xl shadow-md hover:shadow-xl transition duration-300 overflow-hidden flex flex-col">
                    <div class="relative h-56 overflow-hidden">
                        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ6QbC5m9q9wqC2zflJuC-EiUCTTp_WDGJaOQ&s" 
                             onerror="this.src='https://placehold.co/600x400/F8F4E3/A0522D?text=Basreng'"
                             class="w-full h-full object-cover group-hover:scale-110 transition duration-500">
                    </div>
                    <div class="p-6 flex-1 flex flex-col">
                        <h3 class="text-xl font-bold text-brand-dark mb-2">Basreng Daun Jeruk</h3>
                        <p class="text-gray-500 text-sm mb-4 flex-1">Pedas nendang aroma daun jeruk.</p>
                        <div class="flex items-center justify-between mt-auto pt-4 border-t border-gray-100">
                            <span class="text-xl font-bold text-brand-brown">Rp 3.000</span>
                            <button onclick="addToCart(3, 'Basreng Daun Jeruk', 3000, 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ6QbC5m9q9wqC2zflJuC-EiUCTTp_WDGJaOQ&s')" 
                                    class="bg-brand-dark text-brand-white py-2 px-4 rounded-full hover:bg-brand-brown transition text-sm flex items-center">
                                <ion-icon name="add-circle" class="mr-1 text-lg"></ion-icon> Tambah
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Produk 4 -->
                <div class="group bg-brand-white rounded-3xl shadow-md hover:shadow-xl transition duration-300 overflow-hidden flex flex-col">
                    <div class="relative h-56 overflow-hidden">
                        <img src="https://cdn11.bigcommerce.com/s-5wf0xbtgyb/images/stencil/1280x1280/products/4826/13492/276a15ddfe31c3b5f6312c31f63e52a7__50195.1692861471.jpg?c=2" 
                             onerror="this.src='https://placehold.co/600x400/F8F4E3/A0522D?text=Kerupuk+Seblak'"
                             class="w-full h-full object-cover group-hover:scale-110 transition duration-500">
                    </div>
                    <div class="p-6 flex-1 flex flex-col">
                        <h3 class="text-xl font-bold text-brand-dark mb-2">Kerupuk Seblak</h3>
                        <p class="text-gray-500 text-sm mb-4 flex-1">Kerupuk bantet bumbu kencur.</p>
                        <div class="flex items-center justify-between mt-auto pt-4 border-t border-gray-100">
                            <span class="text-xl font-bold text-brand-brown">Rp 3.000</span>
                            <button onclick="addToCart(4, 'Kerupuk Seblak', 3000, 'https://cdn11.bigcommerce.com/s-5wf0xbtgyb/images/stencil/1280x1280/products/4826/13492/276a15ddfe31c3b5f6312c31f63e52a7__50195.1692861471.jpg?c=2')" 
                                    class="bg-brand-dark text-brand-white py-2 px-4 rounded-full hover:bg-brand-brown transition text-sm flex items-center">
                                <ion-icon name="add-circle" class="mr-1 text-lg"></ion-icon> Tambah
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Produk 5 -->
                <div class="group bg-brand-white rounded-3xl shadow-md hover:shadow-xl transition duration-300 overflow-hidden flex flex-col">
                    <div class="relative h-56 overflow-hidden">
                        <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRXuoxEPoaaxt7r7_AV0K5laTavza48lUxX0A&s" 
                             onerror="this.src='https://placehold.co/600x400/F8F4E3/A0522D?text=Kripik+Kaca'"
                             class="w-full h-full object-cover group-hover:scale-110 transition duration-500">
                    </div>
                    <div class="p-6 flex-1 flex flex-col">
                        <h3 class="text-xl font-bold text-brand-dark mb-2">Kripik Kaca</h3>
                        <p class="text-gray-500 text-sm mb-4 flex-1">Tipis bening, pedas nikmat.</p>
                        <div class="flex items-center justify-between mt-auto pt-4 border-t border-gray-100">
                            <span class="text-xl font-bold text-brand-brown">Rp 3.000</span>
                            <button onclick="addToCart(5, 'Kripik Kaca', 3000, 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRXuoxEPoaaxt7r7_AV0K5laTavza48lUxX0A&s')" 
                                    class="bg-brand-dark text-brand-white py-2 px-4 rounded-full hover:bg-brand-brown transition text-sm flex items-center">
                                <ion-icon name="add-circle" class="mr-1 text-lg"></ion-icon> Tambah
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== 4. FORMULIR PEMESANAN ===== -->
    <section id="pesan" class="py-24 bg-brand-white">
        <div class="container mx-auto px-6 max-w-4xl">
            <div class="text-center mb-10">
                <h2 class="text-4xl font-display text-brand-dark mb-4">Formulir Pemesanan</h2>
                <p class="text-gray-600">Cek kembali pesananmu di keranjang, lalu lengkapi data di bawah ini.</p>
            </div>

            <div class="bg-brand-cream p-8 rounded-3xl shadow-inner border border-brand-brown/10">
                <!-- Alert Error -->
                <div id="form-error" class="hidden bg-red-100 border-l-4 border-red-500 text-red-700 p-4 mb-6 rounded-r" role="alert">
                    <p class="font-bold">Oops!</p>
                    <p id="error-text">Mohon lengkapi data.</p>
                </div>
                
                <form class="space-y-6">
                    <div class="grid md:grid-cols-2 gap-6">
                        <div>
                            <label for="nama" class="block text-sm font-bold text-brand-dark mb-2">Nama Lengkap</label>
                            <input type="text" id="nama" class="w-full p-3 border border-brand-brown/20 rounded-xl focus:outline-none focus:ring-2 focus:ring-brand-brown/50 bg-white" placeholder="Nama Kamu">
                        </div>
                        <div>
                            <label for="wa" class="block text-sm font-bold text-brand-dark mb-2">Nomor WhatsApp</label>
                            <input type="tel" id="wa" class="w-full p-3 border border-brand-brown/20 rounded-xl focus:outline-none focus:ring-2 focus:ring-brand-brown/50 bg-white" placeholder="Contoh: 0812xxxx">
                        </div>
                    </div>
                    
                    <div>
                        <label for="alamat" class="block text-sm font-bold text-brand-dark mb-2">Alamat / Kelas</label>
                        <input type="text" id="alamat" class="w-full p-3 border border-brand-brown/20 rounded-xl focus:outline-none focus:ring-2 focus:ring-brand-brown/50 bg-white" placeholder="Jalan... atau Kelas XII-H...">
                    </div>
                    
                    <div>
                        <label for="pesanan" class="block text-sm font-bold text-brand-dark mb-2">
                            Rincian Pesanan 
                            <span class="text-xs font-normal text-gray-500">(Otomatis dari keranjang)</span>
                        </label>
                        <textarea id="pesanan" rows="5" class="w-full p-3 border border-brand-brown/20 rounded-xl focus:outline-none focus:ring-2 focus:ring-brand-brown/50 bg-gray-50 text-gray-700 cursor-not-allowed" readonly placeholder="Pilih snack dan klik 'Tambah' di atas..."></textarea>
                    </div>
                    
                    <button type="button" id="send-wa" class="w-full bg-green-600 text-white font-bold py-4 px-6 rounded-xl shadow-lg hover:bg-green-700 transform hover:-translate-y-1 transition duration-300 flex items-center justify-center space-x-3">
                        <ion-icon name="logo-whatsapp" class="text-2xl"></ion-icon>
                        <span>Kirim Pesanan ke WhatsApp</span>
                    </button>
                </form>
            </div>
        </div>
    </section>

    <!-- ===== 5. PEMBAYARAN ===== -->
    <section id="bayar" class="py-16 bg-brand-cream border-t border-brand-brown/10">
        <div class="container mx-auto px-6 text-center">
            <h2 class="text-3xl font-display text-brand-dark mb-8">Pembayaran</h2>
            <div class="flex flex-wrap justify-center gap-6 text-left">
                <!-- DANA -->
                <div class="bg-white p-6 rounded-2xl shadow-sm border-l-4 border-blue-500 w-full md:w-auto flex-1 max-w-xs">
                    <h4 class="font-bold text-lg mb-2 text-blue-600">DANA</h4>
                    <p class="text-xs text-gray-500">Klik untuk bayar:</p>
                    <a href="https://link.dana.id/minta?full_url=https://qr.dana.id/v1/281012012025051515883781" target="_blank" class="text-blue-500 hover:underline text-sm font-bold">Link DANA &rarr;</a>
                </div>
                <!-- GoPay -->
                <div class="bg-white p-6 rounded-2xl shadow-sm border-l-4 border-green-500 w-full md:w-auto flex-1 max-w-xs">
                    <h4 class="font-bold text-lg mb-2 text-green-600">GoPay</h4>
                    <p class="text-xs text-gray-500">No. Transfer:</p>
                    <p class="font-mono font-bold text-brand-dark">0895-3933-86751</p>
                    <p class="text-xs text-gray-400">a/n Abidah</p>
                </div>
                <!-- COD -->
                <div class="bg-white p-6 rounded-2xl shadow-sm border-l-4 border-brand-brown w-full md:w-auto flex-1 max-w-xs">
                    <h4 class="font-bold text-lg mb-2 text-brand-brown">COD (Tunai)</h4>
                    <p class="text-sm text-gray-600">Bayar saat terima barang di sekolah / lokasi COD.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- ===== FOOTER ===== -->
    <footer class="bg-brand-dark text-brand-cream py-10 mt-12">
        <div class="container mx-auto px-6 text-center">
            <h4 class="text-2xl font-display font-bold mb-2">Snack Murni</h4>
            <p class="text-sm opacity-70 mb-6">Group 10 (XII-H) - SMAN 1 Dramaga</p>
            <div class="flex justify-center space-x-6 text-2xl mb-6">
                <a href="https://www.instagram.com/snackmurni?igsh=czRscTIxYWFzcGpu" class="hover:text-brand-brown"><ion-icon name="logo-instagram"></ion-icon></a>
                <a href="https://wa.me/6285780470040" class="hover:text-brand-brown"><ion-icon name="logo-whatsapp"></ion-icon></a>
            </div>
            <p class="text-xs text-gray-500">&copy; 2025 Snack Murni. All rights reserved.</p>
        </div>
    </footer>

    <!-- ===== CART MODAL & FLOATING BUTTON ===== -->
    
    <!-- Floating Cart Button (Mobile/Desktop) -->
    <button onclick="toggleCart()" class="fixed bottom-6 right-6 z-40 bg-brand-brown text-white p-4 rounded-full shadow-2xl hover:bg-brand-dark transition transform hover:scale-110 group animate-bounce-slow">
        <ion-icon name="cart" class="text-3xl"></ion-icon>
        <span id="cart-badge-float" class="absolute top-0 right-0 bg-red-500 text-white text-xs font-bold w-6 h-6 flex items-center justify-center rounded-full border-2 border-white hidden group-hover:animate-pop">0</span>
    </button>

    <!-- Cart Modal Overlay -->
    <div id="cart-modal" class="fixed inset-0 z-50 hidden">
        <!-- Backdrop -->
        <div class="absolute inset-0 bg-black/60 backdrop-blur-sm transition-opacity" onclick="toggleCart()"></div>
        
        <!-- Modal Content -->
        <div class="absolute top-0 right-0 h-full w-full md:w-[400px] bg-brand-white shadow-2xl transform transition-transform duration-300 flex flex-col">
            <!-- Header Cart -->
            <div class="p-6 border-b border-gray-100 flex justify-between items-center bg-brand-cream">
                <h2 class="text-2xl font-display font-bold text-brand-dark">Keranjang</h2>
                <button onclick="toggleCart()" class="text-2xl text-brand-dark hover:rotate-90 transition">
                    <ion-icon name="close"></ion-icon>
                </button>
            </div>
            
            <!-- Items List -->
            <div id="cart-items" class="flex-1 overflow-y-auto p-6 space-y-4">
                <!-- Item akan dirender lewat JS -->
                <div class="text-center text-gray-400 mt-10 flex flex-col items-center">
                    <ion-icon name="basket-outline" class="text-6xl mb-2 opacity-50"></ion-icon>
                    <p>Keranjang masih kosong nih.</p>
                    <button onclick="toggleCart(); document.getElementById('produk').scrollIntoView();" class="mt-4 text-brand-brown font-bold hover:underline">Belanja Dulu Yuk!</button>
                </div>
            </div>
            
            <!-- Footer Cart -->
            <div class="p-6 border-t border-gray-100 bg-white shadow-[0_-5px_15px_rgba(0,0,0,0.05)]">
                <div class="flex justify-between items-center mb-4">
                    <span class="text-gray-600 font-bold">Total:</span>
                    <span id="cart-total" class="text-2xl font-bold text-brand-brown">Rp 0</span>
                </div>
                <button onclick="processCheckout()" class="w-full bg-brand-dark text-brand-white font-bold py-3 rounded-xl hover:bg-brand-brown transition flex justify-center items-center gap-2">
                    Lanjut Pesan <ion-icon name="arrow-forward"></ion-icon>
                </button>
            </div>
        </div>
    </div>

    <!-- ===== JAVASCRIPT ===== -->
    <script>
        // --- STATE ---
        let cart = [];

        // --- FORMAT CURRENCY ---
        const formatRupiah = (number) => {
            return new Intl.NumberFormat('id-ID', { style: 'currency', currency: 'IDR', minimumFractionDigits: 0 }).format(number);
        };

        // --- ADD TO CART FUNCTION ---
        function addToCart(id, name, price, image) {
            const existingItem = cart.find(item => item.id === id);
            
            if (existingItem) {
                existingItem.qty += 1;
            } else {
                cart.push({ id, name, price, image, qty: 1 });
            }
            
            updateCartUI();
            // Buka cart saat item ditambah (optional UX choice)
            // document.getElementById('cart-modal').classList.remove('hidden');
            
            // Visual Feedback
            const floatBadge = document.getElementById('cart-badge-float');
            floatBadge.classList.add('animate-pop');
            setTimeout(() => floatBadge.classList.remove('animate-pop'), 300);
        }

        // --- REMOVE / DECREMENT ---
        function updateQty(id, change) {
            const item = cart.find(item => item.id === id);
            if (!item) return;

            item.qty += change;
            
            if (item.qty <= 0) {
                cart = cart.filter(i => i.id !== id);
            }
            updateCartUI();
        }

        function removeItem(id) {
            cart = cart.filter(item => item.id !== id);
            updateCartUI();
        }

        // --- RENDER UI ---
        function updateCartUI() {
            const cartItemsContainer = document.getElementById('cart-items');
            const cartTotalElement = document.getElementById('cart-total');
            const badges = [
                document.getElementById('cart-badge-desktop'),
                document.getElementById('cart-badge-mobile'),
                document.getElementById('cart-badge-float')
            ];

            // 1. Update Badges
            const totalQty = cart.reduce((sum, item) => sum + item.qty, 0);
            badges.forEach(badge => {
                badge.innerText = totalQty;
                if (totalQty > 0) {
                    badge.classList.remove('hidden');
                } else {
                    badge.classList.add('hidden');
                }
            });

            // 2. Render Items
            cartItemsContainer.innerHTML = '';
            let grandTotal = 0;

            if (cart.length === 0) {
                cartItemsContainer.innerHTML = `
                    <div class="text-center text-gray-400 mt-10 flex flex-col items-center">
                        <ion-icon name="basket-outline" class="text-6xl mb-2 opacity-50"></ion-icon>
                        <p>Keranjang masih kosong.</p>
                        <button onclick="toggleCart(); document.getElementById('produk').scrollIntoView();" class="mt-4 text-brand-brown font-bold hover:underline">Belanja Dulu Yuk!</button>
                    </div>
                `;
            } else {
                cart.forEach(item => {
                    const totalItemPrice = item.price * item.qty;
                    grandTotal += totalItemPrice;

                    const div = document.createElement('div');
                    div.className = "flex items-center gap-4 bg-brand-cream/30 p-3 rounded-xl border border-gray-100";
                    div.innerHTML = `
                        <img src="${item.image}" class="w-16 h-16 rounded-lg object-cover" onerror="this.src='https://placehold.co/100?text=Snack'">
                        <div class="flex-1">
                            <h4 class="font-bold text-sm text-brand-dark line-clamp-1">${item.name}</h4>
                            <p class="text-brand-brown text-xs font-bold">${formatRupiah(item.price)}</p>
                        </div>
                        <div class="flex flex-col items-end gap-1">
                            <div class="flex items-center bg-white rounded-lg border border-gray-200 overflow-hidden">
                                <button onclick="updateQty(${item.id}, -1)" class="px-2 py-1 text-brand-dark hover:bg-gray-100">-</button>
                                <span class="px-2 text-xs font-bold w-6 text-center">${item.qty}</span>
                                <button onclick="updateQty(${item.id}, 1)" class="px-2 py-1 text-brand-dark hover:bg-gray-100">+</button>
                            </div>
                            <button onclick="removeItem(${item.id})" class="text-red-400 text-xs hover:text-red-600">Hapus</button>
                        </div>
                    `;
                    cartItemsContainer.appendChild(div);
                });
            }

            // 3. Update Total
            cartTotalElement.innerText = formatRupiah(grandTotal);
        }

        // --- UI INTERACTIONS ---
        function toggleCart() {
            const modal = document.getElementById('cart-modal');
            modal.classList.toggle('hidden');
        }

        function processCheckout() {
            if (cart.length === 0) {
                alert("Keranjang kosong kak!");
                return;
            }

            // Generate Text Summary
            let summary = "";
            let grandTotal = 0;
            
            cart.forEach(item => {
                const subtotal = item.price * item.qty;
                summary += `- ${item.name} (${item.qty}x) = ${formatRupiah(subtotal)}\n`;
                grandTotal += subtotal;
            });
            
            summary += `\nTotal: ${formatRupiah(grandTotal)}`;

            // Fill Form Textarea
            const formPesanan = document.getElementById('pesanan');
            formPesanan.value = summary;

            // Close Cart & Scroll to Form
            toggleCart();
            document.getElementById('pesanan').scrollIntoView({ behavior: 'smooth', block: 'center' });
            
            // Focus on Name input
            setTimeout(() => {
                document.getElementById('nama').focus();
            }, 800);
        }

        // --- WHATSAPP LOGIC (EXISTING) ---
        document.getElementById('send-wa').addEventListener('click', () => {
            const nama = document.getElementById('nama').value.trim();
            const wa = document.getElementById('wa').value.trim();
            const alamat = document.getElementById('alamat').value.trim();
            const pesanan = document.getElementById('pesanan').value.trim();
            const errorBox = document.getElementById('form-error');

            // Validasi
            if (!nama || !wa || !alamat || !pesanan) {
                errorBox.classList.remove('hidden');
                document.getElementById('error-text').innerText = "Mohon lengkapi Nama, No WA, Alamat, dan pastikan Keranjang terisi.";
                return;
            } else {
                errorBox.classList.add('hidden');
            }

            const adminWA = '6285780470040'; 
            
            let message = `*Halo Admin Snack Murni!* 👋\nSaya mau order dong.\n\n`;
            message += `👤 *Nama:* ${nama}\n`;
            message += `📱 *No. WA:* ${wa}\n`;
            message += `📍 *Alamat/Kelas:* ${alamat}\n\n`;
            message += `📝 *Detail Pesanan:*\n${pesanan}\n\n`;
            message += `Mohon dikonfirmasi ya. Terima kasih!`;

            const waURL = `https://wa.me/${adminWA}?text=${encodeURIComponent(message)}`;
            window.open(waURL, '_blank');
        });

        // --- MOBILE MENU LOGIC ---
        const menuButton = document.getElementById('menu-button');
        const mobileMenu = document.getElementById('mobile-menu');
        
        menuButton.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        document.querySelectorAll('.mobile-link').forEach(link => {
            link.addEventListener('click', () => mobileMenu.classList.add('hidden'));
        });
    </script>
</body>
</html>**
