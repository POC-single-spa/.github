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

## Contributor
- [hbler](https://github.com/Hbler)
