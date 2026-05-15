# Digital Bookstore

> A student book marketplace for buying, selling, wishlisting, comparing, and managing new or used books.

![React](https://img.shields.io/badge/React-JS-61DAFB?style=for-the-badge&logo=react&logoColor=000)
![Vite](https://img.shields.io/badge/Vite-Build%20Tool-646CFF?style=for-the-badge&logo=vite&logoColor=fff)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=000)
![React Router](https://img.shields.io/badge/React%20Router-Routing-CA4245?style=for-the-badge&logo=reactrouter&logoColor=fff)
![Open Library](https://img.shields.io/badge/API-Open%20Library-2B6CB0?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-College%20Mini%20Project-success?style=for-the-badge)

Digital Bookstore is a React JS and Vite based online book marketplace designed for students. It helps students browse academic and general books, search by subject or author, compare options, manage a wishlist, add books to cart, place demo orders, and list used books for sale.

The project uses the Open Library API to fetch real book data and combines it with local demo marketplace data such as price, condition, seller details, stock, reviews, and ratings. Most user actions are stored in `localStorage`, making the app work like a complete frontend e-commerce prototype without requiring a backend.

## Table of Contents

- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- [Objectives](#objectives)
- [Key Features](#key-features)
- [Extra Features](#extra-features)
- [Tech Stack](#tech-stack)
- [API Used](#api-used)
- [Project Architecture](#project-architecture)
- [Folder Structure](#folder-structure)
- [Installation and Setup](#installation-and-setup)
- [Available Scripts](#available-scripts)
- [How to Use the Website](#how-to-use-the-website)
- [Pages Description](#pages-description)
- [Data Storage](#data-storage)
- [React Concepts Used](#react-concepts-used)
- [Screenshots](#screenshots)
- [Challenges Faced](#challenges-faced)
- [Future Enhancements](#future-enhancements)
- [Learning Outcomes](#learning-outcomes)
- [Project Status](#project-status)
- [Author](#author)
- [License](#license)

## Project Overview

Digital Bookstore is a student-focused online book marketplace where students can buy and sell new or used books. It is useful for college students because course books, reference books, competitive exam books, and technical books can be expensive when purchased new every semester.

The website solves this problem by providing one place where students can:

- Find affordable used books.
- Compare books based on price, rating, condition, and availability.
- Save books to wishlist for later.
- Add books to cart and view complete pricing.
- Sell their own used books by creating a marketplace listing.
- Track demo orders and manage profile information.

For a college project, this application demonstrates a practical e-commerce workflow using React, API integration, routing, state management, reusable components, and browser-based data persistence.

## Problem Statement

"Digital Bookstore is an online store where students can browse, search, and manage a collection of new or used books. It provides dynamic product display, search functionality, shopping cart with pricing, order summary and history, book categorization by genre/author, user reviews and ratings, wishlist, and sorting options."

## Objectives

- To create a student-friendly digital bookstore.
- To allow students to buy and sell used books.
- To provide search, filter, and sorting functionality.
- To manage cart, wishlist, orders, and profile.
- To use API-based book data with fallback local data.
- To build a responsive React web application.

## Key Features

| Feature | Description |
| --- | --- |
| Dynamic product display | Displays local demo books and API books in a responsive book grid with title, author, cover, price, rating, condition, and stock details. |
| Open Library API book fetching | Fetches real books from Open Library based on default and user-entered search terms. |
| Local demo books fallback | Uses local book data when API data is unavailable or when demo marketplace information is needed. |
| Search by title, author, and genre | Allows students to quickly search books using title, author, genre, subject, or publication-related terms. |
| Category and subject chips | Provides quick search chips such as Programming, Computer Science, Data Science, AI, Mathematics, Business, Literature, Design, and Engineering. |
| Advanced filters | Filters books by genre, author, condition, availability, maximum price, and minimum rating. |
| Sorting options | Sorts books by featured order, price low to high, price high to low, rating, and newest books. |
| Shopping cart | Supports adding books to cart, changing quantity, removing items, saving for later, and viewing complete price calculation. |
| Wishlist | Lets users save books for later and move wishlist items to the cart. |
| Compare books | Allows comparison of up to three books based on important marketplace details. |
| Book details page | Shows detailed book information, seller details, reviews, condition notes, and related actions. |
| Quick view modal | Provides a faster way to preview book details without leaving the listing page. |
| User reviews and ratings | Supports demo review submission and updates the displayed average rating. |
| Sell used book form | Allows students to list their used books with book details, price, condition, and contact information. |
| Order summary | Shows subtotal, discount, delivery charge, coupon discount, and final total. |
| Order history | Stores placed orders locally and displays previous order information. |
| Order tracking/status | Shows order progress using demo status steps such as Confirmed, Packed, Shipped, and Delivered. |
| Profile section | Manages student profile, orders, wishlist, listed books, reviews, settings, and account information. |
| Login/signup demo authentication | Provides frontend-only demo login and signup using localStorage. |
| Admin dashboard demo | Includes a demo admin area for managing locally listed books and marketplace data. |
| Dark mode | Supports light and dark themes with saved theme preference. |
| Responsive design | Works across desktop, tablet, and mobile screen sizes. |
| Toast notifications | Displays short feedback messages for actions such as cart updates, wishlist updates, login, and orders. |
| LocalStorage persistence | Saves cart, wishlist, orders, profile, listings, reviews, theme, comparison list, and session data in the browser. |

## Extra Features

- Coupon system with demo coupon codes such as `STUDENT10`, `BOOK50`, and `FREESHIP`.
- Recently viewed books for quick access to previously opened book details.
- Seller information with student seller name, college, and verification status.
- Stock availability labels such as In Stock, Only few left, and Out of Stock.
- Presentation mode for hiding technical API error messages during project demos.
- API timeout handling to prevent long loading states.
- Cached API results in localStorage for faster repeated searches.
- Secondary Google Books fallback in the API service if Open Library fails.
- Book request page for students who want to request unavailable books.
- Save for later option in the cart.

## Tech Stack

| Category | Technology |
| --- | --- |
| Frontend | React JS |
| Build Tool | Vite |
| Language | JavaScript |
| Styling | CSS, shadcn/ui-style components |
| Routing | React Router DOM |
| Icons | lucide-react |
| Animations | ReactBits components, CSS animations |
| Data Storage | localStorage |
| API | Open Library API |
| Fallback API | Google Books API fallback |

## API Used

The project uses the Open Library API to fetch real book data. Open Library provides catalog information such as title, author, subject, publish year, ISBN, and cover IDs.

Example search endpoint:

```text
https://openlibrary.org/search.json?q=programming
```

Example cover image endpoint:

```text
https://covers.openlibrary.org/b/id/COVER_ID-M.jpg
```

Since Open Library is a book catalog and not an e-commerce API, the following marketplace fields are generated or managed locally for demo purposes:

- Price
- Original price
- Book condition
- Stock quantity
- Availability status
- Seller information
- Ratings and reviews
- Sold count
- Cart and order details

API handling in this project includes:

- Request timeout handling.
- Search by user-entered term or subject chip.
- Normalization of API books into a marketplace-friendly format.
- Local cache for recently fetched API results.
- Local demo books as fallback display data.
- Google Books fallback in the service layer if Open Library is unavailable.

## Project Architecture

Digital Bookstore follows a simple frontend architecture suitable for a college mini project:

- `App.jsx` defines application routes and common layout.
- `pages/` contains route-level screens such as Home, Books, Cart, Orders, Profile, Sell Book, and Admin.
- `components/` contains reusable UI components such as Navbar, BookCard, SearchBar, FilterSidebar, PriceSummary, and QuickViewDialog.
- `context/StoreContext.jsx` works as the main state management layer for cart, wishlist, orders, profile, theme, reviews, comparison list, and authentication.
- `services/booksApi.js` manages API calls, timeouts, fallback API handling, and normalization of external book data.
- `data/booksData.js` stores local demo books used as fallback and initial marketplace content.
- `localStorage` is used as a lightweight browser database for demo persistence.

This structure keeps the project beginner-friendly while still showing real-world React patterns such as reusable components, context-based global state, API services, routing, and persistent UI state.

### Component Interaction Diagram

```mermaid
graph TD
    subgraph Core Shell
        App[App.jsx - State Central]
    end

    subgraph Data Layer
        useBooks[useBookCatalog - Custom Hook]
        OpenLib[booksApi.js - API Wrapper]
        BooksData[booksData.js - Fallback Data]
        App -->|query| useBooks
        useBooks -->|fetch| OpenLib
        OpenLib -->|fails| BooksData
    end

    subgraph Header & Navigation
        Navbar[Navbar.jsx - Search & Cart Badge]
        App -->|cartCount, wishlistCount| Navbar
    end

    subgraph Book Grid & Catalog
        Books[Books.jsx - Grid Shell]
        Toolbar[Toolbar - Filters & Search]
        Card[BookCard.jsx - Individual Item]
        App -->|filteredBooks| Books
        Books --> Toolbar
        Books -->|map| Card
    end

    subgraph Cart & Checkout
        Cart[Cart.jsx - Cart Display]
        Checkout[Checkout.jsx - Order Placement]
        App -->|cart, pricing| Cart
        Cart --> Checkout
    end

    subgraph Other Features
        Wishlist[Wishlist.jsx - Saved Items]
        Orders[Orders.jsx - Order History]
        Profile[Profile.jsx - User Data]
        App -->|wishlist| Wishlist
        App -->|orders| Orders
        App -->|profile| Profile
    end

    style App fill:#1a3a34,stroke:#255f57,stroke-width:2px,color:#fff
    style useBooks fill:#2d1b4e,stroke:#513c8c,stroke-width:1px,color:#fff
    style Books fill:#0c2a4a,stroke:#2f527f,stroke-width:1px,color:#fff
    style Cart fill:#4d1e2e,stroke:#7a2f4f,stroke-width:1px,color:#fff
```

---

## 🔍 Feature Deep-Dive

### 1. Dynamic Product Display
*An elegant, grid-based presentation of books mapped with metadata, covers, and fallback states.*

**Where it is made:**
- API Fetching: `services/booksApi.js` - searches the Open Library API
- Data Normalization: `services/booksApi.js` - formats API results into React-friendly structures  
- State Management: `context/StoreContext.jsx` - manages books, loading, and error states
- Grid Presentation: `pages/Books.jsx` - renders items in CSS Grid
- Individual Card: `components/BookCard.jsx` - displays title, author, cover, rating, and pricing

**How it is made:**
1. When the page loads, `useEffect` in `Books.jsx` triggers an API call to Open Library
2. Results are normalized to include consistent fields like title, author, price, rating, and cover
3. If API fails, fallback books from `booksData.js` are loaded instead
4. Each book is rendered as a `BookCard` component with interactive actions
5. Prices and ratings are calculated or assigned for demo purposes

**Alternative Methods:**
- **Server-Side Rendering (SSR)**: Use Next.js to fetch books on the server for faster initial load
- **Static Generation**: Pre-fetch popular books and generate static pages for better performance
- **Image Optimization**: Implement Next Image for automatic responsive image loading

---

### 2. Search Functionality
*Instant, responsive searching across the catalog by typing keywords, titles, or authors.*

**Where it is made:**
- Input Handler: `components/SearchBar.jsx` - captures user input
- State: `App.jsx` - manages search query state
- API Integration: `services/booksApi.js` - sends queries to Open Library
- Display: `pages/Books.jsx` - shows filtered results

**How it is made:**
1. User types in the search bar, triggering `onQueryChange`
2. A debounce delay of **350ms** prevents excessive API calls during typing
3. When debounce completes, the query is passed to the API service
4. Open Library results are fetched and normalized
5. Books are filtered and displayed in real-time
6. If no API results, fallback books matching the query are shown

**Alternative Methods:**
- **Client-side Fuzzy Search**: Use Fuse.js for instant local search without API calls
- **Search Backend (Algolia/Meilisearch)**: Provides typo tolerance, autocomplete, and faceted search
- **Indexed Database Search**: Implement IndexedDB for offline search capability

---

### 3. Shopping Cart with Pricing
*Interactive cart management with calculations for discounts, shipping, and INR formatting.*

**Where it is made:**
- State Management: `context/StoreContext.jsx` - holds cart items array
- Pricing Logic: `context/StoreContext.jsx` - calculates subtotal, discount, shipping, total
- UI Display: `pages/Cart.jsx` - shows cart items and price breakdown
- Quantity Controls: `components/BookCard.jsx` and `pages/Cart.jsx` - add/remove/update quantity

**How it is made:**
1. **Item Structure**: Cart items stored as `{ id, book, quantity }`
2. **Add to Cart**: Checks if book exists; if yes, increments quantity; if no, adds new item
3. **Update Quantity**: Maps through cart, modifies target item, filters out items with quantity ≤ 0
4. **Pricing Calculations** (using `useMemo` for performance):
   - **Subtotal**: `cart.reduce((sum, item) => sum + item.book.price * item.quantity, 0)`
   - **Student Discount**: 10% off subtotal
   - **Shipping**: ₹79 standard; ₹0 if subtotal > ₹2500 or cart is empty
   - **Total**: Subtotal - Discount + Shipping
5. **INR Formatting**: Uses `Intl.NumberFormat('en-IN')` for beautiful currency display (e.g., ₹2,499)

**Alternative Methods:**
- **LocalStorage Sync**: Persist cart across page reloads using Context + localStorage
- **Redux/Zustand**: Centralized state management for large apps
- **Real Payment Gateway**: Integrate Razorpay or Stripe for actual transactions
- **Coupon System**: Add dynamic discount codes with validation

---

### 4. Order Summary & History  
*Tracking and listing finalized transactions with order IDs, dates, and statuses.*

**Where it is made:**
- State: `context/StoreContext.jsx` - stores orders array
- Checkout Logic: `pages/Checkout.jsx` - handles order placement
- Display: `pages/Orders.jsx` - shows order history and timeline

**How it is made:**
1. User clicks "Place Order" after confirming checkout details
2. A new order object is created with:
   ```javascript
   {
     id: `CR-${Math.floor(2000 + Math.random() * 7000)}`,
     date: new Date().toLocaleDateString('en-IN'),
     items: cartItemCount,
     total: calculatedTotal,
     status: 'Processing'
   }
   ```
3. Order is prepended to orders array so newest appears first
4. Cart is cleared and user is redirected to confirmation
5. Orders persist in `localStorage` for browser session

**Alternative Methods:**
- **Backend Database**: Store orders in MongoDB/PostgreSQL for permanent persistence
- **Order Tracking**: Add real-time tracking using APIs or WebSockets
- **Email Confirmation**: Send order confirmation emails using backend service
- **Payment Verification**: Use webhooks from Razorpay/Stripe to confirm payment before order placement

---

### 5. Book Categorization (Genre/Author)
*Filtering books by genre and author with dynamic facet generation.*

**Where it is made:**
- Keyword Mapping: `data/booksData.js` - defines genre keywords
- Category Parsing: `services/booksApi.js` - maps API subjects to genres  
- Filter Generation: `context/StoreContext.jsx` - creates unique genre/author lists
- Filter UI: `components/FilterSidebar.jsx` - displays select dropdowns
- Filtering Logic: `context/StoreContext.jsx` - filters books based on selection

**How it is made:**
1. When books are fetched, their subjects are scanned for keyword matches
2. If subjects contain "programming" or "algorithms" → genre = "Programming"
3. If subjects contain "statistics" → genre = "Mathematics"
4. Unmatched subjects fall back to "General"
5. Unique genres/authors are extracted: `['All', ...new Set(books.map(b => b.genre))]`
6. Filter dropdowns display available options
7. Filtering applies: `books.filter(b => (genre === 'All' || b.genre === genre) && (author === 'All' || b.author === author))`

**Alternative Methods:**
- **Multi-select Checkboxes**: Allow filtering by multiple genres simultaneously
- **Database Faceting**: Use MongoDB aggregation or SQL GROUP BY for scalable facet queries
- **Facet Count Badges**: Show number of items in each category (e.g., "Programming (12)")
- **Hierarchical Categories**: Create nested category structures (Subject > Topic > Subtopic)

---

### 6. User Reviews & Ratings
*Visual rating indicators and review summaries for each book.*

**Where it is made:**
- Rating Generation: `services/booksApi.js` - assigns ratings (real from API or deterministic)
- Review Text: `services/booksApi.js` - generates review based on rating
- UI Display: `components/BookCard.jsx` - shows stars and review text

**How it is made:**
1. If API provides `ratings_average`, use it
2. If missing, generate deterministic rating: `4 + ((index * 7) % 10) / 10` (ensures variety, 4.0-4.9)
3. Review count: `doc.ratings_count || (doc.edition_count * 9 + index * 3)`
4. Review text assigned dynamically:
   - Rating ≥ 4.6 → "Highly rated by readers and suitable for semester planning"
   - Rating < 4.6 → "A practical option for students comparing budget and condition"
5. Display as: `⭐ 4.8 (324 reviews) - "Review text here"`

**Alternative Methods:**
- **Interactive Star Display**: Render 5 filled/half-filled/empty stars using SVG
- **User Submission**: Allow authenticated users to write and submit reviews
- **Review Database**: Store reviews with timestamps, helpful votes, and user info
- **Sentiment Analysis**: Use NLP to analyze review text and auto-generate summary

---

### 7. 'Add to Wishlist' Feature  
*Saving books for later and quick transfer to cart.*

**Where it is made:**
- State: `context/StoreContext.jsx` - wishlist array
- Toggle Handler: `context/StoreContext.jsx` - save/remove logic
- Heart Button: `components/BookCard.jsx` - wishlist toggle UI
- Wishlist Panel: `pages/Wishlist.jsx` - displays saved items

**How it is made:**
1. Clicking heart icon on `BookCard` triggers `onToggleWishlist(book.id)`
2. Logic checks if book exists in wishlist:
   - If exists: `wishlist.filter(item => item.id !== book.id)` (remove)
   - If not exists: `[...wishlist, book]` (add)
3. Heart button displays filled color when `isWishlisted(book.id)` is true
4. Wishlist panel shows saved items with quick "Add to Cart" buttons
5. Clicking wishlist item adds it to cart without removing from wishlist

**Alternative Methods:**
- **Dedicated Wishlist Page**: `/wishlist` route with comparison tables and reviews
- **Wishlist Sharing**: Generate shareable URLs to send wishlists to friends
- **Price Drop Alerts**: Notify user when wishlisted book price decreases
- **Smart Collections**: Auto-organize wishlists by genre or save date

---

### 8. Sorting Options (Price/Rating)  
*Arranging catalog based on selected criteria.*

**Where it is made:**
- Sort State: `App.jsx` (or context) - holds sort selection
- Sorting Logic: `context/StoreContext.jsx` - `useMemo` applies sort
- Sort UI: `components/Toolbar.jsx` - dropdown select for sort options

**How it is made:**
1. User selects sort option from dropdown
2. Sort state updates with selected value: `'featured'`, `'price-low'`, `'price-high'`, `'rating'`
3. `filteredBooks` memoized selector applies sort:
   ```javascript
   .sort((a, b) => {
     if (sort === 'price-low') return a.price - b.price;
     if (sort === 'price-high') return b.price - a.price;
     if (sort === 'rating') return b.rating - a.rating;
     return b.reviews - a.reviews; // featured (most reviews)
   })
   ```
4. Sort recalculates automatically when books, filters, or sort changes (due to `useMemo`)
5. Sorted books are rendered in new order

**Alternative Methods:**
- **Sort Buttons**: Replace dropdown with toggle buttons (e.g., "↓ Price", "↑ Price")
- **Multi-level Sort**: Sort by price, then by rating as secondary criterion
- **API-level Sorting**: Pass sort param to backend API for scalable large datasets
- **Persist Sort Preference**: Save user's preferred sort method in localStorage

---

## 📋 Feature Implementation Summary

| Feature | Key Files | Implementation | Alternative Approach |
| :--- | :--- | :--- | :--- |
| **Dynamic Product Display** | `BookCard.jsx`, `Books.jsx`, `booksApi.js` | Client-side API fetch with fallback data | Server-Side Rendering (Next.js) for SEO |
| **Search Functionality** | `SearchBar.jsx`, `booksApi.js` | 350ms debounced text input with API call | Fuzzy.js for client-side or Algolia backend |
| **Shopping Cart** | `Cart.jsx`, `StoreContext.jsx` | React state array with useMemo pricing | Redux or Context + localStorage |
| **Order History** | `Orders.jsx`, `StoreContext.jsx` | Local state array persisted to localStorage | REST API + Database (MongoDB/PostgreSQL) |
| **Categorization** | `FilterSidebar.jsx`, `booksApi.js` | Dynamic genre mapping from API subjects | Multi-select checkboxes or database faceting |
| **Reviews & Ratings** | `BookCard.jsx`, `booksApi.js` | Deterministic or API-based ratings | User-submitted reviews with database storage |
| **Wishlist Feature** | `Wishlist.jsx`, `BookCard.jsx` | Heart toggle with array management | Dedicated wishlist page with comparisons |
| **Sorting Options** | `Toolbar.jsx`, `StoreContext.jsx` | useMemo-based client-side sorting | Database ORDER BY for paginated datasets |

---

## 🚀 Optimization Roadmap

To level up this e-commerce application, consider implementing:

1. **LocalStorage Persistence Enhancement**
   - Save cart, wishlist, orders to localStorage
   - Restore state on page reload
   - Add versioning for data migrations

2. **State Management Migration**
   - Transition from prop drilling to React Context (already done!)
   - Or upgrade to Redux Toolkit for complex state
   - Implement custom hooks (`useCart()`, `useWishlist()`)

3. **Performance Optimizations**
   - Implement code-splitting for route-based loading
   - Use `React.memo()` for BookCard components
   - Lazy-load images using `<img loading="lazy">`
   - Cache API results with proper invalidation strategy
   - Use virtual scrolling for large book grids

4. **Backend Integration**
   - Migrate to Node.js + Express backend
   - Use MongoDB or PostgreSQL for persistent storage
   - Implement JWT-based authentication
   - Real order processing and payment integration (Razorpay/Stripe)

5. **Advanced Features**
   - User authentication with password hashing
   - Real seller dashboard for inventory management
   - Advanced search with filters and facets
   - Chat between buyer and seller
   - Email notifications for order updates
   - AI-based book recommendations
   - Analytics and admin dashboard

6. **DevOps & Deployment**
   - Set up CI/CD pipeline with GitHub Actions
   - Deploy to Vercel, Netlify, or AWS
   - Implement error tracking (Sentry)
   - Set up monitoring and analytics (Google Analytics)
   - Database backups and disaster recovery

---

## Folder Structure

```text
src/
|-- assets/
|-- components/
|   |-- Navbar.jsx
|   |-- BookCard.jsx
|   |-- SearchBar.jsx
|   |-- FilterSidebar.jsx
|   |-- SortDropdown.jsx
|   |-- QuickViewDialog.jsx
|   |-- ReviewSection.jsx
|   |-- PriceSummary.jsx
|   |-- Footer.jsx
|   `-- ...
|-- components/profile/
|   |-- ProfileHeader.jsx
|   |-- ProfileOrders.jsx
|   |-- ProfileWishlist.jsx
|   |-- ProfileSelling.jsx
|   |-- ProfileReviews.jsx
|   |-- ProfileSettings.jsx
|   `-- ...
|-- components/reactbits/
|   |-- AnimatedEmptyState.jsx
|   |-- AnimatedNumber.jsx
|   |-- MagneticButton.jsx
|   |-- ReactBitsBackground.jsx
|   `-- ...
|-- components/ui/
|   |-- button.jsx
|   |-- card.jsx
|   |-- dialog.jsx
|   |-- input.jsx
|   |-- tabs.jsx
|   `-- ...
|-- context/
|   `-- StoreContext.jsx
|-- data/
|   `-- booksData.js
|-- pages/
|   |-- Home.jsx
|   |-- Books.jsx
|   |-- BookDetails.jsx
|   |-- Cart.jsx
|   |-- Checkout.jsx
|   |-- Wishlist.jsx
|   |-- Orders.jsx
|   |-- Compare.jsx
|   |-- SellBook.jsx
|   |-- BookRequest.jsx
|   |-- Admin.jsx
|   |-- Profile.jsx
|   |-- Login.jsx
|   |-- Signup.jsx
|   `-- About.jsx
|-- services/
|   `-- booksApi.js
|-- utils/
|   `-- formatCurrency.js
|-- App.jsx
|-- main.jsx
`-- styles.css
```

## Installation and Setup

Follow these steps to run the project locally.

### Prerequisites

Make sure the following tools are installed:

- Node.js
- npm
- Git

### Steps

1. Clone the repository.

```bash
git clone YOUR_REPOSITORY_LINK
```

2. Open the project folder.

```bash
cd digital-bookstore
```

3. Install dependencies.

```bash
npm install
```

4. Start the development server.

```bash
npm run dev
```

5. Open the website in your browser.

```text
http://localhost:5173
```

> Note: The development server may use another port if `5173` is already busy. Check the terminal output after running `npm run dev`.

## Available Scripts

| Script | Description |
| --- | --- |
| `npm run dev` | Starts the Vite development server. |
| `npm run build` | Creates a production-ready build of the project. |
| `npm run preview` | Previews the production build locally. |

## How to Use the Website

1. Open the home page and explore the marketplace sections.
2. Go to the Books page to browse available books.
3. Search books by title, author, genre, or subject.
4. Use filters to narrow results by genre, author, condition, availability, price, and rating.
5. Sort books by price, rating, or newest results.
6. Open a book details page to view full information.
7. Add books to cart or wishlist.
8. Compare up to three books before buying.
9. Use the cart page to update quantity, apply coupon, and check pricing.
10. Place a demo order from checkout.
11. View order history and tracking status from the Orders page.
12. List a used book from the Sell page.
13. Edit profile details from the Profile page.
14. Toggle dark mode from the navigation/profile controls.

## Pages Description

| Page | Description |
| --- | --- |
| Home Page | Landing page for the bookstore with featured marketplace sections and quick navigation. |
| Books Page | Main catalog page with API books, local books, search, filters, sorting, and subject chips. |
| Book Details Page | Detailed view of a selected book with seller details, reviews, actions, and related information. |
| Cart Page | Displays selected books, quantity controls, save for later, coupon, and price summary. |
| Checkout Page | Collects demo checkout details and places an order. |
| Wishlist Page | Shows saved books and allows moving items to cart. |
| Compare Page | Compares selected books based on price, rating, condition, stock, and other details. |
| Sell Page | Allows students to list used books for sale. |
| Book Request Page | Allows students to request books that are not currently listed. |
| Orders Page | Shows order history and demo order tracking status. |
| Profile Page | Displays user profile, orders, wishlist, selling activity, reviews, and settings. |
| Admin Page | Demo admin dashboard for managing marketplace book data. |
| About Page | Provides project and platform information. |
| Login/Signup Page | Demo authentication pages for creating and accessing a local account. |

## Data Storage

This project uses `localStorage` for frontend persistence. Data remains saved in the same browser until localStorage is cleared.

| Data | Purpose |
| --- | --- |
| Cart | Stores selected books and quantities. |
| Wishlist | Stores books saved for later. |
| Orders | Stores placed demo orders. |
| User profile | Stores profile details such as name, email, college, phone, and location. |
| Listed books | Stores used books added by students through the sell form. |
| Recently viewed books | Stores recently opened book details. |
| Theme | Stores light or dark mode preference. |
| API cache | Stores recently fetched book results for faster loading. |
| Login session | Stores the currently logged-in demo user. |
| Reviews | Stores locally submitted reviews. |
| Compare list | Stores books selected for comparison. |
| Book requests | Stores requested book details. |

## React Concepts Used

- Components for reusable UI sections.
- Props for passing data between components.
- `useState` for local component state.
- `useEffect` for API fetching, theme updates, and lifecycle behavior.
- `useMemo` for derived data such as filtered books, pricing, and sorted lists.
- Context API for shared store management.
- React Router for page navigation.
- Conditional rendering for loading, empty states, protected pages, and UI feedback.
- Lists and keys for rendering book grids, cart items, orders, and reviews.
- Form handling for login, signup, checkout, profile update, reviews, and sell book forms.
- localStorage for browser-based persistence.
- API fetching with error and timeout handling.
- Basic protected routes for pages that require demo login.

## Screenshots

Add project screenshots inside a `screenshots/` folder using the file names below.

### Home Page

![Home Page](./screenshots/home.png)

### Books Page

![Books Page](./screenshots/books.png)

### Book Details Page

![Book Details Page](./screenshots/book-details.png)

### Cart Page

![Cart Page](./screenshots/cart.png)

### Wishlist Page

![Wishlist Page](./screenshots/wishlist.png)

### Compare Page

![Compare Page](./screenshots/compares.png)

### Orders Page

![Orders Page](./screenshots/orders.png)

### Profile Page

![Profile Page](./screenshots/profile.png)

### Light Mode

![Light Mode](./screenshots/lightmode.png)

## Challenges Faced

- Managing cart and wishlist state across multiple pages.
- Preventing duplicate cart and wishlist items.
- Handling API slow loading and timeout cases.
- Creating fallback data when external API results are not available.
- Making filters work correctly with both API books and local demo books.
- Keeping dark mode readable across all UI sections.
- Maintaining responsive layouts for book grids, filters, cart, and profile screens.
- Creating realistic e-commerce data from a catalog-based API.
- Persisting user actions in localStorage without a backend.

## Future Enhancements

- Backend with Node.js and Express.
- MongoDB or Firebase database.
- Real authentication and password security.
- Real payment gateway integration.
- Real seller dashboard.
- Book delivery tracking with live updates.
- Chat between buyer and seller.
- AI-based book recommendations.
- College-wise book marketplace.
- Admin analytics and reporting.
- Image upload for used book listings.
- Email notifications for orders and book requests.

## Learning Outcomes

Through this project, I learned how to:

- Structure a React project using reusable components.
- Manage state using hooks and Context API.
- Integrate external APIs in a React application.
- Normalize API data for frontend use.
- Store and retrieve data using localStorage.
- Build cart, wishlist, order, and profile workflows.
- Implement search, filtering, sorting, and comparison features.
- Handle forms and validation in React.
- Create responsive layouts for different screen sizes.
- Debug UI issues, API errors, and state management problems.
- Build a real-world e-commerce style application as a college project.

## Project Status

This project is currently under development / completed as a college mini project.

## Author

| Field | Details |
| --- | --- |
| Name | Vishal Pandey |
| Role | B.Tech CSE |
| GitHub | https://github.com/vishalpandey880|
| LinkedIn | https://www.linkedin.com/in/vishal-pandey-5b897a378/ |

## License

This project is created for educational purposes.
