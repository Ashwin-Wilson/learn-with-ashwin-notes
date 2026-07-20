```python
import tkinter as tk

# ---------------------------
# 1. Create the main window
# ---------------------------
root = tk.Tk()
root.title("Simple Calculator")
root.geometry("300x400")  # Width x Height

# ---------------------------
# 2. Create Entry Widget for Display
# ---------------------------
display = tk.Entry(root, font=("Arial", 18), borderwidth=5, relief="ridge", justify="right")
display.pack(fill=tk.BOTH, ipadx=8, ipady=8, pady=10)

# ---------------------------
# 3. Functions for Calculator Logic
# ---------------------------
def button_click(value):
    """When a number or operator button is clicked, add it to the display."""
    current_text = display.get()
    display.delete(0, tk.END)
    display.insert(0, current_text + value)


def clear_display():
    """Clear the display completely."""
    display.delete(0, tk.END)


def calculate():
    """Evaluate the expression and display the result."""
    try:
        result = str(eval(display.get()))  # Use eval to calculate string expressions
        display.delete(0, tk.END)
        display.insert(0, result)
    except Exception:
        display.delete(0, tk.END)
        display.insert(0, "Error")

# ---------------------------
# 4. Create Button Frame
# ---------------------------
button_frame = tk.Frame(root)
button_frame.pack()

# ---------------------------
# 5. Define Button Layout
# ---------------------------
buttons = [
    ['7', '8', '9', '/'],
    ['4', '5', '6', '*'],
    ['1', '2', '3', '-'],
    ['0', 'C', '=', '+']
]

# ---------------------------
# 6. Add Buttons Dynamically
# ---------------------------
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

# ---------------------------
# 7. Run the Main Loop
# ---------------------------
root.mainloop()
```

![[/image 65.png|image 65.png]]