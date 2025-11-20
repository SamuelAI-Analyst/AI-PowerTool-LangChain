
AI Power Tool using LangChain 🔢⚙️

📘 Project Overview

This project is part of the IBM AI Engineering Learning Path, where I built an intelligent AI-powered tool using LangChain and Python.
The tool can understand natural language instructions and calculate exponent operations such as:

> “What is 5 raised to the power of 3?”
“Calculate 2 to the power of 8.”
“7 power 4”



This project demonstrates how LLM agents can interact with custom Python tools to perform real computations.


---

🚀 Key Features

✔️ Understands natural language inputs
✔️ Extracts base & exponent numbers using parsing logic
✔️ Performs xⁿ calculations using a custom Python tool
✔️ Error handling for invalid inputs
✔️ Built using LangChain Tool Agent


---

🛠️ Technologies Used

Tool	Purpose

Python	Core programming
LangChain	Agent & Tool integration
OpenAI LLM / ChatModel	Natural language understanding
Jupyter Notebook / VSCode	Development environment
Git & GitHub	Version control and documentation



---

⚙️ How It Works

1️⃣ User asks a question:

> “Calculate 4 to the power of 5.”



2️⃣ The LangChain agent:

Parses the input

Identifies base (4) and exponent (5)

Calls calculate_power() function

Returns output using the AI agent


3️⃣ Result:

> Answer: 1024




---

📁 Project Structure

AI-PowerTool-LangChain/
│
├── power_tool.ipynb      # Notebook with code and agent interaction tests
├── power_agent.py        # Tool function and agent logic
├── README.md             # Project documentation
├── LICENSE               # MIT License
└── .gitignore            # Ignored files


---

🧠 Code Snippet – Power Tool Function

def calculate_power(input_text: str) -> dict:
    try:
        numbers = [float(num) for num in input_text.replace(",", "").split()]
        if len(numbers) != 2:
            return {"result": "Please provide exactly two numbers: base and exponent."}
        base, exponent = numbers
        return {"result": base ** exponent}
    except ValueError:
        return {"result": "Invalid input format. Example: '2 3' or '5 to the power of 2'."}


💡 What I learned

✔ How AI Agents call external tools
✔ LangChain tool design and integration
✔ Input validation and error handling
✔ GitHub project documentation
✔ Turning simple AI concepts into real applications


---

🙋‍♂️ About Me

I'm a growing AI & Data Science professional exploring:

AI Agents & Automation

Generative AI Applications

Python & LangChain Projects


📩 Open to collaboration, internship, or entry-level AI roles.


⭐ If you like this project, please star it!
