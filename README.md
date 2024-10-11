# Tunebook

# Team Members:
- Robert Ripley - Founder
- Gurleen K Dhaliwal - Software Engineer

## Overview

`TuneBook` is a modern decentralized platform for musicians and music enthusiasts to create, manage, and share musical sessions with the community. It leverages the **Internet Computer** to provide a scalable, secure, and serverless backend using **Rust canisters**. Users can create sessions, provide contact details, add descriptions, and set the recurrence of sessions, whether they be weekly, biweekly, or monthly. The app also features map integration for geolocation, allowing users to easily find musical events near them.

## Features

- **Create Musical Sessions**: Users can create new musical sessions, providing details like location, contact information, and recurring schedules.
- **Browse Sessions**: Users can search for and filter through various musical sessions, using parameters like location or event name.
- **Map Integration**: Uses **Leaflet.js** for map-based visualization of session locations, providing an interactive user experience.
- **Recurrence Options**: Set the frequency of sessions (e.g., Weekly, Biweekly, Monthly).
- **User Authentication**: Leverages the Internet Computer’s identity service to authenticate users and link sessions to their identity.

## Infrastructure Overview

`TuneBook` is built on the Internet Computer (IC) using a variety of tools and libraries that power the backend, frontend, and infrastructure:

### Backend: Internet Computer and Canisters

- **Internet Computer**: The app is hosted on the Internet Computer (IC), which provides serverless, scalable, and secure infrastructure. The IC allows TuneBook to function without traditional cloud services.
- **Rust Canisters**: The core backend logic is written in **Rust**, packaged as **canisters** (smart contracts) that handle session creation, user authentication, and data storage. Canisters are designed to be secure and performant, running directly on the IC.
- **Candid**: The app uses **Candid** (an interface definition language) for defining and interacting with the canister APIs, enabling smooth communication between the frontend and backend.

### Frontend: React.js with Internet Computer SDK

- **React.js**: The frontend is built with **React**, providing a responsive and modern interface for users to interact with the platform.
- **Leaflet.js**: Used for map-based session visualization, Leaflet provides a highly interactive experience with map markers for session locations.
- **React Select**: For the session creation process, users can select recurring options (N/A, Weekly, Biweekly, Monthly) from a dropdown menu implemented with **React Select**.
- **IC Agent & SDK**: The frontend communicates with the canisters on the Internet Computer through the **IC agent** and the IC development SDK. This enables calls to the backend for fetching and managing session data.
- **Identity Management**: User authentication is handled by the Internet Computer's identity management system, allowing secure and decentralized login.


## Getting Started

To work with `TunbBook`, ensure you have the Internet Computer SDK (`dfx`) installed. Here’s how you can get started:

### Local Development

1. Clone the repository:

    ```bash
    git clone https://github.com/GurleenkDhaliwal/tunebook.git
    cd TuneBook
    ```

2. Start the Internet Computer local environment:

    ```bash
    dfx start --background
    ```

3. Deploy the canisters:

    ```bash
    dfx deploy
    ```

4. Generate the Candid interface:

    ```bash
    npm run generate
    ```

5. Start the frontend development server:

    ```bash
    npm start
    ```

### Running on the Internet Computer (IC)

To deploy `TuneBook` on the public Internet Computer network (IC), use the following command:

```bash
dfx deploy --network ic


