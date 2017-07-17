# Effortless logging (Mario Corchero)

- Logging is kind of much better prints,
- Python's logging module is loosely based on Log4J,
- Logger -> Filter -> Handler <-> Formatter and all this stuff. 
- Smart buffer handler:
  - Buffer records, save last N records
  - If error happens, bump the log level to info/debug and replay last N
    records.
