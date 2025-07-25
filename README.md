## Backend – Traditional Medicine Explorer

This is the backend API for the **Traditional Medicine Explorer** project. It serves herbal remedies data, including information about ailments, plant names, communities, and remedy details. The backend is built using [`json-server`] for rapid prototyping and RESTful CRUD operations.

### API Base URL

> **Deployed Backend:**  
> `https://traditional-medicine-backend.onrender.com` 

---

### Project Structure

```
backend/
├── db.json              # Main data file (all remedies, images, and metadata)
├── README.md            # Backend documentation (this file)
├── package.json         # Dependencies and scripts
```

---

###  Sample Endpoints

| Endpoint              | Description                      |
|-----------------------|----------------------------------|
| `/remedies`           | Get all remedies                 |
| `/remedies/:id`       | Get a specific remedy            |
| `POST /remedies`      | Add a new remedy *(local only)*  |
| `PATCH /remedies/:id` | Edit a remedy *(local only)*     |
| `DELETE /remedies/:id`| Delete a remedy *(local only)*   |

---

###  How to Run Locally

1. **Install dependencies**

```bash
npm install
```

2. **Start the server**

```bash
npx json-server --watch db.json --port 3001
```

> The server will run at `http://localhost:3001`

---

### Deployment

-  The backend is deployed on **Render** and connected to the frontend on **Vercel** via a linked API URL.


---

###  Sample Remedy Data

```json
{
      "id": 1,
      "ailment": "Cough",
      "localName": "Mwarubaine",
      "scientificName": "Azadirachta indica (Neem)",
      "community": "Kikuyu",
      "preparation": "Boil 5-7 leaves in 2 cups of water for 10 minutes.",
      "usage": "Drink ½ cup twice daily for 3 days.",
      "warnings": "Avoid during pregnancy. May cause nausea if overused.",
      "image": "https://lightwood.org/wp-content/uploads/2021/08/Bildschirmfoto-2021-08-16-um-09.35.09.png",
      "safetyTags": ["child-safe"],
      "contribution": "Verified by Elder Wanjiku (Kikuyu Herbalist)"
    },
```

---
