# Graded exercise Syntra Web development Promises

## Introduction
Your task is to create a small webshop that specializes in selling paint for miniatures, using Strapi CMS as the backend.

## Objective
Your main objective is to develop a functional webshop with basic CRUD (Create, Read, Update, Delete) operations for miniature paint products. Additionally, you can earn bonus points by starting to implement a shopping cart feature.

## Requirements

### Technical Requirements
- **Frontend:** plain HTML/CSS/JavaScript.
- **Backend:** Use Strapi CMS for handling backend operations.
- **Database:** SQLite (default for Strapi)
- **Version Control:** Use Git for version control and maintain a clear commit history

### Functional Requirements
1. **Create a Paint:** Users should be able to add new paint products to the store.
2. **Update Paint Name:** Users should be able to update the name of an existing paint product.
3. **Delete a Paint:** Users should be able to remove paint products from the store.
4. **Bonus - Shopping Cart:** Start implementing a shopping cart where users can add paints they wish to purchase.
5. **Bonus - Paint Type:** Start implementing a page where you can manage the different types of paint.

## Walkthrough

### 1. Setting Up Strapi --> already done for you
First, install Strapi globally and create a new project:
```bash
npx strapi new my-paint-shop --quickstart
```

### 2. Creating a 'Paint' Content Type --> already done for you
Use Strapi's admin panel to create a new Content Type named `Paint` with fields:
- Name (Text)
- Price (Decimal)
- Description (Rich Text)
- Image (Media)
- Type (wash, speed, metallic, acrylic)

### 3. API Endpoints
Strapi will automatically create the necessary CRUD API endpoints for your Paint content type. For example:
- Create a Paint: `POST /paints`
- Update a Paint: `PUT /paints/:id`
- Delete a Paint: `DELETE /paints/:id`

### 4. Frontend Code Sample
Here's a basic example of how you might interact with the Strapi API from the frontend. This example uses JavaScript's `fetch` API:

#### Create a Paint
```javascript
function createPaint(paintData) {
    fetch('http://localhost:1337/paints', {
        method: 'POST',
        headers: {
            'Content-Type': 'application/json',
        },
        body: JSON.stringify(paintData),
    })
    .then(response => response.json())
    .then(data => console.log('Success:', data))
    .catch((error) => console.error('Error:', error));
}
```

## Deliverables
- Source code for both frontend backend.
- Documentation including setup instructions and API usage.
- A brief report explaining your design decisions, challenges faced, and how you overcame them.

## Evaluation Criteria
- Functionality: Does the webshop perform all the required operations?
- Code Quality: Is the code clean, well-organized, and documented?
- Creativity: How well is the UI/UX designed?
- Bonus Task: Implementation of the shopping cart feature.

Good luck, and have fun with this exercise! Remember, this is an opportunity to demonstrate your skills and creativity in web development. We're excited to see what you build!
