# Amtica E-commerce

Amtica E-commerce is a full-featured, web-based e-commerce platform for managing products, features, categories, and users. The application supports customizable product features and advanced administration through a role-based UI. Built primarily in TypeScript, with supporting HTML, JavaScript, and CSS, it leverages Angular for the frontend and Node.js/Express with MongoDB for backend APIs and persistence.

## Live Demo

You can view a (possibly outdated) deployment at:  
[https://amitca-ecommerce.herokuapp.com/](https://amitca-ecommerce.herokuapp.com/)

## Features

- **Role-Based Admin Panel:** Custom admin experience with `Root Admin` features for deep control.
- **Product Management:** 
  - Create, update, and manage products and their details.
  - Associate products with categories and subcategories.
- **Custom Feature Creation:** 
  - Add single choice, multiple choice, fill-in-the-blank, and other feature types to products.
  - Define possible options (answers) for features.
- **Category & Subcategory Organization:**
  - Organize products under hierarchical categories for easy browsing and management.
- **User Management:** 
  - Support for roles: root, seller, member.
  - User information includes details like full name, email, password (hashed), profile pictures, and contact information.
- **Responsive UI:** 
  - Modern, mobile-friendly frontend using Angular, Bootstrap, and FontAwesome.
  - Dynamic and reactive forms for feature and product creation.
- **API Server:** 
  - REST endpoints for managing users, categories, products, and features.

## Tech Stack

- **Frontend:** Angular (with Angular CLI), TypeScript, Bootstrap, FontAwesome
- **Backend:** Node.js, Express.js
- **Database:** MongoDB (Mongoose ORM)
- **Other:** RxJS, SCSS for styles
- **Testing:** Karma, Protractor (Angular testing tools)

## Getting Started

### Prerequisites

- Node.js >= 10.x
- npm >= 6.x
- MongoDB database (local or remote)

### Installation

#### Backend

1. Clone the repository:
   ```bash
   git clone https://github.com/shubhamcommits/amtica-ecommerce.git
   cd amtica-ecommerce
   ```
2. Install server dependencies:
   ```bash
   cd src
   npm install
   ```
3. Setup environment variables as needed (e.g., MongoDB URI).

4. Start the backend server:
   ```bash
   npm start
   ```

#### Frontend

1. From the `amtica-ecommerce/public/` directory, install dependencies:
   ```bash
   cd ../public
   npm install
   ```

2. Run the development server:
   ```bash
   ng serve
   ```
3. Visit [http://localhost:4200](http://localhost:4200) in your browser.

## Development Scripts (Frontend)

- `ng serve` – Start local Angular dev server.
- `ng build` – Build frontend production bundle.
- `ng test` – Run unit tests via Karma.
- `ng e2e` – Run end-to-end tests via Protractor.

## Project Structure

```
amtica-ecommerce/
├── public/                     # Frontend Angular application
│   ├── src/
│   ├── app/
│   ├── environments/
│   └── ...
├── src/                        # Backend Node/Express API
│   ├── api/
│   │   ├── models/
│   │   ├── routes/
│   │   └── controllers/
│   └── utils/
└── ...
```

## Notable Files

- `public/src/app/root-admin/*`: Admin dashboard components, feature and product UI logic
- `src/api/models/*.js`: Mongoose schemas for core models like user, product, category
- `src/api/routes/*.js`: Express routes for REST API

## Contribution

Pull requests are welcome! For larger changes, please open an issue first to discuss what you would like to change.

## License

No license information is present; please request clarification from the repository owner before contributing or using in production.

---
