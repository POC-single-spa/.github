# Single-SPA E-commerce Proof of Concept (POC)

This project is a simple e-commerce application built with React and TypeScript, utilizing the Single-SPA framework for front-end microservices routing.

## Repositories Overview

1. **root-config**: Orchestrates and organizes all other repositories/components/modules but isn't rendered.
2. **api**: Utility module for handling configuration, fake API (dummyJSON) using Axios, state management using Zustand, and cart utility functions.
3. **style**: Holds Tailwind CSS configuration and a custom Tailwind Watch script to monitor changes across repositories.
4. **header**: Renders the application's header.
5. **product-listing**: Renders a list of products from dummyJSON, enables viewing individual product pages, and manages cart operations.
6. **product-page**: Renders individual product pages.
7. **cart**: Displays added products, allows adding/removing items, and shows the total price of selected products.

### Interconnected components
The `product-listing` component and the `cart` component are rendered on the same page, providing a seamless shopping experience.
Although they are from different repositories, they work together to display product listings and manage the user's shopping cart efficiently.

## Technologies Used

- **React**: JavaScript library for building user interfaces.
- **TypeScript**: Typed superset of JavaScript that compiles to plain JavaScript.
- **Single-SPA**: Front-end microservices router for orchestrating multiple single-page applications.
- **Axios**: Promise-based HTTP client for making API requests.
- **Zustand**: State management library for React applications.
- **Tailwind CSS**: Utility-first CSS framework for designing modern web interfaces.
- **dummyJSON**: Fake API for generating placeholder data.

## Execution Steps

1. Clone all repositories.
2. In each repository, run `npm install`/`pnpm install`/`yarn install` to install dependencies.
3. Run `pnpm start` in each repository.
4. Access the application at `localhost:9000/`.

## Running the Application

To run the application, follow these steps:
(also available with [docker](#running-the-project-with-docker-compose))

1. Clone the repository.
2. Navigate to each repository and install dependencies using your preferred package manager:

```bash
cd root-config
pnpm install | npm install | yarn install
```
3. Start each repository

```bash
cd root-config
pnpm start
```
4. Access the application in your browser at `http://localhost:9000/`.

## Running the Project with Docker Compose

If you have cloned all the repositories into the same directory, you can run the entire project using Docker Compose. Follow these steps:

1. **Create a Docker Compose Configuration File**:
   Create a `docker-compose.yml` file in the root directory (where all repositories are located) with the following configuration:

   ```yaml
   version: '3.8'

   services:
     api:
       build: ./api
       ports:
         - "9001:9001"
     style:
       build: ./style
       ports:
         - "9002:9002"
     header:
       build: ./header
       ports:
         - "8080:8080"
     product-listing:
       build: ./product-listing
       ports:
         - "8082:8082"
     product-page:
       build: ./product-page
       ports:
         - "8083:8083"
     cart:
       build: ./cart
       ports:
         - "8081:8081"
     root-config:
       build: ./root-config
       ports:
         - "9000:9000"
    ```

2. **Run Docker Compose:**
    Open a terminal and navigate to the directory containing the docker-compose.yml file.
    Run the following command to start all services defined in the docker-compose.yml file:

    ```bash
    docker-compose up --build
    ```

3. **Access the Application**
    Once Docker Compose has started all services, you can access the application in your browser at `http://localhost:9000/`.

By using Docker Compose, you can easily manage and run the entire project with a single command, simplifying the development and deployment process.

## Contributor
- [hbler](https://github.com/Hbler)
