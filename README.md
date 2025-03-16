# **Secrets App**

A simple web application that displays randomly fetched secrets along with the username of the person who shared them. The app utilizes the **Secrets API** for data fetching and incorporates a minimal front-end to display the secret in an aesthetically pleasing way.

---

## **Features**
- **Random Secret Display**:
  - Fetches a random secret and its associated username from the Secrets API.
- **Minimalistic Design**:
  - Clean and simple user interface for a distraction-free experience.
- **Dynamic Rendering**:
  - Secrets and usernames are dynamically loaded and displayed on the page.

---

## **Technologies Used**
- **Node.js**: Backend runtime environment for server-side logic.
- **Express.js**: Framework for handling routes and middleware.
- **Axios**: For making HTTP requests to the Secrets API.
- **EJS (Embedded JavaScript Templates)**: For rendering dynamic HTML content.
- **CSS**: For styling the front-end interface.
- **Secrets API**: External API used to fetch random secrets.

---

## **Getting Started**

### **Prerequisites**
- **Node.js**: Ensure that Node.js is installed on your system.

---

### **Installation**
1. Clone the repository:
   ```bash
   git clone https://github.com/Ayu1404/Secrets-App.git
   cd Secrets-App
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the server:
   ```bash
   node app.js
   ```

4. Open your browser and navigate to:
   ```plaintext
   http://localhost:3000
   ```

---

## **How It Works**
1. **Fetching Secrets**:
   - On the home page (`/` route), the app makes a GET request to the **Secrets API**'s `/random` endpoint using Axios.
2. **Dynamic Rendering**:
   - The fetched secret and username are passed to the `index.ejs` template, where they are dynamically displayed.
3. **Error Handling**:
   - If the API request fails, the server logs the error and sends back a 500 status code.

---

## **File Structure**
### **Backend (app.js)**:
- **Endpoints**:
  - **GET `/`**:
    - Fetches a random secret from the Secrets API.
    - Renders the `index.ejs` file, passing the secret and username data.
- **API Integration**:
  - Uses Axios to fetch data from the Secrets API.
- **Error Handling**:
  - Logs errors and handles failures gracefully.

### **Front-End (index.ejs)**:
- **Dynamic Content**:
  - Displays the secret in a styled card format.
  - Shows the username of the individual who shared the secret.

---

## **Sample API Interaction**
### **Secrets API Endpoint**:
- **Endpoint**:
  ```plaintext
  https://secrets-api.appbrewery.com/random
  ```
- **Example Response**:
  ```json
  {
    "secret": "I still sleep with a teddy bear.",
    "username": "Anonymous"
  }
  ```

---

## **Extending Functionality**
- **Showcase Multiple Secrets**:
  - Extend the app to fetch and display multiple secrets at once.
- **User-Submitted Secrets**:
  - Add functionality for users to submit their own secrets to the Secrets API.

---

## **Contributing**
Contributions are welcome! To contribute:
1. Fork this repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add your feature"
   ```
4. Push to your branch:
   ```bash
   git push origin feature/your-feature-name
   ```
5. Open a pull request.

---

## **License**
This project is licensed under the MIT License, allowing you to modify and distribute the project with proper attribution.

---

## **Acknowledgments**
- Thanks to the **Secrets API** for providing the random secret data used in this project.
- Inspired by the fun and simplicity of exploring anonymous confessions.
