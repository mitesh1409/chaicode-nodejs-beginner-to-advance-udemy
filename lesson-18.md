# Node.js vs Browser - key differences

Node.js = JavaScript Runtime Environment
Browser = JavaScript Runtime Environment

Browser specific objects are not available inside Node.js.
For example "window" object is available in Browser but not in Node.js.

Vice versa
Node.js specific objects won't be available inside Browser.
For example "process" object is available in Node.js but not in Browser.

Node.js is a JavaScript runtime.
It does not contain browser specific objects like "window", "document" etc.

| Node.js | Browser |
| ------ | ----------- |
| global | window |
| process | document |
| module | history |
| __filename | location |
| require() | navigator |
