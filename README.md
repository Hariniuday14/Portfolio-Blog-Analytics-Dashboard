# Portfolio + Blog + Analytics Dashboard

A full-stack web application built with HTML, CSS, Bootstrap, JavaScript, Node.js, and MongoDB. This application features a portfolio showcase, blog system, and analytics dashboard.

## Features

- **Portfolio Section**: Showcase your projects with images, descriptions, technologies, and links
- **Blog System**: Create, read, update, and delete blog posts with categories and tags
- **Analytics Dashboard**: Track page views, events, and generate insights with interactive charts
- **Responsive Design**: Built with Bootstrap 5 for mobile-first responsive design
- **Modern UI**: Clean and modern interface with smooth animations

## Tech Stack

- **Frontend**: HTML5, CSS3, Bootstrap 5, JavaScript (DOM manipulation)
- **Backend**: Node.js, Express.js
- **Database**: MongoDB with Mongoose
- **Charts**: Chart.js for analytics visualization

## Prerequisites

- Node.js (v14 or higher)
- MongoDB (v4.4 or higher)
- npm or yarn

## Installation

1. **Clone or navigate to the project directory**
   ```bash
   cd Portfolio
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   - Create a `.env` file in the root directory
   - Add the following:
     ```
     PORT=3000
     MONGODB_URI=mongodb://localhost:27017/portfolio_db
     ```
   - Or use your MongoDB Atlas connection string:
     ```
     MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/portfolio_db
     ```

4. **Start MongoDB**
   - If using local MongoDB, make sure it's running:
     ```bash
     # On Windows
     net start MongoDB
     
     # On macOS/Linux
     sudo systemctl start mongod
     ```

5. **Start the server**
   ```bash
   npm start
   ```
   
   Or for development with auto-reload:
   ```bash
   npm run dev
   ```

6. **Open your browser**
   - Navigate to `http://localhost:3000`

## Project Structure

```
Portfolio/
├── models/              # MongoDB models
│   ├── Portfolio.js
│   ├── Blog.js
│   └── Analytics.js
├── routes/              # API routes
│   ├── portfolio.js
│   ├── blog.js
│   └── analytics.js
├── public/              # Frontend files
│   ├── css/
│   │   └── style.css
│   ├── js/
│   │   ├── app.js
│   │   ├── index.js
│   │   ├── portfolio.js
│   │   ├── blog.js
│   │   └── dashboard.js
│   ├── index.html
│   ├── portfolio.html
│   ├── blog.html
│   └── dashboard.html
├── server.js            # Express server
├── package.json
└── README.md
```

## API Endpoints

### Portfolio
- `GET /api/portfolio` - Get all portfolio items
- `GET /api/portfolio/featured` - Get featured portfolio items
- `GET /api/portfolio/:id` - Get single portfolio item
- `POST /api/portfolio` - Create portfolio item
- `PUT /api/portfolio/:id` - Update portfolio item
- `DELETE /api/portfolio/:id` - Delete portfolio item

### Blog
- `GET /api/blog` - Get all blog posts (with optional query params: published, category, tag)
- `GET /api/blog/published` - Get published blog posts only
- `GET /api/blog/:id` - Get single blog post
- `POST /api/blog` - Create blog post
- `PUT /api/blog/:id` - Update blog post
- `DELETE /api/blog/:id` - Delete blog post
- `POST /api/blog/:id/like` - Like a blog post

### Analytics
- `GET /api/analytics` - Get all analytics (with optional query params: page, event, startDate, endDate, limit)
- `GET /api/analytics/summary` - Get analytics summary with charts data
- `POST /api/analytics/track` - Track custom event

## Usage

### Adding Portfolio Items
1. Navigate to the Portfolio page
2. Use the form to add new portfolio items (you can add this functionality via the dashboard or directly through the API)

### Creating Blog Posts
1. Navigate to the Blog page
2. Use the form to create new blog posts
3. Mark posts as published to make them visible to visitors

### Viewing Analytics
1. Navigate to the Dashboard page
2. View real-time analytics including:
   - Total page views
   - Views by page
   - Events by type
   - Daily views chart
   - Top pages
   - Top blog posts

## Development

The application uses:
- **DOM Manipulation**: All JavaScript uses native DOM APIs for dynamic content
- **Bootstrap 5**: For responsive layout and components
- **Chart.js**: For analytics visualization
- **Express.js**: RESTful API server
- **Mongoose**: MongoDB ODM

## License

ISC

## Author

Your Name

