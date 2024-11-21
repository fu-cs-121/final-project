# Phase 2: Developing the User Interface (UI) and Enhancing User Experience (UX)

In Phase 2, we'll leverage the business logic developed in Phase 1 to create a user-friendly interface (UI) that enhances the user experience (UX).

While Phase 1 focused on the underlying business logic, the UI is the component that users will directly interact with. It’s crucial to adopt the user's perspective during this phase to ensure the interface is intuitive and easy to use.

**What is a UI?**  
The User Interface (UI) is the part of your program that users see and interact with. It encompasses the layout, design, and interactive elements that facilitate user interaction with your application.

---

## Part 1: Choosing Your User Interface

You have the flexibility to choose any type of UI that best aligns with your project goals and personal interests. Below are some common options:

- **Terminal Interface (CLI):**  
  A text-based interface where users interact with your program through the command line. This is ideal for applications that don't require graphical elements.

- **Web Interface using Flask:**  
  A web-based application allowing users to interact with your program through a browser. This option is suitable for projects that benefit from a graphical layout and accessibility from various devices.

- **Game Interface with Pygame:**  
  A graphical interface tailored for game development, offering rich visuals and interactive elements. This is perfect for projects that involve real-time user interactions and multimedia.

- **Report/Document Generation:**  
  Applications that generate formatted documents or reports based on user inputs or data processing. This often complements a simple CLI for user interaction.

- **Something Else?**  
  If you have other UI ideas, feel free to explore them. Discuss your ideas with your instructor or teaching assistants to ensure they align with project requirements.

**Note:** You may implement multiple interfaces for your program, as the business logic developed in Phase 1 can be reused across different UIs.

---

## Part 2: Planning Your User Experience

Before you begin coding, it’s essential to plan how users will interact with your program. Follow these steps to design an effective user experience:

### 1. Identify User Actions

- **Tasks:**  
  Determine what tasks users should be able to perform within your application.

- **Inputs:**  
  Define the types of data or commands users will provide.

- **Outputs/Feedback:**  
  Specify the responses or feedback users will receive after performing actions.

### 2. Design the User Flow

- **Step Mapping:**  
  Outline the sequence of steps a user will take to complete each task.

- **Navigation:**  
  Consider how users will move between different parts of your application, ensuring the flow is logical and seamless.

**Tools:**

### 3. Sketch the Interface

- **Graphical Interfaces:**  
  Create mockups or wireframes of screens or pages to visualize the layout and design.

- **CLI:**  
  Design the structure of commands and prompts, ensuring they are intuitive and easy to use.

You may use any tool you like to sketch out your UI ideas. Here are a few popular options:

- [Whimsical](https://whimsical.com/): A free tool for creating flowcharts and wireframes.
- [tldraw](https://tldraw.com/): Another simple, free tool for creating flowcharts and diagrams.
- [Excalidraw](https://excalidraw.com/): A collaborative professional tool for sketching diagrams and UI flows.
- Pen and Paper: A simple way to sketch out your UI ideas.

---

## Part 3: Coding Your UI

Depending on the type of UI you choose, the implementation steps will vary. Below are guidelines to help you get started:

### Setting Up Your UI Code

Start by setting up the appropriate files for your chosen UI type:

- **CLI (Command Line Interface):**  
  Begin by defining your CLI code in the `main.py` file.

- **Flask Web Interface:**

  - Create a new file named `web.py` to define your Flask application.
  - Set up a `/templates` folder to store your HTML templates.

- **Pygame Interface:**

  - Create a new file named `game.py` to define your Pygame code.

- **Report/Document Generation:**
  - Implement the necessary scripts to generate and format documents.
  - Optionally, use a simple CLI to handle user inputs and trigger report generation.

**Resources:**  
Refer to the [Final Project Example Repositories](https://github.com/fu-cs-121/final-project/blob/main/resources/examples.md) to see practical implementations of different UI types.

### General Guidelines

- **Separation of Concerns:**

  - Your UI code should import and utilize classes and business logic from `core.py`.
  - Ensure that the UI is solely responsible for handling input/output and user interactions. Avoid embedding business logic within the UI layer.

- **Maintainability:**

  - If modifications to the business logic are necessary, make them in `core.py` and update your UI accordingly to reflect these changes.

- **Usability:**
  - Design your UI to be intuitive and easy to navigate. Prioritize a clean layout and responsive interactions to enhance user satisfaction.

### Documenting Your Code

Ensure that your project is well-documented to facilitate testing and usage:

- **README File:**  
  Update your README with clear instructions on how to run and test your UI. Include details specific to the UI type you’ve implemented.

- **Running Instructions:**

  - For **Pygame** or **Flask** applications, provide step-by-step instructions on setting up the environment and running the program locally.
  - Example:
    - **Flask:**
      ```bash
      python web.py
      ```
      Then navigate to `http://localhost:5000` in your browser.
    - **Pygame:**
      ```bash
      python game.py
      ```

- **Reference Example Projects:**  
  Consult the [Example Projects](https://github.com/fu-cs-121/final-project/blob/main/resources/examples.md) for guidance on structuring your documentation effectively.

---

## Final Tips

- **Iterative Development:**  
  Develop your UI incrementally, testing each component as you build to ensure functionality and usability.

- **User Feedback:**  
  If possible, gather feedback from potential users to identify areas for improvement.

- **Consistency:**  
  Maintain a consistent design and interaction pattern throughout your UI to enhance the user experience.
