# Table of Contents
*   [Description](#description)
*   [Features](#features)
*   [Getting Started](#getting-started)
    *   [Prerequisites](#prerequisites)
    *   [Installation](#installation)
    *   [Usage](#usage)
*   [Project Structure](#project-structure)
*   [Tests](#tests)
*   [Acknowledgements](#acknowledgements)

---

## Description

This project is a React-based fitness application designed to help users discover and learn about various exercises. It provides a comprehensive database of exercises, allowing users to search, filter by body part, and view detailed information for each. The application integrates with external APIs to fetch exercise data, display animated GIFs, and link to relevant YouTube instructional videos. It also suggests similar exercises based on target muscle and equipment. Built with Material-UI, the application offers a responsive and user-friendly interface.

## Features

The application provides the following key features:

*   **Exercise Search**: Users can search for exercises by name, target muscle, equipment, or specific body part.
*   **Body Part Filtering**: Browse exercises categorized by different body parts such as chest, back, legs, and more, using an interactive horizontal scroll menu.
*   **Detailed Exercise View**: Access a dedicated page for each exercise, providing in-depth information, including the target muscle group and required equipment.
*   **Animated Exercise Visuals**: Each exercise features an animated GIF to demonstrate the correct form and movement.
*   **Related YouTube Videos**: Discover and watch instructional YouTube videos directly from the exercise detail page, helping users understand execution.
*   **Similar Exercises**: The application suggests exercises that target the same muscle group or utilize similar equipment, aiding in workout planning and variation.
*   **Pagination**: Efficiently browse through a large catalog of exercises with a clear pagination system.
*   **Responsive Design**: The user interface is optimized for various screen sizes, ensuring a consistent experience across desktop and mobile devices.

## Getting Started

Follow these instructions to get a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

Before you begin, ensure you have the following installed:

*   **Node.js**: Version 14 or higher (which includes npm). You can download it from [nodejs.org](https://nodejs.org/).
*   **npm**: Node Package Manager, typically installed with Node.js.
*   **RapidAPI Key**: An API key from [RapidAPI](https://rapidapi.com/) to access the [ExerciseDB API](https://rapidapi.com/justin-sf/api/exercisedb/) and [YouTube Search and Download API](https://rapidapi.com/hctoolbox/api/youtube-search-and-download/).
    *   Note: The YouTube API key is hardcoded in `src/utils/fetchData.js`, but it's good practice to be aware of its dependency. For the ExerciseDB API, you will need to set up an environment variable.

### Installation

1.  **Clone the repository**:
    ```bash
    git clone https://github.com/manishiitmandi/gym_freek.git
    ```
2.  **Navigate to the project directory**:
    ```bash
    cd gym_freek
    ```
3.  **Install dependencies**:
    ```bash
    npm install
    ```
4.  **Create a `.env` file**: In the root of your project directory, create a file named `.env`.
5.  **Add your RapidAPI Key**: Open the `.env` file and add your ExerciseDB API key as follows:
    ```
    REACT_APP_RAPID_API_KEY=YOUR_RAPIDAPI_KEY_HERE
    ```
    Replace `YOUR_RAPIDAPI_KEY_HERE` with the actual key obtained from RapidAPI.

### Usage

To run the application in development mode:

1.  **Start the development server**:
    ```bash
    npm start
    ```
    This will open the application in your default web browser at `http://localhost:3000`.

2.  **Explore the application**:
    *   The home page displays a hero banner and a search bar for exercises.
    *   You can search for exercises by typing keywords or use the horizontal scrollbar to filter exercises by body part.
    *   Click on any exercise card to view its detailed information, including GIFs, target muscles, equipment, and related YouTube videos.
    *   Navigate between the Home and Exercises sections using the Navbar.

## Project Structure

The project follows a standard Create React App structure, organized for modularity and maintainability:

```
gym_freek/
├── public/                 # Static assets and public HTML file
│   ├── index.html          # Main HTML entry point
│   └── ...
├── src/
│   ├── assets/             # Images and icons used in the application
│   ├── components/         # Reusable UI components
│   │   ├── BodyPart.js
│   │   ├── Detail.js
│   │   ├── ExerciseCard.js
│   │   ├── ExerciseVideos.js
│   │   ├── Exercises.js
│   │   ├── Footer.js
│   │   ├── HeroBanner.js
│   │   ├── HorizontalScrollbar.js
│   │   ├── Loader.js
│   │   ├── Navbar.js
│   │   ├── SearchExercises.js
│   │   └── SimilarExercises.js
│   ├── pages/              # Top-level page components for routing
│   │   ├── ExerciseDetail.js
│   │   └── Home.js
│   ├── utils/              # Utility functions, e.g., API fetching
│   │   └── fetchData.js
│   ├── App.js              # Main application component and routing setup
│   ├── App.css             # Global and component-specific styling
│   └── index.js            # React entry point
└── package.json            # Project dependencies and scripts
└── .eslintrc.js            # ESLint configuration
└── README.md               # Project README file
```

## Tests

The `package.json` file includes a script for running tests:

```json
"scripts": {
  "test": "react-scripts test"
}
```

However, no specific test files or frameworks (e.g., Jest tests) are provided within the codebase analysis. Therefore, detailed test instructions or coverage information cannot be provided based on the current files.

## Acknowledgements

This project was made with ❤️ by [JavaScript Mastery](https://www.jsmastery.pro/).