## Final Project Finishing Touches

It's time to put the finishing touches on your final project! Below are a few things to check through that will help shape your project into something you can be proud of.

---

### Part 1: Q/A and Usability

#### Quality Assurance

Ensure your program runs smoothly, even when users provide unexpected inputs. The goal is to make your project as reliable and user-friendly as possible.

**Testing Your Code**

- **Test All Code Paths**: Go through your code and test every possible path, including edge cases.
- **Input Validation**: Check that all user inputs are validated before processing.
  - _Example_: If the program expects a number between 1 and 10, ensure it handles inputs like "0", "11", or "abc" gracefully.
- **Error Handling**: Use `try`/`except` blocks where appropriate to catch exceptions and provide meaningful error messages to the user.
  - _Example_:
    ```python
    try:
        number = int(input("Enter a number: "))
    except ValueError:
        print("Please enter a valid integer.")
    ```

**Tips**

- Think about how users might misuse your program and ensure it doesn't crash.
- Provide clear and helpful feedback to guide users back on track.

#### Usability Testing

To improve your program's usability, consider conducting a simple user test. Here's a script you can follow:

**Usability Testing Script**

1. **Prepare**

   - Briefly explain to the tester what your program is about.
   - Let them know you'll be observing how they use it.

2. **Observation**

   - Ask them to use your program without providing detailed instructions.
   - Encourage them to "think aloud" as they navigate through it.

3. **Take Notes**

   - Note any points where they seem confused or make mistakes.
   - Pay attention to their comments and reactions.

4. **Feedback**
   - After the session, ask them what they found intuitive or challenging.
   - Inquire about any suggestions they might have for improvement.

**Implement Improvements**

- Use the insights gained to refine your program.
- Consider adjusting prompts, improving instructions, or simplifying navigation based on the feedback.

---

### Part 2: Persistence

Enhance your program by allowing it to save user data between sessions. This helps users resume where they left off without re-entering information each time.

**Identify Data to Persist**

Think about what data in your program would benefit from being saved. Examples include:

- User preferences or settings.
- Progress data (e.g., completed tasks, scores).
- User-generated content (e.g., notes, entries).

**Implementing Save/Load Functions**

- **Use JSON for Data Storage**

  - _What is JSON?_ JSON (JavaScript Object Notation) is a lightweight format for storing and transporting data. It's easy to read and write for humans and easy to parse and generate for machines.
  - _Why Use JSON?_ It's ideal for saving complex data structures like dictionaries and lists, making it suitable for most program data.

- **Add Save and Load Methods**
  - Integrate `save_data` and `load_data` methods into your main business logic class.
  - Call `load_data` when your program starts to initialize data.
  - Call `save_data` whenever data that needs to persist changes.

**Example Approach**

```python
import json

class MyProgram:
    def __init__(self):
        self.data = {}
        self.load_data()

    def save_data(self, filename='data.json'):
        with open(filename, 'w') as f:
            json.dump(self.data, f)

    def load_data(self, filename='data.json'):
        try:
            with open(filename, 'r') as f:
                self.data = json.load(f)
        except FileNotFoundError:
            self.data = {}  # Initialize with default values if file doesn't exist
```

**Notes**

- Adjust the example to fit your own data structures and class design.
- Handle exceptions appropriately to prevent crashes due to missing or corrupted files.
- Remember that these are guidelines to help you; feel free to tailor them to your project's needs.

**Reference**

- For a practical example, you can refer to the `save_to_file` and `load_from_file` methods in the [Journal App Example](https://github.com/fu-cs-121/final-project-example-web/blob/main/core.py#L56-L79).

---

### Part 3: Documentation

Update your `readme.md` to include all necessary information to understand, set up, and run your program.

**Tips for Updating Your README**

- **Project Overview**: Briefly describe what your project does and why you made it.
- **Setup Instructions**: List any dependencies and provide instructions on how to install them.
- **Running the Program**: Explain how to run your program, including any command-line instructions.
- **Usage Guide**: Provide details on how to use your program's features.
- **Clean Up**: Remove any placeholder text and ensure the document is clear and free of errors.

**Final Touches**

- Ensure your documentation is clear, concise, and user-friendly.
- Update your `changelog.md` with the latest changes, especially noting any usability improvements based on testing.

---

## Submission

Commit and push your code! Remember, the code examples and instructions provided are guidelines to help you enhance your project. Feel free to adjust them to suit your needs. The goal is to make your project as reliable and simple as possible.

If you'd like a code review or need any assistance, don't hesitate to reach out.
