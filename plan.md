```markdown
# Detailed Implementation Plan for Iluminavoz

## Overview
Iluminavoz is a client-facing web app for a fonoaudióloga. It will include an Appointment Scheduling feature and a Speech Therapy Exercises section. The app will be built using Next.js with the app router and modern UI practices using typography, clean spacing, and a minimalist layout.

## Dependent Files & Order of Review
Before implementation, review the following files:
- **src/app/globals.css** – Global styles and CSS variables.
- **src/app/layout.tsx** – Overall layout and navigation.
- **src/app/page.tsx** – Homepage.
- **Existing UI Components:** Files in _src/components/ui_ (e.g., Button, Card, Input) for consistent styling.
- **tsconfig.json, next.config.ts** – Ensure project configuration is up-to-date.

If any of these files are missing or inadequate, re-plan accordingly.

## Step-by-Step Outline

### 1. Global Styling (src/app/globals.css)
- **Changes:**  
  - Define CSS variables for primary colors, font families, error states, and spacing.
  - Add global classes for headings, paragraphs, buttons, and error messages.
- **Error Handling:**  
  - Provide fallback fonts and cautious CSS resets to avoid layout issues.

### 2. Layout and Navigation (src/app/layout.tsx)
- **Changes:**  
  - Update or create a header with navigation links using `<Link>` from Next.js.  
    - Links: Home (“Iluminavoz”), Agendamento (Appointments), Exercícios (Exercises).
  - Ensure a responsive design with proper margins and padding.
- **UI/UX:**  
  - Use clear typography with a modern font style.
  - No icons; rely on text-only links.
- **Error Handling:**  
  - Validate that navigation links gracefully degrade if the browser fails to render custom fonts.

### 3. Homepage (src/app/page.tsx)
- **Changes:**  
  - Create a welcoming page with a prominent title “Iluminavoz.”  
  - Include brief descriptions and navigation buttons/links to Agendamento and Exercícios.
- **UI/UX:**  
  - Use a hero section with a modern layout and balanced white space.
  - Optionally add a placeholder image using an `<img>` tag if needed (using a placeholder URL following the guidelines).
- **Error Handling:**  
  - Provide alternative text and onerror handlers for any image.

### 4. Appointment Scheduling Page (src/app/appointments/page.tsx)
- **Changes:**  
  - Create a new folder `src/app/appointments` with a `page.tsx` file.
  - Render a header “Agendamento de Consultas” and embed the `AppointmentForm` component.
- **UI/UX:**  
  - Use a card layout for the form with modern spacing and clear form fields.
- **Error Handling:**  
  - Check for component loading issues and display a fallback error message if the form fails to render.

### 5. AppointmentForm Component (src/components/AppointmentForm.tsx)
- **Changes:**  
  - Build a React functional component with controlled form fields for:
    - Full Name
    - Email
    - Phone Number
    - Appointment Date & Time (use a standard `<input type="datetime-local">`)
  - Implement client-side validation; show error messages for empty or invalid fields.
  - Add a submit button that triggers an asynchronous handler to POST data.
  - Use template literals for any dynamic strings.
- **Error Handling:**  
  - Validate input and use try–catch during the API call.
  - Display user-friendly error messages if submission fails.

### 6. API Endpoint for Appointments (src/app/api/appointments/route.ts)
- **Changes:**  
  - Create an API route handling POST requests.
  - Parse the JSON body; validate that required fields are provided.
  - On success, return a JSON response confirming the submission.
  - For unsupported methods, return a 405 status with an error message.
- **Error Handling:**  
  - Use proper status codes (400 for bad requests, 405 for method not allowed).
  - Include try–catch for unexpected errors.

### 7. Exercises Page (src/app/exercises/page.tsx)
- **Changes:**  
  - Create a new folder `src/app/exercises` with a `page.tsx` file.
  - Display a header “Exercícios de Fonoaudiologia” and render multiple `ExerciseCard` components.
  - Hardcode a list of sample exercises (e.g., "Exercício de Pronúncia", "Exercício de Respiração", "Exercício de Articulação") for demonstration.
- **UI/UX:**  
  - Use a grid or list layout with clear cards, readable text, and a consistent call-to-action (“Começar” button).
- **Error Handling:**  
  - Validate existence of exercise data; show placeholder text if data is missing.

### 8. ExerciseCard Component (src/components/ExerciseCard.tsx)
- **Changes:**  
  - Create a reusable card component which accepts props: title, description, and instructions.
  - Include a “Começar” button to indicate the start of the exercise (simulate action with an alert or console log).
  - Style the card using modern spacing, borders, and typography.
- **Error Handling:**  
  - Include prop type validations and default fallback values.

### 9. Testing & API Validation
- **Testing:**  
  - Start the Next.js server and use the following curl command:
    ```bash
    curl -X POST http://localhost:3000/api/appointments \
    -H "Content-Type: application/json" \
    -d '{"name": "Test User", "email": "test@example.com", "phone": "123456789", "date": "2023-10-01T10:00"}'
    ```
  - Validate the returned HTTP status and JSON response.
- **Error Handling:**  
  - Ensure error responses (HTTP 400 or 405) are correctly handled and logged.

## Summary
- Global styling was enhanced in `globals.css` to ensure a modern and responsive design.  
- Navigation enhancements in `layout.tsx` provide clear access to home, appointment scheduling, and exercise pages.  
- A welcoming homepage in `page.tsx` guides users to the core functionalities.  
- The appointment scheduling page and its `AppointmentForm` component implement full validation and API submission via `api/appointments/route.ts`.  
- The exercises page displays multiple modern `ExerciseCard` components in a clean card layout.  
- Error handling and user feedback are integrated into both the form and API modules.  
- All new UI elements prioritize typography, spacing, and layout without external icons or image services.
