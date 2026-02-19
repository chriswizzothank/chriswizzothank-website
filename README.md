# chriswizzothank-website[index.html](https://github.com/user-attachments/files/25422886/index.html)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Huldah Curtains | Design & Shop - Kigali, Rwanda</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">
    <script src="https://unpkg.com/lucide@latest"></script>
    <style>
        body {
            font-family: 'Inter', sans-serif;
        }
        h1, h2, h3, .serif {
            font-family: 'Playfair Display', serif;
        }
        .hero-pattern {
            background-image: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23d4c4b7' fill-opacity='0.1'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
        }
        .curtain-fold {
            background: linear-gradient(90deg, rgba(255,255,255,0.1) 0%, rgba(255,255,255,0.3) 50%, rgba(255,255,255,0.1) 100%);
        }
        .slide-in {
            animation: slideIn 0.6s ease-out forwards;
        }
        @keyframes slideIn {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .cart-drawer {
            transition: transform 0.3s ease-in-out;
        }
        .cart-open {
            transform: translateX(0);
        }
        .cart-closed {
            transform: translateX(100%);
        }
        .product-card:hover .product-overlay {
            opacity: 1;
        }
        .fabric-texture {
            background-image: repeating-linear-gradient(45deg, transparent, transparent 35px, rgba(255,255,255,.05) 35px, rgba(255,255,255,.05) 70px);
        }
        .rwanda-flag {
            background: linear-gradient(to bottom, #00A1DE 33.33%, #FAD201 33.33%, #FAD201 66.66%, #00A651 66.66%);
        }
        .instagram-gradient {
            background: linear-gradient(45deg, #f09433 0%, #e6683c 25%, #dc2743 50%, #cc2366 75%, #bc1888 100%);
        }
    </style>
</head>
<body class="bg-stone-50 text-stone-800 overflow-x-hidden">

    <!-- Top Bar -->
    <div class="bg-stone-900 text-white py-2 text-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex justify-between items-center">
            <div class="flex items-center space-x-4">
                <span class="flex items-center"><i data-lucide="phone" class="w-4 h-4 mr-2"></i>+250 789 543 075</span>
                <span class="hidden sm:flex items-center"><i data-lucide="map-pin" class="w-4 h-4 mr-2"></i>KN 2 St, Kigali, Rwanda</span>
            </div>
            <div class="flex items-center space-x-4">
                <a href="https://www.instagram.com/amarido_kigali_rwanda/" target="_blank" class="flex items-center hover:text-pink-400 transition-colors">
                    <i data-lucide="instagram" class="w-4 h-4 mr-1"></i>
                    @amarido_kigali_rwanda
                </a>
                <div class="w-6 h-4 rounded overflow-hidden inline-block border border-white/20">
                    <div class="rwanda-flag w-full h-full"></div>
                </div>
            </div>
        </div>
    </div>

    <!-- Navigation -->
    <nav class="sticky top-0 w-full bg-white/95 backdrop-blur-md shadow-sm z-50 transition-all duration-300" id="navbar">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <div class="flex items-center space-x-2">
                    <i data-lucide="curtains" class="h-8 w-8 text-amber-700"></i>
                    <div>
                        <span class="serif text-2xl font-bold text-stone-900 block leading-none">Huldah</span>
                        <span class="text-xs text-stone-500 tracking-wider">CURTAINS ONLY</span>
                    </div>
                </div>
                
                <div class="hidden md:flex space-x-8">
                    <a href="#home" class="text-stone-600 hover:text-amber-700 transition-colors">Home</a>
                    <a href="#collections" class="text-stone-600 hover:text-amber-700 transition-colors">Our Curtains</a>
                    <a href="#designer" class="text-stone-600 hover:text-amber-700 transition-colors">Custom Design</a>
                    <a href="#gallery" class="text-stone-600 hover:text-amber-700 transition-colors">Gallery</a>
                    <a href="#visit" class="text-stone-600 hover:text-amber-700 transition-colors">Visit Us</a>
                </div>

                <div class="flex items-center space-x-4">
                    <a href="https://www.instagram.com/amarido_kigali_rwanda/" target="_blank" class="p-2 hover:bg-stone-100 rounded-full transition-colors instagram-gradient text-white">
                        <i data-lucide="instagram" class="h-5 w-5"></i>
                    </a>
                    <button onclick="toggleCart()" class="p-2 hover:bg-stone-100 rounded-full transition-colors relative">
                        <i data-lucide="shopping-bag" class="h-5 w-5 text-stone-600"></i>
                        <span id="cart-badge" class="absolute -top-1 -right-1 bg-amber-700 text-white text-xs rounded-full h-5 w-5 flex items-center justify-center hidden">0</span>
                    </button>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="home" class="relative min-h-screen flex items-center pt-20 hero-pattern overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-r from-stone-100 via-stone-50/80 to-transparent z-0"></div>
        
        <div class="absolute right-0 top-0 h-full w-1/2 hidden lg:block">
            <div class="absolute right-20 top-32 w-96 h-[600px] bg-gradient-to-b from-amber-100 to-amber-50 rounded-t-full shadow-2xl transform rotate-3 curtain-fold"></div>
            <div class="absolute right-32 top-40 w-80 h-[550px] bg-gradient-to-b from-stone-200 to-stone-100 rounded-t-full shadow-xl transform -rotate-2 curtain-fold"></div>
        </div>

        <div class="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 grid lg:grid-cols-2 gap-12 items-center">
            <div class="slide-in">
                <div class="inline-flex items-center px-4 py-1 bg-amber-100 text-amber-800 rounded-full text-sm font-medium mb-4 gap-2">
                    <span>Located in Kigali, Rwanda</span>
                    <span class="w-px h-4 bg-amber-300"></span>
                    <a href="https://www.instagram.com/amarido_kigali_rwanda/" target="_blank" class="flex items-center hover:underline">
                        <i data-lucide="instagram" class="w-3 h-3 mr-1"></i>
                        @amarido_kigali_rwanda
                    </a>
                </div>
                <h1 class="text-5xl lg:text-7xl font-bold text-stone-900 leading-tight mb-6">
                    Premium Curtains for <span class="text-amber-700 italic">Every Rwandan Home</span>
                </h1>
                <p class="text-lg text-stone-600 mb-8 leading-relaxed max-w-lg">
                    Kigali's premier curtain specialist. We design, sew, and install bespoke curtains tailored to your windows. Visit our shop at KN 2 Street or check our latest work on Instagram.
                </p>
                
                <div class="flex flex-col sm:flex-row gap-4 mb-8">
                    <a href="#collections" class="px-8 py-4 bg-amber-700 text-white rounded-full font-medium hover:bg-amber-800 transition-all transform hover:scale-105 shadow-lg text-center">
                        Browse Curtains
                    </a>
                    <a href="https://www.instagram.com/amarido_kigali_rwanda/" target="_blank" class="px-8 py-4 instagram-gradient text-white rounded-full font-medium hover:opacity-90 transition-all flex items-center justify-center gap-2">
                        <i data-lucide="instagram" class="w-5 h-5"></i>
                        View on Instagram
                    </a>
                </div>
                
                <div class="mt-8 flex items-center space-x-8">
                    <div>
                        <p class="text-3xl font-bold text-stone-900 serif">2,500+</p>
                        <p class="text-sm text-stone-500">Homes in Rwanda</p>
                    </div>
                    <div class="h-12 w-px bg-stone-300"></div>
                    <div>
                        <p class="text-3xl font-bold text-stone-900 serif">100%</p>
                        <p class="text-sm text-stone-500">Custom Made</p>
                    </div>
                    <div class="h-12 w-px bg-stone-300"></div>
                    <div>
                        <p class="text-3xl font-bold text-stone-900 serif">9+</p>
                        <p class="text-sm text-stone-500">Years Experience</p>
                    </div>
                </div>
            </div>
            
            <!-- Hero Image - Modern Living Room Curtains -->
            <div class="hidden lg:block relative">
                <img src="https://media.designcafe.com/wp-content/uploads/2020/06/11144550/curtain-design-for-living-room.jpg" 
                     alt="Modern Living Room Curtains" 
                     class="rounded-3xl shadow-2xl w-full h-[600px] object-cover transform hover:scale-105 transition-transform duration-700">
                <div class="absolute -bottom-6 -left-6 bg-white p-6 rounded-2xl shadow-xl">
                    <p class="text-amber-700 font-bold text-lg">2024 Collection</p>
                    <p class="text-stone-600">Modern Designs</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Gallery Section -->
    <section id="gallery" class="py-24 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <div class="inline-flex items-center justify-center p-3 bg-gradient-to-r from-purple-500 via-pink-500 to-orange-500 rounded-full mb-4">
                    <i data-lucide="instagram" class="w-8 h-8 text-white"></i>
                </div>
                <h2 class="text-4xl font-bold text-stone-900 mb-4">Our Work & Inspiration</h2>
                <p class="text-stone-600 max-w-2xl mx-auto mb-6">
                    See our latest curtain designs and installations. Follow <a href="https://www.instagram.com/amarido_kigali_rwanda/" target="_blank" class="text-amber-700 font-semibold hover:underline">@amarido_kigali_rwanda</a> for daily inspiration.
                </p>
                <a href="https://www.instagram.com/amarido_kigali_rwanda/" target="_blank" class="inline-flex items-center px-6 py-3 instagram-gradient text-white rounded-full font-medium hover:opacity-90 transition-all">
                    <i data-lucide="instagram" class="w-5 h-5 mr-2"></i>
                    Visit @amarido_kigali_rwanda
                </a>
            </div>
            
            <!-- Pinterest-Style Gallery Grid -->
            <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
                <div class="space-y-4">
                    <img src="https://curtainlibrary.com.my/wp-content/uploads/2023/12/curtain-library-2024-curtain-trends-and-ideas.jpg" 
                         alt="2024 Curtain Trends" 
                         class="rounded-2xl shadow-lg w-full h-64 object-cover hover:scale-105 transition-transform cursor-pointer"
                         onclick="window.open('https://www.instagram.com/amarido_kigali_rwanda/', '_blank')">
                    <img src="https://bunny-wp-pullzone-dspfxhl1bz.b-cdn.net/wp-content/uploads/2024/04/bedroom-curtains-1024x1024.webp" 
                         alt="Modern Bedroom Curtains" 
                         class="rounded-2xl shadow-lg w-full h-80 object-cover hover:scale-105 transition-transform cursor-pointer"
                         onclick="window.open('https://www.instagram.com/amarido_kigali_rwanda/', '_blank')">
                </div>
                <div class="space-y-4 mt-8">
                    <img src="https://www.theshadestore.com/blog/wp-content/uploads/the-shade-store-flat-roman-shades-tailored-pleat-drapery-victoria-hagan-jasmine-midnight-modern-curtain-ideas-bold-drapery-hero-2023-palm-beach-950x630px.jpg" 
                         alt="Modern Bold Drapery" 
                         class="rounded-2xl shadow-lg w-full h-80 object-cover hover:scale-105 transition-transform cursor-pointer"
                         onclick="window.open('https://www.instagram.com/amarido_kigali_rwanda/', '_blank')">
                    <img src="https://xcdn.next.co.uk/common/items/default/default/itemimages/3_4Ratio/product/lge/T57207s.jpg?im=Resize,width=750" 
                         alt="Natural Stripe Voile Curtains" 
                         class="rounded-2xl shadow-lg w-full h-64 object-cover hover:scale-105 transition-transform cursor-pointer"
                         onclick="window.open('https://www.instagram.com/amarido_kigali_rwanda/', '_blank')">
                </div>
                <div class="space-y-4">
                    <img src="https://www.suecardy.com/wp-content/uploads/2024/02/Sue-Cardy-Pretigious-Textiles-Milan.jpg" 
                         alt="Floral Print Curtains" 
                         class="rounded-2xl shadow-lg w-full h-64 object-cover hover:scale-105 transition-transform cursor-pointer"
                         onclick="window.open('https://www.instagram.com/amarido_kigali_rwanda/', '_blank')">
                    <img src="http://www.smartwingshome.com/cdn/shop/files/8_5d24812d-4ce4-45f4-bbcd-f6d2f77ce4d5.jpg?v=1754888806" 
                         alt="Motorized Blackout Curtains" 
                         class="rounded-2xl shadow-lg w-full h-80 object-cover hover:scale-105 transition-transform cursor-pointer"
                         onclick="window.open('https://www.instagram.com/amarido_kigali_rwanda/', '_blank')">
                </div>
                <div class="space-y-4 mt-8">
                    <img src="https://www.homerilla.com/cdn/shop/articles/Banner4_800_0d30eb6d-5a00-43c6-9160-6fda1bca8030_711x.jpg?v=1705300080" 
                         alt="Minimalist White Curtains" 
                         class="rounded-2xl shadow-lg w-full h-80 object-cover hover:scale-105 transition-transform cursor-pointer"
                         onclick="window.open('https://www.instagram.com/amarido_kigali_rwanda/', '_blank')">
                    <img src="https://xcdn.next.co.uk/common/items/default/default/itemimages/3_4Ratio/product/lge/T70044s2.jpg?im=Resize,width=750" 
                         alt="Grey Blackout Curtains" 
                         class="rounded-2xl shadow-lg w-full h-64 object-cover hover:scale-105 transition-transform cursor-pointer"
                         onclick="window.open('https://www.instagram.com/amarido_kigali_rwanda/', '_blank')">
                </div>
            </div>
        </div>
    </section>

    <!-- Collections Section -->
    <section id="collections" class="py-24 bg-stone-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-4xl font-bold text-stone-900 mb-4">Our Curtain Collections</h2>
                <p class="text-stone-600 max-w-2xl mx-auto">
                    Handcrafted curtains available at our KN 2 Street shop. 
                    <a href="https://www.instagram.com/amarido_kigali_rwanda/" target="_blank" class="text-amber-700 hover:underline">See more on Instagram →</a>
                </p>
            </div>

            <!-- Filters -->
            <div class="flex justify-center space-x-4 mb-12 flex-wrap gap-2">
                <button onclick="filterProducts('all')" class="filter-btn active px-6 py-2 rounded-full border border-stone-300 text-stone-600 hover:bg-amber-700 hover:text-white hover:border-amber-700 transition-all bg-amber-700 text-white border-amber-700" data-filter="all">All Curtains</button>
                <button onclick="filterProducts('sheer')" class="filter-btn px-6 py-2 rounded-full border border-stone-300 text-stone-600 hover:bg-amber-700 hover:text-white hover:border-amber-700 transition-all" data-filter="sheer">Sheer & Voile</button>
                <button onclick="filterProducts('blackout')" class="filter-btn px-6 py-2 rounded-full border border-stone-300 text-stone-600 hover:bg-amber-700 hover:text-white hover:border-amber-700 transition-all" data-filter="blackout">Blackout</button>
                <button onclick="filterProducts('printed')" class="filter-btn px-6 py-2 rounded-full border border-stone-300 text-stone-600 hover:bg-amber-700 hover:text-white hover:border-amber-700 transition-all" data-filter="printed">Printed & Patterned</button>
            </div>

            <!-- Product Grid -->
            <div id="product-grid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Products populated by JS -->
            </div>

            <div class="mt-16 text-center">
                <a href="https://www.instagram.com/amarido_kigali_rwanda/" target="_blank" class="inline-flex items-center px-8 py-4 instagram-gradient text-white rounded-full font-medium hover:opacity-90 transition-all">
                    <i data-lucide="instagram" class="w-5 h-5 mr-2"></i>
                    See More Designs on Instagram
                </a>
            </div>
        </div>
    </section>

    <!-- Custom Designer Section -->
    <section id="designer" class="py-24 bg-white fabric-texture">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid lg:grid-cols-2 gap-16 items-center">
                <div>
                    <h2 class="text-4xl font-bold text-stone-900 mb-6">Design Your Custom Curtains</h2>
                    <p class="text-stone-600 mb-8 text-lg">
                        Visit our KN 2 Street location or DM us on 
                        <a href="https://www.instagram.com/amarido_kigali_rwanda/" target="_blank" class="text-amber-700 hover:underline">Instagram</a> 
                        for custom orders.
                    </p>
                    
                    <div class="space-y-6">
                        <div class="bg-stone-50 p-6 rounded-2xl shadow-sm">
                            <h3 class="font-semibold text-stone-900 mb-3 flex items-center">
                                <i data-lucide="ruler" class="w-5 h-5 mr-2 text-amber-700"></i>
                                Step 1: Measurements (inches)
                            </h3>
                            <div class="grid grid-cols-2 gap-4">
                                <div>
                                    <label class="block text-sm text-stone-600 mb-1">Window Width</label>
                                    <input type="number" id="width-input" class="w-full px-4 py-2 border border-stone-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-amber-700" placeholder="48" onchange="updatePreview()">
                                </div>
                                <div>
                                    <label class="block text-sm text-stone-600 mb-1">Window Length</label>
                                    <input type="number" id="length-input" class="w-full px-4 py-2 border border-stone-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-amber-700" placeholder="84" onchange="updatePreview()">
                                </div>
                            </div>
                        </div>

                        <div class="bg-stone-50 p-6 rounded-2xl shadow-sm">
                            <h3 class="font-semibold text-stone-900 mb-3 flex items-center">
                                <i data-lucide="palette" class="w-5 h-5 mr-2 text-amber-700"></i>
                                Step 2: Select Fabric
                            </h3>
                            <div class="grid grid-cols-4 gap-3" id="fabric-selector">
                                <button onclick="selectFabric('cream')" class="fabric-btn w-full aspect-square rounded-lg bg-[#F5F5DC] border-2 border-transparent hover:scale-110 transition-transform shadow-sm" data-fabric="cream"></button>
                                <button onclick="selectFabric('navy')" class="fabric-btn w-full aspect-square rounded-lg bg-[#1e3a5f] border-2 border-transparent hover:scale-110 transition-transform shadow-sm" data-fabric="navy"></button>
                                <button onclick="selectFabric('sage')" class="fabric-btn w-full aspect-square rounded-lg bg-[#87A878] border-2 border-transparent hover:scale-110 transition-transform shadow-sm" data-fabric="sage"></button>
                                <button onclick="selectFabric('terracotta')" class="fabric-btn w-full aspect-square rounded-lg bg-[#E2725B] border-2 border-transparent hover:scale-110 transition-transform shadow-sm" data-fabric="terracotta"></button>
                                <button onclick="selectFabric('charcoal')" class="fabric-btn w-full aspect-square rounded-lg bg-[#36454F] border-2 border-transparent hover:scale-110 transition-transform shadow-sm" data-fabric="charcoal"></button>
                                <button onclick="selectFabric('blush')" class="fabric-btn w-full aspect-square rounded-lg bg-[#F4C2C2] border-2 border-transparent hover:scale-110 transition-transform shadow-sm" data-fabric="blush"></button>
                                <button onclick="selectFabric('gold')" class="fabric-btn w-full aspect-square rounded-lg bg-[#D4AF37] border-2 border-transparent hover:scale-110 transition-transform shadow-sm" data-fabric="gold"></button>
                                <button onclick="selectFabric('white')" class="fabric-btn w-full aspect-square rounded-lg bg-white border-2 border-stone-200 hover:scale-110 transition-transform shadow-sm" data-fabric="white"></button>
                            </div>
                        </div>

                        <div class="bg-stone-50 p-6 rounded-2xl shadow-sm">
                            <h3 class="font-semibold text-stone-900 mb-3 flex items-center">
                                <i data-lucide="scissors" class="w-5 h-5 mr-2 text-amber-700"></i>
                                Step 3: Style
                            </h3>
                            <select id="style-select" class="w-full px-4 py-2 border border-stone-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-amber-700" onchange="updatePreview()">
                                <option value="pleated">Pinch Pleated</option>
                                <option value="grommet">Grommet Top</option>
                                <option value="rod-pocket">Rod Pocket</option>
                                <option value="tab-top">Tab Top</option>
                            </select>
                        </div>

                        <div class="bg-amber-50 p-6 rounded-2xl border border-amber-200">
                            <div class="flex justify-between items-center mb-2">
                                <span class="text-stone-600">Estimated Price:</span>
                                <span class="text-2xl font-bold text-amber-700 serif" id="custom-price">RWF 0</span>
                            </div>
                            <p class="text-sm text-stone-500 mb-4">Final price confirmed in-store or via DM</p>
                            <div class="flex gap-3">
                                <button onclick="addCustomToCart()" class="flex-1 py-3 bg-amber-700 text-white rounded-lg font-medium hover:bg-amber-800 transition-colors">
                                    Request Quote
                                </button>
                                <a href="https://www.instagram.com/amarido_kigali_rwanda/" target="_blank" class="py-3 px-4 instagram-gradient text-white rounded-lg font-medium hover:opacity-90 transition-colors flex items-center justify-center">
                                    <i data-lucide="instagram" class="w-5 h-5"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="relative">
                    <div class="bg-white p-8 rounded-3xl shadow-xl">
                        <div class="relative bg-stone-100 rounded-2xl overflow-hidden" style="height: 500px;">
                            <div class="absolute inset-8 bg-sky-100 rounded-lg border-8 border-white shadow-inner">
                                <div class="absolute inset-0 bg-gradient-to-b from-blue-200 to-blue-50 opacity-50"></div>
                                <div class="absolute top-4 left-4 w-16 h-8 bg-white rounded-full opacity-60"></div>
                                <div class="absolute top-8 right-8 w-12 h-6 bg-white rounded-full opacity-40"></div>
                            </div>
                            
                            <div id="curtain-preview" class="absolute inset-8 flex justify-between pointer-events-none">
                                <div id="left-curtain" class="w-1/2 bg-[#F5F5DC] shadow-2xl transform origin-top-left transition-all duration-500 curtain-fold" style="border-radius: 0 0 100px 0;"></div>
                                <div id="right-curtain" class="w-1/2 bg-[#F5F5DC] shadow-2xl transform origin-top-right transition-all duration-500 curtain-fold" style="border-radius: 0 0 0 100px;"></div>
                            </div>

                            <div class="absolute top-4 left-4 right-4 h-2 bg-stone-400 rounded-full shadow-md"></div>
                            <div class="absolute top-2 left-4 w-4 h-6 bg-stone-500 rounded-full"></div>
                            <div class="absolute top-2 right-4 w-4 h-6 bg-stone-500 rounded-full"></div>
                        </div>
                        
                        <div class="mt-6 text-center">
                            <p class="text-sm text-stone-500">Live Preview</p>
                            <p class="text-stone-800 font-medium" id="preview-details">Cream • 48" × 84" • Pinch Pleated</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Visit Us Section -->
    <section id="visit" class="py-24 bg-stone-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid lg:grid-cols-2 gap-16 items-center">
                <div>
                    <h2 class="text-4xl font-bold text-stone-900 mb-6">Visit Our Shop</h2>
                    <p class="text-stone-600 mb-8 text-lg">
                        Come see our fabrics in person at KN 2 Street, or connect with us on Instagram 
                        <a href="https://www.instagram.com/amarido_kigali_rwanda/" target="_blank" class="text-amber-700 hover:underline">@amarido_kigali_rwanda</a>
                    </p>
                    
                    <div class="space-y-6">
                        <div class="flex items-start space-x-4 p-6 bg-white rounded-2xl shadow-sm">
                            <div class="p-3 bg-amber-100 rounded-full">
                                <i data-lucide="map-pin" class="w-6 h-6 text-amber-700"></i>
                            </div>
                            <div>
                                <h3 class="font-semibold text-stone-900 text-lg">Address</h3>
                                <p class="text-stone-600">KN 2 Street, Kigali, Rwanda</p>
                                <a href="https://www.google.com/maps/place/Huldah+Curtains+Design%26Shop/@-1.9450125,30.058339,17z" target="_blank" class="inline-flex items-center mt-2 text-amber-700 hover:text-amber-800 font-medium">
                                    View on Google Maps
                                    <i data-lucide="external-link" class="w-4 h-4 ml-1"></i>
                                </a>
                            </div>
                        </div>

                        <div class="flex items-start space-x-4 p-6 bg-white rounded-2xl shadow-sm">
                            <div class="p-3 bg-amber-100 rounded-full">
                                <i data-lucide="phone" class="w-6 h-6 text-amber-700"></i>
                            </div>
                            <div>
                                <h3 class="font-semibold text-stone-900 text-lg">Phone / WhatsApp</h3>
                                <p class="text-stone-600">+250 789 543 075</p>
                                <a href="tel:+250789543075" class="inline-flex items-center mt-2 text-amber-700 hover:text-amber-800 font-medium">
                                    Call Now
                                    <i data-lucide="arrow-right" class="w-4 h-4 ml-1"></i>
                                </a>
                            </div>
                        </div>

                        <div class="flex items-start space-x-4 p-6 bg-white rounded-2xl shadow-sm">
                            <div class="p-3 instagram-gradient rounded-full">
                                <i data-lucide="instagram" class="w-6 h-6 text-white"></i>
                            </div>
                            <div>
                                <h3 class="font-semibold text-stone-900 text-lg">Instagram</h3>
                                <p class="text-stone-600">@amarido_kigali_rwanda</p>
                                <a href="https://www.instagram.com/amarido_kigali_rwanda/" target="_blank" class="inline-flex items-center mt-2 text-amber-700 hover:text-amber-800 font-medium">
                                    Follow Us
                                    <i data-lucide="external-link" class="w-4 h-4 ml-1"></i>
                                </a>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="relative h-96 lg:h-full min-h-[400px] rounded-3xl overflow-hidden shadow-2xl">
                    <iframe 
                        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3987.553682196494!2d30.0583077!3d-1.9450252!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x19dca5bc933e1471%3A0xeb5b318a2e889a6c!2sHuldah+Curtains+Design%26Shop!5e0!3m2!1sen!2srw!4v1708272000000!5m2!1sen!2srw"
                        width="100%" 
                        height="100%" 
                        style="border:0;" 
                        allowfullscreen="" 
                        loading="lazy" 
                        referrerpolicy="no-referrer-when-downgrade"
                        class="absolute inset-0">
                    </iframe>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-stone-900 text-stone-300 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-12">
                <div class="col-span-1 md:col-span-2">
                    <div class="flex items-center space-x-2 mb-6">
                        <i data-lucide="curtains" class="h-8 w-8 text-amber-700"></i>
                        <div>
                            <span class="serif text-2xl font-bold text-white block leading-none">Huldah</span>
                            <span class="text-xs text-stone-500 tracking-wider">CURTAINS ONLY</span>
                        </div>
                    </div>
                    <p class="text-stone-400 mb-6 max-w-md">
                        Kigali's trusted curtain specialist. Custom curtains designed, sewn, and installed for homes across Rwanda. Follow us on Instagram for daily inspiration.
                    </p>
                    <div class="flex space-x-4">
                        <a href="https://www.instagram.com/amarido_kigali_rwanda/" target="_blank" class="instagram-gradient p-2 rounded-full text-white hover:opacity-90 transition-opacity">
                            <i data-lucide="instagram" class="w-5 h-5"></i>
                        </a>
                        <a href="#" class="p-2 bg-stone-800 rounded-full hover:bg-stone-700 transition-colors">
                            <i data-lucide="facebook" class="w-5 h-5"></i>
                        </a>
                        <a href="https://wa.me/250789543075" class="p-2 bg-stone-800 rounded-full hover:bg-green-600 transition-colors">
                            <i data-lucide="message-circle" class="w-5 h-5"></i>
                        </a>
                    </div>
                </div>
                
                <div>
                    <h4 class="text-white font-semibold mb-6">Contact</h4>
                    <ul class="space-y-3">
                        <li class="flex items-center space-x-3">
                            <i data-lucide="map-pin" class="w-5 h-5 text-amber-700"></i>
                            <span>KN 2 Street, Kigali</span>
                        </li>
                        <li class="flex items-center space-x-3">
                            <i data-lucide="phone" class="w-5 h-5 text-amber-700"></i>
                            <a href="tel:+250789543075" class="hover:text-white transition-colors">+250 789 543 075</a>
                        </li>
                        <li class="flex items-center space-x-3">
                            <i data-lucide="instagram" class="w-5 h-5 text-amber-700"></i>
                            <a href="https://www.instagram.com/amarido_kigali_rwanda/" target="_blank" class="hover:text-white transition-colors">@amarido_kigali_rwanda</a>
                        </li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-white font-semibold mb-6">Hours</h4>
                    <ul class="space-y-3">
                        <li class="flex items-center space-x-3">
                            <i data-lucide="clock" class="w-5 h-5 text-amber-700"></i>
                            <span>Mon-Sat: 8AM - 6PM</span>
                        </li>
                        <li class="flex items-center space-x-3">
                            <i data-lucide="x" class="w-5 h-5 text-amber-700"></i>
                            <span>Sunday: Closed</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-stone-800 mt-12 pt-8 flex flex-col md:flex-row justify-between items-center">
                <p class="text-stone-500 text-sm">&copy; 2024 Huldah Curtains. KN 2 St, Kigali, Rwanda.</p>
                <div class="flex space-x-6 mt-4 md:mt-0 text-sm text-stone-500">
                    <span>Follow us: </span>
                    <a href="https://www.instagram.com/amarido_kigali_rwanda/" target="_blank" class="text-amber-700 hover:underline">@amarido_kigali_rwanda</a>
                </div>
            </div>
        </div>
    </footer>

    <!-- Cart Drawer -->
    <div id="cart-overlay" class="fixed inset-0 bg-black/50 z-50 hidden transition-opacity" onclick="toggleCart()"></div>
    <div id="cart-drawer" class="fixed top-0 right-0 h-full w-full max-w-md bg-white shadow-2xl z-50 cart-drawer cart-closed flex flex-col">
        <div class="p-6 border-b border-stone-200 flex justify-between items-center">
            <h2 class="text-2xl font-bold serif text-stone-900">Your Quote Request</h2>
            <button onclick="toggleCart()" class="p-2 hover:bg-stone-100 rounded-full transition-colors">
                <i data-lucide="x" class="w-6 h-6 text-stone-600"></i>
            </button>
        </div>
        
        <div id="cart-items" class="flex-1 overflow-y-auto p-6 space-y-4">
            <p class="text-stone-500 text-center py-12">No items selected. Browse our collection or DM us on Instagram.</p>
        </div>
        
        <div class="p-6 border-t border-stone-200 bg-stone-50 space-y-3">
            <div class="flex justify-between mb-4 text-lg font-semibold">
                <span>Estimated Total</span>
                <span id="cart-total">RWF 0</span>
            </div>
            <button onclick="window.location.href='tel:+250789543075'" class="w-full py-4 bg-amber-700 text-white rounded-lg font-medium hover:bg-amber-800 transition-colors shadow-lg flex items-center justify-center gap-2">
                <i data-lucide="phone" class="w-5 h-5"></i>
                Call to Order
            </button>
            <a href="https://www.instagram.com/amarido_kigali_rwanda/" target="_blank" class="w-full py-4 instagram-gradient text-white rounded-lg font-medium hover:opacity-90 transition-colors shadow-lg flex items-center justify-center gap-2">
                <i data-lucide="instagram" class="w-5 h-5"></i>
                DM on Instagram
            </a>
        </div>
    </div>

    <script>
        lucide.createIcons();

        const products = [
            {
                id: 1,
                name: "Modern Living Room Curtains",
                category: "sheer",
                price: 45000,
                currency: "RWF",
                image: "https://media.designcafe.com/wp-content/uploads/2020/06/11144550/curtain-design-for-living-room.jpg",
                description: "Contemporary designs perfect for modern Rwandan homes"
            },
            {
                id: 2,
                name: "2024 Trendy Curtains Collection",
                category: "printed",
                price: 55000,
                currency: "RWF",
                image: "https://curtainlibrary.com.my/wp-content/uploads/2023/12/curtain-library-2024-curtain-trends-and-ideas.jpg",
                description: "Latest 2024 curtain trends and styles"
            },
            {
                id: 3,
                name: "Elegant Bedroom Blackout",
                category: "blackout",
                price: 48000,
                currency: "RWF",
                image: "https://bunny-wp-pullzone-dspfxhl1bz.b-cdn.net/wp-content/uploads/2024/04/bedroom-curtains-1024x1024.webp",
                description: "Star-patterned blackout curtains for perfect sleep"
            },
            {
                id: 4,
                name: "Bold Modern Drapery",
                category: "printed",
                price: 62000,
                currency: "RWF",
                image: "https://www.theshadestore.com/blog/wp-content/uploads/the-shade-store-flat-roman-shades-tailored-pleat-drapery-victoria-hagan-jasmine-midnight-modern-curtain-ideas-bold-drapery-hero-2023-palm-beach-950x630px.jpg",
                description: "Luxury bold drapery for elegant spaces"
            },
            {
                id: 5,
                name: "Natural Stripe Voile",
                category: "sheer",
                price: 35000,
                currency: "RWF",
                image: "https://xcdn.next.co.uk/common/items/default/default/itemimages/3_4Ratio/product/lge/T57207s.jpg?im=Resize,width=750",
                description: "Light and airy natural stripe curtains"
            },
            {
                id: 6,
                name: "Motorized Smart Blackout",
                category: "blackout",
                price: 85000,
                currency: "RWF",
                image: "http://www.smartwingshome.com/cdn/shop/files/8_5d24812d-4ce4-45f4-bbcd-f6d2f77ce4d5.jpg?v=1754888806",
                description: "90% blackout with motorized convenience"
            }
        ];

        let cart = [];
        let currentFabric = 'cream';

        function renderProducts(filter = 'all') {
            const grid = document.getElementById('product-grid');
            const filtered = filter === 'all' ? products : products.filter(p => p.category === filter);
            
            grid.innerHTML = filtered.map(product => `
                <div class="product-card group bg-white rounded-2xl overflow-hidden shadow-sm hover:shadow-xl transition-all duration-300 border border-stone-100">
                    <div class="relative overflow-hidden aspect-[3/4] bg-stone-100">
                        <img src="${product.image}" alt="${product.name}" class="w-full h-full object-cover transform group-hover:scale-105 transition-transform duration-500">
                        <div class="product-overlay absolute inset-0 bg-black/40 opacity-0 transition-opacity duration-300 flex items-center justify-center">
                            <button onclick="addToCart(${product.id})" class="px-6 py-3 bg-white text-stone-900 rounded-full font-medium hover:bg-amber-700 hover:text-white transition-colors transform translate-y-4 group-hover:translate-y-0 transition-transform">
                                Add to Quote
                            </button>
                        </div>
                        <span class="absolute top-4 left-4 px-3 py-1 bg-white/90 backdrop-blur text-xs font-medium text-stone-600 rounded-full uppercase tracking-wider">${product.category}</span>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-semibold text-stone-900 mb-2">${product.name}</h3>
                        <p class="text-stone-500 text-sm mb-3">${product.description}</p>
                        <div class="flex justify-between items-center">
                            <span class="text-2xl font-bold text-amber-700 serif">${product.currency} ${product.price.toLocaleString()}</span>
                            <div class="flex space-x-1">
                                <i data-lucide="star" class="w-4 h-4 text-amber-500 fill-current"></i>
                                <i data-lucide="star" class="w-4 h-4 text-amber-500 fill-current"></i>
                                <i data-lucide="star" class="w-4 h-4 text-amber-500 fill-current"></i>
                                <i data-lucide="star" class="w-4 h-4 text-amber-500 fill-current"></i>
                                <i data-lucide="star" class="w-4 h-4 text-amber-500 fill-current"></i>
                            </div>
                        </div>
                    </div>
                </div>
            `).join('');
            
            lucide.createIcons();
        }

        function filterProducts(category) {
            document.querySelectorAll('.filter-btn').forEach(btn => {
                if(btn.dataset.filter === category) {
                    btn.classList.add('bg-amber-700', 'text-white', 'border-amber-700');
                    btn.classList.remove('text-stone-600', 'border-stone-300');
                } else {
                    btn.classList.remove('bg-amber-700', 'text-white', 'border-amber-700');
                    btn.classList.add('text-stone-600', 'border-stone-300');
                }
            });
            renderProducts(category);
        }

        function toggleCart() {
            const drawer = document.getElementById('cart-drawer');
            const overlay = document.getElementById('cart-overlay');
            
            if(drawer.classList.contains('cart-closed')) {
                drawer.classList.remove('cart-closed');
                drawer.classList.add('cart-open');
                overlay.classList.remove('hidden');
                setTimeout(() => overlay.classList.remove('opacity-0'), 10);
            } else {
                drawer.classList.remove('cart-open');
                drawer.classList.add('cart-closed');
                overlay.classList.add('opacity-0');
                setTimeout(() => overlay.classList.add('hidden'), 300);
            }
        }

        function addToCart(productId) {
            const product = products.find(p => p.id === productId);
            const existingItem = cart.find(item => item.id === productId);
            
            if(existingItem) {
                existingItem.quantity++;
            } else {
                cart.push({...product, quantity: 1});
            }
            
            updateCart();
            toggleCart();
        }

        function addCustomToCart() {
            const width = document.getElementById('width-input').value || 48;
            const length = document.getElementById('length-input').value || 84;
            const style = document.getElementById('style-select').value;
            const price = calculateCustomPrice();
            
            const customItem = {
                id: 'custom-' + Date.now(),
                name: `Custom ${currentFabric.charAt(0).toUpperCase() + currentFabric.slice(1)} Curtains`,
                price: price,
                currency: "RWF",
                quantity: 1,
                isCustom: true,
                details: `${width}" × ${length}" • ${style}`
            };
            
            cart.push(customItem);
            updateCart();
            toggleCart();
        }

        function removeFromCart(itemId) {
            cart = cart.filter(item => item.id !== itemId);
            updateCart();
        }

        function updateCart() {
            const cartItems = document.getElementById('cart-items');
            const cartBadge = document.getElementById('cart-badge');
            const cartTotal = document.getElementById('cart-total');
            
            const totalItems = cart.reduce((sum, item) => sum + item.quantity, 0);
            const totalPrice = cart.reduce((sum, item) => sum + (item.price * item.quantity), 0);
            
            if(totalItems > 0) {
                cartBadge.textContent = totalItems;
                cartBadge.classList.remove('hidden');
            } else {
                cartBadge.classList.add('hidden');
            }
            
            cartTotal.textContent = 'RWF ' + totalPrice.toLocaleString();
            
            if(cart.length === 0) {
                cartItems.innerHTML = '<p class="text-stone-500 text-center py-12">No items selected. Browse our collection or DM us on Instagram.</p>';
            } else {
                cartItems.innerHTML = cart.map(item => `
                    <div class="flex space-x-4 bg-stone-50 p-4 rounded-xl">
                        <div class="w-20 h-24 bg-stone-200 rounded-lg flex-shrink-0 overflow-hidden">
                            ${item.isCustom ? 
                                `<div class="w-full h-full" style="background-color: ${getFabricColor(item.name.split(' ')[1].toLowerCase())}"></div>` :
                                `<img src="${item.image}" class="w-full h-full object-cover">`
                            }
                        </div>
                        <div class="flex-1">
                            <h4 class="font-semibold text-stone-900">${item.name}</h4>
                            ${item.details ? `<p class="text-sm text-stone-500">${item.details}</p>` : ''}
                            <div class="flex justify-between items-center mt-2">
                                <span class="text-amber-700 font-medium">RWF ${item.price.toLocaleString()} × ${item.quantity}</span>
                                <button onclick="removeFromCart('${item.id}')" class="text-stone-400 hover:text-red-500 transition-colors">
                                    <i data-lucide="trash-2" class="w-4 h-4"></i>
                                </button>
                            </div>
                        </div>
                    </div>
                `).join('');
                lucide.createIcons();
            }
        }

        function selectFabric(fabric) {
            currentFabric = fabric;
            const colors = {
                'cream': '#F5F5DC', 'navy': '#1e3a5f', 'sage': '#87A878',
                'terracotta': '#E2725B', 'charcoal': '#36454F',
                'blush': '#F4C2C2', 'gold': '#D4AF37', 'white': '#FFFFFF'
            };
            
            document.getElementById('left-curtain').style.backgroundColor = colors[fabric];
            document.getElementById('right-curtain').style.backgroundColor = colors[fabric];
            
            document.querySelectorAll('.fabric-btn').forEach(btn => {
                if(btn.dataset.fabric === fabric) {
                    btn.classList.add('border-amber-700', 'ring-2', 'ring-amber-700');
                    btn.classList.remove('border-transparent');
                } else {
                    btn.classList.remove('border-amber-700', 'ring-2', 'ring-amber-700');
                    btn.classList.add('border-transparent');
                }
            });
            
            updatePreview();
        }

        function getFabricColor(fabric) {
            const colors = {
                'cream': '#F5F5DC', 'navy': '#1e3a5f', 'sage': '#87A878',
                'terracotta': '#E2725B', 'charcoal': '#36454F',
                'blush': '#F4C2C2', 'gold': '#D4AF37', 'white': '#FFFFFF'
            };
            return colors[fabric] || '#F5F5DC';
        }

        function updatePreview() {
            const width = document.getElementById('width-input').value || 48;
            const length = document.getElementById('length-input').value || 84;
            const style = document.getElementById('style-select').value;
            const styleNames = {
                'pleated': 'Pinch Pleated', 'grommet': 'Grommet Top',
                'rod-pocket': 'Rod Pocket', 'tab-top': 'Tab Top'
            };
            
            document.getElementById('preview-details').textContent = 
                `${currentFabric.charAt(0).toUpperCase() + currentFabric.slice(1)} • ${width}" × ${length}" • ${styleNames[style]}`;
            
            const price = calculateCustomPrice();
            document.getElementById('custom-price').textContent = 'RWF ' + price.toLocaleString();
        }

        function calculateCustomPrice() {
            const width = parseInt(document.getElementById('width-input').value) || 48;
            const length = parseInt(document.getElementById('length-input').value) || 84;
            const basePrice = 15000;
            const area = (width * length) / 144;
            const fabricMultiplier = {
                'cream': 1, 'white': 1, 'sage': 1.2, 'blush': 1.2,
                'navy': 1.4, 'charcoal': 1.4, 'terracotta': 1.5, 'gold': 1.8
            };
            return Math.round((basePrice + (area * 800)) * (fabricMultiplier[currentFabric] || 1));
        }

        renderProducts();
        selectFabric('cream');
    </script>
</body>
</html>
