# Creating the Main Window

```python
import tkinter as tk

# Create the main application window
root = tk.Tk()
root.title("Simple Calculator")
root.geometry("300x400")  # Width x Height
```

**Explanation:**

- `import tkinter as tk`
    
    - Tkinter is Python’s built-in library for creating GUI applications.
    
    - We import it and give it a shorter alias `tk` to keep our code concise.
    

- `root = tk.Tk()`
    
    - This initializes the main window where all other widgets (buttons, text boxes, etc.) will be placed.
    

- `root.title("Simple Calculator")`
    
    - Sets the window title to **“Simple Calculator”**, which appears at the top of the window.
    

- `root.geometry("300x400")`
    
    - Defines the window size as **300 pixels wide and 400 pixels tall**.
    

This block essentially **starts the app** and **sets up the main working area** for the calculator.

# Creating the Display (Entry Widget)

```python
display = tk.Entry(root, font=("Arial", 18), borderwidth=5, relief="ridge", justify="right")
display.pack(fill=tk.BOTH, ipadx=8, ipady=8, pady=10)
```

**Explanation:**

- The `Entry` widget is like a **single-line text box** that shows:
    
    - User input (numbers/operators).
    
    - Calculation results.
    

- **Parameters:**
    
    - `font=("Arial", 18)` → Sets text style to Arial with a size of 18 for better visibility.
    
    - `borderwidth=5` → Adds a thick border around the display.
    
    - `relief="ridge"` → Gives the border a raised appearance.
    
    - `justify="right"` → Aligns text to the **right side**, like most calculators.
    

- `display.pack(...)` → Places the Entry box in the window.
    
    - `fill=tk.BOTH` → Expands the display horizontally.
    
    - `ipadx` and `ipady` → Internal padding to make the box look spacious.
    
    - `pady=10` → Adds vertical space between the display and the buttons.
    

This block **creates the calculator screen** where the user can see their calculations in real-time.

# Functions for Calculator Logic

```python
def button_click(value):
    current_text = display.get()
    display.delete(0, tk.END)
    display.insert(0, current_text + value)

def clear_display():
    display.delete(0, tk.END)

def calculate():
    try:
        result = str(eval(display.get()))
        display.delete(0, tk.END)
        display.insert(0, result)
    except Exception:
        display.delete(0, tk.END)
        display.insert(0, "Error")
```

**Explanation:**

1. `**button_click(value)**`
    
    - Called when a number or operator button is pressed.
    
    - `display.get()` → Fetches the current text from the display.
    
    - `display.delete(0, tk.END)` → Clears the display temporarily.
    
    - `display.insert(0, current_text + value)` → Adds the new button press to the existing text.
    

1. `**clear_display()**`
    
    - Clears the display completely.
    
    - Useful for the **C (Clear)** button.
    

1. `**calculate()**`
    
    - Called when the **= (Equals)** button is pressed.
    
    - `eval(display.get())` → Evaluates the text inside the display as a mathematical expression.
        
        Example: `"2+3*5"` → `17`.
        
    
    - If an error occurs (e.g., division by zero), the `except` block shows `"Error"` instead of crashing.
    

This block handles **all the core functionality** of the calculator.

# Creating a Frame for Buttons

```python
button_frame = tk.Frame(root)
button_frame.pack()
```

**Explanation:**

- A `Frame` acts like a **container** that groups related widgets.

- Here, it is used to **organize all the calculator buttons** neatly.

- `pack()` adds the frame to the main window.

This block **prepares a dedicated area** to arrange buttons systematically.

# Defining Button Layout

```python
buttons = [
    ['7', '8', '9', '/'],
    ['4', '5', '6', '*'],
    ['1', '2', '3', '-'],
    ['0', 'C', '=', '+']
]
```

**Explanation:**

- This is a **list of lists** where each inner list represents a row of calculator buttons.

- Example:
    
    - `['7', '8', '9', '/']` → First row contains numbers **7-9** and the **division operator (/)**.
    

- This design makes it easy to **generate buttons dynamically** using loops instead of creating each one manually.

# Creating and Placing Buttons Dynamically

```python
for row_index, row in enumerate(buttons):
    for col_index, button_text in enumerate(row):
        if button_text == "C":
            action = clear_display
        elif button_text == "=":
            action = calculate
        else:
            action = lambda x=button_text: button_click(x)

        tk.Button(
            button_frame,
            text=button_text,
            font=("Arial", 14),
            width=5,
            height=2,
            command=action
        ).grid(row=row_index, column=col_index, padx=5, pady=5)
```

**Explanation:**

1. **Outer Loop:**
    
    - `enumerate(buttons)` → Iterates through each **row** of the button layout while also giving a `row_index`.
    

1. **Inner Loop:**
    
    - Iterates through each button inside the current row.
    
    - `button_text` → Label for the current button (e.g., `'7'`, `'+'`, `'C'`).
    

1. **Assigning Actions:**
    
    - If the button is `'C'`, link it to the `clear_display()` function.
    
    - If the button is `'='`, link it to the `calculate()` function.
    
    - Otherwise, link it to `button_click()` to insert its value into the display.
    

1. **Creating the Button:**
    
    - `tk.Button()` → Creates a button widget.
    
    - `command=action` → Assigns the button’s function when clicked.
    

1. **Placing the Button:**
    
    - `.grid(row=row_index, column=col_index)` → Places the button in a **grid layout** at the correct position.
    
    - `padx` and `pady` → Add space between buttons to make the UI cleaner.
    

This block efficiently **builds all calculator buttons dynamically** without repetitive code.

# Running the Application

```python
root.mainloop()
```

**Explanation:**

- This line **starts the Tkinter event loop**, keeping the window open and responsive.

- Without it, the program would run and close immediately.

# **How It Works (Flow)**

1. The user presses buttons → Values appear on the display (`button_click`).

1. The `C` button clears everything (`clear_display`).

1. The `=` button evaluates the full expression (`calculate`).

1. The result is displayed immediately.

1. The app continues running until the user manually closes it.