# Applied Analytics Engineering Principles
# This file guides GitHub Copilot's code generation for this workspace.

## 1. Modularity & Single Responsibility
- Always break down complex requests into smaller, composable helper functions.
- Do not generate single, monolithic functions.
- Each function should do one thing well.

## 2. Low Cognitive Complexity
- Prioritize flat, linear logic.
- Return early to avoid deep nesting.
- Maximum cognitive complexity per function is 15.
- (Workshop demo only: temporarily set to 5 for Phase 3-4 exercises)

## 3. Human-Readable Constraints
- Maximum function length is 50 lines.
- Maximum line width is 88 characters.
- Use descriptive variable names that reflect domain concepts.

## 4. Explicit Over Implicit
- Python 3.10+ type hinting is strictly mandatory.
- Variables must use descriptive, domain-specific naming.
- Functions must include Google-style docstrings.
- Example:
  ```python
  def calculate_revenue(quantity: int, unit_price: float) -> float:
      """Calculate total revenue for a line item.
      
      Args:
          quantity: Number of units sold.
          unit_price: Price per unit in currency.
          
      Returns:
          Total revenue as quantity * unit_price.
      """
      return quantity * unit_price
  ```

## 5. Defensive Data Handling
- Implement explicit schema validation when reading external data files.
- Do not swallow exceptions - let them propagate with clear messages.
- Validate assumptions about data types and ranges early.
- Example:
  ```python
  def load_retail_data(filepath: Path) -> pd.DataFrame:
      """Load and validate retail transaction data.
      
      Args:
          filepath: Path to the CSV file.
          
      Raises:
          FileNotFoundError: If the file does not exist.
          ValueError: If required columns are missing.
          
      Returns:
          Validated DataFrame with parsed dates.
      """
      if not filepath.exists():
          raise FileNotFoundError(f"Data file not found: {filepath}")
      
      df = pd.read_csv(filepath, parse_dates=["InvoiceDate"])
      
      required_cols = {"InvoiceNo", "Quantity", "UnitPrice", "Country"}
      missing = required_cols - set(df.columns)
      if missing:
          raise ValueError(f"Missing required columns: {missing}")
      
      return df
  ```

## Project-Specific Context
- This is a data analytics workshop project.
- Primary datasets are retail transaction data.
- Use pandas for data manipulation, seaborn for visualization.
- All analysis scripts should be runnable from the project root.
