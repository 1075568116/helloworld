# helloworld
<!-- by 冯荣健 -->
# Vue Book Listing

## Project Introduction

Vue Book Listing is a lightweight book management system built with Vue.js 2.x. This project showcases the use of Vue single-file components, props, state management, and Vue Router to implement a basic CRUD (Create, Read, Update, Delete) application for managing books.

The application is structured around modular components and a simple routing system, making it easy to understand and extend. It is suitable for beginners who want to learn Vue.js fundamentals through a practical example.

### Main Features

- **Book List Display:**  
  The `BookList.vue` component displays a dynamic list of books, showing each book’s title, author, and description.
- **Add New Book:**  
  The `BookForm.vue` component provides a user-friendly form for adding new books. Submitted books are immediately reflected in the list.
- **Navigation Bar:**  
  The `Header.vue` component offers navigation links (such as Home and Add Book) and is consistently displayed across all pages.
- **Routing:**  
  The `src/router/index.js` file defines routes for the main book list and the add book page, enabling seamless navigation without full page reloads.
- **State Management:**  
  Book data is centrally managed in the `App.vue` component and shared with child components via props and custom events.

### Typical User Flow

1. The user lands on the homepage and views the current list of books.
2. The user clicks "Add Book" in the navigation bar to access the add book form.
3. After submitting the form, the new book is instantly added to the book list.

### Technology Stack

- **Vue.js 2.x**
- **Vue Router**
- **JavaScript (ES6)**
- **Single File Components (.vue)**
- **Node.js & npm** (for project setup and dependency management)