# Spare Parts E-commerce Website

A modern, responsive spare parts e-commerce website built with the MERN stack (MongoDB, Express.js, React.js, Node.js).

## 🚀 Features

### Core Features
- **Homepage** with hero section, featured categories, popular parts, and testimonials
- **Product Catalog** with advanced search, filtering, and pagination
- **Product Detail Pages** with image galleries and compatibility checkers
- **Inquiry System** for collecting customer inquiries instead of direct purchases
- **User Authentication** with JWT tokens
- **Admin Dashboard** for managing products, categories, and inquiries
- **Responsive Design** optimized for all devices

### Technical Features
- **RESTful API** with Express.js backend
- **MongoDB** database with Mongoose ODM
- **React Hooks** and Context API for state management
- **React Query** for server state management
- **Tailwind CSS** for styling
- **Framer Motion** for animations
- **File Upload** support for images and documents
- **Search & Filtering** with MongoDB text search
- **Pagination** for large datasets
- **Rate Limiting** and security middleware

## 🛠️ Tech Stack

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database
- **Mongoose** - ODM for MongoDB
- **JWT** - Authentication
- **bcryptjs** - Password hashing
- **multer** - File upload handling
- **express-validator** - Input validation
- **helmet** - Security middleware
- **cors** - Cross-origin resource sharing

### Frontend
- **React.js** - UI library
- **React Router** - Client-side routing
- **React Query** - Server state management
- **React Hook Form** - Form handling
- **Tailwind CSS** - Utility-first CSS framework
- **Framer Motion** - Animation library
- **Lucide React** - Icon library
- **Axios** - HTTP client

## 📁 Project Structure

```
spare-parts-website/
├── client/                 # React frontend
│   ├── public/            # Static files
│   ├── src/
│   │   ├── components/    # Reusable components
│   │   ├── contexts/      # React contexts
│   │   ├── pages/         # Page components
│   │   ├── App.js         # Main app component
│   │   └── index.js       # Entry point
│   ├── package.json       # Frontend dependencies
│   └── tailwind.config.js # Tailwind configuration
├── models/                 # MongoDB models
├── routes/                 # API routes
├── middleware/             # Custom middleware
├── server.js              # Express server
├── package.json           # Backend dependencies
└── README.md              # Project documentation
```

## 🚀 Getting Started

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or cloud instance)
- npm or yarn package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd spare-parts-website
   ```

2. **Install backend dependencies**
   ```bash
   npm install
   ```

3. **Install frontend dependencies**
   ```bash
   cd client
   npm install
   cd ..
   ```

4. **Environment Setup**
   Create a `.env` file in the root directory:
   ```env
   NODE_ENV=development
   PORT=5000
   MONGODB_URI=mongodb://localhost:27017/spare-parts
   JWT_SECRET=your_jwt_secret_key_here
   JWT_EXPIRE=30d
   ```

5. **Start the development servers**
   ```bash
   # Start backend server
   npm run server
   
   # In another terminal, start frontend
   npm run client
   
   # Or run both simultaneously
   npm run dev
   ```

6. **Access the application**
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:5000

## 📊 Database Models

### User
- Authentication details (email, password)
- Profile information (name, company, phone, address)
- Role-based access control (customer, admin, staff)
- Preferences and settings

### Product
- Product details (name, part number, brand, description)
- Specifications (dimensions, weight, compatibility)
- Pricing and availability
- Images and ratings
- Search optimization with text indexes

### Category
- Hierarchical category structure
- SEO-friendly slugs
- Featured categories for homepage
- Product count tracking

### Inquiry
- Customer information and requirements
- Product selections with quantities
- Delivery preferences
- Status tracking and responses
- File attachments support

## 🔐 API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `GET /api/auth/user` - Get user profile
- `PUT /api/auth/user` - Update profile
- `PUT /api/auth/password` - Change password

### Products
- `GET /api/products` - Get products with search/filtering
- `GET /api/products/:id` - Get single product
- `POST /api/products` - Create product (admin)
- `PUT /api/products/:id` - Update product (admin)
- `DELETE /api/products/:id` - Delete product (admin)

### Categories
- `GET /api/categories` - Get categories
- `GET /api/categories/:id` - Get single category
- `POST /api/categories` - Create category (admin)
- `PUT /api/categories/:id` - Update category (admin)

### Inquiries
- `GET /api/inquiries` - Get inquiries (admin/staff)
- `POST /api/inquiries` - Create inquiry
- `PUT /api/inquiries/:id` - Update inquiry
- `POST /api/inquiries/:id/status` - Update status

## 🎨 UI Components

### Layout Components
- **Header** - Navigation, search, user menu
- **Footer** - Company info, links, newsletter
- **Sidebar** - Filters and navigation

### Product Components
- **ProductCard** - Product display card
- **ProductGrid** - Responsive product grid
- **ProductDetail** - Detailed product view
- **ImageGallery** - Product image carousel

### Form Components
- **SearchForm** - Product search functionality
- **FilterForm** - Advanced filtering options
- **InquiryForm** - Customer inquiry submission
- **LoginForm** - User authentication

## 🔍 Search & Filtering

### Search Features
- Full-text search across product names, descriptions, and tags
- Part number search
- Brand and model search
- Fuzzy matching and suggestions

### Filtering Options
- Category and subcategory filtering
- Price range filtering
- Availability status
- Brand filtering
- Rating filtering

### Sorting Options
- Price (low to high, high to low)
- Name (A-Z, Z-A)
- Rating (highest to lowest)
- Newest first
- Most popular

## 📱 Responsive Design

- **Mobile-first** approach
- **Responsive grid** layouts
- **Touch-friendly** interactions
- **Optimized images** for different screen sizes
- **Progressive enhancement** for older browsers

## 🚀 Performance Optimization

- **React Query** for efficient data fetching
- **Image optimization** and lazy loading
- **Code splitting** and lazy loading
- **MongoDB indexing** for fast queries
- **Caching strategies** for improved performance

## 🔒 Security Features

- **JWT authentication** with secure tokens
- **Password hashing** with bcrypt
- **Input validation** and sanitization
- **Rate limiting** to prevent abuse
- **CORS configuration** for cross-origin requests
- **Helmet middleware** for security headers

## 📈 Future Enhancements

- **Real-time chat** support
- **Advanced analytics** dashboard
- **Multi-language** support
- **Payment integration** (if needed)
- **Inventory management** system
- **Customer reviews** and ratings
- **Wishlist** functionality
- **Order tracking** system

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Support

For support and questions:
- Email: support@spareparts.com
- Phone: +1 (555) 123-4567
- Documentation: [Wiki](wiki-link)

## 🙏 Acknowledgments

- React.js team for the amazing framework
- Tailwind CSS for the utility-first CSS framework
- MongoDB team for the robust database
- Express.js community for the web framework
- All contributors and supporters

---

**Built with ❤️ for the spare parts industry**

