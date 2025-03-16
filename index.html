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
                            }
                            // Add more coffee items here
                        ]
                    },
                    "specialty-coffee": {
                        title: "Specialty Coffee",
                        items: [
                            // Add specialty coffee items here
                        ]
                    },
                    "hot-chocolate": {
                        title: "Hot Chocolate",
                        items: [
                            // Add hot chocolate items here
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
                            // Add iced coffee items here
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
                title: "Food & Pastries",
                categories: {
                    "breakfast": {
                        title: "Breakfast",
                        items: [
                            // Add breakfast items here
                        ]
                    },
                    "pastries": {
                        title: "Pastries",
                        items: [
                            // Add pastry items here
                        ]
                    },
                    "lunch": {
                        title: "Lunch",
                        items: [
                            // Add lunch items here
                        ]
                    }
                }
            },
            // Specials Tab
            "specials": {
                title: "Seasonal Specials",
                categories: {
                    "seasonal-drinks": {
                        title: "Seasonal Drinks",
                        items: [
                            // Add seasonal drinks here
                        ]
                    },
                    "limited-edition": {
                        title: "Limited Edition",
                        items: [
                            // Add limited edition items here
                        ]
                    },
                    "combo-deals": {
                        title: "Combo Deals",
                        items: [
                            // Add combo deals here
                        ]
                    }
                }
            }
        };
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
            color: black;
        }
        
        /* Make the menu container fill the embed space */
        #menu-container {
            width: 100%;
            height: 100%;
            overflow-y: auto;
            padding: 10px;
            box-sizing: border-box;
        }
        
        /* Tab functionality */
        .tab-content {
            display: none;
        }
        .tab-content.active {
            display: block;
        }
        .menu-item {
            transition: transform 0.2s ease-in-out;
        }
        .menu-item:hover {
            transform: translateY(-2px);
        }
        
        /* Category styles */
        .category-title {
            margin-top: 24px;
            margin-bottom: 12px;
            padding-bottom: 5px;
            border-bottom: 2px solid #f86400;
            display: inline-block;
        }
        
        /* Menu item image styles */
        .menu-image {
            width: 80px !important;
            height: 80px !important;
            object-fit: cover !important;
            border-radius: 8px !important;
            margin-right: 16px !important;
        }
        
        /* Size selector styles */
        .size-options {
            display: flex;
            gap: 8px;
            margin-top: 8px;
        }
        
        .size-btn {
            font-size: 12px;
            padding: 4px 8px;
            border-radius: 4px;
            background-color: #f3f4f6;
            cursor: pointer;
            transition: all 0.2s ease;
            border: 1px solid #e5e7eb;
        }
        
        .size-btn.active {
            background-color: #f86400;
            color: white;
            border-color: #f86400;
        }
        
        /* Responsive fallbacks */
        @media (max-width: 640px) {
            .menu-flex {
                flex-direction: column;
            }
            .menu-image {
                width: 100% !important;
                height: 160px !important;
                margin-right: 0 !important;
                margin-bottom: 12px !important;
                border-radius: 8px !important; /* Keep rounded corners on mobile */
            }
        }

        .empty-category {
            padding: 15px;
            color: #666;
            font-style: italic;
        }
        
        .image-container {
            min-width: 80px;
            margin-right: 16px;
        }
        
        @media (max-width: 640px) {
            .image-container {
                min-width: 100%;
                margin-right: 0;
                margin-bottom: 12px;
            }
        }
    </style>
</head>
<body>
    <div id="menu-container" class="container mx-auto max-w-4xl bg-white">
        <!-- Tab Navigation -->
        <div class="tab-navigation mb-6 flex justify-center overflow-x-auto pb-1 border-b border-gray-200" id="tab-buttons">
            <!-- Tab buttons will be generated here -->
        </div>

        <!-- Menu Content -->
        <div class="tab-container" id="tab-content">
            <!-- Tab content will be generated here -->
        </div>
    </div>

    <script>
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
                tabButton.className = `tab-btn flex-shrink-0 px-4 py-2 mr-2 rounded-t-lg ${isFirst ? 'active bg-primary text-white' : 'bg-gray-200 hover:bg-gray-300 text-black'} font-medium`;
                tabButton.dataset.tab = tabId;
                tabButton.textContent = tab.title;
                tabButton.style.fontFamily = "'Poppins', sans-serif";
                if (isFirst) {
                    tabButton.style.backgroundColor = '#f86400';
                }
                tabButtonsContainer.appendChild(tabButton);
                
                // Create tab content
                const tabContent = document.createElement('div');
                tabContent.id = tabId;
                tabContent.className = `tab-content ${isFirst ? 'active' : ''}`;
                
                // Add tab title
                const tabTitle = document.createElement('h2');
                tabTitle.className = 'text-2xl font-bold mb-4 text-black';
                tabTitle.style.fontFamily = "'Poppins', sans-serif";
                tabTitle.textContent = tab.title;
                tabContent.appendChild(tabTitle);
                
                // Generate categories and items
                for (const categoryId in tab.categories) {
                    const category = tab.categories[categoryId];
                    
                    // Add category title
                    const categoryTitle = document.createElement('h3');
                    categoryTitle.className = 'text-xl font-semibold text-black category-title';
                    categoryTitle.style.fontFamily = "'Poppins', sans-serif";
                    categoryTitle.textContent = category.title;
                    tabContent.appendChild(categoryTitle);
                    
                    // Add items grid
                    const itemsGrid = document.createElement('div');
                    itemsGrid.className = 'grid grid-cols-1 md:grid-cols-2 gap-4';
                    
                    // If no items, show "Coming soon"
                    if (category.items.length === 0) {
                        const emptyMessage = document.createElement('p');
                        emptyMessage.className = 'empty-category';
                        emptyMessage.textContent = 'Coming soon!';
                        itemsGrid.appendChild(emptyMessage);
                    } else {
                        // Generate items
                        category.items.forEach((item, index) => {
                            // Generate a unique ID for this item
                            const itemId = `${categoryId}-item-${index}`;
                            
                            // Create item element
                            const itemElement = document.createElement('div');
                            itemElement.className = 'menu-item p-4 rounded-lg border border-gray-200 bg-white shadow-sm';
                            
                            // Create item content
                            const itemHTML = `
                                <div class="flex menu-flex">
                                    <div class="image-container">
                                        <img src="${item.image}" alt="${item.name}" class="menu-image">
                                    </div>
                                    <div class="flex-1">
                                        <div class="flex justify-between items-start">
                                            <h3 class="text-lg font-semibold text-black" style="font-family: 'Poppins', sans-serif !important;">${item.name}</h3>
                                            <span class="font-semibold item-price" style="color: #f86400; font-family: 'Poppins', sans-serif !important;">£${item.prices[item.defaultSize].toFixed(2)}</span>
                                        </div>
                                        <p class="text-sm text-gray-600 mt-1" style="font-family: 'Poppins', sans-serif !important;">${item.description}</p>
                                        <div class="size-options mt-3" data-prices='${JSON.stringify(item.prices)}' data-item-id="${itemId}">
                                            ${item.sizes.map(size => `
                                                <button class="size-btn ${size === item.defaultSize ? 'active' : ''}" data-size="${size}">${size}</button>
                                            `).join('')}
                                        </div>
                                    </div>
                                </div>
                            `;
                            
                            itemElement.innerHTML = itemHTML;
                            itemsGrid.appendChild(itemElement);
                        });
                    }
                    
                    tabContent.appendChild(itemsGrid);
                }
                
                tabContentContainer.appendChild(tabContent);
                isFirst = false;
            }
            
            // Tab functionality
            document.querySelectorAll('.tab-btn').forEach(button => {
                button.addEventListener('click', function() {
                    // Remove active class from all tabs
                    document.querySelectorAll('.tab-btn').forEach(btn => {
                        btn.classList.remove('active');
                        btn.classList.remove('bg-primary');
                        btn.classList.remove('text-white');
                        btn.classList.add('bg-gray-200');
                        btn.classList.add('text-black');
                        btn.style.backgroundColor = '';
                    });
                    
                    // Add active class to clicked tab
                    this.classList.add('active');
                    this.classList.add('text-white');
                    this.classList.remove('bg-gray-200');
                    this.classList.remove('text-black');
                    this.style.backgroundColor = '#f86400';
                    
                    // Hide all tab contents
                    document.querySelectorAll('.tab-content').forEach(content => {
                        content.classList.remove('active');
                    });
                    
                    // Show the selected tab content
                    const tabId = this.getAttribute('data-tab');
                    document.getElementById(tabId).classList.add('active');
                });
            });
            
            // Size selection functionality
            document.querySelectorAll('.size-btn').forEach(button => {
                button.addEventListener('click', function() {
                    // Get the parent size-options element
                    const sizeOptions = this.closest('.size-options');
                    
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
                    
                    // Update the displayed price
                    const priceElement = sizeOptions.closest('.flex-1').querySelector('.item-price');
                    priceElement.textContent = '£' + pricesData[selectedSize].toFixed(2);
                });
            });
            
            // Handle image errors
            document.querySelectorAll('.menu-image').forEach(img => {
                img.addEventListener('error', function() {
                    // Hide the image if it fails to load
                    this.style.display = 'none';
                });
            });
        });
    </script>
</body>
</html>
