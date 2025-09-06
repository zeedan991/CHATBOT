ChatUser Thread Demo
This Java program demonstrates the use of multithreading with thread priorities, synchronization, and lifecycle management. It simulates two chat users ("Bob" and "Alice") who send messages concurrently using separate threads with pause, resume, and stop capabilities.

Overview
Two chat users are represented by threads (ChatUser class).

Bob's thread runs with maximum priority, and Alice's thread runs with minimum priority.

Each user sends 5 messages, with a half-second delay between messages.

The program controls thread execution with methods to pause, resume, and stop the threads.

The main method coordinates the threads by checking thread states (isAlive()), pausing Bob, waiting for Alice to finish, then resuming and stopping Bob.

Features
Thread priority management via setPriority().

Thread lifecycle control with volatile flags:

paused controls message sending pause.

running controls when the thread stops entirely.

Thread coordination using join() to wait for thread completion.

Demonstrates basic thread synchronization and interaction.

Code Structure
Main class contains main method that creates and manages user threads.

ChatUser class extends Thread and overrides run() to simulate chatting behavior.

Methods within ChatUser:

Pausechat() — Pauses message sending.

Resumechat() — Resumes message sending.

Stopchat() — Stops the thread execution.
Expected Output
Messages from Bob and Alice alternating or prioritized by thread priority.

Indications when Bob pauses and resumes chatting.

Confirmation that Alice finishes chatting before Bob resumes.

Final statements that both threads have completed.

Notes
Threads are controlled using volatile flags to ensure visibility of updates between threads.

The thread pause and resume use a simple flag mechanism without full synchronization primitives (for educational simplicity).

This program is suitable for demonstration of basic Java concurrency concepts but is not production-grade for thread synchronization.
