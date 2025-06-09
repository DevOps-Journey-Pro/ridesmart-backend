# RideSmart Core Backend 🚕

Welcome to the RideSmart Core Backend! This is the engine that powers the RideSmart application, handling everything from user data to trip management and payment processing.

This project is built for developers who want to understand and contribute to a modern backend system. Whether you're a beginner or an experienced developer, you'll find everything you need to get up and running below.

---

## 🛠️ Built With

We use a modern, powerful stack to ensure the RideSmart backend is efficient, scalable, and easy to maintain.

* **[Node.js](https://nodejs.org/)**: The JavaScript runtime environment that lets us run our server.
* **[Express](https://expressjs.com/)**: A fast and minimalist web framework for Node.js that helps us build our API.
* **[TypeScript](https://www.typescriptlang.org/)**: A superset of JavaScript that adds static types, making our code more robust and easier to debug.
* **[MongoDB](https://www.mongodb.com/)**: A NoSQL database where we store all our application data, like user profiles and ride history.
* **[Prisma](https://www.prisma.io/)**: A next-generation ORM (Object-Relational Mapper) that makes it super easy and safe to talk to our MongoDB database.
* **[Flutterwave](https://flutterwave.com/us/)**: Our chosen payment gateway for processing transactions securely.

---

## 🚀 Getting Started

Ready to run the project locally? Follow these steps carefully.

### **Prerequisites**

Before you begin, make sure you have the following installed on your machine:

1.  **Node.js**: You can download it from [nodejs.org](https://nodejs.org/). This will also install `npm`.
2.  **Yarn (Optional)**: A package manager. If you don't have it, you can install it with `npm install --global yarn`.
3.  **Git**: For cloning the repository.
4.  **MongoDB**: You need a running MongoDB instance. You can install it locally or use a free cloud service like [MongoDB Atlas](https://www.mongodb.com/cloud/atlas).

### **Installation & Setup**

1.  **Clone the Repository**
    Open your terminal and run this command to copy the project to your local machine.
    ```sh
    git clone https://github.com/DevOps-Journey-Pro/ridesmart-backend.git
    ```

2.  **Navigate to the Project Directory**
    ```sh
    cd ridesmart-backend
    ```

3.  **Install Dependencies**
    This command will download all the necessary packages (like Express, Prisma, etc.) that the project needs to run.
    ```sh
    yarn install
    ```
    *or if you prefer npm:*
    ```sh
    npm install
    ```

4.  **Set Up Environment Variables**
    Your server needs some secret keys and configuration settings to work. We store these in a special file that you create yourself.

    * Create a new file named `.env` in the root of the project.
    * Open the `.env.example` file that's already in the project.
    * Copy the entire content of `.env.example` and paste it into your new `.env` file.
    * Now, replace the placeholder values (like `YOUR_DATABASE_URL_HERE`) with your actual credentials. For example:
        * `DATABASE_URL`: This will be the connection string for your MongoDB database.
        * `FLUTTERWAVE_SECRET_KEY`: You'll get this from your Flutterwave dashboard.

5.  **Sync Your Database Schema**
    This is a crucial Prisma step. It reads your schema file (`prisma/schema.prisma`) and prepares your database, creating the necessary collections based on your models.
    ```sh
    npm run generate
    ```

6.  **Start the Server!**
    You're all set! This command starts the development server, and it will automatically restart whenever you make changes to the code.
    ```sh
    npm run dev
    ```

You should now see a confirmation message in your terminal indicating that the server is running, usually on `http://localhost:PORT` (the port number will be specified in your `.env` file).

Happy coding! ✨
