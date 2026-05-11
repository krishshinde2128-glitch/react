# Book Catalog & Store Application

A modern React-based book store application built with Vite, featuring dynamic product filtering, shopping cart management, wishlist functionality, and order tracking.

## 🎯 Features

- **Book Catalog**: Browse a comprehensive collection of books with detailed information
- **Advanced Filtering**: Filter books by genre and author
- **Search Functionality**: Real-time search to find books quickly
- **Sorting Options**: Sort by featured, price (low to high), price (high to low), and ratings
- **Shopping Cart**: Add/remove books and manage quantities
- **Wishlist**: Save favorite books for later
- **Order History**: Track previous orders
- **Smart Pricing**:
  - Student discount (10% off on subtotals)
  - Free shipping on orders above threshold
  - Dynamic total calculation
- **Responsive Design**: Works seamlessly on desktop and mobile devices

## 🏗️ Project Structure

```
src/
├── App.jsx              # Main application component
├── main.jsx             # React entry point
├── styles.css           # Global styling
├── components/          # Reusable UI components
│   ├── Header.jsx       # Top navigation and search
│   ├── Sidebar.jsx      # Filters and categories
│   ├── CatalogSection.jsx # Product listings
│   └── Overview.jsx     # Cart and order overview
├── hooks/               # Custom React hooks
│   └── useBookCatalog.jsx # Data fetching and management
├── constants/           # Application constants
│   └── books.js         # Book data and configuration
├── utils/               # Utility functions
├── api/                 # API calls and services
└── assets/              # Static files and images
```

## 🚀 Getting Started

### Prerequisites
- Node.js (14.0 or higher)
- npm or yarn

### Installation

1. **Clone or navigate to the project directory**
   ```bash
   cd mini-React-project
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm run dev
   ```
   The application will be available at `http://localhost:5173` (or the URL shown in your terminal)

### Build for Production
```bash
npm run build
```

### Preview Production Build
```bash
npm run preview
```

## 📦 Dependencies

- **React** (latest): UI library for building components
- **React DOM** (latest): React rendering for browsers
- **Vite** (latest): Fast build tool and dev server
- **@vitejs/plugin-react** (latest): React support for Vite
- **lucide-react** (latest): Modern icon library

## 🎨 Key Components

### App.jsx
Main component that orchestrates the entire application:
- State management for cart, wishlist, and filters
- Data filtering and sorting logic
- Pricing calculations
- Integration of all sub-components

### useBookCatalog Hook
Custom hook that handles:
- Book data fetching
- Genre and author lists
- Loading and error states
- Search query processing

### Sidebar
Provides filtering options:
- Genre selection
- Author selection
- Category navigation

### CatalogSection
Displays books in a grid layout with:
- Product cards
- Add to cart/wishlist buttons
- Rating and review information
- Price display

## 💰 Pricing Logic

The application implements smart pricing:
- **Base Price**: Sum of all items in cart
- **Student Discount**: 10% off on subtotal
- **Shipping**: Standard shipping (₹79) waived on orders above threshold
- **Total**: `(Subtotal - Student Discount) + Shipping`

## 🔄 State Management

The application uses React hooks for state:
- `query`: Search query string
- `genre`: Selected genre filter
- `author`: Selected author filter
- `sort`: Sorting preference
- `cart`: Items in shopping cart
- `wishlist`: Bookmarked items
- `orders`: Order history

## 🎯 Development Tips

1. **Performance Optimization**: Uses `useMemo` for expensive calculations
2. **Dynamic Validation**: Genre and author filters update based on available data
3. **Responsive Layout**: CSS grid for flexible product display
4. **Accessibility**: Semantic HTML and keyboard navigation ready

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## 🛠️ Available Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start development server with hot reload |
| `npm run build` | Create optimized production build |
| `npm run preview` | Preview production build locally |

## 📝 Notes

- The application uses Vite with `--host 0.0.0.0` for development, making it accessible from other machines on the network
- All styling is handled through `styles.css` for maintainability
- Book data is managed through constants and can be easily connected to a backend API

## 🤝 Contributing

Feel free to extend this project with:
- Backend API integration
- User authentication
- Payment gateway integration
- Product reviews and ratings
- Advanced analytics

## 📄 License

This project is part of a React learning series.

---

**Happy coding! 📚✨**
