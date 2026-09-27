Scarlett Nguyen
smnguye3
ECE 309 - 001
Due 9/27/2026

# ECE 309 — Project 2: The Conversation Loop
In this project, I will be building a core memory and streaming components for the execution loop called 'miniharness' through a simple LLM harness in C++.

The program will store a conversation between a user and an assistant and will stop when it detects <|end_conversation|> as seen in the greeting script. 

## Provided vs. Mine
Everything under `include/model/`, `include/harness/`, `src/model_client.cpp`,
`src/scripted_client.cpp`, `src/replay_client.cpp`, `src/harness.cpp`, and
`src/main.cpp` is given, working code — read it, don't modify it.

I wrote the following:
- `include/core/message.h`  
- `include/core/conversation.h`
- `include/core/sentinel_scanner.h
- `src/message.cpp`
- `src/conversation.cpp`
- `src/sentinel_scanner.cpp`
- `tests/p2/test_p2.cpp`
- `docs/design-log-p2.md`

## Build and run
In PowerShell:

```bash
cd < folder address >
# Build
cmake -S . -B build
cmake --build build

# Test; if successful, will just return to normal entry
./build/Debug/test_p2.exe 

# Main program
./build/debug/miniharness --script scripts/greeting.script --save transcript.txt 
```