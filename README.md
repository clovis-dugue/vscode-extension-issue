# HOWTO Reproduce

1. Open this project in VS Code
2. Run the extension in the development host (e.g. by using F5)
3. Bring up the command list (e.g. by using F1) and run "Hello World"
4. Observe the "Activating extension failed" error message, and the "Command not found" (the command could not be registered after activation failed so this is expected)
5. Close the development host
6. Package the extension to a VSIX file using `vsce package`
7. NOTE: The extension uses webpack, but I did not try reproducing it on a standard TSC environment
8. Repeat 3.
9. The error message says that the command is not found, which is a consequence of the failing activation. However nothing is shown to the user about the failing activation

## Noteworthy environment details

I use TypeScript to develop my apps, and webpack to test (with dev mode) and publish it.  
This extension is, apart from my personal configuration tiles such as `eslintrc`, the one generated by `yo code` when providing these environment details.