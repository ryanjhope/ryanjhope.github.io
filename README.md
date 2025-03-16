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
        
        // Available extras for customization
        const extras = [
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
        
        /* Category styles */
        .category-title {
            margin-top: 24px;
            margin-bottom: 12px;
            padding-bottom: 5px;
            border-bottom: 2px solid #f86400;
            display: inline-block;
        }
        
        /* Responsive grid layout */
        .menu-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr); /* 2 columns by default (mobile) */
            gap: 12px;
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
            border: 1px solid #e5e7eb;
            border-radius: 8px;
            background-color: white;
            box-shadow: 0 1px 3px rgba(0,0,0,0.05);
            transition: all 0.2s ease;
            overflow: hidden;
        }
        
        /* Image container - force square aspect ratio */
        .image-container {
            position: relative;
            width: 100%;
            padding-bottom: 100%; /* This creates a square aspect ratio */
            overflow: hidden;
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
            justify-content: space-between;
            align-items: center;
            cursor: pointer;
        }
        
        /* Make menu item name smaller to fit multiple items per row */
        .item-header h4 {
            font-size: 14px;
            margin: 0;
        }
        
        /* Accordion styles */
        .item-details {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.3s ease;
            padding: 0 10px;
        }
        
        .menu-item.expanded .item-details {
            max-height: 800px;
            padding-bottom: 15px;
        }
        
        /* Size and customization options */
        .options-section {
            margin: 15px 0;
        }
        
        .section-title {
            font-weight: 600;
            font-size: 14px;
            margin-bottom: 8px;
            color: #333;
        }
        
        /* Button grid for options */
        .options-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }
        
        /* Option button styles */
        .option-btn {
            font-size: 12px;
            padding: 5px 8px;
            border-radius: 4px;
            background-color: #f3f4f6;
            border: 1px solid #e5e7eb;
            cursor: pointer;
            transition: all 0.2s ease;
        }
        
        .option-btn.active {
            background-color: #f86400;
            color: white;
            border-color: #f86400;
        }
        
        .option-btn:hover {
            background-color: #f9f9f9;
        }
        
        .option-btn.active:hover {
            background-color: #e05a00;
        }
        
        /* Price badge */
        .price-badge {
            position: absolute;
            top: 10px;
            right: 10px;
            background-color: rgba(0, 0, 0, 0.6);
            color: white;
            padding: 3px 8px;
            border-radius: 20px;
            font-weight: 600;
            font-size: 14px;
            z-index: 10;
        }
        
        /* Empty category style */
        .empty-category {
            padding: 15px;
            color: #666;
            font-style: italic;
            grid-column: span 2;
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
        }
    </style>
</head>
<body>
    <div id="menu-container" class="container mx-auto max-w-5xl bg-white">
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
                    itemsGrid.className = 'menu-grid';
                    
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
                            itemElement.className = 'menu-item';
                            itemElement.id = itemId;
                            
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
                            
                            imageContainer.appendChild(img);
                            imageContainer.appendChild(priceBadge);
                            
                            // Create header with name
                            const headerDiv = document.createElement('div');
                            headerDiv.className = 'item-header';
                            
                            // Item name
                            const itemName = document.createElement('h4');
                            itemName.className = 'text-md font-semibold';
                            itemName.textContent = item.name;
                            
                            // Item price (hidden in header when using badge)
                            const priceSpan = document.createElement('span');
                            priceSpan.className = 'item-price font-semibold';
                            priceSpan.style.color = '#f86400';
                            priceSpan.style.display = 'none'; // Hidden but used for calculations
                            priceSpan.dataset.basePrice = item.prices[item.defaultSize];
                            priceSpan.dataset.extras = '0.00';
                            
                            headerDiv.appendChild(itemName);
                            headerDiv.appendChild(priceSpan);
                            
                            // Create expandable details section
                            const detailsDiv = document.createElement('div');
                            detailsDiv.className = 'item-details';
                            
                            // Description
                            const descriptionPara = document.createElement('p');
                            descriptionPara.className = 'text-sm text-gray-600 mt-2';
                            descriptionPara.textContent = item.description;
                            detailsDiv.appendChild(descriptionPara);
                            
                            // Size options section
                            const sizeSection = document.createElement('div');
                            sizeSection.className = 'options-section';
                            
                            // Size heading
                            const sizeHeading = document.createElement('div');
                            sizeHeading.className = 'section-title';
                            sizeHeading.textContent = 'Size:';
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
                            
                            // Extras section
                            const extrasSection = document.createElement('div');
                            extrasSection.className = 'options-section';
                            
                            // Extras heading
                            const extrasHeading = document.createElement('div');
                            extrasHeading.className = 'section-title';
                            extrasHeading.textContent = 'Extras:';
                            extrasSection.appendChild(extrasHeading);
                            
                            // Extras options
                            const extrasGrid = document.createElement('div');
                            extrasGrid.className = 'options-grid';
                            
                            // Add extras as buttons
                            extras.forEach(extra => {
                                const extraBtn = document.createElement('button');
                                extraBtn.className = 'option-btn extra-btn';
                                extraBtn.dataset.extraId = extra.id;
                                extraBtn.dataset.price = extra.price;
                                extraBtn.textContent = `${extra.name} (+£${extra.price.toFixed(2)})`;
                                
                                extraBtn.addEventListener('click', function(e) {
                                    e.stopPropagation(); // Prevent closing the menu
                                    this.classList.toggle('active');
                                    updateTotalPrice(itemElement);
                                });
                                
                                extrasGrid.appendChild(extraBtn);
                            });
                            
                            extrasSection.appendChild(extrasGrid);
                            detailsDiv.appendChild(extrasSection);
                            
                            // Alternative milk section
                            const milkSection = document.createElement('div');
                            milkSection.className = 'options-section';
                            
                            // Milk heading
                            const milkHeading = document.createElement('div');
                            milkHeading.className = 'section-title';
                            milkHeading.textContent = 'Alternative Milk:';
                            milkSection.appendChild(milkHeading);
                            
                            // Milk options
                            const milkGrid = document.createElement('div');
                            milkGrid.className = 'options-grid';
                            
                            // Add milk options as buttons
                            milkOptions.forEach(milk => {
                                const milkBtn = document.createElement('button');
                                milkBtn.className = 'option-btn milk-btn';
                                milkBtn.dataset.milkId = milk.id;
                                milkBtn.dataset.price = milk.price;
                                
                                if (milk.price > 0) {
                                    milkBtn.textContent = `${milk.name} (+£${milk.price.toFixed(2)})`;
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
                            detailsDiv.appendChild(milkSection);
                            
                            // Assemble the item
                            itemElement.appendChild(imageContainer);
                            itemElement.appendChild(headerDiv);
                            itemElement.appendChild(detailsDiv);
                            
                            itemsGrid.appendChild(itemElement);
                            
                            // Make image clickable to toggle accordion
                            img.addEventListener('click', function() {
                                toggleAccordion(itemElement);
                            });
                            
                            // Make header clickable to toggle accordion
                            headerDiv.addEventListener('click', function() {
                                toggleAccordion(itemElement);
                            });
                            
                            // Prevent option buttons from closing accordion when clicked
                            detailsDiv.addEventListener('click', function(e) {
                                e.stopPropagation();
                            });
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
            
            // Toggle accordion function that closes previously opened accordion
            function toggleAccordion(itemElement) {
                // If this item is already expanded, just close it
                if (itemElement === currentlyExpandedItem) {
                    itemElement.classList.remove('expanded');
                    currentlyExpandedItem = null;
                    return;
                }
                
                // Close currently expanded item (if any)
                if (currentlyExpandedItem) {
                    currentlyExpandedItem.classList.remove('expanded');
                }
                
                // Expand the newly clicked item
                itemElement.classList.add('expanded');
                currentlyExpandedItem = itemElement;
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
                const priceBadge = itemElement.querySelector('.price-badge');
                const basePrice = parseFloat(priceElement.dataset.basePrice);
                
                // Calculate extras total
                let extrasTotal = 0;
                
                // Add selected extras
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
                priceBadge.textContent = `£${totalPrice.toFixed(2)}`;
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
