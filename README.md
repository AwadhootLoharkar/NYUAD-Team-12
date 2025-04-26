# NYUAD-Team-12

## Setup Instructions

Follow these steps to set up the environment:

1. **Install `uv`**:
   First, install the `uv` package globally:
   ```bash
   pip install uv
   ```

2. **Create a Virtual Environment**:
   Use `uv` to create a virtual environment named `.venv`:
   ```bash
   uv venv
   ```

3. **Activate the Virtual Environment**:
   Activate the virtual environment using the following command:
   ```bash
   .venv\Scripts\activate
   ```

4. **Install Dependencies**:<br>
   There are two methods to do this<br>
   **Option 1: one easy command to use the .lock file**
   ```bash
   uv sync
   ```
   **Option 2**
   Second: using the requirements.txt file directly using pip or uv pip or even conda if you like:
   ```bash
   pip install -r requirements.txt
   ```

5. **Verify Installation**:
   Ensure all packages are installed correctly by checking their versions:
   ```bash
   pip list
   ```

You are now ready to use the environment!