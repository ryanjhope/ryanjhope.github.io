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
                            },
                            {
                                name: "Gingerbread Latte",
                                image: null,
                                description: "Warm spiced latte with aromatic gingerbread flavoring and a hint of molasses sweetness.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.40,
                                    "20oz": 4.60
                                },
                                defaultSize: "16oz"
                            },
                            {
                                name: "Pumpkin Spice Latte",
                                image: null,
                                description: "Seasonal blend of espresso with pumpkin and warm autumn spices in creamy steamed milk.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.40,
                                    "20oz": 4.60
                                },
                                defaultSize: "16oz"
                            },
                            {
                                name: "Lotus Biscoff Latte",
                                image: null,
                                description: "Rich espresso combined with smooth caramelized biscuit flavor and velvety steamed milk.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.40,
                                    "20oz": 4.60
                                },
                                defaultSize: "16oz"
                            },
                            {
                                name: "Butterscotch Latte",
                                image: null,
                                description: "Indulgent latte with rich butterscotch syrup and smooth steamed milk for a sweet finish.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.40,
                                    "20oz": 4.60
                                },
                                defaultSize: "16oz"
                            },
                            {
                                name: "Chai Latte",
                                image: null,
                                description: "Aromatic blend of traditional chai spices with steamed milk for a warming, comforting drink.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.40,
                                    "20oz": 4.60
                                },
                                defaultSize: "16oz"
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
                            },
                            {
                                name: "Oreo Hot Chocolate",
                                image: null,
                                description: "Decadent hot chocolate blended with crushed Oreo cookies and topped with whipped cream.",
                                sizes: ["12oz", "16oz", "20oz"],
                                prices: {
                                    "12oz": 3.90,
                                    "16oz": 4.10,
                                    "20oz": 4.50
                                },
                                defaultSize: "12oz"
                            },
                            {
                                name: "Kinder Bueno Hot Chocolate",
                                image: null,
                                description: "Creamy hot chocolate with Kinder Bueno pieces, creating a rich hazelnut and chocolate experience.",
                                sizes: ["12oz", "16oz", "20oz"],
                                prices: {
                                    "12oz": 3.90,
                                    "16oz": 4.10,
                                    "20oz": 4.50
                                },
                                defaultSize: "12oz"
                            },
                            {
                                name: "Snickers Hot Chocolate",
                                image: null,
                                description: "Indulgent hot chocolate with Snickers pieces, peanuts, and caramel for the ultimate treat.",
                                sizes: ["12oz", "16oz", "20oz"],
                                prices: {
                                    "12oz": 3.90,
                                    "16oz": 4.10,
                                    "20oz": 4.50
                                },
                                defaultSize: "12oz"
                            },
                            {
                                name: "Ruby Hot Chocolate",
                                image: null,
                                description: "Unique pink ruby chocolate with a naturally fruity and smooth flavor profile.",
                                sizes: ["12oz", "16oz", "20oz"],
                                prices: {
                                    "12oz": 3.90,
                                    "16oz": 4.10,
                                    "20oz": 4.50
                                },
                                defaultSize: "12oz"
                            },
                            {
                                name: "White Hot Chocolate",
                                image: null,
                                description: "Smooth and creamy white chocolate drink with a sweet, vanilla finish.",
                                sizes: ["12oz", "16oz", "20oz"],
                                prices: {
                                    "12oz": 3.90,
                                    "16oz": 4.10,
                                    "20oz": 4.50
                                },
                                defaultSize: "12oz"
                            },
                            {
                                name: "Black Forest Hot Chocolate",
                                image: null,
                                description: "Rich chocolate drink with cherry flavor and whipped cream, inspired by the classic cake.",
                                sizes: ["12oz", "16oz", "20oz"],
                                prices: {
                                    "12oz": 3.90,
                                    "16oz": 4.10,
                                    "20oz": 4.50
                                },
                                defaultSize: "12oz"
                            },
                            {
                                name: "Salted Caramel Hot Chocolate",
                                image: null,
                                description: "Perfect balance of sweet caramel and sea salt in a rich chocolate base.",
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
                                name: "Iced Latte",
                                image: "https://u.cubeupload.com/ryanjhope/icedLatte2.png",
                                description: "Creamy and milky iced coffee.",
                                sizes: ["12oz", "16oz", "20oz"],
                                prices: {
                                    "12oz": 3.45,
                                    "16oz": 3.60,
                                    "20oz": 4.05
                                },
                                defaultSize: "16oz"
                            },
                            {
                                name: "Iced Cappuccino",
                                image: "https://u.cubeupload.com/ryanjhope/icedCappuccino2.png",
                                description: "Creamy and frothy iced coffee.",
                                sizes: ["12oz", "16oz", "20oz"],
                                prices: {
                                    "12oz": 3.45,
                                    "16oz": 3.60,
                                    "20oz": 4.05
                                },
                                defaultSize: "16oz"
                            },
                            {
                                name: "Iced Americano",
                                image: "https://u.cubeupload.com/ryanjhope/icedAmericano.png",
                                description: "Refreshing coffee served over ice.",
                                sizes: ["12oz", "16oz", "20oz"],
                                prices: {
                                    "12oz": 3.10,
                                    "16oz": 3.30,
                                    "20oz": 3.50
                                },
                                defaultSize: "16oz"
                            },
                            {
                                name: "Iced Mocha",
                                image: "https://u.cubeupload.com/ryanjhope/icedMocha.png",
                                description: "Chocolatey and creamy iced coffee.",
                                sizes: ["12oz", "16oz", "20oz"],
                                prices: {
                                    "12oz": 3.60,
                                    "16oz": 3.80,
                                    "20oz": 4.20
                                },
                                defaultSize: "16oz"
                            },
                            {
                                name: "Caramel Frappé",
                                image: "https://u.cubeupload.com/ryanjhope/caramelFrappe.png",
                                description: "Blended ice coffee with a sweet caramel flavouring.",
                                sizes: ["12oz", "16oz", "20oz"],
                                prices: {
                                    "12oz": 4.10,
                                    "16oz": 4.25,
                                    "20oz": 4.70
                                },
                                defaultSize: "16oz"
                            },
                            {
                                name: "Vanilla Frappé",
                                image: "https://u.cubeupload.com/ryanjhope/espressoFrappe.png",
                                description: "Blended ice coffee with an indulgent vanilla flavouring.",
                                sizes: ["12oz", "16oz", "20oz"],
                                prices: {
                                    "12oz": 4.10,
                                    "16oz": 4.25,
                                    "20oz": 4.70
                                },
                                defaultSize: "16oz"
                            },
                            {
                                name: "Pistachio Iced Latte",
                                image: "https://u.cubeupload.com/ryanjhope/pistachioIcedLatte.png",
                                description: "Iced Latte made with creamy and rich pistachio butter.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.10,
                                    "20oz": 4.25
                                },
                                defaultSize: "16oz"
                            },
                            {
                                name: "Biscoff Iced Latte",
                                image: "https://u.cubeupload.com/ryanjhope/biscoffIcedLatte.png",
                                description: "Iced Latte made with smooth caramelized biscuit flavor.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.10,
                                    "20oz": 4.25
                                },
                                defaultSize: "16oz"
                            },
                            {
                                name: "Strawberry Iced Matcha",
                                image: "https://u.cubeupload.com/ryanjhope/strawIcedMatcha.png",
                                description: "Refreshing iced matcha beautifully layered with sweet strawberry.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.40,
                                    "20oz": 4.55
                                },
                                defaultSize: "16oz"
                            }
                        ]
                    },
                    "slushes-freezes": {
                        title: "Slushes & Freezes",
                        items: [
                            {
                                name: "Blue Raspberry Slush",
                                image: "https://u.cubeupload.com/ryanjhope/blueSlush.png",
                                description: "Tangy and sweet blue raspberry flavoured slush.",
                                sizes: ["12oz", "16oz", "20oz"],
                                prices: {
                                    "12oz": 3.85,
                                    "16oz": 4.00,
                                    "20oz": 4.15
                                },
                                defaultSize: "16oz",
                                disableCustomization: true
                            },
                            {
                                name: "Watermelon Slush",
                                image: "https://u.cubeupload.com/ryanjhope/watermelonSlush.png",
                                description: "Refreshing watermelon flavoured slush.",
                                sizes: ["12oz", "16oz", "20oz"],
                                prices: {
                                    "12oz": 3.85,
                                    "16oz": 4.00,
                                    "20oz": 4.15
                                },
                                defaultSize: "16oz",
                                disableCustomization: true
                            },
                            {
                                name: "Dragonfruit Slush",
                                image: "https://u.cubeupload.com/ryanjhope/watermelonSlush2.png",
                                description: "Refreshing, sweet and tangy dragonfruit slush.",
                                sizes: ["12oz", "16oz", "20oz"],
                                prices: {
                                    "12oz": 3.85,
                                    "16oz": 4.00,
                                    "20oz": 4.15
                                },
                                defaultSize: "16oz",
                                disableCustomization: true
                            },
                            {
                                name: "Berry Freeze",
                                image: "https://u.cubeupload.com/ryanjhope/berryFreeze.png",
                                description: "A refreshing frozen berry blend.",
                                sizes: ["12oz", "16oz", "20oz"],
                                prices: {
                                    "12oz": 3.85,
                                    "16oz": 4.00,
                                    "20oz": 4.15
                                },
                                defaultSize: "16oz",
                                disableCustomization: true
                            },
                            {
                                name: "Mango Freeze",
                                image: "https://u.cubeupload.com/ryanjhope/mangoFreeze2.png",
                                description: "A tropical frozen mango treat.",
                                sizes: ["12oz", "16oz", "20oz"],
                                prices: {
                                    "12oz": 3.85,
                                    "16oz": 4.00,
                                    "20oz": 4.15
                                },
                                defaultSize: "16oz",
                                disableCustomization: true
                            }
                        ]
                    },
                    "refreshers": {
                        title: "Iced Tea & Lemonade",
                        items: [
                            {
                                name: "Pineapple Lemonade",
                                image: "https://u.cubeupload.com/ryanjhope/pineappleLemonade.png",
                                description: "A sweet pineapple infused lemonade.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.00,
                                    "20oz": 4.15
                                },
                                defaultSize: "16oz",
                                disableCustomization: true
                            },
                            {
                                name: "Rhubarb Lemonade",
                                image: "https://u.cubeupload.com/ryanjhope/rhubarb.png",
                                description: "A sweet and tangy rhubarb lemonade.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.00,
                                    "20oz": 4.15
                                },
                                defaultSize: "16oz",
                                disableCustomization: true
                            },
                            {
                                name: "Peach & Strawberry Iced Tea",
                                image: "https://u.cubeupload.com/ryanjhope/icedTea.png",
                                description: "A flavourful peach and strawberry infused iced tea.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.00,
                                    "20oz": 4.15
                                },
                                defaultSize: "16oz",
                                disableCustomization: true
                            }
                        ]
                    },
                    "bubble-tea": {
                        title: "Bubble Tea",
                        items: [
                            {
                                name: "Mango Sunrise",
                                image: "https://u.cubeupload.com/ryanjhope/mangoSunrise.png",
                                description: "Refreshing mango juice over strawberry popping bubbles.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.40,
                                    "20oz": 4.55
                                },
                                defaultSize: "16oz",
                                itemType: "bubble-tea"
                            },
                            {
                                name: "Berry Bubbles",
                                image: "https://u.cubeupload.com/ryanjhope/berryBubbles.png",
                                description: "A juicy mix of strawberry and raspberry mixed with strawberry popping bubbles.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.40,
                                    "20oz": 4.55
                                },
                                defaultSize: "16oz",
                                itemType: "bubble-tea"
                            },
                            {
                                name: "Peach Paradise",
                                image: "https://u.cubeupload.com/ryanjhope/peachParadise.png",
                                description: "A refreshing peach juice paired with mango popping bubbles.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.40,
                                    "20oz": 4.55
                                },
                                defaultSize: "16oz",
                                itemType: "bubble-tea"
                            },
                            {
                                name: "Kiwi Krush",
                                image: "https://u.cubeupload.com/ryanjhope/kiwiKrush.png",
                                description: "A sweet and tangy kiwi juice poured over mango popping bubbles.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.40,
                                    "20oz": 4.55
                                },
                                defaultSize: "16oz",
                                itemType: "bubble-tea"
                            },
                            {
                                name: "Dragonfruit Blast",
                                image: "https://u.cubeupload.com/ryanjhope/dragonfruitBlast.png",
                                description: "A bittersweet dragonfruit juice mixed with mango popping bubbles.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.40,
                                    "20oz": 4.55
                                },
                                defaultSize: "16oz",
                                itemType: "bubble-tea"
                            },
                            {
                                name: "Mango Bubble Frappé",
                                image: "https://u.cubeupload.com/ryanjhope/mangobubbleFrappe.png",
                                description: "A blended mango frappé with mango bubbles and whipped cream.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.80,
                                    "20oz": 4.95
                                },
                                defaultSize: "16oz",
                                itemType: "bubble-tea-frappe"
                            }
                        ]
                    },
                    "speciality-frappe": {
                        title: "Speciality Frappé",
                        items: [
                            {
                                name: "Oreo Frappé",
                                image: "https://u.cubeupload.com/ryanjhope/oreoFrappe.png",
                                description: "Indulgent blended coffee with crushed Oreo cookies and whipped cream.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.80,
                                    "20oz": 4.95
                                },
                                defaultSize: "16oz",
                                itemType: "speciality-frappe"
                            },
                            {
                                name: "Kinder Bueno Frappé",
                                image: "https://u.cubeupload.com/ryanjhope/kinderFrappe.png",
                                description: "Rich blended coffee with creamy Kinder Bueno pieces and whipped cream.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.80,
                                    "20oz": 4.95
                                },
                                defaultSize: "16oz",
                                itemType: "speciality-frappe"
                            },
                            {
                                name: "Crunchie Frappé",
                                image: "https://u.cubeupload.com/ryanjhope/crunchieFrappe.png",
                                description: "Decadent blended coffee with honeycomb Crunchie pieces and whipped cream.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.80,
                                    "20oz": 4.95
                                },
                                defaultSize: "16oz",
                                itemType: "speciality-frappe"
                            },
                            {
                                name: "KitKat Frappé",
                                image: "https://u.cubeupload.com/ryanjhope/kitkatFrappe.png",
                                description: "Irresistible blended coffee with crispy KitKat pieces and whipped cream.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.80,
                                    "20oz": 4.95
                                },
                                defaultSize: "16oz",
                                itemType: "speciality-frappe"
                            },
                            {
                                name: "Snickers Frappé",
                                image: "https://u.cubeupload.com/ryanjhope/snickersFrappe.png",
                                description: "Indulgent blended coffee with Snickers pieces, peanuts, and caramel, topped with whipped cream.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.80,
                                    "20oz": 4.95
                                },
                                defaultSize: "16oz",
                                itemType: "speciality-frappe"
                            },
                            {
                                name: "Birthday Cake Frappé",
                                image: "https://u.cubeupload.com/ryanjhope/birthdaycakeFrappe.png",
                                description: "Festive blended coffee with sweet birthday cake flavor, colorful sprinkles, and whipped cream.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.80,
                                    "20oz": 4.95
                                },
                                defaultSize: "16oz",
                                itemType: "speciality-frappe"
                            },
                            {
                                name: "Raspberry Ripple Frappé",
                                image: "https://u.cubeupload.com/ryanjhope/raspberryFrappe.png",
                                description: "Refreshing blended coffee swirled with tangy raspberry sauce and topped with whipped cream and freeze-dried raspberries.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.80,
                                    "20oz": 4.95
                                },
                                defaultSize: "16oz",
                                itemType: "speciality-frappe"
                            },
                            {
                                name: "Pistachio Frappé",
                                image: "https://u.cubeupload.com/ryanjhope/pistachioFrappe.png",
                                description: "Luxurious blended coffee with rich pistachio flavor, topped with whipped cream and crushed pistachios.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.80,
                                    "20oz": 4.95
                                },
                                defaultSize: "16oz",
                                itemType: "speciality-frappe"
                            },
                            {
                                name: "Biscoff Frappé",
                                image: "https://u.cubeupload.com/ryanjhope/biscoffFrappe.png",
                                description: "Smooth blended coffee with caramelized Biscoff cookie flavor, topped with whipped cream and cookie crumbs.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.80,
                                    "20oz": 4.95
                                },
                                defaultSize: "16oz",
                                itemType: "speciality-frappe"
                            },
                            {
                                name: "Matcha Vanilla Frappé",
                                image: "https://u.cubeupload.com/ryanjhope/matchaFrappe.png",
                                description: "Elegant blended coffee with earthy matcha green tea and sweet vanilla, topped with whipped cream.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.80,
                                    "20oz": 4.95
                                },
                                defaultSize: "16oz",
                                itemType: "speciality-frappe"
                            }
                        ]
                    },
                    "shakes": {
                        title: "Shakes",
                        items: [
                            {
                                name: "Caramel Shake",
                                image: "https://u.cubeupload.com/ryanjhope/caramelShake.png",
                                description: "Rich and creamy caramel-flavored milkshake.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.10,
                                    "20oz": 4.25
                                },
                                defaultSize: "16oz",
                                itemType: "shake"
                            },
                            {
                                name: "Mint Chocolate Shake",
                                image: "https://u.cubeupload.com/ryanjhope/mintchocolateShake.png",
                                description: "Refreshing mint and rich chocolate in a creamy milkshake.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.10,
                                    "20oz": 4.25
                                },
                                defaultSize: "16oz",
                                itemType: "shake"
                            },
                            {
                                name: "Strawberry Shake",
                                image: "https://u.cubeupload.com/ryanjhope/strawberryShake.png",
                                description: "Sweet and fruity strawberry-flavored milkshake.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.10,
                                    "20oz": 4.25
                                },
                                defaultSize: "16oz",
                                itemType: "shake"
                            },
                            {
                                name: "Chocolate Shake",
                                image: "https://u.cubeupload.com/ryanjhope/chocolateShake.png",
                                description: "Classic rich and indulgent chocolate milkshake.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.10,
                                    "20oz": 4.25
                                },
                                defaultSize: "16oz",
                                itemType: "shake"
                            },
                            {
                                name: "Malteser Shake",
                                image: "https://u.cubeupload.com/ryanjhope/malteserShake.png",
                                description: "Creamy milkshake with the honeyed crunch of Malteser pieces.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.10,
                                    "20oz": 4.25
                                },
                                defaultSize: "16oz",
                                itemType: "shake"
                            },
                            {
                                name: "Vanilla Shake",
                                image: "https://u.cubeupload.com/ryanjhope/vanillaShake.png",
                                description: "Smooth and classic vanilla-flavored milkshake.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.10,
                                    "20oz": 4.25
                                },
                                defaultSize: "16oz",
                                itemType: "shake"
                            }
                        ]
                    },
                    "smoothies": {
                        title: "Smoothies",
                        items: [
                            {
                                name: "Paradise",
                                image: "https://u.cubeupload.com/ryanjhope/paradiseSmoothie.png",
                                description: "Pineapple, mango and passionfruit in a sweet and refreshing blend.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.15,
                                    "20oz": 4.30
                                },
                                defaultSize: "16oz",
                                disableCustomization: true
                            },
                            {
                                name: "Triple Berry",
                                image: "https://u.cubeupload.com/ryanjhope/trippleBeerry.png",
                                description: "Strawberry, blueberry and raspberry come together in a perfect blend.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.15,
                                    "20oz": 4.30
                                },
                                defaultSize: "16oz",
                                disableCustomization: true
                            },
                            {
                                name: "Reviving Green",
                                image: "https://u.cubeupload.com/ryanjhope/greenSmoothie.png",
                                description: "A healthy blend of mango, broccoli and spinach.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.15,
                                    "20oz": 4.30
                                },
                                defaultSize: "16oz",
                                disableCustomization: true
                            },
                            {
                                name: "Melon Heaven",
                                image: "https://u.cubeupload.com/ryanjhope/strawberryBanana.png",
                                description: "Watermelon, Honeydew and Cantaloupe melon in a refreshing blend.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.15,
                                    "20oz": 4.30
                                },
                                defaultSize: "16oz",
                                disableCustomization: true
                            },
                            {
                                name: "Blueberry Bliss",
                                image: "https://u.cubeupload.com/ryanjhope/blueBerryBliss.png",
                                description: "Blueberry, banana and strawberry come together in a sweet and tangy mix.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.15,
                                    "20oz": 4.30
                                },
                                defaultSize: "16oz",
                                disableCustomization: true
                            }
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
                                description: "Sweet, flaky pastry swirled with aromatic cinnamon and sugar.",
                                price: 2.45,
                                foodItem: true
                            },
                            {
                                name: "Chocolate Twist",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/54e41537c0958d8a12b0c9f3f0607056/58f691da9eaef86b0b51f9b2c483fe63.jpeg",
                                description: "Buttery pastry twisted with rich Belgian chocolate.",
                                price: 2.50,
                                foodItem: true
                            },
                            {
                                name: "Butter Croissant",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/158df3c8bd7a25888f15dcb1bbf1f13b/58f691da9eaef86b0b51f9b2c483fe63.jpeg",
                                description: "Classic French pastry, light and flaky with rich butter layers.",
                                price: 2.20,
                                foodItem: true
                            },
                            {
                                name: "Pain Aux Raisin",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/2c02391621e0537b4d36ef08d3ed9b3c/58f691da9eaef86b0b51f9b2c483fe63.jpeg",
                                description: "Traditional French pastry filled with custard and sweet raisins.",
                                price: 2.45,
                                foodItem: true
                            },
                            {
                                name: "Apple Crown",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/e030340445b6f053a977cca165f3dfc4/58f691da9eaef86b0b51f9b2c483fe63.jpeg",
                                description: "Golden pastry crown filled with spiced apple and custard.",
                                price: 2.80,
                                foodItem: true
                            },
                            {
                                name: "Pistachio Croissant",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/6c48b522cc34eddbf58dfe7fb3c4b8a5/bc9c318a9c96996e2d990faf2b0c65f6.jpeg",
                                description: "Flaky croissant filled with creamy pistachio cream and crushed nuts.",
                                price: 3.45,
                                foodItem: true,
                                badge: "POPULAR" // Added badge
                            },
                            {
                                name: "Almond Croissant",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/55bfb2ff9fed75b5a7d7e171d0686804/bc9c318a9c96996e2d990faf2b0c65f6.jpeg",
                                description: "Buttery croissant filled with sweet almond cream and sliced almonds.",
                                price: 2.40,
                                foodItem: true
                            },
                            {
                                name: "Large Fruit Scone",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/9f842cf2cd1e7f56511fe585a3a6b3bf/bc9c318a9c96996e2d990faf2b0c65f6.jpeg",
                                description: "Traditional British scone studded with juicy mixed fruit.",
                                price: 2.50,
                                foodItem: true
                            },
                            {
                                name: "Toasted Tea Cake",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/307b37e61ae9f702391b615925d89c9b/bc9c318a9c96996e2d990faf2b0c65f6.jpeg",
                                description: "Soft, spiced bun with currants, toasted and served warm.",
                                price: 2.50,
                                foodItem: true
                            },
                            {
                                name: "Cornish Pasty",
                                image: "https://u.cubeupload.com/ryanjhope/cornishPasty.png",
                                description: "Traditional savory pastry filled with seasoned beef and vegetables.",
                                price: 3.25,
                                foodItem: true
                            },
                            {
                                name: "Potato Roll",
                                image: "https://u.cubeupload.com/ryanjhope/potatoRoll.png",
                                description: "Hearty roll filled with seasoned mashed potato and herbs.",
                                price: 2.75,
                                foodItem: true
                            },
                            {
                                name: "Sage & Onion Roll",
                                image: "https://u.cubeupload.com/ryanjhope/sageonionRoll.png",
                                description: "Savory roll filled with aromatic sage and caramelized onion stuffing.",
                                price: 2.75,
                                foodItem: true
                            }
                        ]
                    },
                    "toasties": {
                        title: "Toasties & Paninis",
                        items: [
                            {
                                name: "Ham & Cheese Toastie",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/3f2ab241ff4876626d22488bb6366c97/bc9c318a9c96996e2d990faf2b0c65f6.jpeg",
                                description: "Savory ham and melted cheese grilled to golden perfection.",
                                price: 3.70,
                                foodItem: true
                            },
                            {
                                name: "Cheese & Onion Toastie",
                                image: null,
                                description: "Melted cheese and caramelized onions in golden, crispy bread.",
                                price: 3.70,
                                foodItem: true
                            },
                            {
                                name: "Cheese & Tomato Toastie",
                                image: null,
                                description: "Classic combination of melted cheese and fresh tomato slices.",
                                price: 3.70,
                                foodItem: true
                            },
                            {
                                name: "BBQ Chicken Panini",
                                image: "https://u.cubeupload.com/ryanjhope/bbqchickenPanini.png",
                                description: "Tender chicken with smoky BBQ sauce in a toasted panini.",
                                price: 4.50,
                                foodItem: true
                            },
                            {
                                name: "Sweet Chilli Chicken Panini",
                                image: null,
                                description: "Juicy chicken with sweet chilli sauce in a toasted panini.",
                                price: 4.50,
                                foodItem: true
                            },
                            {
                                name: "Ham & Cheese Panini",
                                image: null,
                                description: "Classic combination of ham and cheese in a toasted panini.",
                                price: 4.50,
                                foodItem: true
                            },
                            {
                                name: "Ham & Cheese Croque",
                                image: "https://u.cubeupload.com/ryanjhope/hamCheeseCroque.png",
                                description: "French-style grilled sandwich with ham, cheese, and creamy sauce.",
                                price: 4.50,
                                foodItem: true
                            },
                            {
                                name: "Mushroom Croque",
                                image: null,
                                description: "Savory grilled sandwich with mushrooms, cheese, and creamy sauce.",
                                price: 4.50,
                                foodItem: true
                            },
                            {
                                name: "Halloumi & Pesto Panini",
                                image: "https://u.cubeupload.com/ryanjhope/pestohalloumiPanini.png",
                                description: "Halloumi cheese with pesto in a toasted panini.",
                                price: 4.50,
                                foodItem: true
                            }
                        ]
                    },
                    "sandwiches": {
                        title: "Sandwiches",
                        items: [
                            {
                                name: "Ham Salad Sandwich",
                                image: "https://u.cubeupload.com/ryanjhope/hamsaladSandwich.png",
                                description: "Sliced ham with fresh lettuce, tomato, and cucumber in soft bread.",
                                price: 3.95,
                                foodItem: true
                            },
                            {
                                name: "Egg Mayo Sandwich",
                                image: null,
                                description: "Creamy egg mayonnaise with fresh cress in soft white bread.",
                                price: 3.75,
                                foodItem: true
                            },
                            {
                                name: "Tuna Sweetcorn Sandwich",
                                image: null,
                                description: "Flaked tuna mixed with sweetcorn and mayonnaise in fresh bread.",
                                price: 3.95,
                                foodItem: true
                            },
                            {
                                name: "Tomato & Cheese Sandwich",
                                image: null,
                                description: "Fresh sliced tomatoes with mature cheddar cheese in soft bread.",
                                price: 3.65,
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
                                description: "Rich chocolate tiffin with crunchy honeycomb pieces and biscuits.",
                                price: 2.60,
                                foodItem: true
                            },
                            {
                                name: "Apple Slice",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/d1de5478b0e171640d594dbf19381255/58f691da9eaef86b0b51f9b2c483fe63.jpeg",
                                description: "Moist cake slice with tender apples and warm cinnamon spices.",
                                price: 2.60,
                                foodItem: true
                            },
                            {
                                name: "Apricot Slice",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/dd850ad4d007baf753597ad302fcb851/bc9c318a9c96996e2d990faf2b0c65f6.jpeg",
                                description: "Sweet and tangy cake slice with juicy apricot pieces.",
                                price: 2.60,
                                foodItem: true
                            },
                            {
                                name: "Tiramisu Slice",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/c1ccbbc0851e35cce954540722bcbcc4/bc9c318a9c96996e2d990faf2b0c65f6.jpeg",
                                description: "Classic Italian dessert with coffee-soaked ladyfingers and mascarpone.",
                                price: 2.60,
                                foodItem: true
                            },
                            {
                                name: "Oreo Muffin",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/e5765c394d426af12b5b32428ab2e748/58f691da9eaef86b0b51f9b2c483fe63.jpeg",
                                description: "Fluffy vanilla muffin studded with crushed Oreo cookies.",
                                price: 2.60,
                                foodItem: true
                            },
                            {
                                name: "Chocolate Muffin",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/e3c835a249d1dd0aa8d3e6ddf2aac756/bc9c318a9c96996e2d990faf2b0c65f6.jpeg",
                                description: "Rich double chocolate muffin with chocolate chips.",
                                price: 2.60,
                                foodItem: true
                            },
                            {
                                name: "Blueberry Muffin",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/f5e690e36716ab783ddee68fce7ed57f/58f691da9eaef86b0b51f9b2c483fe63.jpeg",
                                description: "Classic muffin bursting with fresh, juicy blueberries.",
                                price: 2.60,
                                foodItem: true
                            },
                            {
                                name: "Lemon Drizzle",
                                image: "https://u.cubeupload.com/ryanjhope/lemonDrizzle.png",
                                description: "Zesty lemon sponge cake with a sweet lemon drizzle glaze.",
                                price: 2.60,
                                foodItem: true
                            },
                            {
                                name: "Carrot Cake",
                                image: null,
                                description: "Moist spiced cake with carrots, walnuts, and cream cheese frosting.",
                                price: 2.85,
                                foodItem: true
                            },
                            {
                                name: "Victoria Sponge Cake",
                                image: null,
                                description: "Classic British sponge cake with jam and fresh cream filling.",
                                price: 2.75,
                                foodItem: true
                            },
                            {
                                name: "Strawberry Tart",
                                image: null,
                                description: "Crisp pastry tart filled with vanilla custard and fresh strawberries.",
                                price: 2.95,
                                foodItem: true
                            }
                        ]
                    }
                }
            },
            // Collections Tab
            "collections": {
                title: "Collections",
                categories: {
                    "pistachio-collection": {
                        title: "Pistachio Collection",
                        backgroundColor: "#C7C694",
                        items: [
                            {
                                name: "Pistachio Iced Latte",
                                image: "https://u.cubeupload.com/ryanjhope/pistachioIcedLatte.png",
                                description: "Iced Latte made with creamy and rich pistachio butter.",
                                sizes: ["16oz", "20oz"],
                                prices: {
                                    "16oz": 4.10,
                                    "20oz": 4.25
                                },
                                defaultSize: "16oz",
                                collection: true
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
                                badge: "NEW",
                                collection: true
                            },
                            {
                                name: "Pistachio Croissant",
                                image: "https://tb-static.uber.com/prod/image-proc/processed_images/6c48b522cc34eddbf58dfe7fb3c4b8a5/bc9c318a9c96996e2d990faf2b0c65f6.jpeg",
                                price: 3.45,
                                foodItem: true,
                                badge: "POPULAR",
                                collection: true
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
        
        // Bubble tea specific extras (only Extra Bubbles)
        const bubbleTeaExtras = [
            {
                id: "extra-bubbles",
                name: "Extra Bubbles",
                price: 0.50
            }
        ];
        
        // Speciality Frappé specific extras
        const specialityFrappeExtras = [
            {
                id: "no-whipped-cream",
                name: "No Whipped Cream",
                price: 0.00
            },
            {
                id: "add-coffee-shot",
                name: "Add Coffee Shot",
                price: 0.50
            }
        ];
        
        // Shake specific extras (Add Whipped Cream since it's not included by default)
        const shakeExtras = [
            {
                id: "add-whipped-cream",
                name: "Add Whipped Cream",
                price: 0.50
            }
        ];
        
        // Bubble Tea Frappé specific extras (includes whipped cream by default)
        const bubbleTeaFrappeExtras = [
            {
                id: "no-whipped-cream",
                name: "No Whipped Cream",
                price: 0.00
            },
            {
                id: "extra-bubbles",
                name: "Extra Bubbles",
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
        
        /* View toggle controls */
        .view-controls {
            margin-bottom: 20px;
        }
        
        .view-toggle-container {
            background-color: #f3f4f6;
            border-radius: 25px;
            padding: 4px;
            display: flex;
            gap: 2px;
        }
        
        .view-toggle-btn {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            border: none;
            background-color: transparent;
            color: #6b7280;
            cursor: pointer;
            transition: all 0.2s ease;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .view-toggle-btn:hover {
            color: #374151;
        }
        
        .view-toggle-btn.active {
            background-color: #f86400;
            color: white;
            box-shadow: 0 2px 4px rgba(248, 100, 0, 0.3);
        }




        /* Grid layout */
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
        
        /* List layout */
        .menu-list {
            display: flex;
            flex-direction: column;
            gap: 8px;
            margin: 0 auto;
            max-width: 600px;
        }
        
        /* List view item styles */
        .menu-item.list-view {
            display: flex;
            align-items: center;
            padding: 12px;
            border-radius: 12px;
            background-color: white;
            box-shadow: 0 1px 3px rgba(0,0,0,0.05);
            cursor: pointer;
            transition: all 0.2s ease;
        }
        
        .menu-item.list-view:hover {
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
        }
        
        /* List view image */
        .list-view-image {
            width: 60px;
            height: 60px;
            border-radius: 8px;
            object-fit: cover;
            margin-right: 12px;
            flex-shrink: 0;
        }
        
        /* Invisible placeholder for list view alignment */
        .list-view-image-placeholder {
            width: 60px;
            height: 60px;
            margin-right: 12px;
            flex-shrink: 0;
            /* Completely invisible but maintains space */
        }
        
        /* List view content */
        .list-view-content {
            flex: 1;
            text-align: left;
        }
        
        .list-view-title {
            font-size: 16px;
            font-weight: 700;
            margin: 0 0 4px 0;
            color: #374151;
        }
        
        .list-view-description {
            font-size: 12px;
            color: #6b7280;
            margin: 0 0 4px 0;
            line-height: 1.3;
        }
        
        .list-view-sizes {
            font-size: 11px;
            color: #9ca3af;
            margin: 0;
        }
        
        /* List view price */
        .list-view-price {
            font-size: 16px;
            font-weight: 700;
            color: #f86400;
            margin-left: 12px;
            flex-shrink: 0;
        }
        
        /* List view badge */
        .list-view-badge {
            position: absolute;
            top: 8px;
            left: 8px;
            color: white;
            padding: 2px 6px;
            border-radius: 12px;
            font-weight: 600;
            font-size: 10px;
            z-index: 10;
        }
        
        /* Hide grid-specific elements in list view */
        .list-view .item-header,
        .list-view .price-badge,
        .list-view .inline-price-badge,
        .list-view .food-item-header,
        .list-view .item-details {
            display: none;
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
        
        /* Collection background styling */
        .collection-background {
            border-radius: 16px;
            padding: 12px;
            margin: 8px;
        }
        
        /* Medium screens - adjust padding */
        @media (min-width: 768px) {
            .collection-background {
                padding: 14px;
                margin: 10px;
            }
        }
        
        /* Large screens - adjust padding */
        @media (min-width: 1024px) {
            .collection-background {
                padding: 16px;
                margin: 12px;
            }
        }
        
        /* Tab divider styling */
        .tab-divider {
            width: 60%;
            height: 1px;
            background-color: #e5e7eb;
            margin: 10px auto;
        }
    </style>
</head>
<body>
    <div id="menu-container" class="container mx-auto max-w-5xl bg-white">
        <!-- Tab Navigation -->
        <div class="tab-navigation mb-4" id="tab-buttons">
            <!-- Main tab buttons will be generated here -->
            <div class="main-tabs flex justify-center overflow-x-auto pb-1" id="main-tab-buttons">
            </div>
            <!-- Collections tab separator and button -->
            <div class="collections-tab-section" id="collections-tab-section" style="display: none;">
                <div class="tab-divider"></div>
                <div class="flex justify-center pt-2" id="collections-tab-button">
                </div>
            </div>
        </div>




        <!-- View Toggle Controls -->
        <div class="view-controls flex justify-center items-center mb-4">
            <div class="view-toggle-container bg-gray-100 rounded-full p-1 flex">
                <button id="list-view-btn" class="view-toggle-btn active" data-view="list" title="List View">
                    <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M3 13h2v-2H3v2zm0 4h2v-2H3v2zm0-8h2V7H3v2zm4 4h14v-2H7v2zm0 4h14v-2H7v2zM7 7v2h14V7H7z"/>
                    </svg>
                </button>
                <button id="grid-view-btn" class="view-toggle-btn" data-view="grid" title="Grid View">
                    <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
                        <path d="M3 3h8v8H3V3zm10 0h8v8h-8V3zM3 13h8v8H3v-8zm10 0h8v8h-8v-8z"/>
                    </svg>
                </button>
            </div>
        </div>




        <!-- Menu Content -->
        <div class="tab-container" id="tab-content">
            <!-- Tab content will be generated here -->
        </div>
    </div>




    <script>
        // Global variables
        let currentlyExpandedItem = null;
        let currentView = 'list'; // Default to list view
        
        // Generate menu from configuration
        document.addEventListener('DOMContentLoaded', function() {
            const tabButtonsContainer = document.getElementById('tab-buttons');
            const tabContentContainer = document.getElementById('tab-content');
            
            // Generate tab buttons
            const mainTabButtonsContainer = document.getElementById('main-tab-buttons');
            const collectionsTabButtonContainer = document.getElementById('collections-tab-button');
            const collectionsTabSection = document.getElementById('collections-tab-section');
            
            let hasCollections = false;
            let isFirstVisibleTab = true;
            
            for (const tabId in menuData) {
                const tab = menuData[tabId];
                
                // Check if this is the collections tab (hidden)
                const isCollectionsTab = tabId === 'collections';
                
                // Create tab button
                const tabButton = document.createElement('button');
                // Only make the first non-collections tab active
                const isActiveTab = !isCollectionsTab && isFirstVisibleTab;
                tabButton.className = `tab-btn flex-shrink-0 px-4 py-2 mr-2 rounded-full ${isActiveTab ? 'active bg-primary text-white' : 'bg-gray-200 hover:bg-gray-300'} font-bold`;
                tabButton.dataset.tab = tabId;
                tabButton.textContent = tab.title;
                tabButton.style.fontFamily = "'Poppins', sans-serif";
                if (isActiveTab) {
                    tabButton.style.backgroundColor = '#f86400';
                } else {
                    tabButton.style.color = '#555555';
                }
                
                if (isCollectionsTab) {
                    collectionsTabButtonContainer.appendChild(tabButton);
                    hasCollections = true;
                } else {
                    mainTabButtonsContainer.appendChild(tabButton);
                    // Mark that we've processed the first visible tab
                    if (isFirstVisibleTab) {
                        isFirstVisibleTab = false;
                    }
                }
                
                // Create tab content
                const tabContent = document.createElement('div');
                tabContent.id = tabId;
                // Only make the first non-collections tab active
                tabContent.className = `tab-content ${isActiveTab ? 'active' : ''}`;
                




                
                // Generate categories and items
                for (const categoryId in tab.categories) {
                    const category = tab.categories[categoryId];
                    
                    // Add category title
                    const categoryTitle = document.createElement('h3');
                    categoryTitle.className = 'text-3xl font-bold category-title text-center mx-auto';
                    categoryTitle.style.fontFamily = "'Poppins', sans-serif";
                    categoryTitle.style.color = '#555555';
                    categoryTitle.style.textShadow = '0 0 1px rgba(248, 100, 0, 0.2)';
                    categoryTitle.textContent = category.title;
                    tabContent.appendChild(categoryTitle);
                    
                    // Add items container (grid or list)
                    const itemsContainer = document.createElement('div');
                    itemsContainer.className = currentView === 'grid' ? 'menu-grid' : 'menu-list';
                    
                    // Check if this is a collection category and wrap in special background
                    if (category.backgroundColor) {
                        const collectionBackground = document.createElement('div');
                        collectionBackground.className = 'collection-background';
                        collectionBackground.style.backgroundColor = category.backgroundColor;
                        
                        const innerGrid = document.createElement('div');
                        innerGrid.className = currentView === 'grid' ? 'menu-grid' : 'menu-list';
                        
                        // Generate all items inside the collection background
                        category.items.forEach((item, index) => {
                            const itemId = `${categoryId}-collection-${index}`;
                            const itemElement = createMenuItem(item, itemId, categoryId);
                            innerGrid.appendChild(itemElement);
                        });
                        
                        collectionBackground.appendChild(innerGrid);
                        tabContent.appendChild(collectionBackground);
                        continue; // Skip the normal processing below
                    }
                    
                    // If no items, show "Coming soon"
                    if (category.items.length === 0) {
                        const emptyMessage = document.createElement('p');
                        emptyMessage.className = 'empty-category text-center';
                        emptyMessage.textContent = 'Coming soon!';
                        itemsContainer.appendChild(emptyMessage);
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
                            itemsContainer.appendChild(itemElement);
                        });
                        
                        // If there are items without images, add an invisible divider and then those items (only in grid view)
                        if (itemsWithoutImages.length > 0 && itemsWithImages.length > 0 && currentView === 'grid') {
                            // Add an invisible divider after items with images
                            const divider = document.createElement('div');
                            divider.className = 'section-divider';
                            divider.style.backgroundColor = 'white'; // Make the line invisible
                            itemsContainer.appendChild(divider);
                        }
                        
                        // Then generate items without images
                        itemsWithoutImages.forEach((item, index) => {
                            const itemId = `${categoryId}-without-image-${index}`;
                            const itemElement = createMenuItem(item, itemId, categoryId);
                            itemsContainer.appendChild(itemElement);
                        });
                    }
                    
                    tabContent.appendChild(itemsContainer);
                }
                
                tabContentContainer.appendChild(tabContent);
                isFirst = false;
            }
            
            // Show the collections section if collections exist
            // Temporarily hidden - uncomment to re-enable collections tab
            // if (hasCollections) {
            //     collectionsTabSection.style.display = 'block';
            // }
            
            // Set up view toggle buttons
            document.getElementById('list-view-btn').addEventListener('click', function() {
                if (currentView !== 'list') {
                    currentView = 'list';
                    this.classList.add('active');
                    document.getElementById('grid-view-btn').classList.remove('active');
                    refreshMenuDisplay();
                }
            });
            
            document.getElementById('grid-view-btn').addEventListener('click', function() {
                if (currentView !== 'grid') {
                    currentView = 'grid';
                    this.classList.add('active');
                    document.getElementById('list-view-btn').classList.remove('active');
                    refreshMenuDisplay();
                }
            });
            
            // Function to create a menu item element
            function createMenuItem(item, itemId, categoryId) {
                // Create item element
                const itemElement = document.createElement('div');
                itemElement.className = currentView === 'grid' ? 'menu-item' : 'menu-item list-view';
                itemElement.id = itemId;
                
                // Handle list view layout
                if (currentView === 'list') {
                    return createListViewItem(item, itemElement);
                }
                
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
                        } else if (item.itemType === 'bubble-tea') {
                            itemExtras = bubbleTeaExtras;
                            showMilkOptions = false; // No milk options for bubble tea
                        } else if (item.itemType === 'speciality-frappe') {
                            itemExtras = specialityFrappeExtras;
                            showMilkOptions = false; // No milk options for speciality frappé
                        } else if (item.itemType === 'shake') {
                            itemExtras = shakeExtras;
                            showMilkOptions = false; // No milk options for shakes
                        } else if (item.itemType === 'bubble-tea-frappe') {
                            itemExtras = bubbleTeaFrappeExtras;
                            showMilkOptions = false; // No milk options for bubble tea frappé
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
            
            // Function to create list view item - invisible placeholder for missing images to maintain alignment
            function createListViewItem(item, itemElement) {
                // Create image or invisible placeholder for alignment
                if (item.image) {
                    const img = document.createElement('img');
                    img.className = 'list-view-image';
                    img.src = item.image;
                    img.alt = item.name;
                    itemElement.appendChild(img);
                } else {
                    // Create invisible placeholder to maintain alignment
                    const placeholder = document.createElement('div');
                    placeholder.className = 'list-view-image-placeholder';
                    itemElement.appendChild(placeholder);
                }
                
                // Create content area
                const content = document.createElement('div');
                content.className = 'list-view-content';
                
                // Title
                const title = document.createElement('h4');
                title.className = 'list-view-title';
                title.textContent = item.name;
                content.appendChild(title);
                
                // Description (for both drinks and food)
                if (item.description) {
                    const description = document.createElement('p');
                    description.className = 'list-view-description';
                    description.textContent = item.description;
                    content.appendChild(description);
                }
                
                // Sizes (for drinks)
                if (item.sizes && !item.foodItem) {
                    const sizes = document.createElement('p');
                    sizes.className = 'list-view-sizes';
                    sizes.textContent = `Available in: ${item.sizes.join(', ')}`;
                    content.appendChild(sizes);
                }
                
                itemElement.appendChild(content);
                
                // Price
                const price = document.createElement('div');
                price.className = 'list-view-price';
                if (item.foodItem) {
                    price.textContent = `£${item.price.toFixed(2)}`;
                } else {
                    price.textContent = `£${item.prices[item.defaultSize].toFixed(2)}`;
                }
                itemElement.appendChild(price);
                
                // Add badge if needed
                if (item.badge) {
                    const badge = document.createElement('div');
                    badge.className = `list-view-badge badge-${item.badge.toLowerCase()}`;
                    badge.textContent = item.badge;
                    itemElement.style.position = 'relative';
                    itemElement.appendChild(badge);
                }
                
                return itemElement;
            }
            
            // Function to refresh the entire menu display
            function refreshMenuDisplay() {
                // Clear all tab content
                const tabContentContainer = document.getElementById('tab-content');
                tabContentContainer.innerHTML = '';
                
                // Find which tab is currently active
                const activeTabBtn = document.querySelector('.tab-btn.active');
                const activeTabId = activeTabBtn ? activeTabBtn.getAttribute('data-tab') : 'hot-drinks';
                
                // Regenerate all tabs
                generateAllTabs();
                
                // Reactivate the previously active tab
                document.querySelectorAll('.tab-content').forEach(content => {
                    content.classList.remove('active');
                });
                const activeTab = document.getElementById(activeTabId);
                if (activeTab) {
                    activeTab.classList.add('active');
                }
            }
            
            // Function to generate all tabs
            function generateAllTabs() {
                const tabContentContainer = document.getElementById('tab-content');
                
                for (const tabId in menuData) {
                    const tab = menuData[tabId];
                    
                    // Create tab content
                    const tabContent = document.createElement('div');
                    tabContent.id = tabId;
                    tabContent.className = 'tab-content';
                    
                    // Generate categories and items
                    for (const categoryId in tab.categories) {
                        const category = tab.categories[categoryId];
                        
                        // Add category title
                        const categoryTitle = document.createElement('h3');
                        categoryTitle.className = 'text-3xl font-bold category-title text-center mx-auto';
                        categoryTitle.style.fontFamily = "'Poppins', sans-serif";
                        categoryTitle.style.color = '#555555';
                        categoryTitle.style.textShadow = '0 0 1px rgba(248, 100, 0, 0.2)';
                        categoryTitle.textContent = category.title;
                        tabContent.appendChild(categoryTitle);
                        
                        // Add items container
                        const itemsContainer = document.createElement('div');
                        itemsContainer.className = currentView === 'grid' ? 'menu-grid' : 'menu-list';
                        
                        // Check if this is a collection category
                        if (category.backgroundColor) {
                            const collectionBackground = document.createElement('div');
                            collectionBackground.className = 'collection-background';
                            collectionBackground.style.backgroundColor = category.backgroundColor;
                            
                            const innerContainer = document.createElement('div');
                            innerContainer.className = currentView === 'grid' ? 'menu-grid' : 'menu-list';
                            
                            category.items.forEach((item, index) => {
                                const itemId = `${categoryId}-collection-${index}`;
                                const itemElement = createMenuItem(item, itemId, categoryId);
                                innerContainer.appendChild(itemElement);
                            });
                            
                            collectionBackground.appendChild(innerContainer);
                            tabContent.appendChild(collectionBackground);
                            continue;
                        }
                        
                        // Regular category processing
                        if (category.items.length === 0) {
                            const emptyMessage = document.createElement('p');
                            emptyMessage.className = 'empty-category text-center';
                            emptyMessage.textContent = 'Coming soon!';
                            itemsContainer.appendChild(emptyMessage);
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
                            
                            // Generate items with images
                            itemsWithImages.forEach((item, index) => {
                                const itemId = `${categoryId}-with-image-${index}`;
                                const itemElement = createMenuItem(item, itemId, categoryId);
                                itemsContainer.appendChild(itemElement);
                            });
                            
                            // Add divider only in grid view
                            if (itemsWithoutImages.length > 0 && itemsWithImages.length > 0 && currentView === 'grid') {
                                const divider = document.createElement('div');
                                divider.className = 'section-divider';
                                divider.style.backgroundColor = 'white';
                                itemsContainer.appendChild(divider);
                            }
                            
                            // Generate items without images
                            itemsWithoutImages.forEach((item, index) => {
                                const itemId = `${categoryId}-without-image-${index}`;
                                const itemElement = createMenuItem(item, itemId, categoryId);
                                itemsContainer.appendChild(itemElement);
                            });
                        }
                        
                        tabContent.appendChild(itemsContainer);
                    }
                    
                    tabContentContainer.appendChild(tabContent);
                }
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
