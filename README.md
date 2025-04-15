# Weather Request Agent

This is an agent that makes an API request to retrieve the weather. If the weather is rainy, it recommends taking an umbrella.

---

### **Action class: `action_create_request`**
Performs an API request to retrieve weather information and provides a recommendation based on the weather conditions.

---

### **Parameters:**
- `weather`: The weather condition retrieved from the API (e.g., sunny, rainy, cloudy, etc.)

---



# Recomnadation Agent

   - Receives the weather condition
   - Provides a final recommendation based on the weather condition and the initial recommendation.
   - 
   ### **Action class: `action_recomendation`**
Performs an API request to retrieve weather information and provides a recommendation based on the weather conditions.

---


### **Parameters:**
- `tka_an_umbella`: yes or no
---

### **Workflow:**
   - Makes an API request to retrieve weather data.

---
<img width="351" alt="1" src="https://github.com/user-attachments/assets/f638f10a-9e17-478d-9fe0-c16c6413615c" />




## **Example**

#### **Example of an input structure:**

<img width="248" alt="2" src="https://github.com/user-attachments/assets/424e0ee4-2849-4e49-bfb4-dee25d7ae110" />

#### **Example of an output structure:**

<img width="317" alt="3" src="https://github.com/user-attachments/assets/b950920f-e42a-4f04-b6f4-989a3b40d903" />

## **Result Codes**
Possible result codes:

| Code                             | Description                                   |
|----------------------------------|-----------------------------------------------|
| `SC_RESULT_Take_an_umbrella`      | Weather rainy                           |
| `SC_RESULT_Dont_take_an_umbrella` | Weather sunny                           |
  
