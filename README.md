<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Coffee Shop Menu</title>
    
    <!-- MENU CONFIGURATION - EDIT ITEMS HERE -->
    <script>
        // Menu data structure - edit this to update the menu
        const menuData = {
            // Hot Drinks Tab
            "hot-drinks": {
                title: "Hot Drinks",
                categories: {
                    "coffee": {
                        title: "Coffee",
                        items: [
                            {
                                name: "Latte",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/9fbf6fd11c863fb571814ffec7756f03/58f691da9eaef86b0b51f9b2c483fe63.jpeg",
                                description: "Rich espresso and steamed milk come together in a velvety blend.",
                                sizes: ["12oz", "16oz", "20oz"],
                                prices: {
                                    "12oz": 3.30,
                                    "16oz": 3.50,
                                    "20oz": 3.90
                                },
                                defaultSize: "12oz"
                            },
                            {
                                name: "Cappuccino",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/571316e02dd2dee87b9473a8326292dc/58f691da9eaef86b0b51f9b2c483fe63.jpeg",
                                description: "Bold espresso, smooth steamed milk, and a layer of velvety foam.",
                                sizes: ["12oz", "16oz", "20oz"],
                                prices: {
                                    "12oz": 3.30,
                                    "16oz": 3.50,
                                    "20oz": 3.90
                                },
                                defaultSize: "12oz"
                            },
                            {
                                name: "Mocha",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/ca9f7b7a803ccd75f6e857079a84c2e8/58f691da9eaef86b0b51f9b2c483fe63.jpeg",
                                description: "Bold espresso, steamed milk, and chocolate combine in an indulgent coffee.",
                                sizes: ["12oz", "16oz", "20oz"],
                                prices: {
                                    "12oz": 3.45,
                                    "16oz": 3.65,
                                    "20oz": 4.05
                                },
                                defaultSize: "12oz"
                            },
                            {
                                name: "Flat White",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/29819ed1bdbe2d9be8ade166412a0e89/58f691da9eaef86b0b51f9b2c483fe63.jpeg",
                                description: "Stronger coffee and a subtle layer of microfoam.",
                                sizes: ["8oz", "12oz"],
                                prices: {
                                    "8oz": 3.30,
                                    "12oz": 3.50
                                },
                                defaultSize: "8oz"
                            },
                            {
                                name: "Americano",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/36658a40f506d50b79ffeaa8ca605da8/58f691da9eaef86b0b51f9b2c483fe63.jpeg",
                                description: "A rich, full-bodied coffee made with bold espresso and hot water.",
                                sizes: ["12oz", "16oz", "20oz"],
                                prices: {
                                    "12oz": 2.95,
                                    "16oz": 3.15,
                                    "20oz": 3.35
                                },
                                defaultSize: "12oz"
                            },
                            {
                                name: "Cortado",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/d81e83ef548b0118e1ee0d2bb788dcc9/58f691da9eaef86b0b51f9b2c483fe63.jpeg",
                                description: "A perfect balance of espresso and smooth steamed milk, in a delicate and velvety ratio.",
                                sizes: ["6oz"],
                                prices: {
                                    "6oz": 3.30
                                },
                                defaultSize: "6oz"
                            },
                            {
                                name: "Espresso",
                                image: "https://u.cubeupload.com/ryanjhope/espresso.png",
                                description: "Pure espresso, served in a small cup.",
                                sizes: ["Single", "Double"],
                                prices: {
                                    "Single": 2.30,
                                    "Double": 2.50
                                },
                                defaultSize: "Single",
                                disableCustomization: true
                            }
                            // Add more coffee items here
                        ]
                    },
                    "specialty-coffee": {
                        title: "Specialty Coffee",
                        items: [
                            {
                                name: "Matcha Latte",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/af107c3b5621fdc5ff25d27212f0c0bb/bc9c318a9c96996e2d990faf2b0c65f6.jpeg",
                                description: "Subtle, grassy flavor of green tea combined with smooth steamed milk.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.40,
                                    "20oz": 4.60
                                },
                                defaultSize: "16oz"
                            },
                            {
                                name: "Pistachio Cream Latte",
                                image: "https://u.cubeupload.com/ryanjhope/CopyofpistachioIced.png",
                                description: "Latte made with creamy pistachio butter, topped with sauce and real pistachio crumbs.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.40,
                                    "20oz": 4.60
                                },
                                defaultSize: "16oz",
                                badge: "NEW" // Added badge
                            }
                        ]
                    },
                    "hot-chocolate": {
                        title: "Hot Chocolate",
                        items: [
                            {
                                name: "Crunchie Hot Chocolate",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/dcf9ea138be6a31aef3c03cd64bd25b9/bc9c318a9c96996e2d990faf2b0c65f6.jpeg",
                                description: "Rich chocolate and honeycomb flavouring, topped with real Crunchie.",
                                sizes: ["12oz", "16oz", "20oz"],
                                prices: {
                                    "12oz": 3.90,
                                    "16oz": 4.10,
                                    "20oz": 4.50
                                },
                                defaultSize: "12oz"
                            }
                        ]
                    },
                    "tea": {
                        title: "Tea",
                        items: [
                            {
                                name: "English Breakfast Tea",
                                image: null, // No image provided
                                description: "A traditional blend of black teas with a full-bodied, robust flavor.",
                                sizes: ["16oz"], // Standard size only
                                prices: {
                                    "16oz": 2.60
                                },
                                defaultSize: "16oz",
                                itemType: "tea", // Custom item type for tea-specific options
                                singleSize: true // Flag to indicate this has only one size
                            },
                            {
                                name: "Earl Grey",
                                image: null,
                                description: "Black tea infused with bergamot oil, giving it a distinctive citrus flavor.",
                                sizes: ["16oz"],
                                prices: {
                                    "16oz": 2.60
                                },
                                defaultSize: "16oz",
                                itemType: "herbal-tea",
                                singleSize: true
                            },
                            {
                                name: "Green Tea",
                                image: null,
                                description: "Light, refreshing tea with a smooth, delicate flavor.",
                                sizes: ["16oz"],
                                prices: {
                                    "16oz": 2.60
                                },
                                defaultSize: "16oz",
                                itemType: "herbal-tea",
                                singleSize: true
                            },
                            {
                                name: "Peppermint Tea",
                                image: null,
                                description: "Refreshing and cool herbal tea with a clean, minty flavor.",
                                sizes: ["16oz"],
                                prices: {
                                    "16oz": 2.60
                                },
                                defaultSize: "16oz",
                                itemType: "herbal-tea",
                                singleSize: true
                            },
                            {
                                name: "Lemon & Ginger Tea",
                                image: null,
                                description: "Warming herbal infusion of ginger and lemon, soothing and invigorating.",
                                sizes: ["16oz"],
                                prices: {
                                    "16oz": 2.60
                                },
                                defaultSize: "16oz",
                                itemType: "herbal-tea",
                                singleSize: true
                            },
                            {
                                name: "Blackberry & Raspberry Tea",
                                image: null,
                                description: "Sweet and fruity infusion with bright berry flavors.",
                                sizes: ["16oz"],
                                prices: {
                                    "16oz": 2.60
                                },
                                defaultSize: "16oz",
                                itemType: "herbal-tea",
                                singleSize: true
                            }
                        ]
                    }
                }
            },
            // Cold Drinks Tab
            "cold-drinks": {
                title: "Cold Drinks",
                categories: {
                    "iced-coffee": {
                        title: "Iced Coffee",
                        items: [
                            {
                                name: "Pistachio Iced Latte",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/e06df32a1fb2dc9d9f2d92585a4937c9/58f691da9eaef86b0b51f9b2c483fe63.jpeg",
                                description: "Iced Latte made with creamy and rich pistachio butter.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.10,
                                    "20oz": 4.25
                                },
                                defaultSize: "16oz"
                            }
                        ]
                    },
                    "blended-drinks": {
                        title: "Blended Drinks",
                        items: [
                            // Add blended drinks here
                        ]
                    },
                    "refreshers": {
                        title: "Refreshers",
                        items: [
                            // Add refreshers here
                        ]
                    }
                }
            },
            // Food Tab
            "food": {
                title: "Food",
                categories: {
                    "pastries": {
                        title: "Pastries",
                        items: [
                            {
                                name: "Cinnamon Swirl",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/fb76fa210734e7d46d4708377ed7d354/58f691da9eaef86b0b51f9b2c483fe63.jpeg",
                                price: 2.45,
                                foodItem: true
                            },
                            {
                                name: "Chocolate Twist",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/54e41537c0958d8a12b0c9f3f0607056/58f691da9eaef86b0b51f9b2c483fe63.jpeg",
                                price: 2.50,
                                foodItem: true
                            },
                            {
                                name: "Butter Croissant",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/158df3c8bd7a25888f15dcb1bbf1f13b/58f691da9eaef86b0b51f9b2c483fe63.jpeg",
                                price: 2.20,
                                foodItem: true
                            },
                            {
                                name: "Pain Aux Raisin",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/2c02391621e0537b4d36ef08d3ed9b3c/58f691da9eaef86b0b51f9b2c483fe63.jpeg",
                                price: 2.45,
                                foodItem: true
                            },
                            {
                                name: "Apple Crown",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/e030340445b6f053a977cca165f3dfc4/58f691da9eaef86b0b51f9b2c483fe63.jpeg",
                                price: 2.80,
                                foodItem: true
                            },
                            {
                                name: "Pistachio Croissant",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/6c48b522cc34eddbf58dfe7fb3c4b8a5/bc9c318a9c96996e2d990faf2b0c65f6.jpeg",
                                price: 3.45,
                                foodItem: true,
                                badge: "POPULAR" // Added badge
                            },
                            {
                                name: "Almond Croissant",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/55bfb2ff9fed75b5a7d7e171d0686804/bc9c318a9c96996e2d990faf2b0c65f6.jpeg",
                                price: 2.40,
                                foodItem: true
                            },
                            {
                                name: "Large Fruit Scone",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/9f842cf2cd1e7f56511fe585a3a6b3bf/bc9c318a9c96996e2d990faf2b0c65f6.jpeg",
                                price: 2.50,
                                foodItem: true
                            },
                            {
                                name: "Toasted Tea Cake",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/307b37e61ae9f702391b615925d89c9b/bc9c318a9c96996e2d990faf2b0c65f6.jpeg",
                                price: 2.50,
                                foodItem: true
                            }
                        ]
                    },
                    "toasties": {
                        title: "Toasties",
                        items: [
                            {
                                name: "Ham & Cheese Toastie",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/3f2ab241ff4876626d22488bb6366c97/bc9c318a9c96996e2d990faf2b0c65f6.jpeg",
                                price: 3.70,
                                foodItem: true
                            },
                            {
                                name: "Cheese & Onion Toastie",
                                image: null,
                                price: 3.70,
                                foodItem: true
                            },
                            {
                                name: "Cheese & Tomato Toastie",
                                image: null,
                                price: 3.70,
                                foodItem: true
                            },
                            {
                                name: "BBQ Chicken Panini",
                                image: null,
                                price: 4.50,
                                foodItem: true
                            },
                            {
                                name: "Sweet Chilli Chicken Panini",
                                image: null,
                                price: 4.50,
                                foodItem: true
                            },
                            {
                                name: "Ham & Cheese Panini",
                                image: null,
                                price: 4.50,
                                foodItem: true
                            },
                            {
                                name: "Ham & Cheese Croque",
                                image: null,
                                price: 4.50,
                                foodItem: true
                            },
                            {
                                name: "Mushroom Croque",
                                image: null,
                                price: 4.50,
                                foodItem: true
                            }
                        ]
                    },
                    "cakes-treats": {
                        title: "Cakes & Treats",
                        items: [
                            {
                                name: "Honeycomb Tiffin",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/2fda9f7d2e3f4a111a9fc4295d0d35a1/58f691da9eaef86b0b51f9b2c483fe63.jpeg",
                                price: 2.60,
                                foodItem: true
                            },
                            {
                                name: "Apple Slice",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/d1de5478b0e171640d594dbf19381255/58f691da9eaef86b0b51f9b2c483fe63.jpeg",
                                price: 2.60,
                                foodItem: true
                            },
                            {
                                name: "Apricot Slice",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/dd850ad4d007baf753597ad302fcb851/bc9c318a9c96996e2d990faf2b0c65f6.jpeg",
                                price: 2.60,
                                foodItem: true
                            },
                            {
                                name: "Tiramisu Slice",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/c1ccbbc0851e35cce954540722bcbcc4/bc9c318a9c96996e2d990faf2b0c65f6.jpeg",
                                price: 2.60,
                                foodItem: true
                            },
                            {
                                name: "Oreo Muffin",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/e5765c394d426af12b5b32428ab2e748/58f691da9eaef86b0b51f9b2c483fe63.jpeg",
                                price: 2.60,
                                foodItem: true
                            },
                            {
                                name: "Chocolate Muffin",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/e3c835a249d1dd0aa8d3e6ddf2aac756/bc9c318a9c96996e2d990faf2b0c65f6.jpeg",
                                price: 2.60,
                                foodItem: true
                            },
                            {
                                name: "Blueberry Muffin",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/f5e690e36716ab783ddee68fce7ed57f/58f691da9eaef86b0b51f9b2c483fe63.jpeg",
                                price: 2.60,
                                foodItem: true
                            }
                        ]
                    }
                }
            }
        };
        
        // Available extras for coffee and general items
        const extras = [
            {
                id: "decaf",
                name: "Decaf",
                price: 0.00
            },
            {
                id: "extra-shot",
                name: "Extra Shot",
                price: 0.50
            },
            {
                id: "whipped-cream",
                name: "Whipped Cream",
                price: 0.50
            },
            {
                id: "syrup",
                name: "Add Syrup",
                price: 0.50
            }
        ];
        
        // Tea-specific extras (with decaf)
        const teaExtras = [
            {
                id: "decaf",
                name: "Decaf",
                price: 0.00
            },
            {
                id: "extra-tea-bag",
                name: "Extra Tea Bag",
                price: 0.30
            }
        ];
        
        // Herbal tea extras (without decaf, just extra tea bag)
        const herbalTeaExtras = [
            {
                id: "extra-tea-bag",
                name: "Extra Tea Bag",
                price: 0.30
            }
        ];
        
        // Available milk options
        const milkOptions = [
            {
                id: "soya",
                name: "Soya",
                price: 0.00
            },
            {
                id: "oat",
                name: "Oat",
                price: 0.50
            },
            {
                id: "coconut",
                name: "Coconut",
                price: 0.50
            },
            {
                id: "almond",
                name: "Almond",
                price: 0.50
            }
        ];
        
        // Tea-specific milk options with reduced prices
        const teaMilkOptions = [
            {
                id: "soya",
                name: "Soya",
                price: 0.00
            },
            {
                id: "oat",
                name: "Oat",
                price: 0.25
            },
            {
                id: "coconut",
                name: "Coconut",
                price: 0.25
            },
            {
                id: "almond",
                name: "Almond",
                price: 0.25
            }
        ];
    </script>
    
    <!-- Inline Tailwind to avoid external dependency issues -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: '#f86400',
                    }
                }
            }
        }
    </script>
    <!-- Poppins font -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        /* Essential styles that don't rely on Tailwind */
        html, body {
            width: 100%;
            height: 100%;
            margin: 0;
            padding: 0;
            font-family: 'Poppins', sans-serif !important;
            background-color: white;
            color: #555555;
            font-weight: 500;
            text-shadow: 0 0 1px rgba(255, 255, 255, 0.5);
        }
        
        /* Make the menu container fill the embed space */
        #menu-container {
            width: 100%;
            height: 100%;
            overflow-y: auto;
            padding: 10px;
            box-sizing: border-box;
            text-align: center;
        }
        
        /* Tab functionality */
        .tab-content {
            display: none;
        }
        .tab-content.active {
            display: block;
        }
        
        /* Category styles */
        .category-title {
            margin-top: 16px;
            margin-bottom: 16px;
            padding-bottom: 5px;
            display: inline-block;
            text-align: center;
            font-size: 1.5rem;
        }
        
        /* Responsive grid layout */
        .menu-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr); /* 2 columns by default (mobile) */
            gap: 12px;
            margin: 0 auto;
        }
        
        /* Medium screens - 3 columns */
        @media (min-width: 768px) {
            .menu-grid {
                grid-template-columns: repeat(3, 1fr);
                gap: 14px;
            }
        }
        
        /* Large screens - 4 columns */
        @media (min-width: 1024px) {
            .menu-grid {
                grid-template-columns: repeat(4, 1fr);
                gap: 16px;
            }
        }
        
        /* Menu item specific styles */
        .menu-item {
            border: none;
            border-radius: 16px;
            background-color: white;
            box-shadow: 0 1px 3px rgba(0,0,0,0.05);
            transition: all 0.3s ease, opacity 0.3s ease;
            overflow: hidden;
            text-align: center;
            position: relative;
        }
        
        /* Fade effect when an item is expanded */
        .has-expanded-item .menu-item:not(.expanded) {
            opacity: 0.4;
        }
        
        /* Image container - force square aspect ratio */
        .image-container {
            position: relative;
            width: 100%;
            padding-bottom: 100%; /* This creates a square aspect ratio */
            overflow: hidden;
        }
        
        /* No image placeholder */
        .no-image-placeholder {
            position: relative;
            width: 100%;
            padding-bottom: 60%; /* Shorter than image container */
            background-color: #f9f9f9;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }
        
        .placeholder-content {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            cursor: pointer;
        }
        
        /* Tile image styles - position absolute within the container */
        .item-image {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            cursor: pointer;
        }
        
        /* Item header styles */
        .item-header {
            padding: 10px;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            text-align: center;
            flex-direction: column;
        }
        
        /* Make menu item name smaller to fit multiple items per row */
        .item-header h4 {
            font-size: 16px;
            margin: 0;
            text-align: center;
            font-weight: 700;
        }
        
        /* Larger name for items without images */
        .large-name {
            font-size: 18px;
            font-weight: 700;
            margin: 0 0 8px 0;
        }
        
        /* Badge styling */
        .badge {
            position: absolute;
            top: 10px;
            left: 10px;
            color: white;
            padding: 2px 8px;
            border-radius: 20px;
            font-weight: 600;
            font-size: 12px;
            z-index: 20;
        }
        
        .badge-new {
            background-color: #4CAF50; /* Green */
        }
        
        .badge-popular {
            background-color: #FF9800; /* Orange */
        }
        
        /* Price badge */
        .price-badge {
            position: absolute;
            top: 10px;
            right: 10px;
            background-color: rgba(0, 0, 0, 0.4);
            color: white;
            padding: 3px 8px;
            border-radius: 20px;
            font-weight: 600;
            font-size: 14px;
            z-index: 10;
        }
        
        /* Inline price badge for items without images */
        .inline-price-badge {
            display: inline-block;
            background-color: rgba(0, 0, 0, 0.4);
            color: white;
            padding: 3px 8px;
            border-radius: 20px;
            font-weight: 600;
            font-size: 14px;
            margin-top: 8px;
        }
        
        /* Food item styles */
        .food-item-header {
            padding: 10px;
            text-align: center;
        }
        
        .food-item-name {
            font-size: 16px;
            font-weight: 700;
            margin: 0;
        }
        
        /* Empty category style */
        .empty-category {
            padding: 15px;
            color: #666;
            font-style: italic;
            grid-column: span 2;
            text-align: center;
        }
        
        /* Adjust empty category span for different screen sizes */
        @media (min-width: 768px) {
            .empty-category {
                grid-column: span 3;
            }
        }
        
        @media (min-width: 1024px) {
            .empty-category {
                grid-column: span 4;
            }
        }
        
        /* Description text */
        .item-details p {
            font-size: 12px;
            line-height: 1.4;
            text-align: center;
        }
        
        /* Center all headings */
        h2, h3, h4 {
            text-align: center;
        }
        
        /* Notice for non-customizable items */
        .no-customization-notice {
            font-size: 12px;
            color: #666;
            font-style: italic;
            margin-top: 8px;
        }
        
        /* Size info for single-sized items */
        .size-info {
            font-size: 12px;
            color: #666;
            margin: 8px 0;
        }
        
        /* Accordion styles */
        .item-details {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease;
            padding: 0 10px;
            text-align: center;
        }
        
        .menu-item.expanded .item-details {
            max-height: 800px;
            padding-bottom: 15px;
        }
        
        /* Options section styles */
        .options-section {
            margin: 15px 0;
            text-align: center;
        }
        
        .section-title {
            font-weight: 700;
            font-size: 14px;
            margin-bottom: 8px;
            color: #555555;
            text-align: center;
        }
        
        /* Button grid for options */
        .options-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            justify-content: center;
        }
        
        /* Option button styles */
        .option-btn {
            font-size: 12px;
            padding: 5px 10px;
            border-radius: 50px; /* Pill shape */
            background-color: #f3f4f6;
            border: 1px solid #e5e7eb;
            cursor: pointer;
            transition: all 0.2s ease;
            color: #555555;
            font-weight: 500;
            min-width: 56px;
            text-align: center;
            display: inline-block;
        }
        
        /* Size button styles - smaller padding for mobile */
        .size-btn {
            padding: 5px 8px;
            min-width: 48px;
            font-weight: 700; /* Bold text for size buttons */
        }
        
        .option-btn:hover {
            background-color: #e5e7eb;
        }
        
        .option-btn.active {
            background-color: #f86400;
            color: white;
            border-color: #f86400;
        }
        
        .option-btn.active:hover {
            background-color: #e05a00;
        }
        
        /* Section divider */
        .section-divider {
            width: 100%;
            margin: 20px 0;
            text-align: center;
            height: 2px;
            background-color: #f0f0f0;
            grid-column: 1 / -1;
        }
        
        /* Hidden class for customize container */
        .hidden {
            display: none;
        }
        
        /* Customize button styling */
        .customize-btn {
            display: inline-block;
            background-color: #f3f4f6;
            color: #555555;
            padding: 8px 20px;
            margin-top: 12px;
            border-radius: 50px;
            border: 1px solid #e5e7eb;
            font-weight: 600;
            font-size: 14px;
            cursor: pointer;
            transition: all 0.2s ease;
        }
        
        .customize-btn:hover {
            background-color: #e5e7eb;
        }
        
        .customize-btn.active {
            background-color: #f86400;
            color: white;
            border-color: #f86400;
        }
        
        /* Customize container transition */
        .customize-container {
            margin-top: 12px;
            transition: all 0.3s ease;
        }
    </style>
</head>
<body>
    <div id="menu-container" class="container mx-auto max-w-5xl bg-white">
        <!-- Tab Navigation -->
        <div class="tab-navigation mb-4 flex justify-center overflow-x-auto pb-1" id="tab-buttons">
            <!-- Tab buttons will be generated here -->
        </div>

        <!-- Menu Content -->
        <div class="tab-container" id="tab-content">
            <!-- Tab content will be generated here -->
        </div>
    </div>

    <script>
        // Global variable to track the currently expanded item
        let currentlyExpandedItem = null;
        
        // Generate menu from configuration
        document.addEventListener('DOMContentLoaded', function() {
            const tabButtonsContainer = document.getElementById('tab-buttons');
            const tabContentContainer = document.getElementById('tab-content');
            
            // Generate tab buttons
            let isFirst = true;
            for (const tabId in menuData) {
                const tab = menuData[tabId];
                
                // Create tab button
                const tabButton = document.createElement('button');
                tabButton.className = `tab-btn flex-shrink-0 px-4 py-2 mr-2 rounded-full ${isFirst ? 'active bg-primary text-white' : 'bg-gray-200 hover:bg-gray-300'} font-bold`;
                tabButton.dataset.tab = tabId;
                tabButton.textContent = tab.title;
                tabButton.style.fontFamily = "'Poppins', sans-serif";
                if (isFirst) {
                    tabButton.style.backgroundColor = '#f86400';
                } else {
                    tabButton.style.color = '#555555';
                }
                tabButtonsContainer.appendChild(tabButton);
                
                // Create tab content
                const tabContent = document.createElement('div');
                tabContent.id = tabId;
                tabContent.className = `tab-content ${isFirst ? 'active' : ''}`;
                
                // Add tab title
                const tabTitle = document.createElement('h2');
                tabTitle.className = 'text-3xl font-bold mb-4 text-center';
                tabTitle.style.fontFamily = "'Poppins', sans-serif";
                tabTitle.style.color = '#555555';
                tabTitle.style.textShadow = '0 0 1px rgba(248, 100, 0, 0.2)';
                tabTitle.textContent = tab.title;
                tabContent.appendChild(tabTitle);
                
                // Generate categories and items
                for (const categoryId in tab.categories) {
                    const category = tab.categories[categoryId];
                    
                    // Add category title
                    const categoryTitle = document.createElement('h3');
                    categoryTitle.className = 'text-2xl font-bold category-title text-center mx-auto';
                    categoryTitle.style.fontFamily = "'Poppins', sans-serif";
                    categoryTitle.style.color = '#555555';
                    categoryTitle.style.textShadow = '0 0 1px rgba(248, 100, 0, 0.15)';
                    categoryTitle.textContent = category.title;
                    tabContent.appendChild(categoryTitle);
                    
                    // Add items grid
                    const itemsGrid = document.createElement('div');
                    itemsGrid.className = 'menu-grid';
                    
                    // If no items, show "Coming soon"
                    if (category.items.length === 0) {
                        const emptyMessage = document.createElement('p');
                        emptyMessage.className = 'empty-category text-center';
                        emptyMessage.textContent = 'Coming soon!';
                        itemsGrid.appendChild(emptyMessage);
                    } else {
                        // Split items into those with images and those without
                        const itemsWithImages = [];
                        const itemsWithoutImages = [];
                        
                        category.items.forEach(item => {
                            if (item.image) {
                                itemsWithImages.push(item);
                            } else {
                                itemsWithoutImages.push(item);
                            }
                        });
                        
                        // First generate items with images
                        itemsWithImages.forEach((item, index) => {
                            const itemId = `${categoryId}-with-image-${index}`;
                            const itemElement = createMenuItem(item, itemId, categoryId);
                            itemsGrid.appendChild(itemElement);
                        });
                        
                        // If there are items without images, add a divider and then those items
                        if (itemsWithoutImages.length > 0 && itemsWithImages.length > 0) {
                            // Add a divider after items with images if needed
                            const divider = document.createElement('div');
                            divider.className = 'section-divider';
                            itemsGrid.appendChild(divider);
                        }
                        
                        // Then generate items without images
                        itemsWithoutImages.forEach((item, index) => {
                            const itemId = `${categoryId}-without-image-${index}`;
                            const itemElement = createMenuItem(item, itemId, categoryId);
                            itemsGrid.appendChild(itemElement);
                        });
                    }
                    
                    tabContent.appendChild(itemsGrid);
                }
                
                tabContentContainer.appendChild(tabContent);
                isFirst = false;
            }
            
            // Function to create a menu item element
            function createMenuItem(item, itemId, categoryId) {
                // Create item element
                const itemElement = document.createElement('div');
                itemElement.className = 'menu-item';
                itemElement.id = itemId;
                
                // Handle food items differently
                if (item.foodItem) {
                    // Create image container for the food item (same as drink items)
                    if (item.image) {
                        // Create image container with price badge (identical to drink items)
                        const imageContainer = document.createElement('div');
                        imageContainer.className = 'image-container';
                        
                        // Create image
                        const img = document.createElement('img');
                        img.className = 'item-image';
                        img.src = item.image;
                        img.alt = item.name;
                        
                        // Create price badge
                        const priceBadge = document.createElement('div');
                        priceBadge.className = 'price-badge';
                        priceBadge.textContent = `£${item.price.toFixed(2)}`;
                        
                        // Add badge if needed
                        if (item.badge) {
                            const badge = document.createElement('div');
                            badge.className = `badge badge-${item.badge.toLowerCase()}`;
                            
                            // Convert badge text to title case (first letter capitalized)
                            const badgeText = item.badge.charAt(0).toUpperCase() + item.badge.slice(1).toLowerCase();
                            badge.textContent = badgeText;
                            
                            itemElement.appendChild(badge);
                        }
                        
                        imageContainer.appendChild(img);
                        imageContainer.appendChild(priceBadge);
                        itemElement.appendChild(imageContainer);
                        
                        // Add name
                        const headerDiv = document.createElement('div');
                        headerDiv.className = 'food-item-header';
                        
                        const foodItemName = document.createElement('h4');
                        foodItemName.className = 'food-item-name';
                        foodItemName.textContent = item.name;
                        
                        headerDiv.appendChild(foodItemName);
                        itemElement.appendChild(headerDiv);
                    } else {
                        // Simple layout for food items without images
                        const placeholder = document.createElement('div');
                        placeholder.className = 'no-image-placeholder';
                        
                        const placeholderContent = document.createElement('div');
                        placeholderContent.className = 'placeholder-content';
                        
                        const foodItemName = document.createElement('h3');
                        foodItemName.className = 'large-name';
                        foodItemName.textContent = item.name;
                        
                        const foodItemPrice = document.createElement('div');
                        foodItemPrice.className = 'inline-price-badge';
                        foodItemPrice.textContent = `£${item.price.toFixed(2)}`;
                        
                        // Add badge if needed
                        if (item.badge) {
                            const badge = document.createElement('div');
                            badge.className = `badge badge-${item.badge.toLowerCase()}`;
                            
                            // Convert badge text to title case (first letter capitalized)
                            const badgeText = item.badge.charAt(0).toUpperCase() + item.badge.slice(1).toLowerCase();
                            badge.textContent = badgeText;
                            
                            itemElement.appendChild(badge);
                        }
                        
                        placeholderContent.appendChild(foodItemName);
                        placeholderContent.appendChild(foodItemPrice);
                        placeholder.appendChild(placeholderContent);
                        itemElement.appendChild(placeholder);
                    }
                    
                    return itemElement;
                }
                
                // Create regular item element
                if (item.image) {
                    // Create image container with price badge
                    const imageContainer = document.createElement('div');
                    imageContainer.className = 'image-container';
                    
                    // Create image
                    const img = document.createElement('img');
                    img.className = 'item-image';
                    img.src = item.image;
                    img.alt = item.name;
                    
                    // Create price badge
                    const priceBadge = document.createElement('div');
                    priceBadge.className = 'price-badge';
                    priceBadge.textContent = `£${item.prices[item.defaultSize].toFixed(2)}`;
                    
                    // Add badge if needed
                    if (item.badge) {
                        const badge = document.createElement('div');
                        badge.className = `badge badge-${item.badge.toLowerCase()}`;
                        
                        // Convert badge text to title case (first letter capitalized)
                        const badgeText = item.badge.charAt(0).toUpperCase() + item.badge.slice(1).toLowerCase();
                        badge.textContent = badgeText;
                        
                        itemElement.appendChild(badge);
                    }
                    
                    imageContainer.appendChild(img);
                    imageContainer.appendChild(priceBadge);
                    itemElement.appendChild(imageContainer);
                    
                    // Make image clickable to toggle accordion
                    img.addEventListener('click', function() {
                        toggleAccordion(itemElement);
                    });
                } else {
                    // Create placeholder for items without images - with price below name
                    const placeholder = document.createElement('div');
                    placeholder.className = 'no-image-placeholder';
                    
                    // Create content inside placeholder
                    const placeholderContent = document.createElement('div');
                    placeholderContent.className = 'placeholder-content';
                    
                    // Add large item name
                    const placeholderName = document.createElement('h3');
                    placeholderName.className = 'large-name';
                    placeholderName.textContent = item.name;
                    
                    // Add price below name in the same style as the price badge
                    const inlinePriceBadge = document.createElement('div');
                    inlinePriceBadge.className = 'inline-price-badge';
                    inlinePriceBadge.textContent = `£${item.prices[item.defaultSize].toFixed(2)}`;
                    
                    // Add badge if needed
                    if (item.badge) {
                        const badge = document.createElement('div');
                        badge.className = `badge badge-${item.badge.toLowerCase()}`;
                        badge.textContent = item.badge;
                        itemElement.appendChild(badge);
                    }
                    
                    placeholderContent.appendChild(placeholderName);
                    placeholderContent.appendChild(inlinePriceBadge);
                    placeholder.appendChild(placeholderContent);
                    itemElement.appendChild(placeholder);
                    
                    // Make placeholder clickable to toggle accordion
                    placeholderContent.addEventListener('click', function() {
                        toggleAccordion(itemElement);
                    });
                }
                
                // Create header with name (only for items with images)
                if (item.image) {
                    const headerDiv = document.createElement('div');
                    headerDiv.className = 'item-header text-center';
                    
                    // Item name
                    const itemName = document.createElement('h4');
                    itemName.className = 'text-md font-semibold text-center';
                    itemName.textContent = item.name;
                    
                    // Item price (hidden in header when using badge)
                    const priceSpan = document.createElement('span');
                    priceSpan.className = 'item-price font-semibold';
                    priceSpan.style.color = '#f86400';
                    priceSpan.style.display = 'none'; // Hidden but used for calculations
                    priceSpan.dataset.basePrice = item.prices ? item.prices[item.defaultSize] : item.price;
                    priceSpan.dataset.extras = '0.00';
                    
                    headerDiv.appendChild(itemName);
                    headerDiv.appendChild(priceSpan);
                    itemElement.appendChild(headerDiv);
                    
                    // Make header clickable to toggle accordion
                    headerDiv.addEventListener('click', function() {
                        toggleAccordion(itemElement);
                    });
                } else {
                    // For items without images, we still need the hidden price span
                    const priceSpan = document.createElement('span');
                    priceSpan.className = 'item-price font-semibold';
                    priceSpan.style.color = '#f86400';
                    priceSpan.style.display = 'none'; // Hidden but used for calculations
                    if (item.prices) {
                        priceSpan.dataset.basePrice = item.prices[item.defaultSize];
                    } else {
                        priceSpan.dataset.basePrice = item.price;
                    }
                    priceSpan.dataset.extras = '0.00';
                    itemElement.appendChild(priceSpan);
                }
                
                // Create expandable details section (for drinks)
                if (!item.foodItem) {
                    const detailsDiv = document.createElement('div');
                    detailsDiv.className = 'item-details text-center';
                    
                    // Description
                    const descriptionPara = document.createElement('p');
                    descriptionPara.className = 'text-sm text-gray-600 mt-2 text-center';
                    descriptionPara.textContent = item.description;
                    detailsDiv.appendChild(descriptionPara);
                    
                    // Size options section - only if item doesn't have singleSize flag
                    if (!item.singleSize) {
                        const sizeSection = document.createElement('div');
                        sizeSection.className = 'options-section text-center';
                        
                        // Size heading
                        const sizeHeading = document.createElement('div');
                        sizeHeading.className = 'section-title text-center';
                        sizeHeading.textContent = 'Size';
                        sizeSection.appendChild(sizeHeading);
                        
                        // Size options
                        const sizeOptionsDiv = document.createElement('div');
                        sizeOptionsDiv.className = 'options-grid';
                        sizeOptionsDiv.dataset.prices = JSON.stringify(item.prices);
                        sizeOptionsDiv.dataset.itemId = itemId;
                        
                        // Add size buttons
                        item.sizes.forEach(size => {
                            const sizeBtn = document.createElement('button');
                            sizeBtn.className = `option-btn size-btn ${size === item.defaultSize ? 'active' : ''}`;
                            sizeBtn.dataset.size = size;
                            sizeBtn.textContent = size;
                            sizeOptionsDiv.appendChild(sizeBtn);
                        });
                        
                        sizeSection.appendChild(sizeOptionsDiv);
                        detailsDiv.appendChild(sizeSection);
                    } else {
                        // For single size items like tea, show size info text instead
                        const sizeInfo = document.createElement('p');
                        sizeInfo.className = 'size-info';
                        sizeInfo.textContent = `Standard ${item.defaultSize} size`;
                        detailsDiv.appendChild(sizeInfo);
                    }
                    
                    // Only add customization options if not disabled
                    if (!item.disableCustomization) {
                        // Create a second-tier customization container
                        const customizeContainer = document.createElement('div');
                        customizeContainer.className = 'customize-container hidden';
                        
                        // First determine which extras to use based on item type
                        let itemExtras = extras; // Default
                        let showMilkOptions = true;
                        
                        if (item.itemType === 'tea') {
                            itemExtras = teaExtras;
                            // For regular tea, use tea milk options
                        } else if (item.itemType === 'herbal-tea') {
                            itemExtras = herbalTeaExtras;
                            showMilkOptions = false; // No milk options for herbal tea
                        }
                        
                        // Only show extras section if there are extras to show
                        if (itemExtras.length > 0) {
                            const extrasSection = document.createElement('div');
                            extrasSection.className = 'options-section text-center';
                            
                            // Extras heading
                            const extrasHeading = document.createElement('div');
                            extrasHeading.className = 'section-title text-center';
                            extrasHeading.textContent = 'Extras';
                            extrasSection.appendChild(extrasHeading);
                            
                            // Extras options
                            const extrasGrid = document.createElement('div');
                            extrasGrid.className = 'options-grid';
                            
                            // Add extras as buttons
                            itemExtras.forEach(extra => {
                                const extraBtn = document.createElement('button');
                                extraBtn.className = 'option-btn extra-btn';
                                extraBtn.dataset.extraId = extra.id;
                                extraBtn.dataset.price = extra.price;
                                extraBtn.textContent = `${extra.name} ${extra.price > 0 ? `(£${extra.price.toFixed(2)})` : ''}`;
                                
                                extraBtn.addEventListener('click', function(e) {
                                    e.stopPropagation(); // Prevent closing the menu
                                    this.classList.toggle('active');
                                    updateTotalPrice(itemElement);
                                });
                                
                                extrasGrid.appendChild(extraBtn);
                            });
                            
                            extrasSection.appendChild(extrasGrid);
                            customizeContainer.appendChild(extrasSection);
                        }
                        
                        // Only show milk options for items that should have them
                        if (showMilkOptions) {
                            // Alternative milk section - use tea-specific milk options if item type is tea
                            const milkSection = document.createElement('div');
                            milkSection.className = 'options-section text-center';
                            
                            // Milk heading
                            const milkHeading = document.createElement('div');
                            milkHeading.className = 'section-title text-center';
                            milkHeading.textContent = 'Alternative Milk';
                            milkSection.appendChild(milkHeading);
                            
                            // Milk options
                            const milkGrid = document.createElement('div');
                            milkGrid.className = 'options-grid';
                            
                            // Determine which milk options to use based on item type
                            const itemMilkOptions = item.itemType === 'tea' ? teaMilkOptions : milkOptions;
                            
                            // Add milk options as buttons
                            itemMilkOptions.forEach(milk => {
                                const milkBtn = document.createElement('button');
                                milkBtn.className = 'option-btn milk-btn';
                                milkBtn.dataset.milkId = milk.id;
                                milkBtn.dataset.price = milk.price;
                                
                                if (milk.price > 0) {
                                    milkBtn.textContent = `${milk.name} (£${milk.price.toFixed(2)})`;
                                } else {
                                    milkBtn.textContent = `${milk.name} (Free)`;
                                }
                                
                                milkBtn.addEventListener('click', function(e) {
                                    e.stopPropagation(); // Prevent closing the menu
                                    
                                    // Deactivate all other milk buttons
                                    milkGrid.querySelectorAll('.milk-btn').forEach(btn => {
                                        btn.classList.remove('active');
                                    });
                                    
                                    // Activate this button
                                    this.classList.add('active');
                                    updateTotalPrice(itemElement);
                                });
                                
                                milkGrid.appendChild(milkBtn);
                            });
                            
                            milkSection.appendChild(milkGrid);
                            customizeContainer.appendChild(milkSection);
                        }
                        
                        // Add the customize button
                        const customizeBtn = document.createElement('button');
                        customizeBtn.className = 'customize-btn';
                        customizeBtn.textContent = 'Customize';
                        
                        // Add event listener to toggle customize options
                        customizeBtn.addEventListener('click', function(e) {
                            e.stopPropagation(); // Prevent closing the menu
                            
                            // Toggle customize container visibility
                            if (customizeContainer.classList.contains('hidden')) {
                                customizeContainer.classList.remove('hidden');
                                customizeBtn.textContent = 'Hide options';
                                customizeBtn.classList.add('active');
                            } else {
                                customizeContainer.classList.add('hidden');
                                customizeBtn.textContent = 'Customize';
                                customizeBtn.classList.remove('active');
                            }
                        });
                        
                        // Add customize button and container to details
                        detailsDiv.appendChild(customizeBtn);
                        detailsDiv.appendChild(customizeContainer);
                    } else {
                        // Add notice if customization is disabled
                        const noCustomizationNotice = document.createElement('p');
                        noCustomizationNotice.className = 'no-customization-notice';
                        noCustomizationNotice.textContent = 'No customization available for this item.';
                        detailsDiv.appendChild(noCustomizationNotice);
                    }
                    
                    // Append details to item
                    itemElement.appendChild(detailsDiv);
                    
                    // Prevent option buttons from closing accordion when clicked
                    detailsDiv.addEventListener('click', function(e) {
                        e.stopPropagation();
                    });
                }
                
                return itemElement;
            }
            
            // Tab functionality
            document.querySelectorAll('.tab-btn').forEach(button => {
                button.addEventListener('click', function() {
                    // Close any open accordion when switching tabs
                    if (currentlyExpandedItem) {
                        currentlyExpandedItem.classList.remove('expanded');
                        currentlyExpandedItem = null;
                    }
                    
                    // Remove active class from all tabs
                    document.querySelectorAll('.tab-btn').forEach(btn => {
                        btn.classList.remove('active');
                        btn.classList.remove('bg-primary');
                        btn.classList.remove('text-white');
                        btn.classList.add('bg-gray-200');
                        btn.style.backgroundColor = '';
                        btn.style.color = '#555555';
                    });
                    
                    // Add active class to clicked tab
                    this.classList.add('active');
                    this.classList.add('text-white');
                    this.classList.remove('bg-gray-200');
                    this.style.backgroundColor = '#f86400';
                    this.style.color = 'white';
                    
                    // Hide all tab contents
                    document.querySelectorAll('.tab-content').forEach(content => {
                        content.classList.remove('active');
                    });
                    
                    // Show the selected tab content
                    const tabId = this.getAttribute('data-tab');
                    document.getElementById(tabId).classList.add('active');
                });
            });
            
            // Toggle accordion function that closes previously opened accordion
            function toggleAccordion(itemElement) {
                // Find the parent grid container
                const parentGrid = itemElement.closest('.menu-grid');
                
                // If this item is already expanded, just close it
                if (itemElement === currentlyExpandedItem) {
                    itemElement.classList.remove('expanded');
                    currentlyExpandedItem = null;
                    // Remove the class that fades other items
                    parentGrid.classList.remove('has-expanded-item');
                    return;
                }
                
                // Close currently expanded item (if any)
                if (currentlyExpandedItem) {
                    currentlyExpandedItem.classList.remove('expanded');
                    // If the currently expanded item is in a different grid, remove the fade class from that grid
                    const oldParentGrid = currentlyExpandedItem.closest('.menu-grid');
                    if (oldParentGrid !== parentGrid) {
                        oldParentGrid.classList.remove('has-expanded-item');
                    }
                }
                
                // Expand the newly clicked item
                itemElement.classList.add('expanded');
                currentlyExpandedItem = itemElement;
                
                // Add the class that fades other items
                parentGrid.classList.add('has-expanded-item');
            }
            
            // Size selection functionality
            document.querySelectorAll('.size-btn').forEach(button => {
                button.addEventListener('click', function(e) {
                    e.stopPropagation(); // Prevent closing the menu
                    
                    // Get the parent options grid
                    const sizeOptions = this.closest('.options-grid');
                    
                    // Remove active class from all size buttons in this group
                    sizeOptions.querySelectorAll('.size-btn').forEach(btn => {
                        btn.classList.remove('active');
                    });
                    
                    // Add active class to clicked button
                    this.classList.add('active');
                    
                    // Get the selected size
                    const selectedSize = this.getAttribute('data-size');
                    
                    // Get the prices data from the data-prices attribute
                    const pricesData = JSON.parse(sizeOptions.getAttribute('data-prices'));
                    
                    // Get the item element
                    const itemId = sizeOptions.getAttribute('data-item-id');
                    const itemElement = document.getElementById(itemId);
                    
                    // Update the base price
                    const priceElement = itemElement.querySelector('.item-price');
                    const basePrice = pricesData[selectedSize];
                    priceElement.dataset.basePrice = basePrice;
                    
                    // Update the displayed price (base + extras)
                    updateTotalPrice(itemElement);
                });
            });
            
            // Function to update total price based on base price and selected extras
            function updateTotalPrice(itemElement) {
                const priceElement = itemElement.querySelector('.item-price');
                const inlinePriceBadge = itemElement.querySelector('.inline-price-badge');
                const priceBadge = itemElement.querySelector('.price-badge');
                const basePrice = parseFloat(priceElement.dataset.basePrice);
                
                // Calculate extras total
                let extrasTotal = 0;
                
                // Add selected extras (ignoring decaf since it's free)
                itemElement.querySelectorAll('.extra-btn.active').forEach(btn => {
                    extrasTotal += parseFloat(btn.dataset.price);
                });
                
                // Add selected milk (if any)
                const selectedMilk = itemElement.querySelector('.milk-btn.active');
                if (selectedMilk) {
                    extrasTotal += parseFloat(selectedMilk.dataset.price);
                }
                
                // Update extras data attribute
                priceElement.dataset.extras = extrasTotal.toFixed(2);
                
                // Update displayed price
                const totalPrice = basePrice + extrasTotal;
                
                // Update appropriate price display
                if (inlinePriceBadge) {
                    inlinePriceBadge.textContent = `£${totalPrice.toFixed(2)}`;
                } else if (priceBadge) {
                    priceBadge.textContent = `£${totalPrice.toFixed(2)}`;
                }
            }
            
            // Handle image errors
            document.querySelectorAll('.item-image').forEach(img => {
                img.addEventListener('error', function() {
                    // Hide the image if it fails to load
                    this.style.display = 'none';
                });
            });
        });
    </script>
</body>
</html>
