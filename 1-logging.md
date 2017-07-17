# Effortless logging (Mario Corchero)

- Logging is kind of like prints on steroids,
- Python's logging module is loosely based on Log4J,
- Logger -> Filter -> Handler <-> Formatter and all this stuff. 
- Smart buffering handler:
  - Buffer records, save last N records.
  - If error happens, bump the log level to info/debug and replay last N
    records.
