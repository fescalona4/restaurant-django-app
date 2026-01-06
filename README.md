# Little Lemon Restaurant Website

A full-featured Django web application for the Little Lemon restaurant, a family-owned Mediterranean restaurant based in Chicago, Illinois. This project demonstrates a complete restaurant website with menu display, table booking functionality, and a modern, responsive user interface.

## 🍋 Features

- **Home Page**: Welcome page with special offers and restaurant information
- **About Page**: Information about the restaurant and its owners
- **Menu Page**: Dynamic menu display with all available items and prices
- **Menu Item Details**: Individual pages for each menu item with descriptions and images
- **Table Booking**: Online reservation system for customers to book tables
- **Admin Panel**: Django admin interface for managing menu items and bookings
- **Responsive Design**: Modern UI with CSS styling and static image assets

## 🛠️ Technologies Used

- **Django 4.1.1**: Python web framework
- **SQLite**: Database for storing menu items and bookings
- **HTML/CSS**: Frontend styling and layout
- **Django Template Language (DTL)**: Dynamic template rendering
- **Python 3**: Backend programming language

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
- Python 3.8 or higher
- pip (Python package installer)
- Git (for cloning the repository)

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone <your-repository-url>
   cd restaurant-django-app
   ```

2. **Navigate to the project directory**
   ```bash
   cd workplace/littlelemon
   ```

3. **Create a virtual environment (recommended)**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

4. **Install Django**
   ```bash
   pip install django
   ```

5. **Run migrations**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

6. **Create a superuser (optional, for admin access)**
   ```bash
   python manage.py createsuperuser
   ```

7. **Run the development server**
   ```bash
   python manage.py runserver
   ```

8. **Access the application**
   - Open your browser and navigate to `http://127.0.0.1:8000`
   - Admin panel: `http://127.0.0.1:8000/admin`

## 📁 Project Structure

```
restaurant-django-app/
├── workplace/
│   └── littlelemon/
│       ├── littlelemon/          # Django project settings
│       │   ├── settings.py       # Project configuration
│       │   ├── urls.py           # Project-level URL routing
│       │   └── wsgi.py           # WSGI configuration
│       ├── restaurant/           # Main application
│       │   ├── models.py         # Database models (Menu, Booking)
│       │   ├── views.py          # View functions
│       │   ├── urls.py           # App-level URL routing
│       │   ├── forms.py          # Django forms
│       │   ├── admin.py          # Admin panel configuration
│       │   ├── templates/        # HTML templates
│       │   │   ├── base.html
│       │   │   ├── index.html
│       │   │   ├── about.html
│       │   │   ├── book.html
│       │   │   ├── menu.html
│       │   │   ├── menu_item.html
│       │   │   └── partials/
│       │   │       ├── _header.html
│       │   │       └── _footer.html
│       │   └── static/           # Static files
│       │       ├── css/
│       │       │   └── style.css
│       │       └── img/           # Image assets
│       ├── db.sqlite3            # SQLite database
│       └── manage.py             # Django management script
└── README.md
```

## 🎯 Key Components

### Models
- **Menu**: Stores menu items with name, price, and description
- **Booking**: Stores customer reservations with name, guest count, and comments

### Views
- `home()`: Renders the homepage
- `about()`: Renders the about page
- `book()`: Handles table booking form submission
- `menu()`: Displays all menu items
- `display_menu_item()`: Shows detailed information for a specific menu item

### URLs
- `/` - Home page
- `/about/` - About page
- `/book/` - Booking page
- `/menu/` - Menu listing
- `/menu_item/<int:pk>/` - Individual menu item details

## 💻 Usage

1. **Viewing the Menu**
   - Navigate to the Menu page from the homepage
   - Click on any menu item to view detailed information

2. **Making a Reservation**
   - Go to the Book page
   - Fill in your details (first name, last name, number of guests, comments)
   - Submit the form to create a reservation

3. **Admin Panel**
   - Access the admin panel at `/admin`
   - Log in with your superuser credentials
   - Manage menu items and view bookings

## 🎨 Features in Detail

- **Dynamic Menu Display**: Menu items are loaded from the database and displayed dynamically
- **Menu Item Details**: Each menu item has its own page with full description and image
- **Form Validation**: Booking form includes validation for user input
- **Static File Management**: Properly configured static files for CSS and images
- **Template Inheritance**: Uses Django template inheritance for consistent layout

## 📝 Notes

- This project uses SQLite as the default database, which is suitable for development
- For production, consider switching to PostgreSQL or MySQL
- Remember to set `DEBUG = False` and configure `ALLOWED_HOSTS` for production deployment
- The `SECRET_KEY` in settings.py should be changed and kept secure in production

## 🤝 Contributing

This is a portfolio project. Feel free to fork and modify for your own use.

## 📄 License

This project is open source and available for educational purposes.

## 👤 Author

Created as part of a Django course assessment.

---

**Little Lemon Restaurant** - Bringing Mediterranean flavors to Chicago since [year]
