# [Project Name] - EVE Online Manufacturing Tool

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)](https://github.com/[YourUsername]/[YourRepo])
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A third-party tool for EVE Online to streamline industrial processes. It takes a pasted buy order, breaks down the assembly tree, calculates required materials based on corporation stock and blueprints, and provides a price quote to the buyer.

![Screenshot of the application's main interface](https://i.imgur.com/EiFqQRO.png)

## Description

This tool is designed for EVE Online industrial corporations to manage and quote manufacturing jobs. It simplifies the complex process of material sourcing and pricing by integrating with your corporation's asset and blueprint data. The goal is to provide a seamless experience from receiving a buy order to tracking its build progress.

## Features

-   **Buy Order Parsing:** Simply paste a multi-line buy order (e.g., from the in-game market) to start a new quote.
-   **Assembly Tree Breakdown:** Automatically calculates the full material requirements for any buildable item.
-   **Blueprint Integration:** Takes into account your corporation's blueprint Material Efficiency (ME) and Time Efficiency (TE) levels.
-   **Stock Evaluation:** Checks your corporation's hangars for available materials to reduce costs.
-   **Price Quoting:** Generates a final price for the buyer based on material costs and a configurable markup.
-   **Build Tracking:** Monitor the progress of ongoing manufacturing jobs.

## Tech Stack

-   **Frontend:** React (SPA)
-   **Backend:** Python (Flask/Django)
-   **Database:** PostgreSQL
-   **Authentication:** OIDC via Alliance Auth
-   **Containerization:** Docker & Docker Compose

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

You will need to have [Docker](https://www.docker.com/get-started) and [Docker Compose](https://docs.docker.com/compose/install/) installed on your machine.

### Installation

1.  **Clone the repository:**
    ```sh
    git clone [https://github.com/](https://github.com/)[YourUsername]/[YourRepo].git
    cd [YourRepo]
    ```

2.  **Set up environment variables:**
    Create a `.env` file in the `backend` directory. You will need to add your Alliance Auth OIDC credentials and database connection details here.
    ```env
    # .env file in /backend
    DATABASE_URL=postgresql://user:password@db:5432/mydatabase
    OIDC_CLIENT_ID=your_client_id
    OIDC_CLIENT_SECRET=your_client_secret
    OIDC_ISSUER_URL=[https://your-alliance-auth-url.com/](https://your-alliance-auth-url.com/)
    ```

3.  **Build and run the application:**
    From the root directory, run the following command:
    ```sh
    docker-compose up --build
    ```

The application will be available at `http://localhost:80`.

## Usage

1.  Navigate to the main page.
2.  Paste a buy order from EVE Online into the text area.
3.  Click "Calculate" to see the material breakdown and price quote.
4.  If satisfied, click "Submit Job" to add it to the build tracker.

## Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

## License

Distributed under the MIT License. See `LICENSE` for more information.

## Acknowledgments

-   [Alliance Auth](https://allianceauth.readthedocs.io/)
-   [EVE Swagger Interface (ESI)](https://esi.evetech.net/ui/)
-   [Create React App](https://github.com/facebook/create-react-app)
