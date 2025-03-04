# Zunnoon-Waheed
Nysonian Web Dev

# Tisso Vison Gift Guide - Hiring Test Project

## Overview

This project is a fully functional, responsive, and interactive Gift Guide web page designed for Tisso Vison, a brand that offers sustainable and ethically made clothing. The page is built using HTML, CSS, and JavaScript, and it showcases a curated selection of products with a focus on user experience, interactivity, and modern design principles.

The goal of this project is to demonstrate my ability to create a visually appealing, responsive, and interactive web application that aligns with the brand's values and provides a seamless shopping experience for users.


## Key Features

### 1. Responsive Design
   - The page is fully responsive and adapts to various screen sizes, including mobile, tablet, and desktop.
   - Media queries ensure that the layout, typography, and images adjust dynamically for optimal viewing on all devices.

### 2. Interactive Product Grid
   - A grid of products is displayed with hover effects and interactive indicators.
   - Users can click on the "+" indicator to view detailed product information in a modal.

### 3. Product Modal
   - A modal window opens when a product is clicked, displaying:
     - Product image
     - Title, price, and description
     - Color options (with interactive selection)
     - Size selection dropdown
     - Quantity selector (with increment/decrement buttons)
     - Add to Cart button with hover effects

### 4. Dynamic Cart Functionality
   - The modal allows users to select a product's color, size, and quantity before adding it to the cart.
   - A special promotion is included: if a user selects a Black product in size **M**, a **Soft Winter Jacket** is automatically added to the cart as a bonus.

### 5. Modern UI/UX Design
   - Clean and minimalistic design with a focus on usability.
   - Buttons with hover animations and smooth transitions for a polished user experience.
   - Typography and spacing are carefully chosen to ensure readability and visual hierarchy.

### 6. Sustainability Focus
   - The page emphasizes Tisso Vison's commitment to sustainability and ethical practices, with a dedicated section highlighting their values.

### 7. Custom Illustrations
   - The header section includes a custom SVG illustration that adds a unique and branded touch to the page.


## Technical Details

### HTML
   - Semantic HTML5 elements are used for better accessibility and SEO.
   - The structure is modular, with clear sections for the header, product grid, and modal.

### CSS
   - Modern CSS techniques such as **Flexbox** and **Grid** are used for layout.
   - Custom animations and transitions are applied to buttons and product images.
   - Media queries ensure responsiveness across devices.

### JavaScript
   - Dynamic product data is stored in a JavaScript object.
   - The modal functionality is implemented using vanilla JavaScript, including:
     - Opening/closing the modal
     - Updating product details dynamically
     - Handling user interactions (color selection, size selection, quantity adjustment)
   - A simple cart system is implemented to store selected products.


## How to Use

1. **View the Product Grid**:
   - Scroll down to see the grid of products.
   - Hover over a product to see a subtle zoom effect.

2. **Open Product Details**:
   - Click the **"+"** indicator on any product to open the modal.
   - In the modal, select a color, size, and quantity.

3. **Add to Cart**:
   - Click the **"Add to Cart"** button to add the product to the cart.
   - If you select a **Black** product in size **M**, a **Soft Winter Jacket** will be added as a bonus.

4. **Close the Modal**:
   - Click the **"×"** button or outside the modal to close it.


## Code Highlights

### Dynamic Modal Content
```javascript
function openModal(productId) {
    const product = products[productId];
    modalContent.innerHTML = `
        <img src="${product.image}" alt="${product.title}" class="product-modal-image">
        <div class="product-modal-details">
            <h2 class="product-modal-title">${product.title}</h2>
            <p class="product-modal-price">${product.price}</p>
            <p class="product-modal-description">${product.description}</p>
            <div>
                <p>Color</p>
                <div class="color-options">
                    ${product.colors.map(color => `
                        <div class="color-option" style="background-color: ${color.value};" data-color="${color.name}"></div>
                    `).join('')}
                </div>
            </div>
            <div>
                <p>Size</p>
                <select class="size-select">
                    <option value="">Choose your size</option>
                    ${product.sizes.map(size => `<option value="${size}">${size}</option>`).join('')}
                </select>
            </div>
            <div class="quantity-selector">
                <button class="quantity-btn minus">-</button>
                <span class="quantity-display">1</span>
                <button class="quantity-btn plus">+</button>
            </div>
            <button class="add-to-cart-btn">ADD TO CART →</button>
        </div>
    `;
    modalOverlay.style.display = 'flex';
    setupModalInteractions(productId);
}


### Responsive Product Grid
Css
.product-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}

@media (max-width: 768px) {
    .product-grid {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media (max-width: 480px) {
    .product-grid {
        grid-template-columns: 1fr;
    }


### Special Promotion Logic
Javascript
if (color === 'Black' && size === 'M') {
    cart.push({
        id: 'soft-winter-jacket',
        title: 'Soft Winter Jacket',
        color: 'Default',
        size: 'One Size',
        quantity: 1,
        price: '500,00€'
    });
}
```


## Why This Project?

This project demonstrates my ability to:
- Create **responsive and visually appealing** web pages.
- Implement **interactive features** using JavaScript.
- Write **clean, modular, and maintainable code**.
- Focus on **user experience** and **accessibility**.
- Align the design with the brand's values and aesthetics.


## Future Improvements

1. **Backend Integration**:
   - Connect the cart functionality to a backend for persistent storage and order processing.

2. **Enhanced Animations**:
   - Add more animations for a smoother and more engaging user experience.

3. **Accessibility Enhancements**:
   - Improve keyboard navigation and screen reader support.

4. **Product Filtering and Sorting**:
   - Add filters and sorting options for the product grid.


## Conclusion

This project showcases my skills in front-end development, with a focus on creating a modern, responsive, and interactive web application. I believe it aligns well with Nysonian's values and demonstrates my ability to deliver high-quality work that meets both user and business needs.

Thank you for considering my application! I look forward to the opportunity to contribute to Nysonian's innovative projects.


**Author**: Zunnoon Waheed 
**Date**: 4-3-2025
**Contact**: zunnoonwaheed@gmail.com
**GitHub**: https://github.com/zunnoonwaheed/Zunnoon-Waheed.git
