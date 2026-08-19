# CraveWave - Premium Food Delivery App
## UI/UX Design Specification & Handoff Document

This document serves as the comprehensive UI/UX design handoff for **CraveWave**, a modern, premium food delivery application. It details the brand identity, design system, component library, and all 20 core screens along with their states, flows, and data requirements.

---

## 1. Brand Identity & Design Concept

**App Name:** CraveWave
**Concept:** A food discovery and delivery platform emphasizing high-quality restaurant discovery, blazing-fast delivery, and a premium, clean aesthetic.
**Vibe:** Energetic, appetizing, clean, premium, accessible.

### 1.1 Color Palette
**Light Mode:**
*   **Primary Accent:** Saffron Burst (`#FF5722`) - Used for primary actions, badges, active states.
*   **Primary Dark:** Roasted Pepper (`#D84315`) - Used for pressed states and deep accents.
*   **Background (Base):** Crisp White (`#FFFFFF`) - Main app background.
*   **Background (Secondary):** Pearl Grey (`#F7F8FA`) - Used for cards, elevated elements, and subtle grouping.
*   **Text (Primary):** Charcoal (`#1A1A1A`) - Headings, main text.
*   **Text (Secondary):** Slate Grey (`#757575`) - Subtitles, captions, unselected states.
*   **Success:** Leaf Green (`#4CAF50`) - Delivery tracking, veg indicators, success toasts.
*   **Warning/Offers:** Golden Yellow (`#FFC107`) - Ratings, premium offers.
*   **Error:** Crimson (`#E53935`) - Non-veg indicators, errors, destruct actions.

**Dark Mode:**
*   **Background (Base):** Deep Onyx (`#121212`)
*   **Background (Secondary):** Charcoal Surface (`#1E1E1E`)
*   **Text (Primary):** Off-White (`#F5F5F5`)
*   **Text (Secondary):** Light Slate (`#A0A0A0`)
*   *Note: Primary accents remain similar but are slightly desaturated for better dark-mode contrast.*

### 1.2 Typography Hierarchy
**Font Family:** `Inter` (Clean, highly legible, modern geometric sans-serif)

*   **H1 (Display):** 32px, Bold (Greeting, Major screen headers)
*   **H2 (Title):** 24px, SemiBold (Section headers, Restaurant Names in details)
*   **H3 (Subtitle):** 18px, Medium (Card titles, Dish Names)
*   **Body (Primary):** 14px, Regular (Descriptions, Reviews)
*   **Body (Secondary):** 12px, Regular (Distance, Delivery time, Minor info)
*   **Caption/Badge:** 10px, Bold, Uppercase (Tags, Promos)

---

## 2. Design System Components

### 2.1 Buttons
*   **Primary Button:** Saffron Burst background, White text, full width (or wide), 16px corner radius, subtle drop shadow.
*   **Secondary Button:** Transparent background, Saffron Burst border (1.5px), Saffron Burst text.
*   **Text Button:** No background or border, bold Saffron Burst text.
*   **FAB (Floating Action Button):** Circular, Saffron Burst, prominent drop shadow (used for Cart overlay).

### 2.2 Input Fields & Search
*   **Text Field:** Pearl Grey background (Light mode), no border, 12px corner radius. Placeholder text in Slate Grey. Active state gets a 1.5px Saffron Burst border.
*   **Search Bar:** Large, pill-shaped (full radius), leading search icon (magnifying glass), trailing filter/mic icon. Sticky at the top of Home and Search screens.

### 2.3 Cards
*   **Restaurant Card (Vertical):** 16px corner radius. Top 60% is a high-quality food image. Bottom 40% contains Name, Rating (star icon + number), Cuisine tags, Price for two, Delivery time, and Distance.
*   **Food Card (Horizontal):** Left side holds dish info (veg/non-veg icon, name, price, description, rating). Right side holds a square image (rounded corners) with an overlapping "ADD" button at the bottom edge of the image.
*   **Offer/Promo Card:** Vibrant gradients (Saffron to Deep Orange), bold typography, dynamic shapes or food illustrations on the right side.

### 2.4 Navigation
*   **Top Navigation:** Clean white background, contextual. On Home: Location pin + Address selector dropdown, trailing profile avatar.
*   **Bottom Navigation:** Fixed at the bottom, white background, subtle top shadow. 5 icons: Home, Search, Orders, Favourites, Profile. Selected state: Icon filled with Saffron Burst, small label below. Unselected: Outlined Slate Grey icons.

### 2.5 Chips & Tags
*   **Filter Chips:** Pill-shaped, light grey background, dark text. Active state: Saffron Burst background, white text.
*   **Veg/Non-Veg Badges:** Standard Indian dietary indicators. Green square with green dot (Veg). Red square with red triangle/dot (Non-Veg).

### 2.6 States & Feedback
*   **Loading:** Skeleton screens mimicking the layout of cards/lists with a shimmering grey effect.
*   **Empty States:** Friendly illustration (e.g., empty plate for no orders, magnifying glass for no search results) + Headline + Secondary Text + Primary Action Button.
*   **Bottom Sheets:** Used for Filters, Address Selection, Cart customisations. Drag handle at the top, 24px top corner radii.

---

## 3. Screen Specifications (20 Screens)

### 1. Splash Screen
*   **Visuals:** Full screen Crisp White (or Onyx for dark mode). Centered CraveWave logo (abstract wave merging with a cloche/plate).
*   **Animation:** Logo subtly scales up, a small "Saffron Burst" swoosh traces the wave.
*   **Transition:** Fades smoothly into Onboarding or Home (if logged in).

### 2. Onboarding (3 Pages - Swipeable)
*   **Screen 2.1:** "Discover Local Flavours" - Illustration of a user looking at a floating map with restaurant pins.
*   **Screen 2.2:** "Lightning Fast Delivery" - Illustration of a delivery partner on a scooter leaving a speed trail.
*   **Screen 2.3:** "Satisfy Your Cravings" - Collage of high-res, mouth-watering Indian dishes (Biryani, Dosa, Paneer Tikka).
*   **UI:** Page indicator dots (active dot is longer/capsule shaped), "Skip" text top-right, "Get Started" primary button on the last screen.

### 3. Login / Sign Up
*   **Layout:** Clean header with CraveWave logo.
*   **Inputs:** Large input field for "+91 Mobile Number".
*   **Actions:** "Continue" button. "Or continue with" divider. Social buttons (Google, Apple) as wide buttons with brand icons.
*   **Flow:** Entering number slides to OTP Screen (4 large digit boxes, "Resend in 0:30", Auto-verify animation).

### 4. Home Screen
*   **Header:** Location pin + "Home - Sector 45..." (tap to change). User avatar top right.
*   **Search Bar:** Prominent, sticky on scroll. "Search 'Biryani'..."
*   **Banners:** Horizontal scroll of Offer Cards (e.g., "50% OFF up to ₹100").
*   **Categories:** Grid of circular icons + text (Biryani, Pizza, Burger, Healthy, Thali).
*   **Section 1: Trending Near You:** Horizontal scroll of vertical Restaurant Cards.
*   **Section 2: Crave-Worthy Dishes:** Grid of specific food items.
*   **Section 3: All Restaurants:** Vertical list. Sticky filter chips above it (Sort, Fast Delivery, Pure Veg, Rating 4.0+).

### 5. Search
*   **Header:** Search input focused automatically, back arrow.
*   **Pre-Search State:** "Recent Searches" chips. "Popular Cuisines" grid.
*   **Active Search:** Auto-suggestions split into "Dishes" and "Restaurants".
*   **Results:** Toggle between "Restaurants" and "Dishes" tabs.

### 6. Restaurant Listing (From Category/Search)
*   **Header:** Title of Category/Search term.
*   **Filters:** Sticky row of pills (Rating, Cost, Distance).
*   **List:** Full-width vertical cards. High-res cover photo, prominent delivery ETA and distance overlay on the image.

### 7. Restaurant Details
*   **Hero Image:** Massive edge-to-edge photo of the restaurant's signature dish or interior. Fades into the header on scroll down.
*   **Info Panel:** Floating card overlapping the hero image. Name, Tags (North Indian, Chinese), Star rating box, ETA, Average Cost.
*   **Offers:** Small scrollable row of dotted-border coupon tickets.
*   **Menu Tabs:** Sticky horizontal scroll (Recommended, Starters, Main Course, Breads).
*   **Dish List:** Horizontal Food Cards (detailed in 2.3).
*   **FAB:** "Menu" button bottom-right to jump to categories.
*   **Cart Overlay:** If items added, a bottom bar slides up: "2 items | ₹450 -> View Cart".

### 8. Food Item Details (Bottom Sheet or Screen)
*   **Visuals:** Large square or 4:3 high-res image of the dish.
*   **Details:** Veg/Non-Veg tag, Name, Price, detailed description.
*   **Customisations:** Radio buttons for Size (Half/Full), Checkboxes for Add-ons (Extra Cheese, Dips).
*   **Action:** Quantity stepper (- 1 +), huge "Add Item - ₹X" primary button fixed at the bottom.

### 9. Cart
*   **Header:** "Your Cart from [Restaurant Name]".
*   **Items:** List of added items. Each has Name, Customisation subtext, Price, and a small (- 1 +) stepper.
*   **Upsell:** "Add ₹50 more to save ₹20 on delivery".
*   **Offers:** "Apply Coupon" row with a right arrow.
*   **Bill Details:** Subtotal, GST, Restaurant Charges, Delivery Fee, Total to Pay.
*   **Action:** Fixed bottom bar: Delivery Address summary, "Proceed to Pay" button.

### 10. Address Selection
*   **Map:** Top half shows an interactive map with a pin.
*   **Saved:** Bottom sheet showing "Home", "Work", "Other" with icons.
*   **Input:** Text fields for Flat No, Landmark. Toggle for "Leave at door".

### 11. Payment
*   **Summary:** Total amount at the top.
*   **Methods:** Accordion style list. 
    *   UPI (Google Pay, PhonePe logos).
    *   Credit/Debit Cards (Add new card).
    *   Wallets.
    *   Cash on Delivery.
*   **Action:** "Pay ₹X" button. Secure badge below it.

### 12. Order Confirmation
*   **Visuals:** Full screen. Lottie animation of a success checkmark morphing into a cooking pot or delivery box.
*   **Details:** "Order Received!". Order ID: #CRV-12345.
*   **Action:** "Track Order" primary button.

### 13. Live Order Tracking
*   **Map:** Full screen map showing route from Restaurant to Home. Animated scooter icon moving in real-time.
*   **Status Card (Bottom Sheet):** Swipeable up.
    *   **Timeline:** Vertical progress line (Accepted -> Preparing -> Picked Up -> Arriving).
    *   **ETA:** Giant text "Arriving in 15 mins".
    *   **Partner Info:** Photo, Name, Rating, Call Button.

### 14. Orders (History)
*   **List:** Vertical list of past orders.
*   **Card:** Restaurant Name, Date, Items summary ("1x Butter Chicken, 2x Naan"), Total Price, Status (Delivered/Cancelled).
*   **Actions:** "Reorder" button (Primary), "Rate" button (Secondary).

### 15. Favourites
*   **Tabs:** "Restaurants" | "Dishes".
*   **Grid/List:** Display of saved items. Heart icon in the corner filled with red.

### 16. Reviews & Ratings
*   **Flow:** Opened from Past Orders.
*   **Input:** 5-star interactive row. If 4-5 stars: "What did you love?". If 1-3 stars: "What went wrong?".
*   **Tags:** Multi-select chips (Taste, Packaging, Portion).
*   **Text:** Optional comment box.
*   **Photo:** "Upload Photo" dotted box.

### 17. Profile
*   **Header:** User Photo, Name, Email, Phone.
*   **Menu List:** Clean list with left icons and right chevrons.
    *   Your Orders
    *   Favourite Orders
    *   Address Book
    *   Payment Methods
    *   Settings
    *   Help & Support
*   **Footer:** App Version, Logout button (Red text).

### 18. Notifications
*   **List:** Categorized by "Today", "Yesterday".
*   **Cards:** Icon (Scooter for tracking, Percent for offers), Title, Subtitle, Time. Unread items have a pale Saffron background.

### 19. Offers
*   **Visuals:** Visually rich screen. Confetti graphics at the top.
*   **Coupons:** Rectangular cards with perforated edges. Prominent Code (e.g., "WELCOME50"), "Tap to copy", Terms & Conditions dropdown.

### 20. Help & Support
*   **Header:** "How can we help you, [Name]?"
*   **Quick Links:** Chips for "Recent Order", "Refund Status".
*   **FAQ List:** Accordion style.
*   **Action:** "Chat with us" FAB pinned to the bottom right.

---

## 4. UX Guidelines & Interactions

*   **Haptic Feedback:** Subtle vibrations on adding items to cart, successful payment, and completing the order rating.
*   **Transitions:**
    *   *Hero Image Parallax:* Scrolling down a Restaurant Detail screen pushes the image up slightly slower than the text.
    *   *Shared Element Transitions:* Tapping a restaurant card on Home smoothly expands its image to become the header of the Restaurant Detail screen.
*   **Accessibility:** 
    *   Minimum touch target size: 48x48dp.
    *   High contrast ratio for text elements against backgrounds.
    *   Screen reader compatibility labels defined for all icon buttons.
*   **Localization/Currency:** All prices formatted to Indian Rupees (₹) by default, standard Indian address formats (Landmark, Block).

---
*Generated by CouldAI Design Assistant*