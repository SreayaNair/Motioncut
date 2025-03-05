<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Product Page - Modern E-commerce</title>
    <style>
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }

        body {
            background-color: #f9f9f9;
            color: #333;
            line-height: 1.6;
            margin: 0;
            padding: 0;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background-color: #2c3e50;
            padding: 1rem 2rem;
            color: white;
        }

        .navbar .logo {
            font-size: 1.5rem;
            font-weight: bold;
        }

        .nav-links {
            list-style: none;
            display: flex;
            gap: 1.5rem;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-size: 1rem;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: #f39c12;
        }
        .product-container {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: center;
            padding: 2rem;
            gap: 2rem;
            background-color: white;
            margin: 2rem auto;
            max-width: 1200px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        }
        .product-image img {
            width: 100%;
            max-width: 500px;
            border-radius: 10px;
        }
        .product-details {
            max-width: 500px;
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        .product-name {
            font-size: 2rem;
            color: #2c3e50;
        }

        .product-description {
            font-size: 1rem;
            color: #555;
        }

        .product-price {
            font-size: 1.5rem;
            font-weight: bold;
            color: #e74c3c;
        }

        .add-to-cart {
            padding: 0.8rem 1.5rem;
            font-size: 1rem;
            background-color: #e74c3c;
            color: white;
            border: none;
            cursor: pointer;
            border-radius: 5px;
            transition: background-color 0.3s ease;
        }

        .add-to-cart:hover {
            background-color: #c0392b;
        }
        .footer {
            text-align: center;
            padding: 1rem;
            background-color: #2c3e50;
            color: white;
            margin-top: 2rem;
        }
        @media (max-width: 768px) {
            .product-container {
                flex-direction: column;
                padding: 1rem;
            }

            .nav-links {
                gap: 1rem;
            }

            .product-name {
                font-size: 1.5rem;
            }

            .product-description {
                font-size: 0.9rem;
            }

            .product-price {
                font-size: 1.2rem;
            }

            .add-to-cart {
                font-size: 0.9rem;
            }
        }
    </style>
</head>
<body>

    <nav class="navbar">
        <div class="logo">MyShop</div>
        <ul class="nav-links">
            <li><a href="#">Home</a></li>
            <li><a href="#">Shop</a></li>
            <li><a href="#">Contact</a></li>
            <li><a href="#">Cart</a></li>
        </ul>
    </nav>
    <section class="product-container">
        <div class="product-image">
            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR8KnAmKGk_zEOmoeak2uvWDERR6CFlP0FwQA&s" alt="Product Image">
        </div>

        <div class="product-details">
            <h1 class="product-name">Stylish Modern Chair</h1>
            <p class="product-description">This sleek and comfortable modern chair is perfect for your living room or office. Featuring high-quality materials and a contemporary design, it adds elegance to any space.</p>
            <p class="product-price">$149.99</p>
            <button class="add-to-cart">Add to Cart</button>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <p>&copy; 2025 MyShop. All Rights Reserved.</p>
    </footer>

</body>
</html>
