### Flask Application Design for Markdown-based Blog with Embedded Javascript

**HTML Files:**

- `index.html`: The landing page of the blog, listing all blog posts and their metadata (title, author, date). It includes links to the individual blog post pages.
- `post.html`: A template for individual blog posts. It includes the post's title, author, date, content (parsed Markdown), and any embedded Javascript.

**Routes:**

- `/`: The root route, which serves the `index.html` file and displays the list of blog posts.
- `/post/<post_id>`: A dynamic route that serves a specific blog post. It fetches the post data from the database using the provided `post_id` and renders the `post.html` file with the post's content.
- `/new_post`: A route for creating a new blog post. It serves an HTML form where the user can enter the post's title, author, and content. Upon form submission, it saves the new post to the database and redirects to the post's page.
- `/edit_post/<post_id>`: A route for editing an existing blog post. It fetches the post data from the database, serves an HTML form prepopulated with the post's content, and upon form submission, updates the post in the database and redirects to the post's page.