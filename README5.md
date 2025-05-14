### Contribution Guidelines and Collaboration Process

#### I. Contribution Guidelines

##### 1. Fork the Repository
- **Steps**:
  - Log in to your GitHub account.
  - Navigate to the project's GitHub repository page, for example: `https://github.com/your-org/Vue-BookListing`.
  - Click the **“Fork”** button in the upper right corner of the page.
  - Select your personal GitHub account as the target repository and click **“Create fork”**.

- **Example**:
  If the project repository address is `https://github.com/your-org/Vue-BookListing`, after forking, your repository address will be `https://github.com/your-username/Vue-BookListing`.

##### 2. Clone the Repository to Local
- **Steps**:
  - On your GitHub repository page, click the **“Code”** button and copy the HTTPS link of the repository.
  - Open your terminal (Terminal) or command-line tool and run the following command to clone the repository to your local machine:
    ```bash
    git clone https://github.com/your-username/Vue-BookListing.git
    ```
  - Enter the project directory:
    ```bash
    cd Vue-BookListing
    ```

- **Notes**:
  - Ensure that your local environment has Git and Node.js installed.
  - If you are using SSH to clone, you need to configure your SSH keys first.

##### 3. Create a New Branch
- **Steps**:
  - In your local repository, create a new branch to develop your feature or fix an issue. The branch name should be concise and descriptive of your work. For example:
    ```bash
    git checkout -b feature/add-new-book
    ```
  - Or:
    ```bash
    git checkout -b fix/login-bug
    ```

- **Naming Conventions**:
  - Feature branch: `feature/<feature-description>`, for example, `feature/add-new-book`.
  - Fix branch: `fix/<issue-description>`, for example, `fix/login-bug`.
  - Documentation branch: `docs/<doc-description>`, for example, `docs/update-readme`.

##### 4. Develop Your Changes
- **Steps**:
  - Make code changes in your branch. Ensure that your coding style is consistent with the project and follows the project's coding standards.
  - If necessary, run the project locally to test your changes and ensure that they do not introduce new issues.
  - Install project dependencies:
    ```bash
    npm install
    ```
  - Start the development server:
    ```bash
    npm run serve
    ```

- **Example Code**:
  Suppose you add a new field in `BookForm.vue`:
  ```vue
  <template>
    <form @submit.prevent="submitForm">
      <input v-model="book.title" placeholder="Book Title" />
      <input v-model="book.author" placeholder="Author" />
      <input v-model="book.year" placeholder="Year" />
      <button type="submit">Add Book</button>
    </form>
  </template>

  <script>
  export default {
    data() {
      return {
        book: {
          title: '',
          author: '',
          year: ''
        }
      };
    },
    methods: {
      submitForm() {
        // Form submission logic
        console.log(this.book);
      }
    }
  };
  </script>
  ```

##### 5. Commit Your Changes
- **Steps**:
  - Use meaningful commit messages to describe your changes. For example:
    ```bash
    git add .
    git commit -m "Add new book form component"
    ```

- **Commit Message Conventions**:
  - Start with a verb, such as “Add,” “Fix,” or “Update.”
  - Be concise and clearly describe the main changes.

##### 6. Push to Remote Branch
- **Steps**:
  - Push your changes to your remote branch so that others can review your work:
    ```bash
    git push origin feature/add-new-book
    ```

- **Notes**:
  - Ensure that your local branch name matches the remote branch name.
  - If the remote branch does not exist, Git will create it automatically.

##### 7. Create a Pull Request
- **Steps**:
  - On GitHub, go to your repository page and click the **“Compare & pull request”** button.
  - On the Pull Request page, provide a detailed description of your changes, including the problems you solved or the new features you added.
  - Ensure that your Pull Request title is concise and clear, for example, “Add new book form component.”

- **Example**:
  - **Title**: `Add new book form component`
  - **Description**:
    ```
    This PR adds a new form component to allow users to add new books to the list.
    - Added BookForm.vue component
    - Updated router to include new route
    - Added validation for form fields
    ```

##### 8. Code Review
- **Steps**:
  - Project maintainers or other team members will review your Pull Request. They may raise some questions or suggestions, and you need to make changes according to the feedback.
  - If necessary, continue to push new changes to your branch, which will automatically update your Pull Request.

- **Example Feedback**:
  - **Maintainer's Comment**:
    ```
    @your-username The form validation seems to be missing for the 'year' field. Can you add that?
    ```
  - **Your Response**:
    ```
    @maintainer I've added validation for the 'year' field. Please review the updated code.
    ```

##### 9. Merge to Main Branch
- **Steps**:
  - Once your code passes the review, the project maintainer will merge your changes into the main branch. Congratulations, your contribution has been accepted!
  - Click the **“Merge pull request”** button to complete the merge.

- **Notes**:
  - Ensure that all conflicts are resolved before merging.
  - If necessary, manually merge conflicting files.

---

#### II. Collaboration Process

##### 1. Task Assignment
- **Steps**:
  - At the beginning of the project, team members allocate tasks based on project requirements and individual skills. Each task has a clear assignee and a due date.
  - Use project management tools (such as Trello, Jira) to create task cards and assign them to specific members.
  - Example task card:
    ```
    Title: Add new book form component
    Description: Create a new form component to allow users to add new books.
    Assignee: @your-username
    Due Date: 2025-05-20
    ```

##### 2. Regular Communication
- **Steps**:
  - Team members should communicate regularly to share progress and solve problems.
  - Use instant messaging tools (such as Slack, DingTalk) or hold regular video meetings.
  - Hold at least one team meeting per week to summarize the week's accomplishments and discuss the plan for the following week.
  - Meeting content may include:
    - Tasks completed this week
    - Issues encountered and solutions
    - Plan for next week

##### 3. Code Standards
- **Steps**:
  - Team members should follow unified coding standards to ensure the readability and consistency of the code.
  - Clearly state the coding standards in the project documentation, for example:
    - **Naming Conventions**:
      - Component names: `PascalCase`, for example, `BookForm.vue`.
      - Variable names: `camelCase`, for example, `bookTitle`.
    - **Code Formatting**:
      - Use Prettier or ESLint for code formatting.
      - Example ESLint configuration:
        ```json
        {
          "extends": ["eslint:recommended", "plugin:vue/recommended"],
          "rules": {
            "no-unused-vars": "warn",
            "vue/no-unused-components": "error"
          }
        }
        ```
    - **Commenting Conventions**:
      - Add comments where the logic is complex, for example:
        ```javascript
        // Validate book year to ensure it's a valid number
        if (isNaN(book.year)) {
          console.error('Invalid year');
        }
        ```

##### 4. Local Development and Testing
- **Steps**:
  - After completing local development, each member should ensure that the code runs locally and passes basic tests.
  - Use unit testing (Unit Testing) and integration testing (Integration Testing) to verify the correctness of the code.
  - Example unit test code (using Jest and Vue Test Utils):
    ```javascript
    import { mount } from '@vue/test-utils';
    import BookForm from '@/components/BookForm.vue';

    describe('BookForm.vue', () => {
      it('should validate the book year', () => {
        const wrapper = mount(BookForm);
        const yearInput = wrapper.find('[data-testid="year-input"]');
        yearInput.setValue('abc');
        expect(wrapper.vm.book.year).toBe('abc');
        // Add more validation logic here
      });
    });
    ```