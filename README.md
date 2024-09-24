# Django Todo App

This is a simple Todo application built with Django. Users can add and delete todo items, which are displayed in a list format on the homepage.

## Features

- Add a new todo item.
- View a list of todo items.
- Remove existing todo items.

## Prerequisites

- Python 3.x
- Django 3.x or later

## Installation

1. Clone this repository:

   ```bash
   git clone https://github.com/your-username/todo-app.git
   ```

2. Navigate to the project directory:

   ```bash
   cd todo-app
   ```
   
4. Install the required packages:

   ```bash
   pip install -r requirements.txt
   ```

5. Apply migrations:

   ```bash
   python manage.py migrate
   ```

6. Run the development server:

   ```bash
   python manage.py runserver
   ```

7. Access the app at `http://127.0.0.1:8000/`.

## Project Structure

```plaintext
├── todo
│   ├── forms.py         # Contains the TodoForm for handling todo item creation.
│   ├── models.py        # Defines the Todo model with fields: title, details, and date.
│   ├── views.py         # Contains views for rendering the todo list and handling item removal.
│   └── templates/todo
│       └── index.html   # The main HTML template displaying the todo list and form.
├── todo_site
│   └── urls.py          # URL routing configuration for the app.
└── manage.py            # Django management script.
```

## Models

### `Todo`

- `title` (CharField): The title of the todo item.
- `details` (TextField): Additional details about the todo item.
- `date` (DateTimeField): The timestamp when the item was created.

## Forms

### `TodoForm`

- A Django ModelForm for creating and saving `Todo` items.

## Views

### `index`

- Displays the list of todo items.
- Handles the form submission for adding new items.

### `remove`

- Deletes a todo item based on its ID.

## URLs

- `/` - The homepage that displays the todo list and form.
- `/del/<str:item_id>` - Deletes the todo item with the given `item_id`.

## Templates

- `index.html` - The template for rendering the todo list and form.
