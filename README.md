
## 🚀 Deployment Notes

### Frontend

- **Change API Base URL**:  
  Before deploying, update any hardcoded `localhost` URLs to your production API endpoint.  
  Example:
  ```js
  // Change this
  const BASE_URL = "http://localhost:5000/api";

  // To this (your production URL)
  const BASE_URL = "https://your-production-domain.com/api";
  ```

- **Update Version Number (Optional)**:  
  If your app uses a version number in the frontend (e.g., in a footer or app info), update it in the config or directly in the UI files.

---

### Backend

- **Change Client Origin for CORS**:  
  Update CORS settings to allow your deployed frontend instead of `localhost`.  
  Example in Node.js (Express):
  ```js
  const corsOptions = {
    origin: "https://your-frontend-domain.com", // instead of "http://localhost:3000"
    credentials: true,
  };
  ```

- **Update Environment Variables**:  
  Make sure environment-specific variables like database URIs, secret keys, etc., are correctly set in your hosting platform.

- **Versioning**:  
  If you track API versioning (e.g., `/api/v1`), ensure it matches what's expected by the frontend.

