# devops-labs

## Installation & Setup Instructions

Follow these steps to set up the project:

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/DariyVanya/devops-labs.git
    cd devops-labs
    ```

2.  **Navigate to the `wishlist-ui` directory:**

    ```bash
    cd wishlist-ui
    ```

3.  **Install dependencies:**

    ```bash
    npm install
    ```

4.  **Configure environment variables:**

    *   Create a `.env` file (or use the existing `.env.docker` as a template).
    *   Set any necessary environment variables for your application, such as API endpoints.  Example using a `.env` file:

        ```
        VITE_API_URL=http://localhost:8080/api
        ```

5.  **Run the development server:**

    ```bash
    npm run dev
    ```

    This will start the development server, and you can access the application in your browser.  Typically at `http://localhost:5173/`.


## Configuration Options

*   **`.env` file:** Configure environment variables such as API endpoints.
*   **`vite.config.ts` (if present):**  Configure Vite's build process and development server settings.
*   **`tailwind.config.js` (if present):** Customize the Tailwind CSS configuration.

## Docker Setup

1.  **Build the Docker image:**

    ```bash
    docker build -f wishlist-ui/Dockerfile -t wishlist-ui .
    ```

2.  **Run the Docker container:**

    ```bash
    docker run -p 8080:80 wishlist-ui
    ```

    This will run the application in a Docker container and expose it on port 8080.

3.  **Using Docker Compose (recommended for multi-service deployments):**

    *   Navigate to the root directory where `docker-compose.yml` resides.

    *   Run:

        ```bash
        docker-compose up --build
        ```

        This will build and start all services defined in your `docker-compose.yml` file.

## Contributing Guidelines

Contributions are welcome! To contribute:

1.  Fork the repository.
2.  Create a new branch for your feature or bug fix.
3.  Make your changes and commit them with clear, descriptive messages.
4.  Submit a pull request.

Please follow the existing code style and conventions. Ensure your code is well-documented and tested.

## License Information

License is not specified. Please clarify the license under which this project is released.

## Acknowledgments

*   Vue.js: The progressive JavaScript framework used for building the UI.
*   TypeScript:  For adding static typing to the JavaScript codebase.
*   Vite: The lightning-fast build tool.
*   Tailwind CSS:  For rapid UI development.
*   Node.js: JavaScript runtime environment.
*   Docker: For containerization and deployment.