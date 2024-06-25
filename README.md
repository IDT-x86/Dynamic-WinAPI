# WinAPI Importer

Attempts to mitigate reverse engineering the .IMPORT section of a Window PE file, by dynamically hashing and importing the WinAPI function at runtime.


[TODO]:
 - Forward resolve exports
 - Write better template helper functions
 - Make code cleaner

## Example
```cpp
  // Can be stored in a variable and invoked later, or directly invoked
  const auto get_module_handle = IMPORT( GetModuleHandleA ); 
  IMPORT( GetModuleHandleA )( "kernel32.dll" );
```
