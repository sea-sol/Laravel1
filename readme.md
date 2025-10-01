# CinemaRex - Video Streaming Platform

CinemaRex is a comprehensive video streaming service platform built for CodeCanyon ANKI. This Laravel-based application provides a full-featured streaming solution with support for movies, TV shows, series, and live TV.

## 🎯 Features

### Content Management

- **Movies & Series**: Complete movie and TV series management with episodes
- **Live TV**: Support for live television streaming
- **Video Songs**: Music video streaming capabilities
- **Collections**: Organize content into curated collections
- **Categories**: Flexible categorization system
- **Cast & Crew**: Detailed cast information and management

### User Features

- **User Authentication**: Complete OAuth authentication with Laravel Passport
- **Watch Progress**: Track recently watched content and viewing progress
- **Likes & Favorites**: User engagement features
- **Referral System**: Built-in referral program
- **Multi-device Support**: Device confirmation and activity tracking
- **Subtitles**: Support for multiple subtitle formats

### Admin Panel

- **Role-based Access Control**: Multiple admin roles and permissions
- **Content Management**: Full CRUD operations for all content types
- **User Management**: Complete user administration
- **Analytics Dashboard**: Built with Vue.js and Chart.js
- **Plugin System**: Extensible plugin architecture
- **Backup System**: Automated backup functionality
- **Support Ticket System**: Built-in customer support

### Payment Integration

- **Braintree**: Credit card payments
- **PayPal**: PayPal integration
- **Subscription Management**: Laravel Cashier integration
- **Withdrawal System**: Payment withdrawal functionality

### Media Processing

- **FFmpeg Integration**: Video transcoding and processing
- **AWS S3 Support**: Cloud storage integration
- **CloudFront**: CDN support for video delivery
- **Multiple Video Players**: Support for Flowplayer and Plyr
- **Adaptive Streaming**: Transcoding support

### Additional Features

- **TMDB Integration**: The Movie Database API integration
- **Ad Management**: Advertisement system with Google AdSense support
- **Multilingual Support**: i18n implementation
- **Real-time Updates**: Pusher integration for live updates
- **Social Sharing**: Share content on social media
- **Reporting System**: Content reporting functionality

## 🛠️ Technology Stack

### Backend

- **Framework**: Laravel 5.6
- **PHP**: ^7.1.3
- **Database**: MySQL (cinemarex.sql included)
- **Authentication**: Laravel Passport (OAuth2)
- **Payment**: Laravel Cashier (Braintree), PayPal SDK
- **Storage**: AWS S3, Local Storage
- **Media Processing**: Laravel FFmpeg
- **Backup**: Spatie Laravel Backup

### Frontend

- **Framework**: Vue.js 2.5.7
- **State Management**: Vuex 2.4.1
- **Routing**: Vue Router 2.8.1
- **UI Components**:
  - Bootstrap 4
  - Chart.js for analytics
  - Plyr & Flowplayer for video playback
  - Vue Carousel
  - Sweetalert for notifications
- **Build Tool**: Laravel Mix (Webpack)

### Third-party Services

- **AWS**: S3 storage and CloudFront CDN
- **Pusher**: Real-time broadcasting
- **Firebase**: Real-time features
- **TMDB**: Movie database API
- **Google AdSense**: Advertisement platform

## 📋 Requirements

- PHP >= 7.1.3
- MySQL >= 5.7
- Composer
- Node.js & NPM
- FFmpeg (for video transcoding)
- AWS Account (optional, for S3 storage)
- Braintree Account (for payments)
- PayPal Account (for payments)
- Pusher Account (for real-time features)

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone <repository-url>
cd Laravel1
```

### 2. Install PHP Dependencies

```bash
composer install
```

### 3. Install Node Dependencies

```bash
npm install
```

### 4. Environment Configuration

```bash
cp .env.example .env
php artisan key:generate
```

### 5. Configure Environment Variables

Edit the `.env` file and configure:

- Database credentials
- AWS credentials (S3, CloudFront)
- Braintree credentials
- PayPal credentials
- Pusher credentials
- TMDB API key
- Mail configuration

### 6. Database Setup

```bash
# Import the database
mysql -u username -p database_name < cinemarex.sql

# Or run migrations and seeders
php artisan migrate
php artisan db:seed
```

### 7. Storage Setup

```bash
php artisan storage:link
```

### 8. Compile Assets

```bash
# Development
npm run dev

# Production
npm run production

# Watch for changes
npm run watch
```

### 9. OAuth Setup

```bash
php artisan passport:install
```

### 10. Start Development Server

```bash
php artisan serve
```

## 📁 Project Structure

```
├── app/                    # Application core
│   ├── Http/              # Controllers, Middleware
│   ├── Models/            # Eloquent models
│   ├── Events/            # Event classes
│   ├── Listeners/         # Event listeners
│   ├── Mail/              # Email templates
│   └── Traits/            # Reusable traits
├── config/                # Configuration files
├── database/              # Migrations, seeders, factories
├── resources/             # Views, assets
│   ├── assets/
│   │   ├── js/           # Vue.js components
│   │   └── sass/         # Stylesheets
│   └── views/            # Blade templates
├── routes/               # Application routes
├── storage/              # File storage
└── public/               # Public assets
```

## 🔑 Default Credentials

After seeding the database, you can login with:

- Check the `AdminsTableSeeder.php` for admin credentials
- Check the `UserTableSeeder.php` for user credentials

## 🎬 Available Commands

```bash
# Development
npm run dev              # Compile assets for development
npm run watch           # Watch and recompile on changes
npm run hot             # Hot module replacement

# Production
npm run production      # Compile and minify for production

# Testing
phpunit                 # Run PHP tests

# Artisan Commands
php artisan backup:run  # Run backup
php artisan queue:work  # Process queue jobs
```

## 🎨 Admin Panel

Access the admin panel at: `/admin`

Features include:

- Dashboard with analytics
- Content management (Movies, Series, TV, Videos)
- User management
- Payment management
- Plugin management
- System settings
- Backup management

## 📱 User Interface

The user interface is built with Vue.js and includes:

- Responsive design
- Video player with subtitles
- Content browsing and search
- User profile management
- Watch history
- Payment integration
- Social sharing

## 🔐 Security Features

- OAuth2 authentication via Laravel Passport
- CSRF protection
- XSS protection
- SQL injection prevention
- Encrypted cookies
- Device confirmation for new logins
- Activity logging

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Copyright (c) 2024 Mufasa

## 🤝 Support

For support and bug reports, use the built-in support ticket system within the admin panel.

## 📝 Notes

- This is a CodeCanyon ANKI version
- Ensure FFmpeg is properly configured for video transcoding
- Configure AWS S3 and CloudFront for optimal video delivery
- Regular backups are recommended using the built-in backup system
- Keep all dependencies up to date for security

## 🔄 Updates & Maintenance

- Regular database backups are automated via Spatie Backup
- Monitor the `storage/logs/laravel.log` for errors
- Keep composer and npm dependencies updated
- Review and update security patches regularly
