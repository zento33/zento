<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MarketHub - Sell Anything</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* CSS Reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Arial, sans-serif;
        }
        
        /* Main Styles */
        body {
            background-color: #ffffff;
            color: #333333;
            line-height: 1.6;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* Header */
        header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
            position: sticky;
            top: 0;
            z-index: 100;
            padding: 15px 0;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 24px;
            font-weight: 700;
            color: #333;
        }
        
        .logo span {
            color: #4a6bff;
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 25px;
        }
        
        nav ul li a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: #4a6bff;
        }
        
        .user-actions a {
            margin-left: 15px;
            color: #333;
            text-decoration: none;
            font-size: 18px;
        }
        
        /* Hero Section */
        .hero {
            background-color: #f9f9f9;
            padding: 80px 0;
            text-align: center;
        }
        
        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
            color: #222;
        }
        
        .hero p {
            font-size: 20px;
            color: #666;
            max-width: 700px;
            margin: 0 auto 30px;
        }
        
        .btn {
            display: inline-block;
            padding: 12px 30px;
            border-radius: 4px;
            text-decoration: none;
            font-weight: 600;
            margin: 0 10px;
            transition: all 0.3s;
        }
        
        .btn-primary {
            background-color: #4a6bff;
            color: white;
        }
        
        .btn-primary:hover {
            background-color: #3a5bef;
            transform: translateY(-2px);
        }
        
        .btn-secondary {
            background-color: white;
            color: #4a6bff;
            border: 1px solid #4a6bff;
        }
        
        .btn-secondary:hover {
            background-color: #f5f7ff;
        }
        
        /* Categories */
        .categories {
            padding: 60px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 40px;
            font-size: 32px;
            color: #222;
        }
        
        .category-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }
        
        .category-card {
            background: white;
            border-radius: 8px;
            padding: 30px 20px;
            text-align: center;
            box-shadow: 0 3px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s;
            cursor: pointer;
        }
        
        .category-card:hover {
            transform: translateY(-5px);
        }
        
        .category-card i {
            font-size: 40px;
            color: #4a6bff;
            margin-bottom: 15px;
        }
        
        .category-card h3 {
            font-size: 18px;
        }
        
        /* Products */
        .products {
            padding: 60px 0;
            background-color: #f9f9f9;
        }
        
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 25px;
        }
        
        .product-card {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 3px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s;
        }
        
        .product-card:hover {
            transform: translateY(-5px);
        }
        
        .product-image {
            height: 200px;
            background-color: #eee;
            background-size: cover;
            background-position: center;
        }
        
        .product-info {
            padding: 20px;
        }
        
        .product-title {
            font-size: 18px;
            margin-bottom: 10px;
        }
        
        .product-price {
            font-weight: 700;
            color: #4a6bff;
            font-size: 20px;
            margin-bottom: 15px;
        }
        
        .product-seller {
            color: #666;
            font-size: 14px;
            margin-bottom: 15px;
        }
        
        .product-rating {
            color: #ffc107;
            margin-bottom: 15px;
        }
        
        .add-to-cart {
            width: 100%;
            padding: 10px;
            background-color: #4a6bff;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-weight: 600;
            transition: background-color 0.3s;
        }
        
        .add-to-cart:hover {
            background-color: #3a5bef;
        }
        
        /* Footer */
        footer {
            background-color: white;
            padding: 60px 0 20px;
            box-shadow: 0 -2px 10px rgba(0,0,0,0.05);
        }
        
        .footer-columns {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }
        
        .footer-column h3 {
            font-size: 18px;
            margin-bottom: 20px;
            color: #222;
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column ul li a {
            text-decoration: none;
            color: #666;
            transition: color 0.3s;
        }
        
        .footer-column ul li a:hover {
            color: #4a6bff;
        }
        
        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid #eee;
            color: #666;
            font-size: 14px;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
            }
            
            nav ul {
                margin: 20px 0;
            }
            
            .user-actions {
                margin-top: 15px;
            }
            
            .hero h1 {
                font-size: 36px;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">Market<span>Hub</span></div>
                
                <nav>
                    <ul>
                        <li><a href="#">Home</a></li>
                        <li><a href="#">Browse</a></li>
                        <li><a href="#">Sell</a></li>
                        <li><a href="#">About</a></li>
                        <li><a href="#">Contact</a></li>
                    </ul>
                </nav>
                
                <div class="user-actions">
                    <a href="#"><i class="fas fa-search"></i></a>
                    <a href="#"><i class="fas fa-heart"></i></a>
                    <a href="#"><i class="fas fa-user"></i></a>
                    <a href="#"><i class="fas fa-shopping-cart"></i></a>
                </div>
            </div>
        </div>
    </header>
    
    <section class="hero">
        <div class="container">
            <h1>Sell Anything, Buy Everything</h1>
            <p>The ultimate marketplace for all your buying and selling needs. Join thousands of happy users today.</p>
            <div class="cta-buttons">
                <a href="#" class="btn btn-primary">Start Selling</a>
                <a href="#" class="btn btn-secondary">Browse Items</a>
            </div>
        </div>
    </section>
    
    <section class="categories">
        <div class="container">
            <h2 class="section-title">Popular Categories</h2>
            <div class="category-grid">
                <div class="category-card">
                    <i class="fas fa-tshirt"></i>
                    <h3>Clothing</h3>
                </div>
                <div class="category-card">
                    <i class="fas fa-laptop"></i>
                    <h3>Electronics</h3>
                </div>
                <div class="category-card">
                    <i class="fas fa-home"></i>
                    <h3>Home Goods</h3>
                </div>
                <div class="category-card">
                    <i class="fas fa-book"></i>
                    <h3>Books</h3>
                </div>
                <div class="category-card">
                    <i class="fas fa-gamepad"></i>
                    <h3>Games</h3>
                </div>
            </div>
        </div>
    </section>
    
    <section class="products">
        <div class="container">
            <h2 class="section-title">Featured Products</h2>
            <div class="product-grid" id="productGrid">
                <!-- Products will be loaded here -->
            </div>
        </div>
    </section>
    
    <footer>
        <div class="container">
            <div class="footer-columns">
                <div class="footer-column">
                    <h3>MarketHub</h3>
                    <p>The best online marketplace for buying and selling new and used items.</p>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#">Home</a></li>
                        <li><a href="#">Browse</a></li>
                        <li><a href="#">Sell</a></li>
                        <li><a href="#">My Account</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Help</h3>
                    <ul>
                        <li><a href="#">FAQs</a></li>
                        <li><a href="#">Shipping</a></li>
                        <li><a href="#">Returns</a></li>
                        <li><a href="#">Contact Us</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Legal</h3>
                    <ul>
                        <li><a href="#">Terms of Service</a></li>
                        <li><a href="#">Privacy Policy</a></li>
                        <li><a href="#">Cookie Policy</a></li>
                    </ul>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 MarketHub. All rights reserved.</p>
            </div>
        </div>
    </footer>
    
    <script>
        // Sample product data
        const products = [
            {
                id: 1,
                title: "Wireless Headphones",
                price: 89.99,
                seller: "AudioTech",
                rating: 4,
                image: "https://images.unsplash.com/photo-1505740420928-5e560c06d30e?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
            },
            {
                id: 2,
                title: "Smart Watch",
                price: 199.99,
                seller: "TechGadgets",
                rating: 5,
                image: "https://images.unsplash.com/photo-1523275335684-37898b6baf30?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
            },
            {
                id: 3,
                title: "Leather Wallet",
                price: 29.99,
                seller: "FashionHub",
                rating: 4,
                image: "https://images.unsplash.com/photo-1591561954555-607968c989ab?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
            },
            {
                id: 4,
                title: "Coffee Maker",
                price: 49.99,
                seller: "HomeEssentials",
                rating: 3,
                image: "https://images.unsplash.com/photo-1550583724-b2692b85b150?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
            },
            {
                id: 5,
                title: "Running Shoes",
                price: 79.99,
                seller: "SportZone",
                rating: 5,
                image: "https://images.unsplash.com/photo-1542291026-7eec264c27ff?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
            },
            {
                id: 6,
                title: "Backpack",
                price: 39.99,
                seller: "TravelGear",
                rating: 4,
                image: "https://images.unsplash.com/photo-1553062407-98eeb64c6a62?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60"
            }
        ];
        
        // Load products into the grid
        document.addEventListener('DOMContentLoaded', function() {
            const productGrid = document.getElementById('productGrid');
            
            products.forEach(product => {
                const productCard = document.createElement('div');
                productCard.className = 'product-card';
                
                let stars = '';
                for (let i = 0; i < 5; i++) {
                    if (i < product.rating) {
                        stars += '<i class="fas fa-star"></i>';
                    } else {
                        stars += '<i class="far fa-star"></i>';
                    }
                }
                
                productCard.innerHTML = `
                    <div class="product-image" style="background-image: url('${product.image}')"></div>
                    <div class="product-info">
                        <h3 class="product-title">${product.title}</h3>
                        <div class="product-price">$${product.price.toFixed(2)}</div>
                        <div class="product-seller">Sold by ${product.seller}</div>
                        <div class="product-rating">${stars}</div>
                        <button class="add-to-cart">Add to Cart</button>
                    </div>
                `;
                
                productGrid.appendChild(productCard);
            });
        });
    </script>
</body>
</html>
