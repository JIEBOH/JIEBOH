# Type expression agent

Is an agent that receives a reference to a mathematical expression. If the expression contains x, x^2, or x^3, it outputs the corresponding result.

---

#### **Action class: `action_translation_expression`**
Generates an equation based on a template and performs argument mapping if needed.

#### **Parameters:**
- `amountX`: The number of x in the expression

#### **Workflow:**
1. The first agent receives a reference to a mathematical expression and an input_structure. Then it translates the received expression and receives the number of X in the expression.
2. The second agent receives a structure and a translated mathematical expression and a set of rules to determine its type. Then the type is determined, for example: square and the agent produces the result.
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
| `SC_RESULT_LINEAR_EQUATION`      | Linear equation                               |
| `SC_RESULT_QUADRATIC_EQUATION`   | Quadratic equation                            |
| `SC_RESULT_CUBIC_EQUATION`       | Cubic equation                                |    
