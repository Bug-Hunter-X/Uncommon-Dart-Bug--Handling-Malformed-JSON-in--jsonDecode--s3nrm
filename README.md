# Uncommon Dart Bug: Handling Malformed JSON in `jsonDecode`

This repository demonstrates a common yet often overlooked bug in Dart related to handling malformed JSON responses.  The `jsonDecode` function throws a `FormatException` if the JSON is invalid, which can be tricky to debug.  The example code showcases the error and a robust solution.

## Bug Description

The provided `bug.dart` file contains a function `fetchData` that fetches JSON data from a URL.  If the response is not valid JSON, `jsonDecode` throws a `FormatException`, halting execution.  This example highlights the importance of handling this potential exception gracefully.

## Solution

The `bugSolution.dart` file demonstrates a robust solution. It wraps the `jsonDecode` call within a `try-catch` block, handling the `FormatException` and providing informative error messages.