# Infina Test Automation Suite

This repository contains a Playwright automation test suite written in TypeScript for testing registration and login scenarios on the Infina application (`https://nomi-staging-3c09.up.railway.app/`).

The project adheres to the **Page Object Model (POM)** design pattern.

## Project Structure

```text
├── pages/
│   ├── home.page.ts
│   ├── register.page.ts
│   ├── login.page.ts
│   └── otp.page.ts
├── tests/
│   ├── api/
│   │   └── api_authentication.spec.ts
│   └── web/
│       └── authentication.spec.ts
├── playwright.config.ts
├── .env
├── .gitignore
├── package.json
└── README.md
```

## Setup Instructions

### 1. Prerequisites

Make sure you have [Node.js](https://nodejs.org/) installed (v18+ recommended).

### 2. Install Dependencies

Clone this repository and run the following command to install the required packages:

```bash
npm install
```

Install Playwright browsers (if not already installed):

```bash
npx playwright install
```

### 3. Environment Variables Configuration

Create a `.env` file in the root directory (or use the automatically generated one):

```env
BASE_URL=https://nomi-staging-3c09.up.railway.app/
TEST_OTP=000000
INVALID_OTP=111111
TEST_NAME=AutoTest
```

## Running the Tests

To execute all tests (both web and api) in headless mode (default):

```bash
npx playwright test
```

### Running Specific Test Groups

To run only the Web/UI E2E tests:

```bash
npx playwright test tests/web/
```

To run only the API tests:

```bash
npx playwright test tests/api/
```

### Running with UI / Headed Mode

To open the Playwright interactive Test Runner UI:

```bash
npx playwright test --ui
```

To run the tests in headed mode:

```bash
npx playwright test --headed
```

### Viewing Test Reports

If any test fails or to see the run details, view the HTML report:

```bash
npx playwright show-report
```
