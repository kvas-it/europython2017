# Pandas -- not just for data scientists (Uzi Halaby Senerman, BlueVine)

- The slowness of Python comes from its dynamic nature, not the fact that it's
  interpreted.
- NumPy and Pandas use statically typed arrays and vector functions.
- Pandas data frames are like Excel tables and pandas gives us an API for
  working with data in them.
- If you use Jupiter, there are also GUI-ish components.
- You can apply regular functions to data via `apply` but that's much slower
  than using vector functions (ufuncs) and should generally be avoided.
- Thinking in SQL-like terms (instead of iterating over rows) and using pandas
  accordingly often produces much better performance.

## References

- Python for Data Analysis
