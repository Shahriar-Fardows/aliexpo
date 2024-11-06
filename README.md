# AliExpo - Data Collection Website

AliExpo is a simple web application designed to collect user data and send it to an API endpoint. The site allows users to enter product details from AliExpress, including the URL, price, category, shipping time, shipping cost, and average rating, and submit this information to a database via the SheetDB API.

## Features

- Collects product data from users
- Validates the AliExpress URL
- Sends user data to the SheetDB API
- Responsive design using Tailwind CSS
- Simple and easy-to-use interface

## Demo

You can view the live demo of the website here:  
[https://aliexpo.vercel.app/](https://aliexpo.vercel.app/)

## Technologies Used

- **HTML** for the website structure
- **Tailwind CSS** for styling
- **JavaScript** for form handling and API interaction

## How It Works

1. **Database Key Input**:
   - When the user visits the website, they are prompted to enter their **database key**. This key is used to generate the correct API endpoint URL:  
   `https://sheetdb.io/api/v1/${key}`

2. **Form to Collect Product Data**:
   - After entering the database key, the user is presented with a form that includes the following fields:
     - **AliExpress URL** (Text input)
     - **Price** (Text input)
     - **Category** (Text input)
     - **Shipping Time** (Dropdown with options like "1-5 days", "5-10 days", "10-15 days")
     - **Shipping Cost** (Dropdown with options like "Free", "Low", "Medium", "High")
     - **Average Rating** (Dropdown with options from "1" to "5")

3. **API Submission**:
   - When the user submits the form, the data is sent to the generated API endpoint via a POST request.
   - The website ensures that the AliExpress URL is truncated to the base URL ending with `.html` (e.g., `https://www.aliexpress.com/item/1234567890.html`).

4. **Validation**:
   - All form fields are required, and basic validation is in place to ensure the data is correctly submitted.

## Installation

To run the website locally, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/aliexpo.git
