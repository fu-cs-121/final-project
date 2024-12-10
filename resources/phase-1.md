In Phase 1, we'll create and test the core functionality of our program before adding any user interface. This helps us think through what our program needs to do and ensure it works correctly.

> Before starting on Part 1 and 2, take a few minutes to update your project's `readme.md` file with your project title, description, and core features.

## Part 1: Business Logic Modeling

First, we need to define what data and functions our program needs. Let's look at an example:

Imagine we're building a simple journaling app. What would it need to do?

- Store journal entries (date, title, content)
- Add new entries
- View entries
- Find entries by date or title

We can map these needs to a Python class in `core.py`. Here's how we think through this:

1. What data does each journal entry need? → This becomes our entry attributes
2. What actions can we do with entries? → These become our methods

```python
class JournalEntry:
    def __init__(self, title, content):
        self.title = title
        self.content = content
        self.date = datetime.now()  # Automatically set to current time

class Journal:
    def __init__(self):
        self.entries = []  # List to store all entries

    def add_entry(self, title, content):
        """Add a new entry to the journal"""
        entry = JournalEntry(title, content)
        self.entries.append(entry)
        return entry

    def get_all_entries(self):
        """Return all journal entries"""
        return self.entries

    def find_by_title(self, title):
        """Find an entry by its title"""
        for entry in self.entries:
            if entry.title == title:
                return entry
        return None
```

## Part 2: Testing Our Code

Before adding a user interface, we need to make sure our business logic works correctly. We do this by writing tests in `test.py`.

Think of tests like a checklist:

- Did the journal start empty?
- Can we add an entry?
- Can we find an entry we added?
- Does the entry have the correct title and content?

We use Python's `assert` statement to check these things. The `assert` statement is like saying "make sure this is true":

```python
assert 5 > 3  # This passes silently
assert 5 < 3  # This raises an AssertionError
```

Here are some example tests for our journal:

```python
def test_new_journal():
    journal = Journal()
    assert len(journal.entries) == 0, "New journal should be empty"
    print("✓ New journal test passed")

def test_add_entry():
    journal = Journal()

    # Add an entry
    title = "My First Entry"
    content = "This is my first journal entry!"
    entry = journal.add_entry(title, content)

    # Check if entry was added
    assert len(journal.entries) == 1, "Journal should have one entry"
    assert entry.title == title, "Entry should have correct title"
    assert entry.content == content, "Entry should have correct content"
    print("✓ Add entry test passed")

def test_find_entry():
    journal = Journal()
    title = "Test Entry"
    journal.add_entry(title, "Test content")

    # Try to find the entry
    entry = journal.find_by_title(title)
    assert entry is not None, "Should find entry with matching title"
    assert entry.title == title, "Found entry should have correct title"
    print("✓ Find entry test passed")

if __name__ == "__main__":
    print("Running journal tests...\n")
    try:
        test_new_journal()
        test_add_entry()
        test_find_entry()
        print("\nAll tests passed! ✨")
    except AssertionError as e:
        print(f"\n❌ Test failed: {str(e)}")
```

When you run `test.py`, it will check if everything works as expected. If all tests pass, you know your business logic is working correctly!

## Submitting Phase 1

Your submission should include:

1. `core.py` with your business logic class(es)
2. `test.py` with tests for your core functionality
3. Both files should be well-commented explaining what the code does

After Phase 1 is approved, you'll move on to Phase 2 where you'll add a user interface to your working business logic.

Remember:

- Keep your business logic simple and focused
- Test all important functionality
- Use clear, descriptive names for classes, methods, and tests
- Add comments explaining any complex parts
