# helloworld
<!-- by 冯荣健 -->

# Vue Book Listing

## Project Introduction

Vue Book Listing is a simple book management system built with Vue.js 2.x. The project demonstrates how to use Vue single-file components, props, state management, and Vue Router to create a basic CRUD (Create, Read, Update, Delete) application for books.

**Key features based on the code:**
- **Book List Display:**  
  The `BookList.vue` component fetches and displays a list of books. Each book entry shows its title, author, and description.
- **Add New Book:**  
  The `BookForm.vue` component provides a form for users to input new book information. Upon submission, the new book is added to the list.
- **Navigation Bar:**  
  The `Header.vue` component provides navigation links (e.g., Home, Add Book) and is used across all pages.
- **Routing:**  
  The `src/router/index.js` file configures routes for the main book list and the add book page, enabling navigation without page reloads.
- **State Management:**  
  Book data is managed in the main `App.vue` component and passed down to child components via props and events.

